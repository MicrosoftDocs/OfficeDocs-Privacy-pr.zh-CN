---
title: '在主题权限请求中自动执行任务 '
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
description: 了解如何使用 Microsoft Power Automate帮助自动执行在亚里雅纳执行主体权限请求的基本任务。
ms.openlocfilehash: 2e1fa97b9e2cc5889471fa163dec26a5a5e37d56
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248853"
---
# <a name="automate-tasks-in-subject-rights-requests"></a>在主题权限请求中自动执行任务 

Microsoft Power Automate 是一种工作流服务，可跨应用程序和服务自动执行操作。 当你为 Microsoft Power Automate权限请求启用流时，可以自动执行事例和用户的重要任务，如在 ServiceNow 中创建票证或添加有关截止日期的日历提醒。 若要了解有关网站Power Automate，请访问他们的[文档网站](/power-automate/getting-started)。

具有主题权限请求订阅的客户不需要其他 Power Automate 许可证来使用为用户推荐Power Automate模板。 可以自定义这些模板以支持您的组织并涵盖核心主题权限请求方案。 如果您选择使用这些模板中的高级 Power Automate 功能、使用 Microsoft 365 合规性连接器创建自定义模板或使用 Microsoft 365 中其他合规性领域的 Power Automate 模板，您可能需要更多 Power Automate 许可证。

## <a name="create-a-new-power-automate-flow-from-a-template"></a>从模板Power Automate流

1. In the [Microsoft 365 合规中心](https://compliance.microsoft.com/)， go to the Rightsa section of the navigation and select **Priva Subject Rights Requests**.
1. 从列表中打开要处理的主题权限请求，然后选择"自动化"，然后选择"管理Power Automate **流"**。 这将打开"流"飞出窗格。
1. 使用 **"新建** "选项，然后从可用选项中选择想要使用的模板。 在此处，按照向导中的提示完成设置。 根据您的模板类型，选项将有所不同。

保存模板的实例后，必须从主题权限请求的详细信息页执行它，以便流实例具有正确的上下文和 ID。 打开请求，返回到" **自动"** 菜单，选择模板，然后选择" **运行流"**。 可以通过选择"查看流运行活动" **来查看过去的活动**。

### <a name="power-automate-templates-in-priva"></a>Power Automate中的模板

- **在 ServiceNow** 中为隐私管理案例创建记录：此模板适用于想要使用其 ServiceNow 解决方案跟踪主题权限请求案例的组织。 将要求您输入 ServiceNow 实例详细信息，包括用于连接到 ServiceNow 的帐户。 此帐户必须能够在 ServiceNow 中创建事件并填写事件详细信息。 连接到实例后，主题权限请求管理员可以在 ServiceNow 中为案例创建记录，如果需要，可以自定义模板将填充到选定字段中的内容。 有关连接器详细信息，请参阅 [ServiceNow 连接器参考页](/connectors/service-now/)。
- **创建日历提醒**：此模板用于为主题权限请求Outlook日历中的截止日期提醒。 该工具将基于请求的属性（如请求的名称及其截止日期）填充某些详细信息。 您可以添加描述性详细信息、指定收件人以及调整其他高级设置。
- **按标记获取主题权限请求的文件**：通过此模板，您可以搜索已给定特定标记的主题权限请求的文件。 您可以编辑流以执行自定义操作，或查看返回的文件列表以用于内部进程或工具。

## <a name="share-a-power-automate-flow"></a>共享Power Automate流

通过共享Power Automate流，可以添加另一个所有者并允许他们编辑、更新和删除流。 所有所有者还可以访问运行历史记录并添加或删除其他所有者。 若要共享流，请打开要处理的主题权限请求，选择"自动化"，然后选择"管理Power Automate **流"**。 从此窗格中，可以选择现有流，然后使用"共享"选项添加用户或组。

此窗格还为您提供了管理嵌入连接的选项，这些连接与正在流中使用的服务Power Automate连接。 更改这些设置可能会影响执行流的能力。

## <a name="edit-or-delete-power-automate-flow"></a>编辑或删除Power Automate流

若要调整流的详细信息，Power Automate主题权限请求，选择"自动化"，然后选择"管理Power Automate **流"**。 从此窗格中，可以选择一个现有流来查看详细信息。 在任何部分中使用"编辑"更改属性，然后保存。

若要完全删除流，请使用"删除 **"** 选项。 它将删除所有所有者的流，并卸载所有用户的流。 以前的流实例将继续运行以避免数据丢失。 您可以在删除完成之前确认您的选择。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
