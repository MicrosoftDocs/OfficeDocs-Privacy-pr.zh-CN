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
ms.openlocfilehash: b906fbc3a07ac67cec2c2a4b0433065d42c665e2
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248922"
---
# <a name="create-a-subject-rights-request"></a>创建主题权限请求

主题权限管理管理员可以通过用户的主"主题权限请求"页面打开新请求。 向导将指导你完成查找有关数据主体的个人数据并启动完成其请求的过程的过程。

还可以选择上传其他材料，以便用户能够根据提供的确切数据值识别数据主体。 若要了解更多信息，请参阅 [主体权限请求的数据匹配](subject-rights-requests-data-match.md)。

## <a name="use-the-subject-rights-request-creation-wizard"></a>使用主题权限请求创建向导

1. In the [Microsoft 365 合规中心](https://compliance.microsoft.com/)， go to the Rightsa section and select **RightsA Subject Rights Requests**.
1. 若要启动新请求，请选择" **创建请求"**。
1. 确定提出请求的数据主体并指定他们与贵公司的关系。
1. 我们将对与数据主体相关的项目运行默认搜索。 如果你想要在检索数据之前优化搜索或获取估计值，可以在此阶段进行这些选择。 还可以保留所有项为空，并进入下一步。 有关选项的详细信息，请参阅定义[搜索设置和](#define-search-settings)[优化搜索](#refine-your-search)。
1. 根据数据主体希望你使用其数据执行哪些操作，选择请求类型。 如果他们的请求与特定数据隐私法规相关，则还可以从提供的列表中选择请求以添加更多上下文。 将截止时间 (设置为) 可以轻松排序接近或过期的请求，并及时解决它们。 请求类型包括：
   - **Access**：提供组织在 Microsoft 365 中存储的数据主体个人信息的摘要。
   - **导出**：提供数据主体个人信息的摘要和导出，在查看过程中收集并添加注释。
   - **用于跟进的** 带标记列表：生成用户在审阅期间标记可能需要在"管理"之外执行其他操作的任何文件的摘要。 例如，您可能需要根据数据主体的请求促进删除数据主体的个人信息。 可以在全局策略中管理主题权限请求的自定义数据审阅 **设置。**
1. 确认此请求的名称，并添加可选说明供参考。
1. 查看在上一步骤中输入内容摘要。 选择"创建请求"之前，可以 **编辑任何字段**。

### <a name="define-search-settings"></a>定义搜索设置

创建主题权限请求时，可以选择以下一个或全部搜索选项来查找有关主题的数据：

- **包括数据主体创作的内容**：这包括由数据主体创作的内容，并且可能会返回更多数据。
- **优化搜索**：这将允许你指定有助于标识数据主体的额外属性。 你可以在此处将搜索范围Microsoft 365特定的服务或资源，或选择其他条件来调整请求的范围。 选择此选项后，系统将提示您输入自定义搜索参数。
- **首先获取估计** 值：这使你可以查看在自动检索数据之前，我们希望找到多少数据。

### <a name="refine-your-search"></a>优化搜索

如果在定义搜索设置时选择优化搜索，将要求您填写高级搜索参数。 您可以添加 **标识符、** 设置 **条件** 并选择要搜索Microsoft 365特定位置。

- **添加标识符**：提供有关数据主体的更多标识信息，如姓名、电子邮件地址和/或其他选项。 用分号分隔每个字段中的多个值。
- **条件**：通过从下拉列表选择类型开始为搜索添加条件。 这些类型对应于数据可能的属性，如时间范围、大小、保留标签、发件人和收件人以及许多其他属性。 选择任意类型进行添加，然后设置所需的属性。 对于文本字段条目，可以添加用分号分隔的多个关键字。 您可以添加任何需要的内容类型。
- **位置**：可以将搜索范围确定为SharePoint网站、Teams频道OneDrive for Business位置。 对于每个位置，可以选择所有实例（如所有Exchange邮箱）或特定实例（如一个用户的邮箱）。 选择每个 **位置** 的"选择..."链接选项以输入有关特定实例的信息。 有关标识相应搜索词的帮助，请参阅以下内容：
  - [管理新网站管理](/sharepoint/manage-sites-in-new-admin-center)SharePoint：提供有关如何排序和筛选网站以及如何搜索网站SharePoint指南。 使用此查询查找搜索SharePoint URL。
  - [Get-Team](/powershell/module/teams/get-team)：提供有关如何按特定属性/信息Microsoft Teams团队的信息。 使用它可帮助你识别Teams和频道。
  - [关于OneDrive URL](/onedrive/list-onedrive-urls#about-onedrive-urls)：提供有关用户的 URL 的正确格式和属性OneDrive的信息。 使用它可帮助你识别OneDrive网站。

我们建议仔细查看你的选择，以确保确定正确的数据主体。 例如，如果按名称搜索邮箱并查找多个姓名相似的个人，请验证正确的个人，然后再将它们添加到请求中。

## <a name="next-steps"></a>后续步骤

创建请求后，你将在主题权限请求页面上看到它列出。 若要详细了解如何继续查看，请参阅 [查看数据和协作处理请求](subject-rights-requests-data-review.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
