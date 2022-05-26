---
title: Priva 入门
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
description: 了解如何为组织设置Microsoft Priva、设置角色和权限以及配置重要设置。
ms.openlocfilehash: 945cbfd2625be50cb89eeaa8fe09e0effaea79d5
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678209"
---
# <a name="get-started-with-priva"></a>Priva 入门

如果已准备好开始使用Microsoft Priva来帮助组织识别和缓解隐私风险，请按照以下步骤帮助进行设置。

## <a name="confirm-subscriptions-and-licensing"></a>确认订阅和许可

Priva在[Microsoft Purview 合规门户](https://compliance.microsoft.com/)中可用，可由具有以下许可证的组织购买：

- Microsoft 365 E3、E5、A3、A5
- Office 365 E1、E3、E5、A1、A3、A5

Priva为两种不同的解决方案提供许可选项：Priva 隐私风险管理和Priva 主体权利请求。 这些可以单独购买或一起购买。 获取使用者权限请求的许可证时，可以针对需要处理的请求数选择适当的许可层。 可以随时购买其他请求。

有关详细的许可指南，请参阅 [适用于安全性与合规性的 Microsoft 365 许可指南](/office365/servicedescriptions/microsoft-365-service-descriptions/microsoft-365-tenantlevel-services-licensing-guidance/microsoft-365-security-compliance-licensing-guidance#microsoft-priva)。

> [!Note]
> Priva不适用于美国政府Community (GCC) 中度、GCC高或国防部 (DoD) 客户。

### <a name="start-a-free-trial"></a>启动免费试用版

使用免费试用版订阅浏览Priva解决方案的所有功能。 了解如何注册[Priva试用版](priva-trial.md)。

## <a name="enable-the-microsoft-365-audit-log"></a>启用Microsoft 365审核日志

Microsoft 365审核日志是组织内所有活动的摘要。 隐私风险管理策略可以使用这些活动来生成策略见解。

你的组织可能已打开审核日志。 如果需要首次开始使用它们，请参阅 [打开或关闭审核日志搜索](/microsoft-365/compliance/turn-audit-log-search-on-or-off) 以获取启用审核的分步说明。 打开审核之后，将显示一条消息，内容为正在准备审核日志，你可以在准备完成后几个小时内运行搜索。 此操作只需要执行一次。 有关使用Microsoft 365审核日志的详细信息，请[参阅“搜索审核日志](/microsoft-365/compliance/search-the-audit-log-in-security-and-compliance)”。

## <a name="set-user-permissions-and-assign-roles"></a>设置用户权限并分配角色

Priva使用基于角色的访问控制 (RBAC) 权限模型。 只有分配了角色的用户才能访问Priva，并且每个用户允许的操作受角色类型限制。

全局管理员有权访问Priva并将其他用户分配给角色。 他们可以在[Priva的Microsoft Purview 合规门户](https://compliance.microsoft.com/)中登录并设置用户权限。 为了快速入门，隐私管理角色组有权访问Priva的所有功能。 此组可能非常适合同一个人可以执行所有职责的组织。 其他隐私角色允许你进行更精细的控制，并将用户分配到所选的功能或函数。

若要详细了解角色组以及如何授予访问权限，请参阅[在Priva中设置用户权限和分配角色](priva-permissions.md)。

## <a name="start-finding-and-visualizing-your-data"></a>"开始"菜单查找和可视化数据

登录到Priva后，将看到 **“概述**”页。 本页提供有关个人数据在Microsoft 365环境中如何演变的动态见解，以帮助你快速发现问题、识别风险指标并采取措施解决问题。 “概述”应在注册后的头 24 小时内填充初始见解。 继续使用Priva时，概述页将刷新以继续提供当前信息。

为了进一步深入了解随时间推移的数据，**数据配置文件** 页将提供更多的可视化效果和分析功能，并提供组织数据的整体视图（按地理位置和Microsoft 365位置）。

若要了解有关这些页面的详细信息，请参阅[Priva中查找和可视化个人数据](priva-data-profile.md)。

## <a name="start-managing-risks-with-default-policies"></a>"开始"菜单使用默认策略管理风险

隐私风险管理将开始评估数据，并了解数据最小化、数据过度表达和数据传输的关键风险方案。 默认情况下，这些策略处于打开状态。 可以使用这些策略来评估风险所在位置，然后打开用户电子邮件通知，让用户关注问题，并指导解决这些风险。 此外，还可以从提供的策略模板创建和自定义自己的策略。 可以根据与法律顾问协商时确定的符合法律和法规要求，定制策略以满足组织的法律和法规合规性需求。 若要了解详细信息，请参阅 [在隐私风险管理中创建策略](risk-management-policies.md)。

## <a name="get-started-with-subject-rights-requests"></a>使用使用者权限请求开始

Priva 主体权利请求自动执行主题权限请求履行过程，从而轻松访问适合现有业务流程的数据和可自定义工作流。 可以轻松查找相关数据、查看结果并生成报表。 一路上，你可以与组织中的其他专家进行安全协作，以完成主题权限请求。 还可以使用内置模板管理和自定义业务工作流。 若要详细了解如何使用这些功能，请[参阅了解Priva 主体权利请求](subject-rights-requests.md)。

## <a name="priva-availability"></a>Priva可用性

Microsoft Priva可供全球客户使用。 如果组织在下面列出的本地数据中心之一预配了租户以满足数据驻留要求，则Microsoft Purview 合规门户左侧导航中将无法使用Priva解决方案：

- 挪威
- Poland（波兰）
- 卡塔尔
- 新加坡
- 南非
- 韩国
- 西班牙
- 瑞典
- Switzerland（瑞士）
- 阿拉伯联合酋长国

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)
