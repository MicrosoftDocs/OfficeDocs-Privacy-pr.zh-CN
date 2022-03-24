---
title: 配置 Priva 设置
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: 了解 Microsoft 用户全局设置选项。
ms.openlocfilehash: 1cbb508d8c1dd98dfa846595d81e8aaeecdbaeb4
ms.sourcegitcommit: 02921b2dd438a517191522567908046b136a89e2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "63758421"
---
# <a name="configure-priva-settings"></a>配置 Priva 设置

可以通过选择屏幕右上角的齿轮图标来管理 Microsoft 用户设置。 此处的选项允许你设置高级首选项和自定义关键属性。 此页面概述了主要类别设置概述。

## <a name="anonymization"></a>匿名化

可以在隐私风险管理功能中向特定角色的用户显示用户名的匿名版本。 匿名功能将可识别的显示名称替换为通用标签，以帮助在查看敏感数据时屏蔽用户的身份。 此选项不适用于"主体权限请求"解决方案。

## <a name="user-notification-emails"></a>用户通知电子邮件  

隐私风险管理中的策略允许你设置用于评估环境中的潜在隐私风险的参数。 当检测到策略匹配时，隐私风险管理会向用户发送电子邮件，提供要采取的更正操作的建议以及指向隐私培训的链接。 在 **设置** 中，可以整体启用或禁用隐私风险管理的电子邮件通知功能。 如果在邮件中关闭通知设置，将禁用所有电子邮件。 若要了解有关策略的信息，请参阅 [在隐私风险管理中创建策略](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams collaboration  

将Microsoft Teams权限请求集成在一起，以增强与利益干系人之间的协作。 每次创建主题权限请求时，都会在权限请求中创建Teams。 可以从请求的协作者选项卡将用户添加到团队。若要详细了解主题权限请求，请参阅 [了解 Rightsa Subject Rights Requests](subject-rights-requests.md)。

## <a name="data-matching"></a>数据匹配  

使用此部分可上载描述数据主体的属性的数据架构，这有助于在用户环境中搜索个人数据时Microsoft 365主体。 以 XML 格式创建和上载架构和规则包。 在 **"个人数据上载**"下，还可以提交与提供的架构匹配的个人数据。 你可以创建和上传你自己的文件，也可以选择从 Azure 上传个人数据。 若要详细了解主题权限请求，请参阅 [了解 Rightsa Subject Rights Requests](subject-rights-requests.md)。

## <a name="data-retention-periods"></a>数据保留期

此设置与权限主体权限请求相关。 它允许您控制您希望在关闭请求后保留收集的数据和报告生成的首选项。 这可设置为 30 天或 90 天，并适用于您创建的所有主体权限请求。 我们建议验证数据保留期是否符合组织的策略和法律要求。 详细了解如何 [设置主体权限请求的数据保留](subject-rights-requests-reports.md#manage-data-retention)。

## <a name="data-review-tags"></a>数据审阅标记

数据审阅标记可用于标记在主题权限请求中检索的内容项。 此区域设置允许你管理标记。 用户提供了三个默认标记 **：跟踪****、删除****和更新**。 无法编辑这些标记名称，但您可以提供对组织有意义的这些标记的说明。

该标记还提供两个自定义标记，你可以为组织使用命名和定义这些标记。 在编辑名称之前，你将看到这些列为 **"自定义标记 1** "和" **自定义标记 2** "。

按照以下步骤编辑标记名称和说明：

- 从"**用户设置，** 选择 **"数据审阅标记"**。
- 在要编辑的列表上查找标记，然后选择其名称旁边的"编辑铅笔"图标。
- 在飞出窗格中，在可用字段中进行编辑。 对于系统标记，只能编辑说明。 对于自定义标记，可以编辑名称和说明。
- 完成后，选择提交 **以** 保存更改。

标记设置适用于所有主体权限请求。

详细了解在 [查看主体权限请求的数据时应用标记](subject-rights-requests-data-review.md#apply-tags)。