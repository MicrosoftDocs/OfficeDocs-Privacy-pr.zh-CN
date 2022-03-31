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
description: 了解如何在 Microsoft 管理中心中创建新的主题权限请求。
ms.openlocfilehash: 9de1047950a556b4456fd4453ea8d860a0a01c38
ms.sourcegitcommit: 16dd1c0320bf1c58ad75edbbe2113fc79013f504
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/25/2022
ms.locfileid: "64404606"
---
# <a name="create-a-subject-rights-request"></a>创建主题权限请求

主题权限管理管理员可以通过用户的主"主题权限请求"页面打开新请求。 向导将指导你完成查找有关数据主体的个人数据并启动完成其请求的过程的过程。

还可以选择上传其他材料，以便用户能够根据提供的确切数据值识别数据主体。 若要了解更多信息，请参阅 [主体权限请求的数据匹配](subject-rights-requests-data-match.md)。

## <a name="request-types"></a>请求类型

用户主体权限请求支持三种不同类型的请求：

1. **Access**：提供组织在 Microsoft 365 中存储的数据主体个人信息的摘要。

2. **导出**：提供包含数据主体个人信息的内容项的摘要和导出文件。 这些项目在查看由搜索设置收集的数据期间被审阅并标记为"已包含"。

3. **要跟踪的** 带标记列表：生成在数据审阅期间标记可能需要在一些用户之外执行其他操作的任何文件的摘要。 例如，您可能需要根据数据主体的请求促进删除数据主体的个人信息。 可以在"管理设置"中查看包含的标记，并设置 [组织的自定义标记](priva-settings.md)。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用主题权限请求创建向导

1. 在"[Microsoft 365 合规中心](https://compliance.microsoft.com/)，从左侧导航栏中选择"**用户** 主体权限请求"。

2. 在右上角，选择" **创建请求"**。

3. 在 **"数据主体信息** "页上，添加数据主体的名字和姓氏、电子邮件地址、居住地的国家/地区，并指定他们与贵公司的关系。 然后选择“**下一步**”。

