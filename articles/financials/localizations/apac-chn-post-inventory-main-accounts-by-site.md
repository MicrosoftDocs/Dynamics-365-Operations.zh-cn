---
title: 按中国站点过帐主库存科目
description: 此主题提供有关按中国的站点过帐库存主科目过帐的信息。
author: ShylaThompson
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPostingParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 262754
ms.assetid: f8e0b34d-006a-4baf-86ae-60625ba4b442
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec9cedcd93f04914a1a6e9e5ec680cb56d3f574a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573388"
---
# <a name="post-inventory-main-accounts-by-site-for-china"></a><span data-ttu-id="96488-103">按中国站点过帐主库存科目</span><span class="sxs-lookup"><span data-stu-id="96488-103">Post inventory main accounts by site for China</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96488-104">此主题提供有关按中国的站点过帐库存主科目过帐的信息。</span><span class="sxs-lookup"><span data-stu-id="96488-104">This topic provides information about the posting of inventory main accounts by site for China.</span></span>

<span data-ttu-id="96488-105">您可以设置或修改物料的过帐到会计科目，基于库存交易记录的物料组和仓库站点。</span><span class="sxs-lookup"><span data-stu-id="96488-105">You can set up or modify the posting of items to ledger accounts, based on item groups and warehouse sites for inventory transactions.</span></span> <span data-ttu-id="96488-106">通过按站点设置库存的会计科目值，可以过帐各站点的库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="96488-106">By setting up ledger accounts of inventory value by site, you can post inventory transactions for each site.</span></span> <span data-ttu-id="96488-107">这些交易记录包括库存日记帐、销售订单、采购订单、生产日记帐和项目物料日记帐。</span><span class="sxs-lookup"><span data-stu-id="96488-107">These transactions include inventory journals, sales orders, purchase orders, production journals, and project item journals.</span></span> <span data-ttu-id="96488-108">仅当**库存和仓库管理参数**页上的**按站点分隔库存成本的会计科目**选项设置为**是**，**交易组合**和**过帐**页上才有与站点有关的字段。</span><span class="sxs-lookup"><span data-stu-id="96488-108">The site-related fields are available on the **Transaction combinations** and **Posting** pages only if the **Separate ledger accounts of inventory value by sites** option is set to **Yes** on the **Inventory and warehouse management parameters** page.</span></span> <span data-ttu-id="96488-109">在特定报告期间，必须确定库存物料的值以确定现有库存量、库存上的应纳税金额和库存收货和发货的期初和期末余额。</span><span class="sxs-lookup"><span data-stu-id="96488-109">You must determine the value of your inventory items to determine on-hand inventory, taxable amount on inventory, and opening and closing balances for inventory receipts and issues during a specific reporting period.</span></span> <span data-ttu-id="96488-110">可以为库存创建主科目。</span><span class="sxs-lookup"><span data-stu-id="96488-110">You can create main accounts for inventory.</span></span> <span data-ttu-id="96488-111">也可以选择显示可用于库存过帐的库存物料的库存值的主科目。</span><span class="sxs-lookup"><span data-stu-id="96488-111">Alternatively, you can select the main accounts that show the value of your inventory for inventory item groups that can be used for inventory posting.</span></span> <span data-ttu-id="96488-112">您可以从相应的主科目中计算物料组的库存成本。</span><span class="sxs-lookup"><span data-stu-id="96488-112">You can calculate the inventory value for an item group from the corresponding main account.</span></span> <span data-ttu-id="96488-113">例如，您可以创建“原材料”物料组的主科目来跟踪其库存成本。</span><span class="sxs-lookup"><span data-stu-id="96488-113">For example, you can create a main account for the Raw materials item group to track its inventory value.</span></span>

