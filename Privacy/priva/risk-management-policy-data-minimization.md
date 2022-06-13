---
title: 隐私风险管理中的数据最小化策略
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
description: 了解如何在Microsoft Priva 隐私风险管理中创建数据最小化策略，以减少组织中未使用的个人数据量。
ms.openlocfilehash: 251bd0ad73c840f818c945b7f68e4557299ad406
ms.sourcegitcommit: 3c83e8133a5a71f4e1d76a0b2981ab3ec9cd6602
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2022
ms.locfileid: "66046616"
---
# <a name="data-minimization-policies-in-privacy-risk-management"></a>隐私风险管理中的数据最小化策略

数据最小化策略侧重于内容的年龄，以及自上次修改内容以来所用的时间。 监视仍在旧内容中保留的个人数据，可帮助更好地管理存储的数据并降低风险。

隐私风险管理允许你创建策略来监视在所选时间范围内尚未修改的数据。 检测到策略匹配时，可以向用户发送电子邮件通知，其中包含修正选项，包括标记要删除的项目、通知内容所有者或标记项目以供进一步查看。

通过策略设置过程，可以轻松设置策略条件。 你可以完全控制警报时间和电子邮件的频率，使用户注意安全的数据处理做法。

可通过两种方式创建策略：从 **模板**，即使用默认设置的快速“开箱即用”选项;或 **自定义** 选项，这是用于设置条件、警报和通知的引导过程。

## <a name="quick-setup-use-a-template-with-default-settings"></a>快速设置：将模板与默认设置配合使用

默认数据最小化策略检测包含至少 30 天前创建或修改的个人数据的内容。

按照以下步骤创建默认数据传输策略：

