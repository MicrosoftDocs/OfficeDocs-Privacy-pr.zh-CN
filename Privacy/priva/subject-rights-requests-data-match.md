---
title: 主体权限请求的数据匹配
f1.keywords:
- CSH
ms.author: chvukosw
author: chvukosw
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- M365-security-compliance
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: 了解如何将有关数据主体的其他信息上载到 Microsoft 管理中心。
ms.openlocfilehash: 1339962a1c4dba18a1d0b21d8a2cebb17ad0f91a
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248926"
---
# <a name="data-matching-for-subject-rights-requests"></a>主体权限请求的数据匹配

通过数据匹配，组织可以允许 Microsoft 用户根据提供的确切数据值来标识数据主体。 这有助于提高为内部人员和与之交互的外部用户找到与这些数据值对应的数据主体内容的准确性。 它还简化了创建主题权限请求期间手动提供字段的要求，并提供了主题权限请求中的上下文，以及展示具有最多数据主体内容的项的"概述"磁贴。 若要了解有关该视图的更多信息，请参阅 [在"管理"中查找和可视化个人数据](priva-data-profile.md#items-with-the-most-data-subject-content)。

若要使用数据匹配功能，你需要是隐私管理角色组的成员。 在导航按钮的"[Microsoft 365 合规中心](https://compliance.microsoft.com/)中，设置顶部 **导航中的"** 数据匹配"，然后选择"**数据匹配"**。 在这里，你需要定义个人数据架构并提供个人数据上载，如下所示。 请注意，你可以添加项目，并且你可以删除通过 UI 添加的项目。 但是，此时无法从 UI 就地修改项。

## <a name="prepare-for-data-import"></a>准备数据导入

定义架构或上载数据之前，需要确定数据主体信息的来源。 必需的文件格式是.csv，应用程序（如应用程序）可以读取Microsoft Excel。 构造此导出，以便列标题显示在第一行中。 这些标头应包括个人数据架构的属性名称。 检查每个字段中数据的格式。 如果任何数据包含逗号，则使用双引号将这些值括起来，以确保不会将这些数据分入单独的字段中。

## <a name="define-the-personal-data-schema"></a>定义个人数据架构

个人数据架构将描述数据主体的属性。 Upload数据匹配设置区域的第一个选项卡上设置此架构。 所需文件包括 **个人数据架构** XML 文件和 **规则包** XML 文件。

### <a name="personal-data-schema-xml"></a>个人数据架构 XML

个人数据架构文件是一个 XML 文件，它将定义期望的列名称。

- 将此 *架构文件pdm.xml*。
- 使用 Field Name 标记定义每个列名称，如下面的示例所示。
- 对要搜索的字段使用可搜索 = "true"，最多五个字段。 至少一个字段名称必须可搜索。 示例语法： `\<Field name="" searchable=""/>`。
- 个人数据架构具有 DataStore 标记部分。 必须将四个必填字段映射到字段名称：primaryKeyField、upnField、firstNameField、lastNameField。

例如，以下 XML 文件定义一个示例架构，其中五个字段指定为可搜索：PatientID、MRN、SSN、电话 和 DOB。 primaryKeyField 映射到 PatientID，upnField 映射到 MRN，firstNameField 映射到 FirstName，lastNameField 映射到 LastName。

可复制、修改和使用我们的示例。

 ```xml
<PdmSchema xmlns="http://schemas.microsoft.com/office/2020/pdm">
      <DataStore name="Patientrecords" description="Schema for patient records" version="1" primaryKeyField="PatientID" upnField="MRN" firstNameField="FirstName" lastNameField="LastName">
            <Field name="PatientID" searchable="true"/>
            <Field name="MRN" searchable="true" />
            <Field name="FirstName" />
            <Field name="LastName" />
            <Field name="SSN" searchable="true" />
            <Field name="Phone" searchable="true" />
            <Field name="DOB" searchable="true" />
            <Field name="Gender" />
            <Field name="Address" />
      </DataStore>
</PdmSchema>
 ```

### <a name="rule-package-xml"></a>规则包 XML

设置规则包时，请确保正确引用上面创建的个人数据架构文件：pdm.xml。 在下面的示例规则包 XML 中，需要自定义以下字段以创建数据匹配敏感类型：

- **RulePack id** & **PrivacyMatch id**：使用 New-GUID 生成 GUID。
- **数据存储**：此字段指定要使用的个人数据匹配查找数据存储。 提供已配置的个人数据架构的定义 DataStore 名称。
- **idMatch**：此字段指向个人数据匹配的主元素。
  - **匹配**：指定要用于精确查找的字段。 提供个人数据架构中的可搜索字段名称。
  - **分类**：此字段指定触发个人数据匹配查找的敏感类型匹配。 可提供现有内建或自定义敏感信息类型的名称或 GUID。 为了避免导致性能问题，如果在个人数据匹配中将自定义敏感信息类型用作 Classification 元素，请不要使用与大部分内容类型匹配的自定义敏感信息类型 (如"任意数字"或"任何五个字母的单词") 。 我们建议添加支持关键字或在自定义分类敏感信息类型的定义中添加格式。
- **Match**：此字段指向在 idMatch 邻近感应中发现的其他证据。
  - **匹配**：在个人数据架构中为 DataStore 提供任何字段名称。
- **资源**：此部分指定多个区域设置中敏感类型的名称和说明。
  - **idRef**：提供 ExactMatch ID 的 GUID。
  - **名称&说明**：根据需要自定义。

在下面的规则包 XML 示例中，我们将引用上一pdm.xml创建个人数据架构 XML 的示例文件：

- **Datastore**：dataStore 名称引用我们之前创建的架构文件：dataStore = "PatientRecords"。
- **idMatch**：idMatch 值引用我们之前创建的 pdm.xml 文件中列出的可搜索字段：idMatch 匹配 = "SSN"。
  - **分类**：分类值引用现有或自定义敏感信息类型：classification = "U.SSN (SSN) "。 （在此情况下，我们使用美国社会保障号的现有敏感信息类型。）

使用 Unicode 编码 (创建 XML 格式的规则) ，如以下示例代码所示。 您可以复制、修改和使用此示例。

 ```xml
<RulePackage xmlns="http://schemas.microsoft.com/office/2020/pdm">
  <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b21">
    <Version build="0" major="2" minor="0" revision="0" />
    <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
    <Details defaultLangCode="en-us">
      <LocalizedDetails langcode="en-us">
        <PublisherName>IP DLP</PublisherName>
        <Name>Health Care PDM Rulepack</Name>
        <Description>This rule package contains the Personal Data Match sensitive type for health care sensitive types.</Description>
      </LocalizedDetails>
    </Details>
  </RulePack>
  <Rules>
    <PrivacyMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB381" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
      <Pattern confidenceLevel="75">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
        <Any minMatches ="3" maxMatches ="6">
          <match matches="PatientID" />
          <match matches="MRN"/>
          <match matches="FirstName"/>
          <match matches="LastName"/>
          <match matches="Phone"/>
          <match matches="DOB"/>
        </Any>
      </Pattern>
    </PrivacyMatch>
    <LocalizedStrings>
      <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB381">
        <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
        <Description default="true" langcode="en-us">PDM Sensitive type for detecting Patient SSN.</Description>
      </Resource>
    </LocalizedStrings>
  </Rules>
</RulePackage>
 ```

## <a name="upload-personal-data"></a>Upload个人数据
定义个人数据架构后，可以在数据匹配设置页的第二个选项卡上执行个人数据上载。 选择" **添加"** 时，选择第一步中定义的个人架构，然后上载包含个人数据的文件。

可以通过选择本地文件或向包含个人数据文件的现有位置提供 SAS MICROSOFT AZURE 存储上载此个人数据。
如果您准备一个文件作为此过程的第一步，且该文件符合创建的架构，您可以使用该文件进行上载。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
