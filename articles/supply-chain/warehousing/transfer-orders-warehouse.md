---
title: 设置转移单的仓库
description: 此主题介绍如何设置转移单的仓库。
author: Mirzaab
manager: tfehr
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 7dfb215683b4ee5d186626492bd90116d1a06a1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976830"
---
# <a name="set-up-warehouses-for-transfer-orders"></a><span data-ttu-id="f6b8f-103">设置转移单的仓库</span><span class="sxs-lookup"><span data-stu-id="f6b8f-103">Set up warehouses for transfer orders</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6b8f-104">您可以使用仓库级别创建支持在仓库之间转移订单的层次结构。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-104">You can use warehouse levels to create a hierarchy that supports transfer orders between warehouses.</span></span> <span data-ttu-id="f6b8f-105">基于此设置，主计划编制计算单个仓库级别的物料需求，并从分配的源仓库生成计划转移单以完成订单。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-105">Based on this setup, master scheduling calculates item requirements at the individual warehouse level and generates planned transfer orders from an assigned source warehouse to fulfill them.</span></span>

1.  <span data-ttu-id="f6b8f-106">单击 **库存管理**>“设置”>“库存细分”>“仓库”.</span><span class="sxs-lookup"><span data-stu-id="f6b8f-106">Click **Inventory management > Setup > Inventory breakdown > Warehouses**.</span></span>

2.  <span data-ttu-id="f6b8f-107">选择您要重填物料的仓库。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-107">Select the warehouse that you want to refill.</span></span>

3.  <span data-ttu-id="f6b8f-108">在 **主计划** 快速选项卡上，选择 **重填** 复选框。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-108">On the **Master planning** FastTab, select the **Refilling** check box.</span></span>

4.  <span data-ttu-id="f6b8f-109">在 **主仓库** 字段中，选择要分配为重填物料仓库的仓库。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-109">In the **Main warehouse** field, select the warehouse that you want to assign as the refilling warehouse.</span></span> <span data-ttu-id="f6b8f-110">主计划编制计算选定仓库的物料转移需求并从分配的 **主仓库** 中生成计划转移单。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-110">Master scheduling calculates a transfer requirement for the selected warehouse and generates a planned transfer order from the assigned **Main warehouse**.</span></span>
   
    > [!NOTE]
    > <P><span data-ttu-id="f6b8f-111">如果您将<STRONG>重填</STRONG>复选框清除，将为选定的仓库分配一个与<STRONG>主仓库</STRONG>有关的仓库级别，但并不将<STRONG>主仓库</STRONG>设置为重填仓库。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-111">If you clear the <STRONG>Refilling</STRONG> check box, the selected warehouse is assigned a warehouse level in regard to the <STRONG>Main warehouse</STRONG>, but the <STRONG>Main warehouse</STRONG> is not set up as a refilling warehouse.</span></span></P>

5.  <span data-ttu-id="f6b8f-112">关闭页面以应用新设置。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-112">Close the page to apply the new setup.</span></span>


> [!TIP]
> <P><span data-ttu-id="f6b8f-113">如果您要分配一个仓库用于重填，必须首先在<STRONG>库存维度组</STRONG>页面将此仓库设置为存储维度。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-113">If you want to assign a warehouse for refilling, you must first set up the warehouse as a storage dimension on the <STRONG>Storage dimension groups</STRONG> page.</span></span> <span data-ttu-id="f6b8f-114">在此页面上，选择仓库的<STRONG>有效</STRONG>和<STRONG>按维度的覆盖范围计划</STRONG>字段。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-114">On this page, select the <STRONG>Active</STRONG> field and the <STRONG>Coverage plan by dimension</STRONG> field for the warehouse.</span></span></P>

## <a name="set-up-transport-lead-time"></a><span data-ttu-id="f6b8f-115">设置运输提前期</span><span class="sxs-lookup"><span data-stu-id="f6b8f-115">Set up transport lead time</span></span>

<span data-ttu-id="f6b8f-116">您还必须设置 **运输天数** 页面的仓库之间的运输提前期。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-116">You must also set up the transport lead time between the warehouses on the **Transport days** page.</span></span> 
1. <span data-ttu-id="f6b8f-117">转到 **库存管理 > 设置 > 配送 > 运输天数**。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-117">Go to **Inventory management > Setup > Distribution > Transport days**.</span></span>
2. <span data-ttu-id="f6b8f-118">在 **接收点** 字段中，选择 **仓库**。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-118">In the **Receiving point** field, select **warehouse**.</span></span>
3. <span data-ttu-id="f6b8f-119">选择 **装运仓库**、**接收仓库** 和 **运输天数**。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-119">Select the **Shipping warehouse**, **Receiving warehouse**, and **Transport days**.</span></span> 
4. <span data-ttu-id="f6b8f-120">（可选）还可以根据交货方式设置运输时间，在 **每个交货模式的运输天数** 选项卡下。</span><span class="sxs-lookup"><span data-stu-id="f6b8f-120">(Optional) You can also set transport time, depending on the mode of delivery, under the **Transport days per mode of delivery** tab.</span></span>