1. 在 [Microsoft Purview 合规性门户](https://compliance.microsoft.com/)中，在左侧导航中查找Priva 隐私风险管理并选择 **“策略**”。

2. 选择屏幕右上角的 **“创建策略** ”，其中显示一个浮出窗格，其中列出了所有策略创建选项。

3. 在 **“数据最小化** ”框中，选择 **“创建**”。

4. 浮出窗格包含策略详细信息。 选择 **“视图”设置** 将显示默认设置。 可以从此处编辑设置，这会使你进入下面所述的引导式过程。 若要继续使用默认设置创建策略，只需输入描述性名称，然后选择 **“创建策略**”。

将创建策略，你会发现它在 **“警察** ”页面上列出。 它以 [测试模式](risk-management-policies.md#testing-a-policy) 开始，因此可以在打开它之前监视其性能。

#### <a name="default-data-minimization-policy-settings"></a>默认数据最小化策略设置

从模板创建的数据最小化策略将检测到：
- 包含至少在过去 30 天内未修改的个人数据的内容项。
- 存储在组织内任一位置的数据：Exchange、OneDrive、SharePoint、Teams。
- 基于以下 [分类组](risk-management-policies.md#classification-groups)的数据类型：
    - 欧盟一般数据保护条例 (GDPR) 
    - 美国个人身份信息
    - 美国爱国者法案
    - 美国州违规通知法
    - 美国格拉姆-利奇-布利法案 (GLBA) 
    - 美国健康保险可移植性和责任法案 (HIPAA) 
    - 澳大利亚健康记录法 (HRIP) 
    - 澳大利亚隐私法案
    - 日本个人身份信息
    - 日本个人信息保护

## <a name="custom-setup-guided-policy-creation-process"></a>自定义设置：引导式策略创建过程

自定义策略选项是一个引导式过程，通过设置条件、指定警报严重性和频率以及打开用户电子邮件通知来创建新策略。

完成以下步骤以创建新的数据传输策略：

1. 在 [Microsoft Purview 合规性门户](https://compliance.microsoft.com/)中，在左侧导航中查找Priva 隐私风险管理并选择 **“策略**”。

2. 选择屏幕右上角的 **“创建策略** ”按钮，其中显示一个浮出窗格，其中列出了所有策略创建选项。

3. 在“ **自定义** ”框中，选择 **“创建**”。

4. 在 **“名称和类型** ”页上，选择 **“数据最小化** ”策略模板。 输入一个策略名称，帮助你在“ **策略** ”页上轻松地从列表中标识它，并输入可选说明，然后选择 **“下一步**”。

5. 在 **“要监视的数据”** 页上，选择要监视策略的个人数据类型。 有两个选项：
    - **分类组**：用于检测与个人数据或特定法规相关的内容的敏感信息类型的分组。 如果选择此选项，则需要选择 **“+添加分类组** ”以从提供的列表中选择一个或多个组。
    - **单个敏感信息类型**：选择此选项可从单个 [敏感信息类型的](/microsoft-365/compliance/sensitive-information-type-entity-definitions)列表中进行选择。

    详细了解如何 [选择要监视的数据](risk-management-policies.md#choose-data-to-monitor)。 选择要监视的数据后，选择 **“下一步**”。

6. 在 **“用户和组** ”页上，选择策略将应用于组织中的用户。 可以选择所有单个用户和所有Office 365通讯组，也可以选择特定的用户和组。 详细了解如何 [选择用户和组](risk-management-policies.md#choose-users-and-groups)。 完成时选择“**下一步**”。

7. 在 **“位置”** 页上，选择要覆盖策略Microsoft 365中的所有数据位置。 从Exchange电子邮件帐户、OneDrive帐户、Teams聊天和频道消息以及SharePoint网站中进行选择。

    在SharePoint中，可以指定所有网站或特定网站。 如果选择 **“特定SharePoint网站**”，则可以在 URL 字段中输入网站 URL。 还可以选择 **“+选择网站**”，然后在浮出窗格中选中要选择的网站名称左侧的框。

    详细了解 [如何选择位置](risk-management-policies.md#choose-locations)。 选择完位置后，选择 **“下一步**”。

8. 在 **“条件”** 页上，使用下拉菜单选择自上次修改项目以来的天数，策略将检测到：
    - 30 天
    - 60 天
    - 90 天
    - 120 天
    
     完成时选择“**下一步**”。

9. 在 **“结果”页上** ，决定是否在用户匹配策略设置的条件时通知用户。 如果选中电子邮件通知框，当用户的操作与策略条件匹配时，用户将收到电子邮件通知。 电子邮件将包含直接从电子邮件执行补救措施的说明，以及隐私培训链接。 你将指定电子邮件的频率和首选隐私培训的 URL。
     
    详细了解如何设置 [用户通知](risk-management-notifications.md)。 选择结果后，选择 **“下一步**”。

10. 在 **“警报”** 页上，使用切换开关打开管理员将在隐私风险管理的“策略 **”部分的****“警报”** 页上看到的警报。 你将指定生成警报的频率、生成警报之前匹配的阈值以及警报严重性。 详细了解如何 [设置策略匹配项的警报](risk-management-policies.md#set-alerts)。 完成时选择“**下一步**”。

11. 在 **“模式”** 页上，决定在首次创建策略时是否要在测试模式下运行策略，这意味着不会发送任何警报或通知。 若要使策略保持测试模式，建议选择切换开关到 **“打开** ”位置。 详细了解如何 [测试策略](risk-management-policies.md#testing-a-policy)。

> [!NOTE]
> 如果 **将测试模式下的运行** 切换到 **“关闭** ”位置，则在创建完策略后 *会打开* 策略。 这意味着，在检测到匹配项后，设置的任何警报或用户通知都将开始生成。

12. 在 **“完成”** 页上，查看你的选择。 选择任意部分下方的 **“编辑** ”以调整设置。 如果对策略的设置感到满意，请选择 **“提交** ”以创建策略。

几秒钟后，你将看到已创建策略的确认。 在确认页上选择 **“完成** ”，该页面将转到“策略 **”页，** 此时会在表顶部看到新策略。

## <a name="next-steps"></a>后续步骤

有关如何编辑和管理策略的详细信息，请访问 [隐私风险管理策略](risk-management-policies.md) 。