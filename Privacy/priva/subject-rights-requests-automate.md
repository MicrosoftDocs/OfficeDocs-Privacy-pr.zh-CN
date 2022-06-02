---
title: 与 Microsoft 图形 API 和 Power Automate 集成
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
description: 了解如何通过与 Microsoft 图形 API 和Power Automate集成来扩展Priva 主体权利请求功能。
ms.openlocfilehash: e4fcad2067ece3d1a6338e6d4891c59d91205a33
ms.sourcegitcommit: 9315064bf5bb9e889318e61ec5f082f36c815e1e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/02/2022
ms.locfileid: "65851637"
---
# <a name="integrate-and-extend-through-microsoft-graph-api-and-power-automate"></a>通过 Microsoft 图形 API 和 Power Automate 集成和扩展

可以使用 Microsoft Graph使用者权限请求 API 将Priva 主体权利请求与现有业务流程和工具集成。 还可以使用内置的Power Automate流来扩展使用者权限请求的自动化功能，例如在 ServiceNow 中设置日历提醒和创建事例。

## <a name="microsoft-graph-subject-rights-requests-api"></a>Microsoft Graph使用者权限请求 API

Microsoft 365使用者权限请求 API 提供了一种简单而强大的方法，用于将自动化引入现有主题权限策略。 当个人从组织请求信息时，我们的 API 允许你根据该请求的条件在Microsoft 365中创建这些请求。 可以在Microsoft 365中创建主题权限请求，跟踪其进度，并确认请求何时已完成处理且内容已准备好检索。

我们的 API 可供任何人使用，以使其解决方案更易于扩展，例如 ISV、希望在其解决方案中容纳Microsoft 365的合作伙伴，以及希望将 API 与业务线应用程序配合使用的组织。

在[“使用 Microsoft Graph主题权限请求 API”中](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)查看完整文档。

## <a name="power-automate-templates-for-subject-rights-requests"></a>使用者权限请求的Power Automate模板

Microsoft Power Automate是一项工作流服务，可在应用程序和服务之间自动执行操作。 使用者权限请求包括内置Power Automate模板，以帮助用户管理主题权限请求。 用户可以为进程设置自动化流，例如在 ServiceNow 中创建票证，以及添加有关截止日期的日历提醒。 若要详细了解Power Automate，请访问[Power Automate文档](/power-automate/getting-started)。

如果已购买“使用者权限请求”订阅，则不需要单独的Power Automate许可证即可使用建议的Power Automate模板。 可以自定义这些模板以支持组织并涵盖核心主题权限请求方案。 但是，可能需要额外的许可证才能在这些模板中使用高级Power Automate功能或创建自己的模板。

### <a name="available-templates"></a>可用模板

- **在 ServiceNow 中创建Priva隐私管理案例的记录**：此模板适用于想要使用其 ServiceNow 解决方案跟踪主题权限请求案例的组织。 系统将要求输入 ServiceNow 实例详细信息，包括要连接到 ServiceNow 的帐户。 此帐户必须能够在 ServiceNow 中创建事件并填写事件详细信息。 连接到实例后，使用者权限请求管理员将能够在 ServiceNow 中为案例创建记录，如果需要，可以自定义模板将填充到所选字段中的内容。 有关连接器的详细信息，请参阅 [ServiceNow 连接器文档](/connectors/service-now/)。

- **添加日历提醒以跟进Priva隐私管理案例**：此模板用于在主题权限请求的Outlook日历中设置截止日期提醒。 该工具将从请求的属性中填充某些详细信息，例如请求的名称及其截止日期。 可以添加描述性详细信息、指定收件人并调整其他高级设置。

- **通过标记获取Priva主题权限请求的文件**：此模板允许你搜索给定特定标记的主题权限请求的文件。 可以编辑流以执行自定义操作，或查看要用于内部进程或工具的返回文件列表。

### <a name="create-a-new-power-automate-flow-from-a-template"></a>从模板创建新的Power Automate流

1. 在 [Microsoft Purview 合规门户](https://compliance.microsoft.com/)中，在左侧导航栏中选择 **Priva 主体权利请求**。

2. 查找要处理的主题权限请求，然后从列表中选择该请求以打开其详细信息页。

3. 在右上角，选择 **“自动执行**”，然后选择 **“管理Power Automate流**”以打开流浮出窗格。

4. 选择 **“新建** ”，然后从可用选项中选择要使用的模板。 在此处，请按照提示自定义并添加步骤以完成流的生成。 选项将因使用的模板而异 (请参阅下面的模板类型) 。

5. 完成后，选择“**保存**”。

保存模板实例后，必须从请求的详细信息页运行它，以便流实例具有正确的上下文和 ID。 打开请求，返回到 **“自动”** 菜单，选择模板，然后选择 **“运行流**”。 可以通过选择 **“查看流运行”活动** 来查看过去的活动。

### <a name="share-a-power-automate-flow"></a>共享Power Automate流

共享Power Automate流可以添加另一个所有者，并允许他们编辑、更新和删除流。 所有所有者都可以访问运行历史记录并添加或删除其他所有者。 

若要共享流，请打开要处理的主题权限请求，选择 **“自动”**，然后选择 **“管理Power Automate流**”。 在此窗格中，可以选择现有流，然后使用 **“共享** ”选项添加用户或组。

此窗格还提供用于管理与Power Automate流中使用的服务的嵌入连接的选项。 更改这些设置可能会影响运行流的能力。

### <a name="edit-or-delete-power-automate-flow"></a>编辑或删除Power Automate流

若要调整Power Automate流的详细信息，请选择请求详细信息页右上角的 **“自动执行**”，然后选择 **“管理Power Automate流**”。

在 **Power Automate流** 窗格中，选择要编辑的流，然后从命令栏中选择 **“编辑**”以编辑或添加步骤。 完成后，选择 **“保存**”。

若要删除流，请从 **Power Automate流** 窗格上的列表中选择它，然后从命令栏中选择 **“删除**”。 将删除所有所有者的流，并为所有用户卸载该流。 以前的流实例将继续运行，以避免数据丢失。 在最终删除之前，系统会要求你确认。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)
