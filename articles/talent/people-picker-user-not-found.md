---
title: 没有在 Attract 或 Onboard 的人员选择器中找到用户
description: 本主题说明当公司租户中的用户未在 Dynamics 365 for Talent Attract 或 Onboard 应用程序的人员选择器中显示时应该做什么。
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
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517420"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="0f2bd-103">未在人员选择器中找到 Azure Active Directory 用户</span><span class="sxs-lookup"><span data-stu-id="0f2bd-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="0f2bd-104">发货</span><span class="sxs-lookup"><span data-stu-id="0f2bd-104">Issue</span></span>

<span data-ttu-id="0f2bd-105">当在 Dynamics 365 for Talent Attract 或 Onboard 应用程序的人员选择器中搜索姓名时，租户的 Microsoft Azure Active Directory (Azure AD) 中的某些有效用户不显示。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="0f2bd-106">原因</span><span class="sxs-lookup"><span data-stu-id="0f2bd-106">Cause</span></span>

<span data-ttu-id="0f2bd-107">某些用户类型当前在 Attract 和 Onboard 应用程序中不支持。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="0f2bd-108">验证用户不是 Azure AD 企业到企业 (B2B) 来宾用户。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="0f2bd-109">“用户类型”信息可以在 Azure 门户的 Azure Active Directory 边栏选项卡中找到。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="0f2bd-110">有关 Azure B2B 的详细信息，请参阅 [Azure Active Directory B2B 中的来宾用户访问是什么](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b)。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="0f2bd-111">对于非 B2B 用户，存在某些可能在**用户**对象中具有不完整“用户类型”属性的用户。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="0f2bd-112">这可以使用 Azure AD Powershell 模块验证和修复。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="0f2bd-113">有关详细信息，请参阅[Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0)。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="0f2bd-114">解决方法</span><span class="sxs-lookup"><span data-stu-id="0f2bd-114">Resolution</span></span>

<span data-ttu-id="0f2bd-115">若要完成以下步骤以解决问题，您需要在 Azure Active Directory 租户上具有“全局管理员”权限或 **User.ReadWrite.All** 的权限。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="0f2bd-116">验证受影响用户的“用户类型”。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="0f2bd-117">命令返回以下信息。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="0f2bd-118">请注意用户的 **UserType** 属性。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="0f2bd-119">如果 **UserType** 为空，例如，不是“成员”或“来宾”，则使用以下命令更新 **UserType**。</span><span class="sxs-lookup"><span data-stu-id="0f2bd-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
