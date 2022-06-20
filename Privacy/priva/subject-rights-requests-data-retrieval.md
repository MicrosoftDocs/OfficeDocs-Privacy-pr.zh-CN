---
title: 使用者权限请求中的数据估计和检索
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
description: 了解如何检索数据，以及如何修改Microsoft Priva 主体权利请求中的搜索设置。
ms.openlocfilehash: a2586e987f7a03905feedfd587aab43dba3d9e6b
ms.sourcegitcommit: 8cbafebb1a1b26a0bd92e500a1e6d6c60243c64b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/20/2022
ms.locfileid: "66166661"
---
# <a name="data-estimate-and-retrieval"></a>数据估计和检索

**本文**：了解主题权限请求的数据估计和数据检索阶段。 了解如何查看请求的搜索查询并进行编辑以优化搜索。

## <a name="data-estimate"></a>数据估算
创建请求后，Priva立即开始在Microsoft 365环境中查找与数据主体在内容中的匹配项。 确定我们认为符合条件的所有项后，你将在请求的 **“概述**”页上 **的数据估算摘要** 卡中看到估算。 搜索范围内的数据量将影响完成估算所需的时间长度。

请求将自动移动到 **数据检索** 的下一阶段，其中所有内容项将汇集在一起，以便利益干系人协作查看数据。 在某些情况下，我们会在开始检索之前暂停数据估计，并通知你后续步骤，然后再继续。

### <a name="pause-in-data-estimate"></a>数据估计暂停

请求在 **数据估算** 阶段暂停的原因有两个：

1. 创建请求时，可以选择先获取估算。 有关详细信息，请参阅 [创建自定义请求](subject-rights-requests-create.md#custom-setup-guided-process-to-choose-all-settings) 的步骤 6。

2. 如果预计估算将返回大量项以查看 (超过 10，000 个项) ，则工作流将暂停。 此时，可以预览结果并决定是 [编辑搜索查询](subject-rights-requests-create.md#refining-your-search) 还是继续检索标识的项目。

当请求在 **数据估算** 处暂停时，你将在请求的详细信息页上看到一张卡片，其中包含有关项数、卷、其位置的摘要信息，以及一个允许查看 **搜索查询详细信息** 的链接。

![数据估算卡。](../media/priva-srr-data-estimate.png)

## <a name="view-and-edit-search-queries"></a>查看和编辑搜索查询

若要查看有关请求搜索的详细信息，请在 **数据估算摘要** 卡上选择 **“查看搜索查询详细信息**”。 将打开一个浮出窗格，该窗格汇总查询并显示有关找到内容的更多详细信息。 在此处，有以下选项：

- 选择 **预览结果** 以获取将在当前搜索设置下返回的内容类型的预览。
- 选择 **“编辑搜索查询** ”以更改搜索设置。

选择 **“编辑搜索查询**”时，将引导你完成一个引导式过程，以更改或添加属性以标识数据主体、更改条件，并调整希望搜索覆盖的位置。 按照 [优化搜索](subject-rights-requests-create.md#refining-your-search) 的说明获取更详细的信息。 可以查看新搜索查询的最终版本，然后选择 **“保存** ”以重新开始搜索。

将生成新的估计值，请求的状态将返回到 **数据估计**。 新的搜索可能需要长达 60 分钟才能完成。 完成后，将在请求的详细信息页上看到更新的结果。

准备好继续操作后，选择屏幕右上角的 **“检索数据** ”以进入数据检索阶段。

## <a name="retrieve-data"></a>检索数据

数据检索阶段是检索包含数据主体个人数据的所有文件、电子邮件、聊天、图像和其他内容项。 这些项目放在一个Azure Blob 存储容器中供审阅。 数据检索可能需要几分钟或更长的时间，具体取决于数据量。

此阶段完成后，请求会自动移动到 **“审阅”数据** 的下一阶段。

## <a name="next-steps"></a>后续步骤

访问 [评审数据以获取主题权限请求](subject-rights-requests-data-review.md) ，了解关键任务，并与利益干系人协作 **以完成“审阅”数据** 步骤。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)