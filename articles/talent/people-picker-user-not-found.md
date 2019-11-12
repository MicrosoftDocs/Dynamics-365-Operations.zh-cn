---
title: 没有在 Attract 或 Onboard 的人员选择器中找到用户
description: 本主题说明当公司租户中的用户未在 Dynamics 365 Talent - Attract 或 Onboard 的人员选择器中显示时应该做什么。
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d84dd9c22738a1b4fc5edb5331d4aa213b82facb
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551925"
---
# <a name="user-not-found-in-people-picker-in-attract-or-onboard"></a>没有在 Attract 或 Onboard 的人员选择器中找到用户
[!include [banner](includes/banner.md)]

## <a name="issue"></a>发货

当在 Dynamics 365 Talent: Attract 或 Dynamics 365 Talent: Onboard 的人员选择器中搜索姓名时，租户的 Microsoft Azure Active Directory (Azure AD) 中的某些有效用户不显示。

## <a name="cause"></a>原因

某些用户类型当前在 Attract 和 Onboard 中不支持。 验证用户不是 Azure AD 企业到企业 (B2B) 来宾用户。 “用户类型”信息可以在 Azure 门户的 Azure Active Directory 边栏选项卡中找到。

有关 Azure B2B 的详细信息，请参阅 [Azure Active Directory B2B 中的来宾用户访问是什么](https://docs.microsoft.com/azure/active-directory/b2b/what-is-b2b)。

对于非 B2B 用户，存在某些可能在**用户**对象中具有不完整“用户类型”属性的用户。 这可以使用 Azure AD Powershell 模块验证和修复。 有关详细信息，请参阅[Azure AD](https://docs.microsoft.com/powershell/module/azuread/?view=azureadps-2.0)。

## <a name="resolution"></a>解决方法

若要完成以下步骤以解决问题，您需要在 Azure Active Directory 租户上具有“全局管理员”权限或 **User.ReadWrite.All** 的权限。

验证受影响用户的“用户类型”。

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
命令返回以下信息。
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
请注意用户的 **UserType** 属性。 如果 **UserType** 为空，例如，不是“成员”或“来宾”，则使用以下命令更新 **UserType**。

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
