--- 
title: "将产品从接收仓库越库配送到商店"
description: "此程序会逐步演示如何创建和处理越库配送，以将产品从采购订单的收货位置配送到一个或许多商店。"
author: BibiSp
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: daa42bb83d6b988e8fd18db6ad8386c67fd3e6e5
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="eb99b-103">将产品从接收仓库越库配送到商店</span><span class="sxs-lookup"><span data-stu-id="eb99b-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eb99b-104">此程序会逐步演示如何创建和处理越库配送，以将产品从采购订单的收货位置配送到一个或许多商店。</span><span class="sxs-lookup"><span data-stu-id="eb99b-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="eb99b-105">用户可以定义多个配置，并让系统建议如何配送产品，或手动输入物料的配送目的地，以及如何配送到每一个商店。</span><span class="sxs-lookup"><span data-stu-id="eb99b-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="eb99b-106">该程序不包括可用于越库配送的数据的设置，例如补货规则、组织层次结构和商店权重。</span><span class="sxs-lookup"><span data-stu-id="eb99b-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="eb99b-107">该程序使用 USRT 演示公司。</span><span class="sxs-lookup"><span data-stu-id="eb99b-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="eb99b-108">转到“所有采购订单”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="eb99b-109">选择列表中的一个采购订单，然后单击链接以打开该订单。</span><span class="sxs-lookup"><span data-stu-id="eb99b-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="eb99b-110">在“操作窗格”上，单击“零售”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-110">On the Action Pane, click Retail.</span></span>
4. <span data-ttu-id="eb99b-111">单击“越库配送”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-111">Click Cross docking.</span></span>
5. <span data-ttu-id="eb99b-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-112">Click Edit.</span></span>
    * <span data-ttu-id="eb99b-113">该类别可用于过滤“行”部分中的物料。</span><span class="sxs-lookup"><span data-stu-id="eb99b-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="eb99b-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="eb99b-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="eb99b-115">在“越库配送数量”字段中，输入一个值，以指定所采购的选定产品的应配送数量。</span><span class="sxs-lookup"><span data-stu-id="eb99b-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="eb99b-116">在“其他越库配送数量”字段中，输入一个值，以指定所采购的可用产品的配送数量</span><span class="sxs-lookup"><span data-stu-id="eb99b-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="eb99b-117">在“配送”字段中，输入“位置权重”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="eb99b-118">您可以选择其他类型，以使用其他配送规则。</span><span class="sxs-lookup"><span data-stu-id="eb99b-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="eb99b-119">在“补货层次结构”字段中，选择一个值。</span><span class="sxs-lookup"><span data-stu-id="eb99b-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="eb99b-120">选择“遵守分类”字段中的“是”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="eb99b-121">单击“计算数量”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="eb99b-122">单击“创建订单”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-122">Click Create order.</span></span>
14. <span data-ttu-id="eb99b-123">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="eb99b-123">Click Yes.</span></span>
15. <span data-ttu-id="eb99b-124">在列表中，查找和选择一个已收到产品的仓库。</span><span class="sxs-lookup"><span data-stu-id="eb99b-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="eb99b-125">单击“订单”以查看为选定仓库创建的订单</span><span class="sxs-lookup"><span data-stu-id="eb99b-125">Click Order to view the orders that got created for the selected warehouse</span></span>