| <span data-ttu-id="96488-114">主科目</span><span class="sxs-lookup"><span data-stu-id="96488-114">Main account</span></span> | <span data-ttu-id="96488-115">物料组</span><span class="sxs-lookup"><span data-stu-id="96488-115">Item group</span></span>    | <span data-ttu-id="96488-116">余额</span><span class="sxs-lookup"><span data-stu-id="96488-116">Balance</span></span>    |
|--------------|---------------|------------|
| <span data-ttu-id="96488-117">15067</span><span class="sxs-lookup"><span data-stu-id="96488-117">15067</span></span>        | <span data-ttu-id="96488-118">灯泡</span><span class="sxs-lookup"><span data-stu-id="96488-118">Bulbs</span></span>         | <span data-ttu-id="96488-119">10,721,065</span><span class="sxs-lookup"><span data-stu-id="96488-119">10,721,065</span></span> |
| <span data-ttu-id="96488-120">15065</span><span class="sxs-lookup"><span data-stu-id="96488-120">15065</span></span>        | <span data-ttu-id="96488-121">原材料</span><span class="sxs-lookup"><span data-stu-id="96488-121">Raw materials</span></span> | <span data-ttu-id="96488-122">6,299,398</span><span class="sxs-lookup"><span data-stu-id="96488-122">6,299,398</span></span>  |

<span data-ttu-id="96488-123">存货超过 100 库存物料并可维护多个站点的组织必须按站点和物料组要求组织主科目。</span><span class="sxs-lookup"><span data-stu-id="96488-123">Organizations that stock more than 100 inventory items and also maintain several sites must organize their main accounts by both site and item group.</span></span> <span data-ttu-id="96488-124">例如，一个组织可以有多个站点，并且，每个站点可以有多个物料组。</span><span class="sxs-lookup"><span data-stu-id="96488-124">For example, an organization can have more than one site, and each site can have multiple groups of items.</span></span> <span data-ttu-id="96488-125">在下表中，您可以查看站点 1 的“灯泡”物料组的库存成本和站点 2 的“原材料”物料组的库存成本。</span><span class="sxs-lookup"><span data-stu-id="96488-125">In the following table, you can view the inventory value of the Bulbs item group for site 1 and the inventory value of the Raw materials item group for site 2.</span></span>

| <span data-ttu-id="96488-126">主科目</span><span class="sxs-lookup"><span data-stu-id="96488-126">Main account</span></span> | <span data-ttu-id="96488-127">物料组</span><span class="sxs-lookup"><span data-stu-id="96488-127">Item group</span></span>    | <span data-ttu-id="96488-128">站点</span><span class="sxs-lookup"><span data-stu-id="96488-128">Site</span></span>   | <span data-ttu-id="96488-129">所有者权益</span><span class="sxs-lookup"><span data-stu-id="96488-129">Balance</span></span>   |
|--------------|---------------|--------|-----------|
| <span data-ttu-id="96488-130">15080</span><span class="sxs-lookup"><span data-stu-id="96488-130">15080</span></span>        | <span data-ttu-id="96488-131">灯泡</span><span class="sxs-lookup"><span data-stu-id="96488-131">Bulbs</span></span>         | <span data-ttu-id="96488-132">站点 1</span><span class="sxs-lookup"><span data-stu-id="96488-132">Site 1</span></span> | <span data-ttu-id="96488-133">5,721,065</span><span class="sxs-lookup"><span data-stu-id="96488-133">5,721,065</span></span> |
| <span data-ttu-id="96488-134">15085</span><span class="sxs-lookup"><span data-stu-id="96488-134">15085</span></span>        | <span data-ttu-id="96488-135">原材料</span><span class="sxs-lookup"><span data-stu-id="96488-135">Raw materials</span></span> | <span data-ttu-id="96488-136">站点 2</span><span class="sxs-lookup"><span data-stu-id="96488-136">Site 2</span></span> | <span data-ttu-id="96488-137">3,299,398</span><span class="sxs-lookup"><span data-stu-id="96488-137">3,299,398</span></span> |

<span data-ttu-id="96488-138">通过按站点设置库存成本的主科目，您可以过帐库存交易，如每个站点的库存日志、销售订单、采购订单，生产日志和项目物料日志。</span><span class="sxs-lookup"><span data-stu-id="96488-138">By setting up main accounts for inventory values by site, you can post inventory transactions, such as inventory journals, sales orders, purchase orders, production journals, and project item journals, for each site.</span></span>
