---
title: "向 POS 设备上的交易记录页添加建议控件"
description: "此主题介绍如何使用 Microsoft Dynamics 365 for Retail 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cdfcbdcafdbbbab21c398ebc8002a45742e33e6
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="5784a-103">向 POS 设备上的交易记录页添加建议控件</span><span class="sxs-lookup"><span data-stu-id="5784a-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5784a-104">此主题介绍如何使用 Microsoft Dynamics 365 for Retail 中的屏幕布局设计器，向销售点 (POS) 设备的交易记录屏幕添加建议控件。</span><span class="sxs-lookup"><span data-stu-id="5784a-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="5784a-105">使用 Microsoft Dynamics 365 for Retail 时，可以在 POS 设备上显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="5784a-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="5784a-106">*建议*是客户可能根据其购买历史记录感兴趣的商品、其愿望列表中的商品，以及其他客户在线商店和实体商店购买的商品。</span><span class="sxs-lookup"><span data-stu-id="5784a-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="5784a-107">若要显示产品建议，需要使用屏幕布局设计器向交易记录屏幕添加控件。</span><span class="sxs-lookup"><span data-stu-id="5784a-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="5784a-108">打开布局设计器</span><span class="sxs-lookup"><span data-stu-id="5784a-108">Open Layout designer</span></span>
1.  <span data-ttu-id="5784a-109">转至**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS** &gt; **屏幕布局**。</span><span class="sxs-lookup"><span data-stu-id="5784a-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="5784a-110">使用快速筛选查找要为其添加控件的屏幕。</span><span class="sxs-lookup"><span data-stu-id="5784a-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="5784a-111">例如，使用值“F2CP16:9M”在**屏幕布局 ID** 字段中筛选：</span><span class="sxs-lookup"><span data-stu-id="5784a-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="5784a-112">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="5784a-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="5784a-113">例如，选择“名称: F2CP16:9M 屏幕布局 ID: F2CP16:9M”。</span><span class="sxs-lookup"><span data-stu-id="5784a-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="5784a-114">单击**布局设计器**。</span><span class="sxs-lookup"><span data-stu-id="5784a-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="5784a-115">按照提示启动布局设计器。</span><span class="sxs-lookup"><span data-stu-id="5784a-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="5784a-116">在提示输入凭据时，输入从**屏幕布局**页启动布局设计器时使用的相同凭据。</span><span class="sxs-lookup"><span data-stu-id="5784a-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="5784a-117">在登录时，将显示如下页面。</span><span class="sxs-lookup"><span data-stu-id="5784a-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="5784a-118">布局将由为您的商店执行的自定义决定。</span><span class="sxs-lookup"><span data-stu-id="5784a-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="5784a-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) 选择显示选项</span><span class="sxs-lookup"><span data-stu-id="5784a-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="5784a-120">可用配置选项有两个。</span><span class="sxs-lookup"><span data-stu-id="5784a-120">There are two configurations options available.</span></span> <span data-ttu-id="5784a-121">选择最适合您的商店的选项，然后按照其余说明完成控件的设置。</span><span class="sxs-lookup"><span data-stu-id="5784a-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="5784a-122">这两个选项是：</span><span class="sxs-lookup"><span data-stu-id="5784a-122">The two options are:</span></span>
-   <span data-ttu-id="5784a-123">始终显示建议。</span><span class="sxs-lookup"><span data-stu-id="5784a-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="5784a-124">在屏幕右侧的网格中显示**建议**选项卡。</span><span class="sxs-lookup"><span data-stu-id="5784a-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="5784a-125">始终显示建议</span><span class="sxs-lookup"><span data-stu-id="5784a-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="5784a-126">缩小交易记录行明细区域的高度，使其与其左侧的客户面板高度相同。[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="5784a-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="5784a-127">将建议控件从左侧菜单拖放到交易记录屏幕底部中央的交易记录行明细与按钮窗格之间。</span><span class="sxs-lookup"><span data-stu-id="5784a-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="5784a-128">调整控件大小，使其适合该空间。[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="5784a-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="5784a-129">单击 **X** 保存并退出布局设计器。</span><span class="sxs-lookup"><span data-stu-id="5784a-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="5784a-130">在 Dynamics 365 for Retail 中，转至**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="5784a-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="5784a-131">在列表中，选择 **1090 收银机**。</span><span class="sxs-lookup"><span data-stu-id="5784a-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="5784a-132">单击**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="5784a-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="5784a-133">向屏幕右侧的按钮网格添加“建议”选项卡</span><span class="sxs-lookup"><span data-stu-id="5784a-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="5784a-134">在页面右侧按钮网格中最后一个选项卡下空白区域中右键单击。</span><span class="sxs-lookup"><span data-stu-id="5784a-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="5784a-135">单击**自定义**。[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="5784a-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="5784a-136">单击**新建选项卡**。</span><span class="sxs-lookup"><span data-stu-id="5784a-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="5784a-137">找到刚添加的新选项卡。</span><span class="sxs-lookup"><span data-stu-id="5784a-137">Find the new tab that you just added.</span></span> <span data-ttu-id="5784a-138">您可能需要向下滚动。</span><span class="sxs-lookup"><span data-stu-id="5784a-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="5784a-139">在**目录**下拉菜单中，选择**建议的产品**。</span><span class="sxs-lookup"><span data-stu-id="5784a-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="5784a-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="5784a-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="5784a-141">在**标签**字段，键入建议选项卡的名称。例如，键入“建议的产品”。</span><span class="sxs-lookup"><span data-stu-id="5784a-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="5784a-142">在**图像**字段中，选择要在该选项卡上显示的图像。</span><span class="sxs-lookup"><span data-stu-id="5784a-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="5784a-143">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="5784a-143">Click **OK**.</span></span> <span data-ttu-id="5784a-144">将在按钮网格中显示新选项卡。</span><span class="sxs-lookup"><span data-stu-id="5784a-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="5784a-145">单击 **X** 保存并退出布局设计器。</span><span class="sxs-lookup"><span data-stu-id="5784a-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="5784a-146">在 Dynamics 365 for Retail 中，转至**零售** &gt; **零售 IT** &gt; **配送计划**。</span><span class="sxs-lookup"><span data-stu-id="5784a-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="5784a-147">在列表中，选择 **1090 收银机**。</span><span class="sxs-lookup"><span data-stu-id="5784a-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="5784a-148">单击**立即运行**。</span><span class="sxs-lookup"><span data-stu-id="5784a-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="5784a-149">请参阅</span><span class="sxs-lookup"><span data-stu-id="5784a-149">See also</span></span>
--------

[<span data-ttu-id="5784a-150">个性化产品建议概览</span><span class="sxs-lookup"><span data-stu-id="5784a-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




