---
title: "调整现有库存量成本价值"
description: "使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: AndersGirke
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 09c1ebc2d461bcfaf0db3f1613ce991c22c1dbd7
ms.contentlocale: zh-cn
ms.lasthandoff: 10/13/2017

---

# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="82035-103">调整现有库存量成本价值</span><span class="sxs-lookup"><span data-stu-id="82035-103">Adjust on-hand inventory cost values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="82035-104">使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。</span><span class="sxs-lookup"><span data-stu-id="82035-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="82035-105">您可以使用**现有库存量调整**页调整库存结转流程运行后的现有库存量数量的成本价值。</span><span class="sxs-lookup"><span data-stu-id="82035-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="82035-106">**注意：**若要打开**现有库存量调整**页，在**结转与调整**页上，选择已完成的库存结转流程的记录，然后单击**调整** &gt; **现有**。</span><span class="sxs-lookup"><span data-stu-id="82035-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="82035-107">**示例：**您在 2 月份具有以下交易记录：</span><span class="sxs-lookup"><span data-stu-id="82035-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="82035-108">2 月 1 日：以 10.00 美元的成本有数量为 2 的库存财务收货</span><span class="sxs-lookup"><span data-stu-id="82035-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="82035-109">2 月 5 日：以 13.00 美元的成本有数量为 1 的库存财务收货</span><span class="sxs-lookup"><span data-stu-id="82035-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="82035-110">2 月 19 日：以 11.00 美元的移动平均成本有数量为 1 的库存财务发货</span><span class="sxs-lookup"><span data-stu-id="82035-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="82035-111">此物料以先进先出 (FIFO) 库存模型设置，并在 2 月 28 日结转库存。</span><span class="sxs-lookup"><span data-stu-id="82035-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="82035-112">11.00 美元的财务发货交易记录将对照 2 月 1 日的财务收货结算，并将做 1.00 美元的调整。</span><span class="sxs-lookup"><span data-stu-id="82035-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="82035-113">以下库存收货将包含未结库存数量：</span><span class="sxs-lookup"><span data-stu-id="82035-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="82035-114">2 月 1 日：成本为 10 美元的数量 1</span><span class="sxs-lookup"><span data-stu-id="82035-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="82035-115">2 月 5 日：成本为 13.00 美元的数量 1</span><span class="sxs-lookup"><span data-stu-id="82035-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="82035-116">若要将这两个物料的成本设置为 USD 15.00，请使用现有量调整选项来调整截至最后库存结转期间的未结现有数量。</span><span class="sxs-lookup"><span data-stu-id="82035-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="82035-117">**注意：**现有量调整交易记录的过帐日期将是上一次库存结转的日期。</span><span class="sxs-lookup"><span data-stu-id="82035-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="82035-118">不能修改此日期。</span><span class="sxs-lookup"><span data-stu-id="82035-118">This date can't be modified.</span></span>

