---
title: 在隐私风险管理中发送用户通知
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
description: 了解如何通知内容所有者隐私风险管理找到的策略匹配项，以及他们如何使用这些电子邮件通知来修正问题。
ms.openlocfilehash: 2215224adf932f806f16429560d4a694cd47a859
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248855"
---
# <a name="send-user-notifications-in-privacy-risk-management"></a>在隐私风险管理中发送用户通知

Microsoft 管理中的隐私风险管理可以直接向内容所有者通知数据过度显示、数据最小化和数据传输策略的匹配项。 使用电子邮件通知，用户可以轻松了解他们需要查看的内容，并可以使用电子邮件中的提示应用相应的更正操作。 这些电子邮件还包括指向你自己的隐私培训的链接。 对于数据传输策略，还可以在频道中共享Teams提示。

## <a name="prepare-training-content-for-policy-notifications"></a>为策略通知准备培训内容

生成通知的策略需要包含指向隐私培训的链接。 提供对组织隐私准则的访问，使用户可以随时了解自己的最佳做法和策略。 它还可以在电子邮件中提供建议的修正操作上下文，并帮助你的用户为将来的数据管理决策做好准备。

在设置策略之前，请确定要包含的培训 URL。 每个策略都可以提供一个链接，因此我们建议选择特定于每个方案的引用。

## <a name="set-up-email-notifications-for-policies"></a>设置策略电子邮件通知

可以在创建自定义策略或编辑任何策略时配置电子邮件通知。 有关 [完整说明，请参阅在隐私风险管理](risk-management-policies.md) 中创建策略。 可以在策略向导的结果 **选项卡** 上找到电子邮件通知设置。 你可以在此处决定发送通知的频率、设置隐私培训 URL，并输入电子邮件主题或正文的任何自定义文本。

## <a name="remediate-issues-from-email-notifications"></a>修正电子邮件通知中的问题

当用户收到有关策略匹配项的电子邮件通知时，他们可以按照电子邮件中的提示立即采取纠正措施。 例如，如果数据过度公开策略找到可能过于广泛可访问的个人数据匹配项，则生成的电子邮件可能会提供按钮提示，使项目成为私有项。 如果应保留指示的项目，则用户还可以选择保留该项目。 提供的建议操作将与每种不同类型的策略相关。

## <a name="send-notifications-in-teams"></a>在邮件中Teams

对于数据传输策略，当检测到策略匹配时，用户可以在安全Teams接收策略提示和建议。 这些提示将指导用户负责使用个人数据。 使用技巧还将包含指向相关培训的链接。

若要了解有关设置这些通知的信息，请参阅在 [隐私风险管理中创建策略](risk-management-policies.md#set-user-email-notifications)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
