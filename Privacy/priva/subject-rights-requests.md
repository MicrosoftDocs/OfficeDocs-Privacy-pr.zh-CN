---
title: 了解权限主体权限请求
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
description: Microsoft 管理中心中的"主体权限请求"解决方案可帮助你查找个人数据，并协作查看内容和创建报告。
ms.openlocfilehash: 2aba05ded8940331cedf21fdf67861f5fe403dac
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248947"
---
# <a name="learn-about-priva-subject-rights-requests"></a>了解权限主体权限请求

根据全球的某些隐私法规， (或数据) 可以请求查看或管理公司收集的有关自己的个人数据。 这些请求有时也称为数据主体请求 （DSR）、数据主体访问请求 （DSAR） 或使用者权限请求。 对于存储大量信息的公司，查找相关的数据可能是一项非常强大的任务。

Microsoft 用户可以通过主题权限请求解决方案处理这些查询。 它提供了工作流、自动化和协作功能，有助于搜索主题数据、查看发现内容、收集相应的文件和生成报告。

## <a name="how-priva-supports-subject-rights-request-fulfillment"></a>用户如何支持主体权利请求履行

主体权限请求周期从个人向组织提出请求开始。 一旦收到，你可使用一些功能收集该数据、协作、审阅和创建报告。 然后，你可以通知数据主体你的发现，并执行在一些操作之外需要执行的其他操作，如删除数据。 为了帮助管理工作流并自动执行工作流，您还可以利用用户集成工作流Power Automate模板。

![主题权限请求的工作流。](../media/priva-srr-cycle.png)

### <a name="create-requests-and-collect-data"></a>创建请求并收集数据

国家/部门提供了强大的搜索选项，用于查找与组织存储在 Microsoft 365 中的内容中数据主体Microsoft 365。 它还可帮助你在为这些请求收集的数据中确定要审阅的项目的优先级。 省/市/Microsoft 信息保护识别敏感度标签，这些标签指示可能机密的内容，可能需要进行特殊审查，并标记带这些标签的项目。 此外，在将内容提供给数据主体之前，可能需要修订其中可能包含多个人员的数据的项目，并且可检测并标记这些项。

若要了解更多信息，请参阅 [创建主题权限请求](subject-rights-requests-create.md)。

### <a name="data-matching"></a>数据匹配

通过数据匹配，你可以启用"管理"以根据提供的确切数据值标识数据主体。 上载这种类型的信息可帮助提高内容定位的准确性，并简化了创建主题权限请求期间手动提供字段的要求。 它还提供主题权限请求中的上下文，以及展示具有最多数据主体内容的项的"概述"磁贴。 若要了解更多信息，请参阅 [主体权限请求的数据匹配](subject-rights-requests-data-match.md)。

### <a name="review-data-and-collaborate-on-requests"></a>查看数据并协作处理请求

收集数据后，您可以评估结果，选择要包括在报告和导出中的最相关的项目，并进行必要的修订。 这可以在主题权限请求管道内由团队成员协作完成。

若要了解更多信息，请参阅 [查看主体权限请求的数据](subject-rights-requests-data-review.md)。

### <a name="fulfill-requests"></a>完成请求

用户可以使用数据主体创建报表和收集文件，以发送回数据主体。 若要了解更多信息，请参阅 [生成报告并履行主题权限请求](subject-rights-requests-reports.md)。

### <a name="automate-tasks"></a>自动执行任务

可以使用内置的工作流模板在一个功能区内创建和自动Power Automate流程。 这些模板支持 ServiceNow 中的归档票证或设置日历邀请等任务。 若要了解更多信息，请参阅自动 [执行主题权限请求中的任务](subject-rights-requests-automate.md)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
