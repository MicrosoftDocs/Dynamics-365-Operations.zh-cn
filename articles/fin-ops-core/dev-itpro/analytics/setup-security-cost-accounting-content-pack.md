---
title: 设置成本核算分析 Power BI 内容的安全性
description: 此主题介绍在 Microsoft Power BI 中如何将成本核算中的访问级别安全性传播到行级别安全性。 此功能有助于确保用户仅查看有权访问的 Power BI 数据。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d371d35352348b1cfe1dd2a5ba25e1b2b20d7d71
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769893"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="d16f4-104">设置成本核算分析 Power BI 内容的安全性</span><span class="sxs-lookup"><span data-stu-id="d16f4-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d16f4-105">此主题介绍在 Microsoft Power BI 中如何将成本核算中的访问级别安全性传播到行级别安全性。</span><span class="sxs-lookup"><span data-stu-id="d16f4-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="d16f4-106">此功能有助于确保用户仅查看有权访问的 Power BI 数据。</span><span class="sxs-lookup"><span data-stu-id="d16f4-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="d16f4-107">概览</span><span class="sxs-lookup"><span data-stu-id="d16f4-107">Overview</span></span>

<span data-ttu-id="d16f4-108">**成本核算分析** Microsoft Power BI 内容使用 Power BI 低级别安全性限制用户的访问权限。</span><span class="sxs-lookup"><span data-stu-id="d16f4-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="d16f4-109">安全性基于“成本核算”参数中设置的访问级别组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d16f4-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="d16f4-110">有关**成本核算分析** Power BI 内容的详细信息，请参阅[成本核算分析 Power BI 内容](cost-accounting-analysis-content-pack.md)。</span><span class="sxs-lookup"><span data-stu-id="d16f4-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="d16f4-111">设置</span><span class="sxs-lookup"><span data-stu-id="d16f4-111">Setup</span></span>
<span data-ttu-id="d16f4-112">若要将访问级别的安全性传播到 Power BI，Power BI 内容的所有者必须执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d16f4-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d16f4-113">发布**成本核算分析** Power BI 内容的用户将自动成为所有者。</span><span class="sxs-lookup"><span data-stu-id="d16f4-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="d16f4-114">只有所有者才能在 Power BI 中设置安全性。</span><span class="sxs-lookup"><span data-stu-id="d16f4-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="d16f4-115">此外，所有者在 PowerBI.com 中添加其他用户之前，只有所有者才能查看**成本核算分析** Power BI 内容中的数据。</span><span class="sxs-lookup"><span data-stu-id="d16f4-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="d16f4-116">将定义文件发布到 Power BI。</span><span class="sxs-lookup"><span data-stu-id="d16f4-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="d16f4-117">登录 PowerBI.com，</span><span class="sxs-lookup"><span data-stu-id="d16f4-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="d16f4-118">找到**成本核算分析** Power BI 内容的数据集。</span><span class="sxs-lookup"><span data-stu-id="d16f4-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="d16f4-119">打开安全性页面。</span><span class="sxs-lookup"><span data-stu-id="d16f4-119">Open the security page.</span></span>

    ![打开安全性页面](./media/CA-picture-1.png)

5. <span data-ttu-id="d16f4-121">已创建了**成本对象控制员**角色。</span><span class="sxs-lookup"><span data-stu-id="d16f4-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="d16f4-122">添加属于成本核算访问级别组织层次结构的其他成员。</span><span class="sxs-lookup"><span data-stu-id="d16f4-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![添加成员](./media/CA-picture-2.png)

<span data-ttu-id="d16f4-124">添加到**成本对象控制员**角色的用户只能查看根据成本核算访问级别组织层次结构中的定义允许其查看的数据。</span><span class="sxs-lookup"><span data-stu-id="d16f4-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="d16f4-125">行级别安全性适用于从 Power BI 嵌入的磁贴和报表。</span><span class="sxs-lookup"><span data-stu-id="d16f4-125">Row-level security applies to tiles and reports that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="d16f4-126">更新安全性</span><span class="sxs-lookup"><span data-stu-id="d16f4-126">Updating security</span></span>
<span data-ttu-id="d16f4-127">如果对成本核算中的访问级别安全性进行更新，并且希望 Power BI 体现这些更新，则必须更新**成本核算分析** Power BI 内容的实体商店。</span><span class="sxs-lookup"><span data-stu-id="d16f4-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="d16f4-128">完成了实体商店更新之后，必须更新 PowerBI.com 中的项目。</span><span class="sxs-lookup"><span data-stu-id="d16f4-128">After you complete the entity store update you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="d16f4-129">有关如何执行实体商店更新的详细信息，请参阅 [Power BI 与实体商店的集成](power-bi-integration-entity-store.md#update-entity-store)。</span><span class="sxs-lookup"><span data-stu-id="d16f4-129">For more information about how to do an entity store update, see [Power BI integration with Entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="d16f4-130">如果为新用户授予了组织层次结构的访问权限，**成本核算分析** Power BI 内容的所有者还必须执行实体商店更新。</span><span class="sxs-lookup"><span data-stu-id="d16f4-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="d16f4-131">此外，该所有者还必须在 PowerBI.com 上将新用户添加到**成本对象控制员**角色，以便为其应用行级别的安全性。</span><span class="sxs-lookup"><span data-stu-id="d16f4-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="d16f4-132">禁用安全性</span><span class="sxs-lookup"><span data-stu-id="d16f4-132">Disabling security</span></span>
<span data-ttu-id="d16f4-133">假设您的组织希望限制数据访问权限。</span><span class="sxs-lookup"><span data-stu-id="d16f4-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="d16f4-134">如果出于某种原因，当您运行成本核算时禁用了安全性参数，则所有者必须改为在 Power BI 中将用户添加到**成本会计师**角色。</span><span class="sxs-lookup"><span data-stu-id="d16f4-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="d16f4-135">如果您将安全性从已启用状态更改为已禁用状态，建议从**成本对象控制员**角色删除用户。</span><span class="sxs-lookup"><span data-stu-id="d16f4-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="d16f4-136">如果重新启用安全性，则执行相反操作。</span><span class="sxs-lookup"><span data-stu-id="d16f4-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="d16f4-137">用户可以同时属于两种角色。</span><span class="sxs-lookup"><span data-stu-id="d16f4-137">Users can belong to both roles.</span></span> <span data-ttu-id="d16f4-138">联合访问权限是两种角色的结合。</span><span class="sxs-lookup"><span data-stu-id="d16f4-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="d16f4-139">在**成本核算分析** Power BI 内容中，具有联合访问权限的用户的数据访问权限不受限制。</span><span class="sxs-lookup"><span data-stu-id="d16f4-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="d16f4-140">如果您的目标是应用受限访问权限，则必须仅为用户分配**成本对象控制员**角色。</span><span class="sxs-lookup"><span data-stu-id="d16f4-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="d16f4-141">这些行级别的安全性更新立即生效。</span><span class="sxs-lookup"><span data-stu-id="d16f4-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="d16f4-142">受影响的用户应刷新自己的浏览器。</span><span class="sxs-lookup"><span data-stu-id="d16f4-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d16f4-143">其他资源</span><span class="sxs-lookup"><span data-stu-id="d16f4-143">Additional resources</span></span>
<span data-ttu-id="d16f4-144">若要了解有关 Power BI 行级别安全性的详细信息，请参阅[在 Power BI 中管理模型的安全性](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)。</span><span class="sxs-lookup"><span data-stu-id="d16f4-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
