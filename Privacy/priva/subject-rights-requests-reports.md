---
title: 生成报告并满足主体权限请求
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
description: 了解如何管理 Microsoft 用户为主体权利请求创建的数据包，以及满足对数据主体的请求。
ms.openlocfilehash: a72dfb53e4f642cd2c567896c854af2beaedd416
ms.sourcegitcommit: beeb693075ef692e95d679f366301df8517b2ac3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "63765515"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>生成报告并满足主体权限请求

完成对 Microsoft 用户权限请求的数据审阅后，可以继续完成请求。 在数据审阅过程中，用户会创建报告并收集标记为"包含"的文件。 可以将这些数据包中的选定文件提交到数据主体以完成其请求。 同时，还支持利用Microsoft 365权限请求 API 引入自动化功能。

## <a name="understanding-reports"></a>了解报告

在主题 **权限请求** 的" **审阅** 数据"阶段中选择"完成审阅"后，请求的最终报告将开始自动生成。 在"**主题** 权限请求详细信息"页的"报告"选项卡上，"状态"列指示报告生成正在进行以及报告何时可供 **下载**。 可能需要 30 分钟才能完成报告创建。

报告分为两个部分：
1. **数据主体的报告：** 这些报告包含可在请求履行过程中返回给数据主体的信息。 你将在此找到包含要发送到数据主体的文件的数据包。
   > [!IMPORTANT]
   > 只有在数据审阅期间将项目标记为 **"包含** "时，才生成数据包。

   > [!IMPORTANT]
   > 将仅为导出 **和访问类型的****请求** 生成数据包。 不会为后续请求的 **标记列表生成数据包** 。 查看有关 [主题权限请求类型的详细信息](subject-rights-requests-create.md#use-the-subject-rights-request-creation-wizard)。

2. **供内部使用** 的报告：这些报告针对与主题权限请求相关的组织内部记录。 它们包括审核日志数据审阅期间应用标记的所有文件的列表，以便跟进或进一步操作。

> [!NOTE]
> 生成报告后，组织通过以安全方式向数据主体发送相应报告来完成请求，以便满足主体权利请求。 如果数据主体请求删除其数据，则组织负责确定要删除的项目并执行删除操作。

## <a name="data-package"></a>数据包

在此过程的数据审阅阶段，主题权限请求数据包包含标记为 **Include** 的项目。 数据包生成为 zip 文件。 准备好下载后，在主题权限请求详细信息页面的"报告"选项卡上选择报告行。 将打开一个飞出面板，并添加" **下载报告** "按钮。 The **What do next** instructions on the flyout panel provide a quick reference for how to work with the contents.

准备好下载数据包后，选择"下载"，查找下载，然后打开下载的 zip 文件。

### <a name="contents-of-the-data-package"></a>数据包的内容

数据包 zip 文件包含以下项：

- 名为 **Azure** 的文件夹：此文件夹包含数据主体的关键材料。 请参阅下面的详细说明。
- Azure **文件夹外部的文件** ：其中可能包括两个名为 **"结果** "和"摘要"的 **电子表格**。 Azure 文件夹之外的这些文件仅供参考，应主要由组织的管理员使用。

当一个 Subjecta 标识并检索主题权限请求的文件时，它将使用唯一标识符重命名此过程中导出的文件，以帮助保护个人数据。 可以使用原始文件名交叉引用唯一名称，**Export_load_file.csv文件。** 由于原始文件名可能包含敏感信息，因此应遵循适用于此类信息的策略。

> [!NOTE]
> 我们建议仔细查看此文件夹的内容，并仅向数据主体提交必要的文件。 您应评估您的回复，以确保其定制符合适用法律的要求。

### <a name="azure-folder-contents"></a>Azure 文件夹内容

打开 **Azure** 文件夹，然后打开 **AEDExport.zip文件，** 其中包含另一个包含数字和字母的长名称文件文件夹。 打开具有长名称的文件夹以显示如下内容：

- **Extracted_text_files** 文件夹：包含从本机文件中提取的文本 (支持) 。
- **NativeFiles** 文件夹：包含数据审阅期间标记为"已包含"的所有项目（以本机文件格式表示）。 此文件夹中的每个项目都有一个唯一的文件名来保护个人数据。 您可以使用以下说明的 Export_load_file.csv 文件交叉引用这些唯一名称及其原始文件名。
  - 在数据审阅过程中使用 **"注释** "函数修订的文件位于 **NativeFiles** 文件夹中，其后缀为"_burn.pdf"。
- **Export_load_file.csv** 文件：包含原始文件名，因此可以使用 NativeFiles 文件夹中提供的唯一文件名交叉引用它们。
- **摘要** 文本文件：提供数据包中文件类型、文件数量及其大小的摘要。

##### <a name="what-to-do-with-the-folder-contents"></a>对文件夹内容执行哪些处理

打开 **Azure** 文件夹和 zip 文件，如上所述。 下一个任务是查看项目、确定要发送给数据主体的内容，并根据需要修改 zip 文件内容。

例如，对于数据主体希望接收包含组织保留的个人数据的所有项目副本的导出请求，需要仔细查看 **NativeFiles** 文件夹中的项目，并删除不希望发送回数据主体的任何项目。

对于数据主体希望接收由组织保存的所有个人信息的摘要的访问请求，你需要重点关注摘要文本文件。

修改 zip 文件以删除不希望包括在最终包中的内容。 完成后，以安全方式将 zip 文件发送给发出主体权限请求的数据主体。

## <a name="audit-log"></a>审核日志

the 审核日志 is a CSV file providing a record of the stages for each subject rights request. 它列出过程的每个阶段以及完成的日期和时间，以及完成该步骤的个人的用户名。

## <a name="tagged-files-reports"></a>带标记的文件报告

标记为 **"标记为...** "的报告是 CSV 文件，其中列出了在数据审阅过程中应用了标记的内容项。 标记用于标记内容项，供组织进一步关注或采取措施。 详细了解标记 [设置](priva-settings.md#data-review-tags)。

## <a name="retention-periods-for-reports-and-data"></a>报告和数据的保留期

由主体权限请求生成的报告和相关数据（如保存在 Azure 中的批注文件）将存储一段指定时间。 默认保留期为自主题权限请求关闭之日起的 30 天。

数据保留期在"管理 **设置并适用于所有** 主体权限请求。 若要查看或更改数据保留期，请按照以下步骤操作：

1. 在"权限主体权限请求"中的任意位置，设置 ( 右上角的齿轮) 选择齿轮图标。
2. 在 **左侧导航上选择** "数据保留期"。
3. 从" **收集和报告的数据** "下拉菜单中，选择"30 天"或"90 天"作为保留期。
4. 选择 **"保存** "以保存设置。

请务必验证所选的数据保留期是否符合组织的策略和法律要求。

## <a name="integrate-with-partner-solutions"></a>与合作伙伴解决方案集成

您可以通过利用用户权限请求 API，将"用户主体权限请求"解决方案与现有业务流程和工具Microsoft 365集成。 这提供了一种简单但强大的方法，将自动化引入主题权限策略。

当数据主体从你的组织请求信息时，你可以利用我们的 API 根据针对该请求Microsoft 365条件在内部创建这些请求。 您可以在 Microsoft 365 创建主题权限请求，跟踪请求的阶段进度，并确认请求完成处理和内容准备检索。 我们的 API 可供任何人用于使其解决方案更加可扩展：无论是适用于 ISV、合作伙伴以适应 Microsoft 365 解决方案，还是供组织用于其业务线应用程序。

若要了解更多信息，请参阅[使用 Microsoft Graph权限请求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
