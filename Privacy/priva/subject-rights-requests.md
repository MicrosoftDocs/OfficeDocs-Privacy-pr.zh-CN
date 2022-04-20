---
title: 了解 Priva 主题权限请求
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
description: Microsoft Priva 中的“主题权限请求”解决方案可帮助你查找个人数据，并协作查看内容和创建报表。
ms.openlocfilehash: 37ee3fc795559d216a7a8cd620cff2c3ca689c2b
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930623"
---
# <a name="learn-about-priva-subject-rights-requests"></a>了解 Priva 主题权限请求

根据世界各地的某些隐私法规，个人 (或 *数据主体*) 可以请求审查或管理公司收集的有关自己的个人数据。 这些请求有时也称为数据主体请求 （DSR）、数据主体访问请求 （DSAR） 或使用者权限请求。 对于存储大量信息的公司来说，查找相关数据可能是一项艰巨的任务。

Microsoft Priva 可通过“使用者权限请求”解决方案帮助你处理这些查询。 它提供工作流、自动化和协作功能，可帮助你搜索主题数据、查看发现、收集相应的文件并生成报表。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>Priva 如何支持主体权限请求履行

主题权限请求周期从个人向组织发出的请求开始。 收到后，可以使用 Priva 的功能来收集数据、协作、查看和创建报表。 然后，可以通知数据主体发现结果，并采取 Priva 外部所需的任何其他操作来满足请求，例如删除数据。 若要帮助管理和自动化工作流，还可以使用集成Power Automate模板。

### <a name="create-requests-and-collect-data"></a>创建请求并收集数据

Priva 提供了强大的搜索选项，用于在组织存储Microsoft 365的内容中查找与数据主题相关的数据。 它还可帮助你确定要查看这些请求的数据中的项的优先级。 Priva 知道 Microsoft Purview 信息保护中的敏感度标签，这些标签指示可能保密且可能需要特别评审的内容，并且会使用这些标签标记项目。 此外，Priva 可以检测和标记可能包含多人数据的项目，在向数据主体提供内容之前，可能需要在其中编辑内容。

若要了解详细信息，请参阅 [“创建主题权限请求](subject-rights-requests-create.md)”。

### <a name="data-matching"></a>数据匹配

通过数据匹配，可以让 Priva 根据确切提供的数据值来标识数据主体。 上传此类信息有助于提高查找内容的准确性，并简化了在创建主题权限请求期间手动提供字段的需求。 它还在主题权限请求和概述磁贴中提供上下文，该磁贴显示包含最多数据主题内容的项。 若要了解详细信息，请参阅 [使用者权限请求的数据匹配](subject-rights-requests-data-match.md)。

### <a name="review-data-and-collaborate-on-requests"></a>查看数据并协作处理请求

收集数据后，可以评估结果，选择要包含在报表和导出中的最相关项，并进行任何必要的修改。 可以在“使用者权限请求”管道中的团队成员之间协作完成此操作。

若要了解详细信息，请参阅 [查看主题权限请求的数据](subject-rights-requests-data-review.md)。

### <a name="fulfill-requests"></a>满足请求

Priva 提供用于创建报表和收集文件以发送回数据主体的工具。 若要了解详细信息，请参阅 [“生成报表”并完成主题权限请求](subject-rights-requests-reports.md)。

### <a name="automate-tasks"></a>自动执行任务

可以使用内置Power Automate模板在 Priva 中创建和自动化工作流进程。 这些模板支持诸如在 ServiceNow 中提交票证或设置日历邀请等任务。 若要了解详细信息，请参阅 [“使用者权限请求”中的自动执行任务](subject-rights-requests-automate.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva 法律免责声明](priva-disclaimer.md)
