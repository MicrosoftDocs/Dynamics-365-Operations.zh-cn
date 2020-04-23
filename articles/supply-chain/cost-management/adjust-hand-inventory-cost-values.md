---
title: 调整现有库存量成本价值
description: 使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc97db0f0b637e27ece904fe24e91a92044bc17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208792"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="e96b8-103">调整现有库存量成本价值</span><span class="sxs-lookup"><span data-stu-id="e96b8-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e96b8-104">使用”现有库存量调整“页调整库存结转流程运行后的现有库存量数量的成本价值。</span><span class="sxs-lookup"><span data-stu-id="e96b8-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="e96b8-105">您可以使用**现有库存量调整**页调整库存结转流程运行后的现有库存量数量的成本价值。</span><span class="sxs-lookup"><span data-stu-id="e96b8-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="e96b8-106">**注意：** 若要打开**现有库存量调整**页，在**结转与调整**页上，选择已完成的库存结转流程的记录，然后单击**调整** &gt; **现有**。</span><span class="sxs-lookup"><span data-stu-id="e96b8-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="e96b8-107">**示例：** 您在 2 月份具有以下交易记录：</span><span class="sxs-lookup"><span data-stu-id="e96b8-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="e96b8-108">2 月 1 日：以 10.00 美元的成本有数量为 2 的库存财务收货</span><span class="sxs-lookup"><span data-stu-id="e96b8-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="e96b8-109">2 月 5 日：以 13.00 美元的成本有数量为 1 的库存财务收货</span><span class="sxs-lookup"><span data-stu-id="e96b8-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="e96b8-110">2 月 19 日：以 11.00 美元的移动平均成本有数量为 1 的库存财务发货</span><span class="sxs-lookup"><span data-stu-id="e96b8-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="e96b8-111">此物料以先进先出 (FIFO) 库存模型设置，并在 2 月 28 日结转库存。</span><span class="sxs-lookup"><span data-stu-id="e96b8-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="e96b8-112">11.00 美元的财务发货交易记录将对照 2 月 1 日的财务收货结算，并将做 1.00 美元的调整。</span><span class="sxs-lookup"><span data-stu-id="e96b8-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="e96b8-113">以下库存收货将包含未结库存数量：</span><span class="sxs-lookup"><span data-stu-id="e96b8-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="e96b8-114">2 月 1 日：成本为 10 美元的数量 1</span><span class="sxs-lookup"><span data-stu-id="e96b8-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="e96b8-115">2 月 5 日：成本为 13.00 美元的数量 1</span><span class="sxs-lookup"><span data-stu-id="e96b8-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="e96b8-116">若要将这两个物料的成本设置为 USD 15.00，请使用现有量调整选项来调整截至最后库存结转期间的未结现有数量。</span><span class="sxs-lookup"><span data-stu-id="e96b8-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="e96b8-117">**注意：** 现有量调整交易记录的过帐日期将是上一次库存结转的日期。</span><span class="sxs-lookup"><span data-stu-id="e96b8-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="e96b8-118">不能修改此日期。</span><span class="sxs-lookup"><span data-stu-id="e96b8-118">This date can't be modified.</span></span>
