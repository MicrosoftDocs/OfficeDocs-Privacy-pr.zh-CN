---
title: 配置省/市/市/区设置
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
ms.openlocfilehash: d0dfe4fa303a5382e9a673127308fe1bf448062e
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248858"
---
# <a name="configure-priva-settings"></a>配置省/市/市/区设置

可以通过选择屏幕右上角的齿轮图标来管理 Microsoft 用户设置。 此处的选项允许你设置高级首选项和自定义关键属性。 此页概述了主要类别设置概述。

## <a name="anonymization"></a>匿名化

利用此功能，您可以在隐私风险管理功能中向特定角色的用户显示用户名的匿名版本。 它将使用通用标签替换可识别的显示名称，以帮助在查看敏感数据时屏蔽用户的身份。 此选项不适用于"主体权限请求"解决方案。

## <a name="user-notification-emails"></a>用户通知电子邮件  

隐私风险管理中的策略允许你设置用于评估环境中的潜在隐私风险的参数。 当我们检测到策略匹配时，隐私风险管理会向用户发送电子邮件，提供要采取的更正措施的建议以及指向隐私培训的链接。 在设置中，可以整体启用或禁用隐私风险管理的电子邮件通知功能。 如果通知功能在电子邮件设置，将禁用所有电子邮件。 若要了解有关策略的信息，请参阅 [在隐私风险管理中创建策略](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams collaboration  

将Microsoft Teams权限请求集成在一起，以增强与利益干系人之间的协作。 每次创建主题权限请求时，都会在请求中创建Teams。 可以从请求的协作者选项卡将用户添加到团队。若要详细了解主题权限请求，请参阅 [了解 Rightsa Subject Rights Requests](subject-rights-requests.md)。

## <a name="data-matching"></a>数据匹配  

使用此部分可上载描述数据主体的属性的数据架构，这有助于在数据环境中搜索个人数据时Microsoft 365主体。 以 XML 格式创建和上载架构和规则包。 在 **"个人数据上载**"下，还可以提交与提供的架构匹配的个人数据。 你可以创建和上传你自己的文件，也可以选择从 Azure 上传个人数据。 若要详细了解主题权限请求，请参阅 [了解 Rightsa Subject Rights Requests](subject-rights-requests.md)。

## <a name="data-retention-periods"></a>数据保留期

此设置与权限主体权限请求相关。 它允许您控制您希望在关闭请求后保留所收集的数据和报告所生成的首选项。 这可设置为 30 天或 90 天。 请验证这些数据保留期是否符合您的策略和法律要求。 若要详细了解主题权限请求，请参阅 [了解 Rightsa Subject Rights Requests](subject-rights-requests.md)。

## <a name="data-review-tags"></a>数据审阅标记

管理用于标记在主题权限请求中检索的文件的标记。 这些标记可用于指示需要进一步关注的内容，例如可能需要手动删除的内容。 在设置的这一部分中，您可以编辑自定义标记的名称和说明。 还可以编辑系统提供的内置标记的标记说明。 无法更改系统标记的名称。 若要了解有关主题权限请求的信息，请参阅 [查看主题权限请求的数据](subject-rights-requests-data-review.md#step-3-review-data)。
