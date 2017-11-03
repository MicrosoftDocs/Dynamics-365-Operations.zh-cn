---
title: "供应商门户用户安全性"
description: "本文说明如何设置使用供应商门户的外部供应商的安全性。 此信息仅适用于 Dynamics AX 2016 年 2 月 &amp; 2016 年 5 月版本。"
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="e6afc-104">供应商门户用户安全性</span><span class="sxs-lookup"><span data-stu-id="e6afc-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e6afc-105">本文说明如何设置使用供应商门户的外部供应商的安全性。</span><span class="sxs-lookup"><span data-stu-id="e6afc-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="e6afc-106">此信息仅适用于 Dynamics AX 2016 年 2 月 &amp; 2016 年 5 月版本。</span><span class="sxs-lookup"><span data-stu-id="e6afc-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="e6afc-107">在 Dynamics 365 for Operations 1611 版本中，供应商门户功能被扩展的供应商协作功能所取代。</span><span class="sxs-lookup"><span data-stu-id="e6afc-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="e6afc-108">有关设置供应商协作安全性的详细信息，请参阅[设置和维护供应商协作](set-up-maintain-vendor-collaboration.md)。</span><span class="sxs-lookup"><span data-stu-id="e6afc-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="e6afc-109">供应商门户向外部供应商公开了有关采购订单 (PO) 的一组有限的信息。</span><span class="sxs-lookup"><span data-stu-id="e6afc-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="e6afc-110">请您务必在 Microsoft Dynamics AX 中为供应商门户正确设置用户权限，这样供应商就不会意外访问您 Dynamics AX 安装中的其他信息。</span><span class="sxs-lookup"><span data-stu-id="e6afc-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="e6afc-111">**重要信息：**与其他用户不同，外部供应商不应具有**“系统用户”**角色。</span><span class="sxs-lookup"><span data-stu-id="e6afc-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="e6afc-112">**“系统用户”**角色将授予对一组不适用于外部用户的特权的访问权限。</span><span class="sxs-lookup"><span data-stu-id="e6afc-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="e6afc-113">设置供应商门户用户</span><span class="sxs-lookup"><span data-stu-id="e6afc-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="e6afc-114">在为即将使用供应商门户的人创建用户帐户之前，您必须设置供应商以允许供应商门户协作。</span><span class="sxs-lookup"><span data-stu-id="e6afc-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="e6afc-115">在**“供应商”**页面的**“常规”**选项卡上，使用**“采购订单协作”**字段。</span><span class="sxs-lookup"><span data-stu-id="e6afc-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="e6afc-116">使用供应商门户的外部供应商必须具有以下设置：</span><span class="sxs-lookup"><span data-stu-id="e6afc-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="e6afc-117">供应商必须在 Dynamics AX 中的**“用户”**页面上注册一个 Microsoft Azure Active Directory (AAD) 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="e6afc-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="e6afc-118">供应商必须具有**“供应商（外部）”**安全角色，而不是**“系统用户”**角色。</span><span class="sxs-lookup"><span data-stu-id="e6afc-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="e6afc-119">**注意：**您在 Dynamics AX 中创建新用户帐户时，将自动授予**“系统用户”**角色。</span><span class="sxs-lookup"><span data-stu-id="e6afc-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="e6afc-120">因此，您必须删除该角色并确认收到的警告消息。</span><span class="sxs-lookup"><span data-stu-id="e6afc-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="e6afc-121">不应向供应商用户授予将 PO 表中的其他字段添加到他们的 PO 视图的权限。</span><span class="sxs-lookup"><span data-stu-id="e6afc-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="e6afc-122">在**“个性化”**选项卡上，在**“用户”**选项卡上，将用户的**“允许显式个性化设置”**选项设置为**“否”**。</span><span class="sxs-lookup"><span data-stu-id="e6afc-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="e6afc-123">用户帐户必须与已注册的联系人相关联。</span><span class="sxs-lookup"><span data-stu-id="e6afc-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="e6afc-124">在**“用户”**页面上的**“名称”**字段中选择一个联系人。</span><span class="sxs-lookup"><span data-stu-id="e6afc-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="e6afc-125">您选择的人员应具有相关供应商的**“联系人”**角色。</span><span class="sxs-lookup"><span data-stu-id="e6afc-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="e6afc-126">如果同一个人需要访问多个供应商帐户（可能是不同的法人）的供应商门户，那么这个人的每一个用户帐户都必须与相同的已注册联系人相关联。</span><span class="sxs-lookup"><span data-stu-id="e6afc-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="e6afc-127">**“供应商（外部）”**角色包括使用供应商门户中提供的功能所需的所有基本功能。</span><span class="sxs-lookup"><span data-stu-id="e6afc-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="e6afc-128">此设置有助于确保外部用户看到的用户界面仅集中于预期场景。</span><span class="sxs-lookup"><span data-stu-id="e6afc-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="e6afc-129">请参阅</span><span class="sxs-lookup"><span data-stu-id="e6afc-129">See also</span></span>
--------

[<span data-ttu-id="e6afc-130">供应商协作</span><span class="sxs-lookup"><span data-stu-id="e6afc-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




