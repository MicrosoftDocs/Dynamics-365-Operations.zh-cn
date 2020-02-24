---
title: 向 POS 设备上的交易记录屏幕添加建议控件
description: 此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021693"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="19f91-103">向 POS 设备上的交易记录屏幕添加建议控件</span><span class="sxs-lookup"><span data-stu-id="19f91-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="19f91-104">此主题介绍如何使用 Microsoft Dynamics 365 Commerce 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。</span><span class="sxs-lookup"><span data-stu-id="19f91-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="19f91-105">有关产品建议的详细信息，请参阅[“POS 中的产品建议”一文](product.md)。</span><span class="sxs-lookup"><span data-stu-id="19f91-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="19f91-106">使用 Commerce 时，可以在 POS 设备上显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="19f91-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="19f91-107">若要显示产品建议，需要使用屏幕布局设计器向交易记录屏幕添加控件。</span><span class="sxs-lookup"><span data-stu-id="19f91-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="19f91-108">打开布局设计器</span><span class="sxs-lookup"><span data-stu-id="19f91-108">Open Layout designer</span></span>

1. <span data-ttu-id="19f91-109">转至 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="19f91-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="19f91-110">使用快速筛选查找要为其添加控件的屏幕。</span><span class="sxs-lookup"><span data-stu-id="19f91-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="19f91-111">例如，使用值 **F2CP16:9M** 在**屏幕布局 ID** 字段中筛选。</span><span class="sxs-lookup"><span data-stu-id="19f91-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="19f91-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="19f91-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="19f91-113">例如，选择**名称: F2CP16:9M 屏幕布局 ID: F2CP16:9M**。</span><span class="sxs-lookup"><span data-stu-id="19f91-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="19f91-114">单击**布局设计器**。</span><span class="sxs-lookup"><span data-stu-id="19f91-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="19f91-115">按照提示启动布局设计器。</span><span class="sxs-lookup"><span data-stu-id="19f91-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="19f91-116">在提示输入凭据时，输入从**屏幕布局**页启动布局设计器时使用的相同凭据。</span><span class="sxs-lookup"><span data-stu-id="19f91-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="19f91-117">在登录时，将显示如下页面。</span><span class="sxs-lookup"><span data-stu-id="19f91-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="19f91-118">布局将由为您的商店执行的自定义决定。</span><span class="sxs-lookup"><span data-stu-id="19f91-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="19f91-119">[![布局设计器](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="19f91-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="19f91-120">选择显示选项</span><span class="sxs-lookup"><span data-stu-id="19f91-120">Choose a display option</span></span>

<span data-ttu-id="19f91-121">可用配置选项有两个。</span><span class="sxs-lookup"><span data-stu-id="19f91-121">There are two configurations options available.</span></span> <span data-ttu-id="19f91-122">选择最适合您的商店的选项，然后按照其余说明完成控件的设置。</span><span class="sxs-lookup"><span data-stu-id="19f91-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="19f91-123">这两个选项是：</span><span class="sxs-lookup"><span data-stu-id="19f91-123">The two options are:</span></span>

- <span data-ttu-id="19f91-124">始终显示建议。</span><span class="sxs-lookup"><span data-stu-id="19f91-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="19f91-125">在屏幕右侧的网格中显示**建议**选项卡。</span><span class="sxs-lookup"><span data-stu-id="19f91-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="19f91-126">始终显示建议</span><span class="sxs-lookup"><span data-stu-id="19f91-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="19f91-127">缩小交易记录行明细区域的高度，使其与其左侧的客户面板高度相同。</span><span class="sxs-lookup"><span data-stu-id="19f91-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="19f91-128">[![减少的交易记录行详细信息区域高度](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="19f91-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="19f91-129">将建议控件从左侧菜单拖放到交易记录屏幕底部中央的交易记录行明细与按钮窗格之间。</span><span class="sxs-lookup"><span data-stu-id="19f91-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="19f91-130">调整控件大小，使其适合该空间。</span><span class="sxs-lookup"><span data-stu-id="19f91-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="19f91-131">[![添加到布局中的建议控件](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="19f91-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="19f91-132">单击 **X** 保存并退出布局设计器。</span><span class="sxs-lookup"><span data-stu-id="19f91-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="19f91-133">在 Commerce 中，转至 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**。</span><span class="sxs-lookup"><span data-stu-id="19f91-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="19f91-134">在列表中，选择 **1090 收银机**。</span><span class="sxs-lookup"><span data-stu-id="19f91-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="19f91-135">单击**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="19f91-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="19f91-136">向屏幕右侧的按钮网格添加“建议”选项卡</span><span class="sxs-lookup"><span data-stu-id="19f91-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="19f91-137">在页面右侧按钮网格中最后一个选项卡下空白区域中右键单击。</span><span class="sxs-lookup"><span data-stu-id="19f91-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="19f91-138">单击**自定义**。</span><span class="sxs-lookup"><span data-stu-id="19f91-138">Click **Customize**.</span></span>

    <span data-ttu-id="19f91-139">[![自定义 - 选项卡控件对话框](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="19f91-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="19f91-140">单击**新建选项卡**。</span><span class="sxs-lookup"><span data-stu-id="19f91-140">Click **New tab**.</span></span>
4. <span data-ttu-id="19f91-141">找到刚添加的新选项卡。</span><span class="sxs-lookup"><span data-stu-id="19f91-141">Find the new tab that you just added.</span></span> <span data-ttu-id="19f91-142">您可能需要向下滚动。</span><span class="sxs-lookup"><span data-stu-id="19f91-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="19f91-143">在**目录**下拉菜单中，选择**建议的产品**。</span><span class="sxs-lookup"><span data-stu-id="19f91-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="19f91-144">[![在“目录”字段中选择“建议的产品”](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="19f91-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="19f91-145">在**标签**字段，键入建议选项卡的名称。例如，键入“建议的产品”。</span><span class="sxs-lookup"><span data-stu-id="19f91-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="19f91-146">在**图像**字段中，选择要在该选项卡上显示的图像。</span><span class="sxs-lookup"><span data-stu-id="19f91-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="19f91-147">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="19f91-147">Click **OK**.</span></span> <span data-ttu-id="19f91-148">将在按钮网格中显示新选项卡。</span><span class="sxs-lookup"><span data-stu-id="19f91-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="19f91-149">单击 **X** 保存并退出布局设计器。</span><span class="sxs-lookup"><span data-stu-id="19f91-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="19f91-150">在 Commerce 中，转至 **Retail 和 Commerce** &gt; **Retail 和 Commerce IT** &gt; **分配计划**。</span><span class="sxs-lookup"><span data-stu-id="19f91-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="19f91-151">在列表中，选择 **1090 收银机**。</span><span class="sxs-lookup"><span data-stu-id="19f91-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="19f91-152">单击**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="19f91-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19f91-153">其他资源</span><span class="sxs-lookup"><span data-stu-id="19f91-153">Additional resources</span></span>

[<span data-ttu-id="19f91-154">有关 POS 的产品建议</span><span class="sxs-lookup"><span data-stu-id="19f91-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="19f91-155">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="19f91-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
