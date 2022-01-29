---
title: 使用管理入门
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
- MET150fcf
description: 了解如何为组织设置 Microsoft 管理中心、设置角色和权限以及配置重要设置。
ms.openlocfilehash: 62e28361b57dd866b95ce566616473ed1a71e4ad
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248859"
---
# <a name="get-started-with-priva"></a>使用管理入门

如果你已准备好开始使用 Microsoft 管理程序帮助识别和缓解隐私风险，请按照以下步骤设置先决条件并开始探索隐私见解。

## <a name="step-1-confirm-subscriptions-and-licensing"></a>步骤 1：确认订阅和许可

国家/[Microsoft 365 合规中心内提供](https://compliance.microsoft.com/)，并且可供具有以下许可证的组织购买：

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1、E3、E5、A1、A3、A5

同时，还针对以下两个不同的解决方案提供许可选项：Rightsa 隐私风险管理和权限主体权利请求。 可以单独或一起购买。 获取主题权限请求的许可证时，可以选择相应的许可层来处理多少请求。 你随时都可以购买其他请求。

有关详细的许可指南，请参阅 [适用于安全性与合规性的 Microsoft 365 许可指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#privacy-management)。

> [!Note]
> 美国政府国防Community (GCC) 、GCC或国防部 (客户) 。

### <a name="get-free-trial-license"></a>获取免费试用版许可证

可以使用免费试用版许可证开始使用管理。 若要了解资格以及如何加入，请参阅 [了解免费管理试用版](priva-trial.md)。

## <a name="step-2-enable-the-microsoft-365-audit-log"></a>步骤 2：启用Microsoft 365 审核日志

Microsoft 365审核日志是组织中所有活动的摘要。 隐私风险管理策略可以使用这些活动生成策略见解。

你的组织可能已经打开审核日志。 如果需要首次使用它们，请参阅打开或审核日志打开或关闭搜索，[](/microsoft-365/compliance/turn-audit-log-search-on-or-off)了解启用审核的分步说明。 打开审核之后，将显示一条消息，内容为正在准备审核日志，你可以在准备完成后几个小时内运行搜索。 此操作只需要执行一次。 有关使用搜索Microsoft 365 审核日志，请参阅搜索[审核日志](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)。

## <a name="step-3-set-user-permissions-and-assign-roles"></a>步骤 3：设置用户权限和分配角色

Permissiona 使用基于角色的访问控制 (RBAC) 权限模型。 只有分配了角色的用户才能访问"管理"，并且每个用户允许的操作受角色类型限制。

全局管理员有权访问"管理中心"，并将其他用户分配给角色。 他们可以登录并设置用户权限，[Microsoft 365 合规中心用户权限](https://compliance.microsoft.com/)。 为快速入门，隐私管理角色组具有访问管理中心的所有功能的权限。 此组可能非常适合同一个人可能履行所有职责的组织。 其他隐私角色允许你进行更精细的控制，并将用户分配给所选功能。

若要详细了解角色组以及如何授予访问权限，请参阅在管理中设置用户权限和 [分配角色](priva-permissions.md)。

## <a name="step-4-start-finding-and-visualizing-your-data"></a>步骤 4：开始查找和可视化数据

登录到"国家/市/区"后，你将看到" **概述"** 页。 此页面提供有关个人数据在 Microsoft 365 环境中如何发展的动态见解，以帮助你快速发现问题、识别风险指标并采取措施解决问题。 你的概述应在注册前 24 小时内填充初始见解。 当你继续使用"管理"时，概述页面将刷新以继续提供当前信息。

为了进一步深入了解数据，数据配置文件页将提供更多的可视化和分析，并按地理位置和位置提供组织数据的整体Microsoft 365视图。

若要了解有关这些页面的信息，请参阅 [在管理中查找和可视化个人数据](priva-data-profile.md)。

## <a name="step-5-start-managing-risks-with-default-policies"></a>步骤 5：开始使用默认策略管理风险

隐私风险管理将开始评估数据，并让你了解数据最小化、数据过度使用和数据传输的关键风险方案。 默认情况下，这些策略是打开的。 您可以使用这些策略来评估风险在哪里，然后为用户打开用户电子邮件通知，以提醒用户注意问题并指导这些风险的修复。 此外，您还可以从所提供的策略模板创建和自定义自己的策略。 你可以定制策略，以满足与法律顾问联系时可能确定的组织法律和法规合规性需求。 若要了解更多信息，请参阅 [在隐私风险管理中创建策略](risk-management-policies.md)。

## <a name="step-6-get-started-with-subject-rights-requests"></a>步骤 6：主题权限请求入门

用户主体权限请求可自动执行主体权利请求履行流程，从而提供对适合现有业务流程的数据和可自定义工作流的轻松访问。 您可以轻松地查找相关的数据、查看结果并生成报告。 同时，您可以安全地与组织的其他专家协作，以完成主题权限请求。 您还可以使用内置模板管理和自定义业务工作流。 若要了解有关使用这些功能的信息，请参阅 [了解用户主体权限请求](subject-rights-requests.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
