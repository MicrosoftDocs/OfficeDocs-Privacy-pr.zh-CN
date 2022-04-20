---
title: '在使用者权限请求中自动执行任务 '
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
description: 了解如何使用 Microsoft Power Automate来帮助你自动完成 Priva 中的主题权限请求的基本任务。
ms.openlocfilehash: ec9edde16b60c2326ca899e587dfe5dc7a1e32f5
ms.sourcegitcommit: 09ecdaded9a9f8f79587f2acb978dc53b83e5c01
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/19/2022
ms.locfileid: "64930493"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>在使用者权限请求中自动执行任务 

Microsoft Power Automate是一项工作流服务，可在应用程序和服务之间自动执行操作。 为 Microsoft Priva 主题权限请求启用Power Automate流时，可以自动执行事例和用户的重要任务，例如在 ServiceNow 中创建票证或添加有关截止日期的日历提醒。 若要详细了解Power Automate，请访问其[文档网站](/power-automate/getting-started)。

拥有“使用者权利请求”订阅的客户不需要其他Power Automate许可证来使用建议的 priva Power Automate 模板。 可以自定义这些模板以支持组织并涵盖核心主题权限请求方案。 如果选择在这些模板中使用高级Power Automate功能，请使用Microsoft 365合规性连接器创建自定义模板，或者将Power Automate模板用于Microsoft 365中的其他合规性领域，则可能需要更多Power Automate许可证。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>从模板创建新的Power Automate流

1. 在 [Microsoft Purview 合规性门户](https://compliance.microsoft.com/)中，转到导航的 Priva 部分，然后选择 **“Priva 主题权限请求**”。
1. 从列表中打开要处理的主题权限请求，然后选择 **“自动执行**”，然后 **管理Power Automate流**。 这将打开“流”浮出窗格。
1. 使用 **“新建** ”选项，并从可用选项中选择要使用的模板。 在此处，按照向导中的提示完成设置。 选项将因模板类型而异。

保存模板实例后，必须从主题权限请求的详细信息页执行该模板，以便流实例具有正确的上下文和 ID。 打开请求，返回到 **“自动”** 菜单，选择模板，然后选择 **“运行流**”。 可以通过选择 **“查看流运行”活动** 来查看过去的活动。

### <a name="power-automate-templates-in-priva"></a>在 Priva 中Power Automate模板

- **在 ServiceNow 中创建隐私管理案例记录**：此模板适用于想要使用其 ServiceNow 解决方案跟踪主题权限请求案例的组织。 系统将要求输入 ServiceNow 实例详细信息，包括要连接到 ServiceNow 的帐户。 此帐户必须能够在 ServiceNow 中创建事件并填写事件详细信息。 连接到实例后，使用者权限请求管理员将能够在 ServiceNow 中为案例创建记录，如果需要，可以自定义模板将填充到所选字段中的内容。 有关连接器的详细信息，请参阅 [ServiceNow 连接器参考页](/connectors/service-now/)。
- **创建日历提醒**：此模板用于在Outlook日历中为主题权限请求设置截止日期提醒。 该工具将从请求的属性中填充某些详细信息，例如请求的名称及其截止日期。 可以添加描述性详细信息、指定收件人并调整其他高级设置。
- **按标记获取主题权限请求的文件**：此模板允许搜索给定特定标记的主题权限请求的文件。 可以编辑流以执行自定义操作，或查看返回的文件列表，以利用内部进程或工具。

## <a name="share-a-power-automate-flow"></a>共享Power Automate流

通过共享Power Automate流，可以添加另一个所有者，并允许他们编辑、更新和删除流。 所有所有者还可以访问运行历史记录并添加或删除其他所有者。 若要共享流，请打开要处理的主题权限请求，选择 **“自动”**，然后选择 **“管理Power Automate流**”。 在此窗格中，可以选择现有流，然后使用“共享”选项添加用户或组。

此窗格还提供用于管理与Power Automate流中使用的服务的嵌入连接的选项。 更改这些设置可能会影响执行流的能力。

## <a name="edit-or-delete-power-automate-flow"></a>编辑或删除Power Automate流

若要调整Power Automate流的详细信息，请打开主题权限请求，选择 **“自动”**，然后选择 **“管理Power Automate流**”。 在此窗格中，可以选择现有流来查看详细信息。 使用任意部分中的“编辑”更改属性，然后保存。

若要完全删除流，请使用 **“删除”** 选项。 它将删除所有所有者的流，并将其卸载给所有用户。 以前的流实例将继续运行，以避免数据丢失。 你可以在删除完成之前确认你的选择。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva 法律免责声明](priva-disclaimer.md)
