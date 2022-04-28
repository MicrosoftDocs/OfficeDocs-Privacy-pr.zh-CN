---
title: 使用者权限请求的数据匹配
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
description: 了解如何将有关数据主题的其他信息上传到 Microsoft Priva。
ms.openlocfilehash: 90ee0e8e21d25954c11113992cbb7ece847c85ab
ms.sourcegitcommit: bbaa4400bc9c7db9bdb2784e3af160daf5d08290
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/27/2022
ms.locfileid: "65059736"
---
# <a name="data-matching-for-subject-rights-requests"></a>使用者权限请求的数据匹配

借助数据匹配，组织可以使 Microsoft Priva 能够根据确切提供的数据值来标识数据主体。 这有助于提高查找数据主体内容的准确性，这些内容对应于内部人员和与之交互的外部用户的数据值。 它还简化了在创建主题权限请求期间手动提供字段的需要，并在主题权限请求和概述磁贴中提供上下文，该磁贴显示具有最多数据主题内容的项目。 若要了解有关该视图的详细信息，请参阅 [Priva 中的查找和可视化个人数据](priva-data-profile.md#items-with-the-most-data-subject-content)。

若要使用数据匹配功能，需要成为隐私管理角色组的成员。 在 [Microsoft Purview 合规性门户](https://compliance.microsoft.com/)中的 Priva 中，在顶部导航中选择 **设置**，然后 **选择数据匹配**。 在此处，需要定义个人数据架构并提供个人数据上传，如下所示。 请注意，可以添加项，并且可以删除添加的项，但不能修改项目。

## <a name="prepare-for-data-import"></a>准备数据导入

在定义架构或上传数据之前，需要标识数据主体信息的源。 所需的文件格式.csv，应用程序（如Microsoft Excel）可以读取该格式。 构造此导出，使列标题显示在第一行中。 这些标头应包含个人数据架构的属性的名称。 检查每个字段中数据的格式。 如果任何数据包含逗号，请使用双引号括住这些值，以确保不会将其分析为单独的字段。

## <a name="define-the-personal-data-schema"></a>定义个人数据架构

设置数据匹配的第一步是定义个人数据架构，该架构将描述数据主体的属性。 你将在数据匹配设置区域的第一个选项卡上传此架构。 所需的文件包括 **个人数据架构** XML 文件和 **规则包** XML 文件。

### <a name="personal-data-schema-xml"></a>个人数据架构 XML

个人数据架构文件是一个 XML 文件，用于定义预期的列名。

- 将此架构文件命名 *为pdm.xml*。
- 使用字段名称标记定义每个列名称，如下面的示例所示。
- 对要搜索的字段使用可搜索 = “true”，最多可搜索 5 个字段。 必须可以搜索至少一个字段名称。 示例语法： `\<Field name="" searchable=""/>`.
- 个人数据架构具有 DataStore 标记部分。 必须将四个必需字段映射到字段名称：primaryKeyField、upnField、firstNameField、lastNameField。

例如，以下 XML 文件定义了一个示例架构，其中五个字段指定为可搜索：PatientID、MRN、SSN、电话 和 DOB。 primaryKeyField 映射到 PatientID，upnField 映射到 MRN，firstNameField 映射到 FirstName，lastNameField 映射到 LastName。

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

设置规则包时，请确保正确引用上面创建的个人数据架构文件：pdm.xml。 在以下示例规则包 XML 中，需要自定义以下字段以创建数据匹配敏感类型：

- **RulePack ID** & **PrivacyMatch ID**：使用 New-GUID 生成 GUID。
- **数据存储**：此字段指定要使用的个人数据匹配查找数据存储。 提供已配置的个人数据架构的定义 DataStore 名称。
- **idMatch**：此字段指向个人数据匹配的主要元素。
  - **匹配**：指定要在精确查找中使用的字段。 提供个人数据架构中的可搜索字段名称。
  - **分类**：此字段指定触发个人数据匹配查找的敏感类型匹配项。 可提供现有内建或自定义敏感信息类型的名称或 GUID。 为了避免导致性能问题，如果在个人数据匹配中使用自定义敏感信息类型作为 Classification 元素，请不要使用与大量内容 (（如“任意数字”或“任何五个字母的单词”) ）匹配的自定义敏感信息类型。 建议添加支持关键字，或在自定义分类敏感信息类型的定义中包括格式设置。
- **匹配**：此字段指向在 idMatch 附近找到的其他证据。
  - **匹配**：在 DataStore 的个人数据架构中提供任何字段名称。
- **资源**：本部分指定多个区域设置中敏感类型的名称和说明。
  - **idRef**：为 ExactMatch ID 提供 GUID。
  - **名称&说明**：根据需要自定义。

在下面的规则包 XML 示例中，我们引用了上一步创建个人数据架构 XML 的pdm.xml示例文件：

- **数据存储：dataStore** 名称引用我们之前创建的架构文件：dataStore = “PatientRecords”。
- **idMatch**：idMatch 值引用前面创建的pdm.xml文件中列出的可搜索字段：idMatch 匹配项 = “SSN”。
  - **分类**：分类值引用现有或自定义敏感信息类型：分类 = “美国社会保障号码 (SSN) ”。 （在此情况下，我们使用美国社会保障号的现有敏感信息类型。）

使用 Unicode 编码) 创建 XML 格式的规则包 (，如以下示例代码所示。 可以复制、修改和使用此示例。

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

## <a name="sensitive-info-types"></a>敏感信息类型

设置数据匹配的第二步是为个人数据匹配创建唯一的敏感信息类型 (PDM) 。 [ (SIT) 的敏感信息类型 ](/microsoft-365/compliance/sensitive-information-type-learn-about)是基于模式的分类器，用于检测诸如社会保障或信用卡号等敏感信息。 通过设置 PDM 敏感信息类型，可以使用确切的数据值而不是泛型值来检测匹配项。 若要开始此步骤，请选择 **“创建 PDM 敏感信息类型** ”以启动创建向导。

## <a name="upload-personal-data"></a>Upload个人数据

定义个人数据架构和敏感信息类型后，第三步是上传个人数据。 转到 **“个人数据上传** ”选项卡，选择 **“添加**”，然后选择在第一步中定义的个人架构，然后上传包含个人数据的文件。

可以通过选择本地文件或向包含个人数据文件的现有Microsoft Azure 存储位置提供 SAS URL 来上传此个人数据。
如果将文件准备为此过程中符合所创建架构的第一步，则可以使用该文件进行上传。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva 法律免责声明](priva-disclaimer.md)
