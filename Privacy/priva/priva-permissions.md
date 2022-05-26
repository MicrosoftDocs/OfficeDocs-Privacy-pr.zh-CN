---
title: 在Microsoft Priva中设置用户权限并分配角色
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
description: 了解如何设置Microsoft Priva权限并将用户分配到角色组。
ms.openlocfilehash: eca08327e2db909475dbf4c072b8f6843de3d57b
ms.sourcegitcommit: 3c27ecf7c86c8a3db38cae8819fc090eed192b4f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/25/2022
ms.locfileid: "65678219"
---
# <a name="set-user-permissions-and-assign-roles-in-microsoft-priva"></a>在Microsoft Priva中设置用户权限并分配角色

若要向组织成员授予使用Microsoft Priva的权限，请将其分配给Microsoft Purview 合规门户中的相应角色组。

> [!NOTE]
> 大多数Priva角色当前被指定为“隐私管理”。 有关完整列表，请参阅下文。 特定于Priva的角色不会出现在Azure Active Directory中。

## <a name="sign-in-and-set-permissions"></a>登录并设置权限

1. 转到 [Microsoft Purview 合规门户](https://compliance.microsoft.com/)并在左侧导航栏中选择 **“权** 限”。  
2. 在 **Microsoft Purview解决方案** 下拉列表下，选择 **“角色**”。 将显示角色组的完整列表。
3. 找到要向其添加一个或多个用户的角色组 (查看下面) 的角色组说明，然后选中组名称左侧的框。
4. 在该组的浮出窗格的 **“成员** ”标头下，选择 **“编辑**”。  
5. 在浮出窗格中，选择左侧导航栏上 **的成员** 。 将显示另一个浮出窗口。
6. 选择 **“+ 添加** ”以选择要添加到组中的一个或多个用户。  
7. 选中要添加的名称旁边的复选框，然后选择底部的 **“添加** ”按钮。  
8. 分配完用户后，选择 **“完成**”，然后 **“保存**”，然后 **“关闭**”。

## <a name="learn-more-about-role-groups-and-roles"></a>详细了解角色组和角色

根据团队的结构，你可以选择将用户分配到特定的角色组，以管理不同的Priva功能集。 应将成员分配给角色组，具体取决于需要完成的任务以及文件访问级别合适。 每个角色组包括一个或多个角色。 这些角色可能与为该组的成员启用或限制的特定Priva任务或关键函数相关。 因此，不同的用户可能具有不同级别的可见性和对某些Priva功能的访问权限。

如果需要，可以自定义角色组。 为了避免意外失去访问权限，我们建议创建要自定义的现有角色组的副本，为副本提供可识别的名称，对新组进行更改并验证更改，并根据需要将人员分配给该组。

## <a name="privacy-management-role-group"></a>隐私管理角色组

此组包含单个组中的所有Priva权限角色。 此角色组可能非常适合同一个人可以执行所有职责的组织。 在此角色组中提供成员身份将授予该帐户对你持有许可证的Priva的所有功能的完全访问权限。

建议确保此组中始终至少有一个活动成员。

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
- 使用者权限请求管理员  
- View-Only案例

## <a name="privacy-management-administrators-role-group"></a>隐私管理管理员角色组

此角色组的成员可以广泛访问Priva函数，包括创建、读取、更新和删除隐私风险管理策略、主体权限请求、权限和设置。

角色包括：

- 案例管理  
- 隐私管理管理员  
- View-Only案例

## <a name="privacy-management-analysts-role-group"></a>隐私管理分析师角色组

此角色组的成员充当案例分析员。 他们可以调查策略匹配项、查看文件元数据并执行修正操作。 此组无法通过内容资源管理器访问完整文件。

角色包括：

- 案例管理  
- 数据分类列表查看器  
- 隐私管理分析  
- View-Only案例

### <a name="privacy-management-investigators-role-group"></a>隐私管理调查员角色组

此组的成员充当数据调查员。 他们可以调查策略匹配项、查看关联的文件内容，并执行修正操作。 此组可以通过内容资源管理器访问文件。

角色包括：

- 案例管理  
- 数据分类内容查看器  
- 数据分类列表查看器  
- 隐私管理调查  
- View-Only案例

## <a name="privacy-management-viewer-role-group"></a>隐私管理查看器角色组

此组的成员可以在Priva中查看分析信息，例如概述、数据配置文件和主题请求报告。

角色包括：

- 隐私管理查看器

## <a name="subject-rights-request-administrators-role-group"></a>使用者权限请求管理员角色组

此组的成员可以完全访问管理和创建使用者权限请求。

角色包括：

- 使用者权限请求管理员

## <a name="privacy-management-contributors-role-group"></a>隐私管理参与者角色组

此组的成员有权访问已添加为协作者的主题权限请求。  

角色包括：

- 隐私管理临时贡献  
- 隐私管理永久贡献

## <a name="legal-disclaimer"></a>法律免责声明

[Microsoft Priva法律免责声明](priva-disclaimer.md)