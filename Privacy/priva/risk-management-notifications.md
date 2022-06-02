---
title: 隐私风险管理中的用户通知
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
- M365-priva-privacy-risk-management
search.appverid:
- MOE150
- MET150
description: 了解如何向内容所有者通知Microsoft Priva 隐私风险管理找到的策略匹配项，以及如何使用这些电子邮件通知来修正问题。
ms.openlocfilehash: ae02d3bca9c63f8645cd9671628de61d83cb6117
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851647"
---
# <a name="user-notifications-in-privacy-risk-management"></a>隐私风险管理中的用户通知

在隐私风险管理中设置策略时，可以选择在用户的操作符合策略中设置的条件时通知用户。 有两种类型的通知：可用于所有三种策略类型的电子邮件，以及Teams中显示的提示，这些提示仅适用于数据传输策略类型。 创建或编辑策略时，可以决定是否打开这些通知、发送这些通知的频率，以及是否可以自定义其内容。

向用户发送通知可能是帮助组织实现其隐私目标的重要组成部分。 通知旨在：

- 当用户的行为可能会使个人数据面临隐私风险时，立即提高用户的意识。
- 直接在电子邮件中提供修正方法，以便用户可以迅速采取措施保护有风险的数据。
- 将用户定向到组织的隐私准则和最佳做法。

告知用户当前的潜在问题，并使他们能够修正问题并刷新其技能，可以成为在整个组织中构建健全数据处理实践的强大工具。

查看以下部分，帮助你准备和管理策略匹配的用户通知。

## <a name="prepare-training-content-for-notifications"></a>为通知准备训练内容

如果选择在检测到策略匹配时发送用户通知，则需要包含隐私培训链接。 通过提供对组织隐私准则的访问权限，可以让用户了解自己的最佳做法和策略。 它还可以为电子邮件中建议的修正操作提供上下文，并帮助用户为将来良好的数据管理决策做好准备。

在设置策略之前，请决定要包含的训练 URL。 每个策略可以提供一个链接，因此建议选择特定于每个方案的引用。

## <a name="set-user-email-notifications"></a>设置用户电子邮件通知

创建新策略或编辑现有策略时，可以为所有策略类型设置电子邮件通知。 这些设置位于策略创建向导的 **“结果** ”页上。 访问 [定义结果：用户通知和有关](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips) 完整说明的提示。

> [!NOTE]
> 隐私风险管理发送电子邮件通知的总体功能控制在Priva **设置** 中。 默认情况下处于启用状态。 关闭此设置将停止所有电子邮件，即使已在单个策略级别配置了通知。 详细了解 [用户通知电子邮件设置](priva-settings.md#user-notification-emails)。

## <a name="send-notifications-in-teams"></a>在Teams中发送通知

对于数据传输策略，可以在检测到策略匹配时，选择用户在安全Teams通道中接收策略提示和建议。 这些提示可帮助用户负责任地使用个人数据。 使用技巧还将包含相关培训的链接。

若要详细了解如何设置这些通知，请访问 [“定义结果：用户通知和提示](risk-management-policies.md#define-outcomes-user-email-notifications-and-tips)”。

## <a name="preview-and-customize-email-content"></a>预览和自定义电子邮件内容

当用户收到有关策略匹配的电子邮件通知时，他们可以按照电子邮件中的提示立即采取纠正措施。 例如，如果数据过度表达策略查找个人数据的匹配项可能访问过于广泛，则通知电子邮件包含指向内容项的链接，以便用户可以对其进行审阅，并为用户按钮将项目标记为私有或保持其当前访问级别。 建议的操作将与每种不同类型的策略相关。

在策略创建或编辑过程中调整此设置时，可以预览电子邮件内容并进行自己的更改。 若要预览和编辑通知电子邮件内容，请按照以下步骤操作：

1. 通过启动 [引导式策略创建过程中](risk-management-policies.md#custom-setup-guided-process-to-choose-all-settings)所述的步骤来创建或编辑策略。

2. 在过程的 **“结果** ”步骤中，选择 **策略匹配时向用户发送通知电子邮件旁边的** 框。

3. 选择通知电子邮件复选框下方显示的 **“预览”和“编辑通知电子邮件** ”按钮。

4. 将显示一个浮出窗格，其中包含预先填充了默认电子邮件内容的文本字段。 可以编辑任何或所有字段，其中包括：电子邮件的主题行、正文标头、正文内容、隐私培训显示名称和训练 URL。电子邮件的预览位于浮出窗格的底部，在编辑默认文本时会更改。 对电子邮件内容感到满意时，选择 **“保存** ”以保存设置。 若要放弃对默认电子邮件所做的任何更改，请选择浮出窗格右上角的 **X** 将其关闭并还原到默认内容。

5. 返回“ **结果”** 页，选择 **“下一步**”。 继续完成向导，到达最终的 **“完成”** 页时，查看设置并选择“ **提交**”。

通知设置现在将对此策略生效。 如果策略正在测试，则不会发送通知。 如果策略已启用，将发送通知。 查看有关 [创建和管理策略的](risk-management-policies.md)更多详细信息。


## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)
