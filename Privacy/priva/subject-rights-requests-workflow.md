---
title: 使用者权限请求的工作流
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
description: 了解Microsoft Priva 主体权利请求中的工作流步骤和请求详细信息页。
ms.openlocfilehash: 794176260f6377862d34a66dc71cef1e811188b9
ms.sourcegitcommit: fe651dab4c89e67b21d37531c04e3996b7af1138
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2022
ms.locfileid: "66060080"
---
# <a name="understand-the-workflow-and-request-details-pages"></a>了解工作流和请求详细信息页

**本文**：了解在创建和处理请求时所执行的进度步骤。 了解如何在每个请求的详细信息页上使用见解和功能。

在“主题权限请求”解决方案中[创建请求](subject-rights-requests-create.md)时，你提供的信息用于查找有关组织Microsoft 365环境中的数据主题的匹配项。 匹配项符合要求，以便查看、选择要包含的内容，并根据需要修改信息。 多个用户可以在“使用者权限请求”界面中协作执行这些步骤。 请求的 [“概述](#overview-tab) ”页提供有关进度阶段的状态以及有关后续步骤的指南。

## <a name="progress-stages-for-requests"></a>请求的进度阶段

每个请求都会经历多个阶段。 某些阶段自动进行，其他阶段在完成某些步骤（如查看文件）后手动高级。

- **数据估计**：在检索数据之前，Priva估计其预期查找的数据量。 根据数据量，请求可能或可能不会自动移动到下一阶段的数据检索。 在收集数据之前，可以将请求设置为在估算阶段暂停;详细了解 [数据估算和检索](subject-rights-requests-data-retrieval.md)。

- **检索数据**：将所有文件、电子邮件、聊天、图像和其他内容项拉到一起。 此阶段完成后，请求会自动移动到下一阶段查看数据。 详细了解 [数据估算和检索](subject-rights-requests-data-retrieval.md)。

- **查看数据**：协作者查看收集的所有数据，确定与请求相关的数据，并执行编辑文件和添加案例说明等任务。 详细了解如何 [查看主题权限请求的数据](subject-rights-requests-data-review.md)。 完成数据评审后，手动转到下一阶段以生成报表。

- **生成报表**：完成数据评审后，用户会手动转到此步骤。 Priva生成最终报表，其中包括要与数据主体共享的数据包，以及组织记录的内部报表。 详细了解 [如何生成报表](subject-rights-requests-reports.md)。

- **关闭请求**：所有工作完成后，关闭请求以指示该请求已被视为已完成。 详细了解如何 [生成报表](subject-rights-requests-reports.md) ，以便能够完成并关闭请求。

## <a name="understanding-the-request-details-page"></a>了解请求详细信息页

从 Microsoft Purview 合规性门户的左侧导航中选择 **Priva 主体权利请求**，以访问组织创建的请求并查看其状态。 主“使用者权限请求”页上的状态卡（如下所示）显示活动、已关闭和过期请求数，以及顶部请求类型。 状态卡下表列出了组织创建的所有请求，其中最近创建的请求位于顶部。

**使用者权限请求主页：** 
![使用者权限请求主页。](../media/priva-srr-overview.png)

若要打开请求的详细信息页，请从表中选择请求名称。 可在此处详细了解请求的属性、搜索结果和请求的状态。 下面显示的详细信息页将成为你的工作和协作中心，用于管理找到的文件、创建报表和导出以及完成请求。

**请求详细信息页：**
![“主题权限请求详细信息”页。](../media/priva-srr-detailspage.png)

### <a name="overview-tab"></a>“概述”选项卡

请求详细信息页的 **“概述** ”选项卡提供有关请求的详细信息、显示当前步骤的进度指示器以及有关找到的数据的关键信息。 此页包含下面所述的单个状态卡。

##### <a name="details"></a>详细信息

**“详细信息**”卡片显示基本信息，使你能够访问请求，例如其截止日期、创建日期、说明和相关隐私法规。

##### <a name="progress"></a>Progress

**进度** 卡列出了过程中的每个步骤：数据估算、检索数据、查看数据、生成报表和关闭请求。 该步骤旁边的一个填充的蓝色圆圈指示当前正在执行的步骤。 蓝色圆圈内的复选标记表示步骤已完成。 空白的空圆表示该步骤尚未启动。

##### <a name="data-estimate-summary"></a>数据估算摘要

当请求在 [数据估算阶段](subject-rights-requests-data-retrieval.md#data-estimate)暂停时，**将显示数据估算摘要** 卡片。 它显示搜索预期要检索的项的位置和数量。

##### <a name="total-number-of-items-found"></a>找到的项总数

**找到的卡片的项总数** 显示找到的内容项数及其在Microsoft 365中的位置。

##### <a name="priority-items-to-review"></a>要审阅的优先级项目

要查看磁贴的 **“优先级”项目** 显示在开始审阅时可能需要确定优先级的项目。 该磁贴显示属于以下类别的项计数：
- **机密**：这些项目应用了 [Microsoft 敏感度标签](/microsoft-365/compliance/sensitivity-labels) 。 例如，具有“高度机密”标签的 Word 文档。 
- **多人数据**：这些项目包含多个人员的个人数据。 如果要将这些项作为最终数据包的一部分，则需要在文件中编辑不相关的数据。 获取 [有关查看数据的详细信息](subject-rights-requests-data-review.md)。 为了Priva标识具有多人数据的项目，组织需要[为主题权限请求设置数据匹配](subject-rights-requests-data-match.md)。

**如何查找优先级项：**

首先，请按照以下步骤，确保已在 **数据收集** 的项表中启用了它们的视图：

- 在 **“收集的数据”** 选项卡上，选择项列表顶部的“ **自定义”列** 。
- 在 **“编辑列”** 浮出窗格中，在 **“优先级”类型** 旁边进行检查。
- 选择“**应用**”。 项目列表现在将具有“ **优先级类型** ”列。

现在，可以通过对 **“优先级”类型** 列进行排序以对类似类型进行分组来标识优先级项并找到它们。

### <a name="data-collected-tab"></a>收集的数据选项卡

识别出与搜索设置匹配的所有项目后，会在“ **数据收集** ”选项卡上收集并显示它们。项列表旁边是一个预览屏幕，用于查看每个项、进行修订以及将项目标记为包含或排除为请求的一部分。 阅读有关 [数据评审和协作步骤](subject-rights-requests-data-review.md)的更多详细信息。

### <a name="notes-tab"></a>“备注”选项卡

“ **备注** ”选项卡允许协作者输入有关在请求上完成的工作的备注。 对于处理请求但不会包含在最终报表中或以其他方式与数据主体共享的每个人，这些备注都可见。

### <a name="collaborators-tab"></a>“协作者”选项卡

“协作者”选项卡显示所有受邀协作处理所收集数据的用户，以及请求的任何关联Teams通道。 请求的创建者自动列为协作者。 通过选择 **“添加协作者** ”命令并输入用户的名称从列表中选择新协作者来邀请新协作者。 了解有关[数据评审协作的](subject-rights-requests-data-review.md#collaboration-for-data-review)更多详细信息

### <a name="reports-tab"></a>报告选项卡

“ **报** 表”选项卡显示在进入“生成报表”阶段时自动生成的所有 **报表** 。 报表分为两个类别：用于与数据主体共享的报表，以及用于组织内部使用的报表。 获取有关 [使用报表的](subject-rights-requests-reports.md)详细信息。

### <a name="history-tab"></a>“历史记录”选项卡

“ **历史记录** ”选项卡汇总了请求的顶级事件，包括包含、排除和修改的项目数的进度阶段更改和聚合。

## <a name="next-steps"></a>后续步骤

访问 [“创建主题权限”请求](subject-rights-requests-create.md) ，了解如何通过第一个请求进行说明。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)