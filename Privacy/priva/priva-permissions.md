---
title: 在 Microsoft 管理中设置用户权限和分配角色
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
- M365-priva-subject-rights-requests
search.appverid:
- MOE150
- MET150
description: 了解如何设置 Microsoft 管理权限并将用户分配给角色组。
ms.openlocfilehash: bcc2e108f10e427e55034621f2f8b5c40e6d9184
ms.sourcegitcommit: f145dff5e387a8e26db2f3a2c7de125978fbacc9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2022
ms.locfileid: "62248860"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>在 Microsoft 管理中设置用户权限和分配角色

若要向组织成员授予使用 Microsoft 用户的权限，请将其分配给组织中相应的Microsoft 365 合规中心。

> [!NOTE]
> 大多数管理角色当前被指定为"隐私管理"。 有关完整列表，请参阅下文。 特定于用户的角色将不会显示在Azure Active Directory。

## <a name="sign-in-and-set-permissions"></a>登录并设置权限

1. 转到 ["Microsoft 365 合规中心左侧](https://compliance.microsoft.com/)导航栏中 **选择**"权限"。  
2. 在" **合规中心"** 下拉列表下，选择" **角色"**。 将显示角色组的完整列表。
3. 查找要添加一个或多个用户的角色组，并选中组名称左侧的框。
4. 在该组的飞出窗格中，选择"成员 **"** 标题下的 **"编辑** "。  
5. 选择 **"选择成员"**。 将显示另一个弹出窗口。
6. 选择 **+ 添加** 以选择要添加到组的一个或多个用户。  
7. 选中要添加的名称旁边的复选框，然后选择底部的 **"添加** "按钮。  
8. 分配完用户后，选择"完成"**，然后选择"****保存**"，然后选择"**关闭"**。

## <a name="learn-more-about-role-groups-and-roles"></a>详细了解角色组和角色

根据团队的结构，你具有将用户分配给特定角色组的选项，以管理不同的一组用户功能。 根据成员需要完成的任务以及适当的文件访问级别，应将其分配给角色组。 每个角色组包括一个或多个角色。 这些角色可能属于为该组的成员启用或限制的特定管理任务或关键功能。 因此，不同的用户对某些管理功能具有不同级别的可见性和访问权限。

如果需要，可以自定义角色组。 为了避免意外丢失访问权限，我们建议创建要自定义的现有角色组的副本，为副本指定可识别名称，对新组进行更改并验证更改，并根据需要为其分配人员。

## <a name="privacy-management-role-group"></a>隐私管理角色组

此组包含单个组中所有一个组的权限角色。 此角色组可能非常适合同一个人可能履行所有职责的组织。 如果在此角色组中提供成员身份，则该帐户将授予该帐户对具有其许可证的一切功能的完整访问权限。

我们建议确保此组中始终至少有一个活动成员。

角色包括：

- 案例管理  
- 数据分类内容查看器  
- 数据分类列表查看器  
- 隐私管理管理员  
- 隐私管理分析  
- 隐私管理调查  
- 隐私管理永久贡献  
- 隐私管理临时贡献  
- 隐私管理查看器  
- 主体权限请求管理员  
- View-Only Case

## <a name="privacy-management-administrators-role-group"></a>隐私管理管理员角色组

此角色组的成员可广泛访问管理功能，包括创建、读取、更新和删除隐私风险管理策略、主题权限请求、权限和设置。

角色包括：

- 案例管理  
- 隐私管理管理员  
- View-Only Case

## <a name="privacy-management-analysts-role-group"></a>隐私管理分析师角色组

此角色组的成员充当案例分析员。 他们可以调查策略匹配项、查看文件元数据以及执行修正操作。 此组无法通过内容资源管理器访问完整文件。

角色包括：

- 案例管理  
- 数据分类列表查看器  
- 隐私管理分析  
- View-Only Case

### <a name="privacy-management-investigators-role-group"></a>隐私管理调查人员角色组

此组的成员充当数据调查人员。 他们可以调查策略匹配项、查看关联的文件内容，以及执行修正操作。 此组可以通过内容资源管理器访问文件。

角色包括：

- 案例管理  
- 数据分类内容查看器  
- 数据分类列表查看器  
- 隐私管理调查  
- View-Only Case

## <a name="privacy-management-viewer-role-group"></a>隐私管理查看器角色组

此组的成员可以在"管理"中查看分析信息，如概述、数据配置文件和主题请求报告。

角色包括：

- 隐私管理查看器

## <a name="subject-rights-request-administrators-role-group"></a>主题权限请求管理员角色组

此组的成员具有管理和创建主题权限请求的完全访问权限。

角色包括：

- 主体权限请求管理员

## <a name="privacy-management-contributors-role-group"></a>隐私管理参与者角色组

此组的成员有权访问已添加为协作者的主题权限请求。  

角色包括：

- 隐私管理临时贡献  
- 隐私管理永久贡献

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft 管理中心法律免责声明](priva-disclaimer.md)