4. 在 **"位置"** 页面上，Microsoft 365要查找数据主体的个人数据的位置。 获取有关位置 [设置的详细信息](#choose-locations)。 完成位置选择后，选择"下一 **步"。**

5. 在 **"搜索设置** "页上，可以更改搜索设置以优化搜索，并选择是否在检索数据之前先获取估计值。 不必在此页面上选择任何选项，这将基于在上一步中指定的位置产生默认搜索。 有关此处的选项的详细信息，请参阅定义 [搜索设置](#define-search-settings)。 准备好继续后，选择“**下一步**”。

6. 在 **"请求类型**"页上，根据 [](#request-types)数据主体希望您处理其数据的内容选择请求类型：**Access**、**Export** 或 **Tagged list for follow up**。 如果他们的请求与特定数据隐私法规相关，则还可以从提供的列表中选择请求以添加更多上下文。 通过设置 (请求) ，可以轻松排序接近或过期的请求，并及时解决它们。 完成后，选择"下一 **步"**。

7. 在 **"请求名称**"上，确认或编辑此请求的名称，并添加可选说明作为参考。 然后选择“**下一步**”。

8. 在" **审阅并完成"** 页上，查看您的选择。 可以编辑任何节。 完成后，选择创建 **请求**。

你的请求将有自己的详细信息页面，并且将在主"主体权限请求"页面上列出。 创建请求后，用户将开始查找你在指定位置提供的数据主体信息的匹配项。 可能需要几分钟时间，才能在请求的详细信息页面上显示数据估计值，具体取决于搜索范围。

## <a name="choose-locations"></a>选择位置

对于每个主题权限请求，您可以将搜索设置为在 sharepoint 和 sharepoint 内的所有或特定位置Exchange数据。 通过将其切换开关移动到"开"位置来 **选择** 位置。 可以选择搜索所有帐户和网站，也可以指定每个位置中的特定帐户或网站。 阅读以下有关每个位置涵盖的内容的详细信息。

- **Exchange**：此选项将在邮箱中查找Exchange以及单个或群组聊天Teams数据。 可以选择搜索组织中所有Exchange帐户，或选择"选择帐户"从"邮箱"**Exchange列表中选择单个** 用户。

- **SharePoint**：此选项将在网站、SharePoint网站OneDrive for Business中查找Teams数据。 可以选择搜索组织中所有SharePoint网站，也可以选择"选择网站"从"网站"SharePoint **列表中选择** 单个用户。

有关标识相应搜索词的帮助，请参阅以下主题：

- **SharePoint网站和 URL**：管理 [SharePoint 管理](/sharepoint/manage-sites-in-new-admin-center)中心中的网站提供了有关如何排序和筛选网站以及如何搜索网站SharePoint指南。 使用此功能可查找在"网站"飞出窗格中的搜索SharePoint **输入** 的 URL。

- **Teams聊天** 和频道：[Get-Team](/powershell/module/teams/get-team) 演示如何通过提供特定属性或信息Microsoft Teams查找团队。

- **OneDrive网站和 URL**：关于OneDrive [URL](/onedrive/list-onedrive-urls#about-onedrive-urls) 提供了有关用户的 URL 的正确格式和属性OneDrive的信息。 使用它可帮助你识别OneDrive网站。

我们建议仔细查看你的选择，以确保确定正确的数据主体。 例如，如果按名称搜索邮箱并查找多个姓名相似的个人，请验证正确的个人，然后再将它们添加到请求中。

## <a name="define-search-settings"></a>定义搜索设置

创建主题权限请求时，默认搜索将基于你在创建向导的"位置 **"** 页上的选择运行。 如果要执行更有针对性的搜索，或者希望选择在检索内容项之前获取数据的估计值，可以在请求创建向导的"搜索设置"页上进行这些选择。

### <a name="advanced-search-options"></a>高级搜索选项

- **优化搜索**：此选项允许您指定其他属性以帮助在组织数据中标识数据主体。 选择此选项后，系统将提示你添加更多搜索参数，如以下优化 [搜索所述](#refine-your-search)。
- **包括数据主体创作的内容**：此选项将查找由数据主体创作的内容。 示例包括数据主体创建SharePoint上载到数据主体的文件。 选择此选项可能会显著增加返回的数据量。
- **包括所有版本的** 项目：如果选择SharePoint作为搜索位置，则默认搜索查询将仅返回当前版本的SharePoint项。 选中此框将返回当前及所有以前版本的SharePoint项目，产生明显更多的数据供你查看。

### <a name="data-estimate"></a>数据估计

" **获取估计值第** 一"选项将估计在自动检索数据之前预期找到的数据。 当您的估计值显示在请求的详细信息页面上时，您可以选择查看搜索结果并预览已发现的项目的采样。 如果项目表示预期结果，则需要选择"检索数据"，才能继续实际检索内容项。

## <a name="refine-your-search"></a>优化搜索

如果在"搜索 **设置**"页上选择"优化搜索"，则当您选择"下一步"时，系统将提示你提供个人属性和条件的详细信息，以进一步定向搜索结果。 您可以在任一类别或这两个类别中添加内容。 在此部分中完成选择后，请求的数据检索将基于搜索设置。

#### <a name="add-personal-attributes"></a>添加个人属性

在文本字段中输入数据主体的姓名、昵称、电子邮件地址和地址的值。 可以添加其他标识符（如出生日期或电话号码）和文本字段支持用分号分隔的多个条目。 完成后，选择"下一 **步"** 继续"条件 **"** 页。

#### <a name="conditions"></a>条件

选择"添加条件"按钮，以从一系列条件中选择以进一步定向搜索，包括项目名称、发件人和收件人名称、个人 数据类型 以及项目是否在组织外部共享。 文本字段支持用分号分隔的多个条目。 完成后，选择"下一步"保存搜索设置并进度到请求类型设置。

## <a name="next-steps"></a>后续步骤

创建请求后，你将在主题权限请求页面上看到它列出。 若要详细了解如何继续查看，请参阅 [查看数据和协作处理请求](subject-rights-requests-data-review.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
