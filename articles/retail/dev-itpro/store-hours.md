---
title: 创建和更新商店营业时间
description: 此主题介绍如何在 Retail Headquarters 中创建和更新商店营业时间。
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 811d499a3eb8133e5ffd29bb4ae6a0c57708accd
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023434"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="c124d-103">创建和更新商店营业时间</span><span class="sxs-lookup"><span data-stu-id="c124d-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="c124d-104">概览</span><span class="sxs-lookup"><span data-stu-id="c124d-104">Overview</span></span>

<span data-ttu-id="c124d-105">零售商可以从一个位置为不同地理区域的不同商店创建、维护和管理商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="c124d-106">然后可以在销售点 (POS) 终端显示商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="c124d-107">通过这种方法，收银员可以与客户共享商店营业时间，并更好地帮助对其他商店库存感兴趣的购物者。</span><span class="sxs-lookup"><span data-stu-id="c124d-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="c124d-108">也可以将商店营业时间打印到收银条上，以防客户希望以后再来商店。</span><span class="sxs-lookup"><span data-stu-id="c124d-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="c124d-109">可以为不同渠道配置多个商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="c124d-110">这些渠道包括实体商店、呼叫中心、移动设备和电子商务网站。</span><span class="sxs-lookup"><span data-stu-id="c124d-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="c124d-111">如果客户有其他商店的提货单，收银员可以选择该商店的可提货日期。</span><span class="sxs-lookup"><span data-stu-id="c124d-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="c124d-112">商店查找将提供对日期和商店营业时间的引用。</span><span class="sxs-lookup"><span data-stu-id="c124d-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="c124d-113">收银员可选择日期和位置，还可以打印其中包括商店营业时间的提货收据。</span><span class="sxs-lookup"><span data-stu-id="c124d-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="c124d-114">Microsoft Dynamics 365 Retail 版本 8.1.2 及更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="c124d-114">This functionality is available in Microsoft Dynamics 365 Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="c124d-115">配置商店营业时间</span><span class="sxs-lookup"><span data-stu-id="c124d-115">Configure store hours</span></span>

<span data-ttu-id="c124d-116">请执行以下步骤配置商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="c124d-117">转到 **Retail** \> **渠道设置** \> **商店营业时间**。</span><span class="sxs-lookup"><span data-stu-id="c124d-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="c124d-118">选择**新建**以创建新的商店营业时间模板。</span><span class="sxs-lookup"><span data-stu-id="c124d-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="c124d-119">若要使用现有模板，请在左窗格中选择模板。</span><span class="sxs-lookup"><span data-stu-id="c124d-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="c124d-120">在**添加范围**对话框中，定义所需日期范围、商店营业时间和任何节假日。</span><span class="sxs-lookup"><span data-stu-id="c124d-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="c124d-121">如果商店营业时间不会改变，请在**结束日期**字段中选择**一直持续**。</span><span class="sxs-lookup"><span data-stu-id="c124d-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="c124d-122">如果商店营业时间适用于特定月份、周或日期，请在**开始日期**和**结束日期**字段中设置相应日期。</span><span class="sxs-lookup"><span data-stu-id="c124d-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c124d-123">可创建开始和结束日期重合的多个模板。</span><span class="sxs-lookup"><span data-stu-id="c124d-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="c124d-124">因此，可以执行为不同时区的商店定义商店营业时间之类操作。</span><span class="sxs-lookup"><span data-stu-id="c124d-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="c124d-125">![添加范围对话框](../dev-itpro/media/Storehours1.png "添加范围对话框")</span><span class="sxs-lookup"><span data-stu-id="c124d-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="c124d-126">将商店营业时间模板与其使用商店关联。</span><span class="sxs-lookup"><span data-stu-id="c124d-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="c124d-127">在**选择组织节点**对话框中，选择应与模板关联的商店、地区和组织。</span><span class="sxs-lookup"><span data-stu-id="c124d-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="c124d-128">只能为每个商店关联一个商店营业时间模板。</span><span class="sxs-lookup"><span data-stu-id="c124d-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="c124d-129">使用箭头按钮选择商店、地区或组织。</span><span class="sxs-lookup"><span data-stu-id="c124d-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="c124d-130">商店或商店组可使用日历，POS 中将显示日历供参考。</span><span class="sxs-lookup"><span data-stu-id="c124d-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="c124d-131">![选择组织节点对话框](../dev-itpro/media/Storehours2.png "选择组织节点对话框")</span><span class="sxs-lookup"><span data-stu-id="c124d-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="c124d-132">在**配送计划**页中，运行 **1070** 和 **1090** 作业以便将商店营业时间提供给 POS。</span><span class="sxs-lookup"><span data-stu-id="c124d-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="c124d-133">向纸质收银条添加商店营业时间</span><span class="sxs-lookup"><span data-stu-id="c124d-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="c124d-134">执行以下步骤向纸质 POS 收银条添加商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="c124d-135">打开收银条设计器。</span><span class="sxs-lookup"><span data-stu-id="c124d-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="c124d-136">在左下角选择**页脚**。</span><span class="sxs-lookup"><span data-stu-id="c124d-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="c124d-137">将**商店营业时间**元素从左窗格拖到收银条模板底部的页脚。</span><span class="sxs-lookup"><span data-stu-id="c124d-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="c124d-138">可根据需要编辑**商店营业时间**元素上的默认标签。</span><span class="sxs-lookup"><span data-stu-id="c124d-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="c124d-139">保存收银条，然后关闭收银条设计器。</span><span class="sxs-lookup"><span data-stu-id="c124d-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="c124d-140">在**配送计划**页上，运行 **1070** 和 **1090** 作业。</span><span class="sxs-lookup"><span data-stu-id="c124d-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="c124d-141">登录到 POS。</span><span class="sxs-lookup"><span data-stu-id="c124d-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="c124d-142">完成一笔交易，然后选择打印收银条。</span><span class="sxs-lookup"><span data-stu-id="c124d-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="c124d-143">POS 收银条中现在包含商店营业时间。</span><span class="sxs-lookup"><span data-stu-id="c124d-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="c124d-144">如果模板中包含任何节假日，将在收银条中显示这些节假日。</span><span class="sxs-lookup"><span data-stu-id="c124d-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="c124d-145">![收银条示例](../dev-itpro/media/Storehours3.png "收银条示例")</span><span class="sxs-lookup"><span data-stu-id="c124d-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
