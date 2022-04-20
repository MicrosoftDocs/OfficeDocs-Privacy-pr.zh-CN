---
title: 创建主题权限请求
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
description: 了解如何在 Microsoft Priva 中创建新的主题权限请求。
ms.openlocfilehash: b2d846aa4020be315705bbd16e00378c7514146c
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930603"
---
# <a name="create-a-subject-rights-request"></a>创建主题权限请求

使用者权限管理管理员可以通过 Priva 的主要“主题权限请求”页打开新请求。 向导将指导你完成查找有关数据主体的个人数据并开始完成其请求的过程的过程。

还可以选择上传其他材料，使 Priva 能够根据确切提供的数据值来识别数据主体。 若要了解详细信息，请参阅 [使用者权限请求的数据匹配](subject-rights-requests-data-match.md)。

## <a name="request-types"></a>请求类型

Priva 使用者权限请求支持三种不同类型的请求：

1. **访问**：提供组织在Microsoft 365中保存的数据主体的个人信息摘要。

2. **导** 出：提供包含数据主体个人信息的内容项的摘要和导出文件。 这些项目在查看搜索设置收集的数据时已审阅并标记为 **“包含** ”。

3. **用于跟进的标记列表**：生成在数据评审期间标记的任何文件的摘要，这些文件可能需要在 Priva 之外执行其他操作。 例如，可能需要根据数据主体的请求帮助删除其个人信息。 可以在 [Priva 设置](priva-settings.md)中查看包含的标记并为组织设置自定义标记。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用使用者权限请求创建向导

