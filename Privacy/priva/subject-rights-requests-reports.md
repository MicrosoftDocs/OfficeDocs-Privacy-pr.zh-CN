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
ms.openlocfilehash: 861a08b1f2ca5b3f82546c54db16c4518a8e9a70
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248930"
---
# <a name="generate-reports-and-fulfill-a-subject-rights-request"></a>生成报告并满足主体权限请求

完成对 Microsoft 用户权限请求的数据审阅后，可以继续请求实施。 在数据审阅过程中，用户会创建报告并收集标记为 **"** 包含"的文件。 可以将这些数据包中的选定文件提交到数据主体以完成其请求。 同时，还支持利用Microsoft 365权限请求 API 引入自动化功能。

## <a name="prepare-final-reports-for-the-data-subject"></a>为数据主体准备最终报告

主体权限请求数据包生成为 zip 文件。 生成此程序包可能需要 30 分钟。 准备就绪后，从主题权限请求页面打开主题权限请求，打开"报告"选项卡，查找下载，然后打开 zip 文件。

数据包包含各种文件。 Azure 文件夹外部的文件仅供参考，应主要供管理员使用。 数据主体的关键材料包含在 **Azure** 文件夹中。

我们建议仔细查看此文件夹的内容，并仅向数据主体提交必要的文件。 您应评估您的回复，以确保其定制符合适用法律的要求。

### <a name="azure-folder-contents"></a>Azure 文件夹内容

打开此文件夹，然后 **打开AEDExport.zip文件** 。 内容包括：

- the **Extracted_text_files** folder contains text extracted from the native files (where supported) .
- **NativeFiles** 文件夹包含其本机文件格式的所有 **已** 包含项目。
- 修订的文件位于 **NativeFiles** 文件夹中，并且具有后缀"_burn.pdf"。
- 导出的文件使用唯一标识符重命名，以帮助保护个人数据。 您可以使用文件的原始文件名交叉引用唯一的名称 **Export_load_file.csv。** 由于原始文件名可能包含敏感信息，因此应遵循适用于此类信息的策略。

查看 zip 文件的内容后，根据需要对其进行修改，以删除不希望包括在最终包中的内容。 完成后，将其安全地发送给数据主体。

## <a name="integrate-with-partner-solutions"></a>与合作伙伴解决方案集成

通过利用"用户权限请求 API"，可以将"Microsoft 365权限请求"解决方案与现有业务流程和工具集成。 这提供了一种简单但强大的方法，将自动化引入主题权限策略。

当数据主体从组织请求信息时，你可以利用我们的 API 根据自定义Microsoft 365请求的条件，在内部创建这些请求。 您可以在 Microsoft 365 创建主题权限请求，跟踪请求的阶段进度，并确认请求完成处理和内容准备检索。 我们的 API 可供任何人用于使其解决方案更加可扩展：无论是适用于 ISV、合作伙伴以适应 Microsoft 365 解决方案，还是供组织用于其业务线应用程序。

若要了解更多信息，请参阅[使用 Microsoft Graph权限请求 API](/graph/api/resources/subjectrightsrequest-subjectrightsrequestapioverview)。

## <a name="manage-data-retention"></a>管理数据保留

通过此工具生成的报表和关联数据（如保存在 Azure 中的批注文件）将存储一段指定时间。 此持续时间在全局级别定义，设置"数据保留期"部分，允许您选择 30 到 90 天。 请验证这些数据保留期是否符合您的策略和法律要求。

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)
