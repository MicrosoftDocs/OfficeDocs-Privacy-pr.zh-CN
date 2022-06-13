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
description: 了解Microsoft Priva的全局设置选项。
ms.openlocfilehash: a6f2fe55600d6cc3018c9d15f05a6d9e459a1486
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046596"
---
# <a name="configure-priva-settings"></a>配置 Priva 设置

可以通过选择屏幕右上角的齿轮图标来管理Microsoft Priva的设置。 此处的选项允许设置高级首选项并自定义密钥属性。 本页概述了主要设置类别。

## <a name="anonymization"></a>匿名化

可以在隐私风险管理功能中向某些角色的用户显示匿名版本的用户名。 匿名功能将可识别的显示名称替换为泛型标签，以帮助在查看敏感数据时屏蔽用户的标识。 此选项不适用于“使用者权限请求”解决方案。

## <a name="user-notification-emails"></a>用户通知电子邮件  

隐私风险管理中的策略允许你设置用于评估环境中潜在隐私风险的参数。 检测到策略匹配时，隐私风险管理可以向用户发送一封电子邮件，其中包含有关要采取的纠正措施的建议和隐私培训链接。 在 **设置** 中，可以启用或禁用隐私风险管理作为一个整体的电子邮件通知功能。 如果在设置中关闭通知功能，则将禁用所有电子邮件。 若要了解有关策略的详细信息，请 [参阅在隐私风险管理中创建策略](risk-management-policies.md)。

## <a name="teams-collaboration"></a>Teams collaboration  

将Microsoft Teams功能与Priva 主体权利请求集成，以加强与利益干系人的合作。 选中用于启用 **主题权限请求Microsoft Teams功能的** 复选框会自动为每个请求创建关联的Teams通道。 可以从请求 **的“协作者**”选项卡将用户添加到Teams通道。

打开此功能将对所有请求应用Teams功能。 取消选中框会关闭所有请求的这些功能。 详细了解[数据评审过程中的协作。](subject-rights-requests-data-review.md#collaboration-for-data-review)

## <a name="data-matching"></a>数据匹配  

使用本部分上传描述数据主体属性的数据架构，这将有助于在Microsoft 365环境中搜索个人数据时识别正确的数据主体。 架构和规则包是以 XML 格式创建和上传的。 在 **“个人数据上传**”下，还可以提交与提供的架构匹配的个人数据。 可以创建和上传自己的文件，也可以选择从 Azure 上传个人数据。 详细了解 [使用者权限请求的数据匹配](subject-rights-requests-data-match.md)。

## <a name="data-retention-periods"></a>数据保留期

此设置与Priva 主体权利请求相关。 它允许你控制首选项，以便保留请求关闭后生成的收集的数据和报表的保留时间。 这可以设置为 30 或 90 天，并适用于创建的所有使用者权限请求。 建议验证数据保留期是否符合组织的策略和法律义务。 详细了解 [使用者权限请求的数据保留](subject-rights-requests-reports.md#retention-periods-for-reports-and-data)。

## <a name="data-review-tags"></a>数据审阅标记

数据审阅标记可用于标记在主题权限请求中检索的内容项。 使用此设置区域可以管理标记。 Priva提供三个默认标记：**跟进**、**删除** 和 **更新**。 无法编辑这些标记名称，但你可以为这些标记提供对组织有意义的说明。

Priva还提供了两个自定义标记，你可以为组织命名和定义这些标记。 在编辑名称之前，你会看到这些标记列为 **自定义标记 1** 和 **自定义标记 2** 。

按照以下步骤编辑标记名称和说明：

- 在Priva **设置** 页中，选择 **“数据审阅”标记**。
- 找到要编辑的列表上的标记，然后选择其名称旁边的 **“编辑** 铅笔”图标。
- 在浮出窗格中，在可用字段中进行编辑。 对于系统标记，只能编辑说明。 对于自定义标记，可以编辑名称和说明。
- 完成后，选择“ **提交** ”以保存所做的更改。

标记设置适用于所有使用者权限请求。

详细了解在 [查看主题权限请求的数据时应用标记](subject-rights-requests-data-review.md#apply-tags)。