1. 在 [Microsoft Purview 合规性门户](https://compliance.microsoft.com/)中，转到“Priva”部分，然后选择 **“Priva 主题权限请求**”。
1. 若要启动新请求，请选择 **“创建请求**”。
1. 确定发出请求的数据主体，并指定他们与公司的关系。
1. 我们将对与数据主题相关的项运行默认搜索。 如果要在检索数据之前优化搜索或获取估计值，可在此阶段进行这些选择。 还可以将所有项留空并转到下一步。 有关选项的详细信息，请参阅 [“定义搜索设置](#define-search-settings) ”并 [优化搜索](#refine-your-search)。
1. 根据数据主体希望你对其数据执行的操作，选择请求类型。 如果他们的请求与特定的数据隐私法规相关，也可以从提供的列表中选择它以添加更多上下文。 设置所需的截止时间 () 可以轻松排序以处理或逾期请求，并及时解决。 请求类型包括：
   - **访问**：提供组织在Microsoft 365中保存的数据主体的个人信息摘要。
   - **导出**：提供数据主体的个人信息的摘要和导出，如审阅期间收集和批注的那样。
   - **标记的后续列表**：生成用户在评审期间标记的任何文件的摘要，这些文件可能需要在 Priva 之外执行其他操作。 例如，可能需要根据数据主体的请求帮助删除其个人信息。 可以在全局设置中管理主题权限请求的自定义数据评审标记 **。**
1. 确认此请求的名称，并添加可选的引用说明。
1. 查看在前面的步骤中输入的内容的摘要。 在选择 **“创建”请求** 之前，可以编辑任何字段。

对于每个主题权限请求，可以将搜索设置为在 Exchange 和 Sharepoint 中的所有或特定位置查找数据。 通过将其切换开关移动到 **On** 位置来选择位置。 可以选择搜索所有帐户和网站，或指定每个位置内的特定帐户或网站。 阅读下面有关每个位置所涵盖内容的详细信息。

- **Exchange**：此选项将在Exchange邮箱以及单独或组Teams聊天中查找数据。 可以选择搜索组织中的所有Exchange帐户，或选择 **“选择帐户**”，从 **Exchange邮箱** 浮出窗格中选择单个用户。

- **SharePoint**：此选项将在SharePoint站点、OneDrive for Business站点和Teams通道中查找数据。 可以选择搜索组织中的所有SharePoint网站，或选择 **“选择网站**”，从 **SharePoint网站** 浮出窗格中选择单个用户。

有关识别相应搜索词的帮助，请参阅以下主题：

- **SharePoint网站和 URL**：[管理SharePoint管理中心的网站](/sharepoint/manage-sites-in-new-admin-center)，提供有关如何对网站进行排序和筛选以及如何搜索SharePoint网站的指导。 使用此功能可在SharePoint **站点** 浮出窗格上的搜索字段中查找要输入的 URL。

- **Teams聊天和频道**：[Get-Team](/powershell/module/teams/get-team) 演示如何通过提供特定属性或信息在Microsoft Teams中查找团队。

- **OneDrive站点和 URL**：[关于OneDrive URL](/onedrive/list-onedrive-urls#about-onedrive-urls) 提供有关用户OneDrive URL 的正确格式和属性的信息。 使用此方法可帮助你识别搜索中的OneDrive网站。

建议仔细查看所选内容，以确保确定正确的数据主体。 例如，如果按名称搜索邮箱并找到多个名称相似的个人，请在将邮箱添加到请求之前验证正确的邮箱。

## <a name="define-search-settings"></a>定义搜索设置

创建主题权限请求时，将根据创建向导的“ **位置** ”页上的选择运行默认搜索。 如果要进行更有针对性的搜索，或者如果要在检索内容项之前选择获取数据估算，则可以在请求创建向导的 **“搜索设置”** 页上进行这些选择。

### <a name="advanced-search-options"></a>高级搜索选项

- **优化搜索**：此选项允许指定其他属性，以帮助在组织的数据中识别数据主体。 选择此选项后，系统会提示添加更多搜索参数，下面在 [“优化搜索](#refine-your-search)”中进行了说明。
- **包括由数据主体创作的内容**：此选项将查找由数据主体创作的内容。 示例包括由数据主体创建或上传到SharePoint者的文件。 选择此选项可能会显著增加返回的数据量。
- **包括所有版本的项目**：如果选择SharePoint作为搜索位置，默认搜索查询将仅返回当前版本的SharePoint项。 选中此框将返回当前和所有以前版本的SharePoint项，从而产生大量数据供你查看。

### <a name="data-estimate"></a>数据估算

“ **获取估算第一个** ”选项将显示在自动检索数据之前预期要查找的数据量的估计值。 当估算显示在请求的详细信息页上时，可以选择查看搜索结果并预览已发现的项的采样。 如果项目表示预期的结果，则需要选择 **“检索数据** ”，以继续实际检索内容项。

## <a name="refine-your-search"></a>优化搜索

如果在 **“搜索设置”** 页上选择 **“优化搜索**”，则在选择 **“下一步**”时，系统会提示你提供个人属性和条件的详细信息，以进一步定位搜索结果。 可在任一类别或两个类别中进行添加。 完成本部分中的选择后，请求的数据检索将基于搜索设置。

#### <a name="add-personal-attributes"></a>添加个人属性

在文本字段中输入数据主体名称、昵称、电子邮件地址和地址的值。 可以添加其他标识符，例如出生日期或电话号码，文本字段支持多个用分号分隔的条目。 完成后，选择 **“下一步** ”以继续访问 **“条件”** 页。

#### <a name="conditions"></a>条件

选择 **“添加条件** ”按钮可在一系列条件中进行选择，以进一步定位搜索，包括项目名称、发件人和收件人姓名、个人数据类型，以及项目是否在组织外部共享。 文本字段支持用分号分隔的多个条目。 完成后，选择 **“下一步** ”以保存搜索设置并将其进度保存到请求类型设置。

## <a name="next-steps"></a>后续步骤

创建请求后，会在主题权限请求页上看到它。 若要详细了解如何继续查看，请 [参阅“查看数据”并协作处理请求](subject-rights-requests-data-review.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva 法律免责声明](priva-disclaimer.md)
