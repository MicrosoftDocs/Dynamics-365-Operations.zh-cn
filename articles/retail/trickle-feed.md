---
title: 为零售商店交易记录创建基于缓慢馈送的订单
description: 本主题介绍如何为 Microsoft Dynamics 365 Retail 中的零售商店交易记录创建基于缓慢馈送的订单。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693081"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="a5fbd-103">为零售商店交易记录创建基于缓慢馈送的订单（公共预览）</span><span class="sxs-lookup"><span data-stu-id="a5fbd-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a5fbd-104">在 Dynamics 365 Retail 10.0.4 及早期版本中，零售对帐单过帐是日结操作，于一天结束时在帐簿中过帐所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-104">In Dynamics 365 Retail versions 10.0.4 and earlier, retail statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="a5fbd-105">大量的交易记录必须在有限的时间范围内处理，有时会导致加载、锁定和对帐单过帐失败。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="a5fbd-106">零售商也无法全天在其帐簿中确认收入和付款。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="a5fbd-107">通过 Retail 版本 10.0.5 中推出的、基于缓慢馈送的订单创建的公共预览版，可在全天中处理交易记录，并且在一天结束时仅处理支付方式和其他现金管理交易记录的财务对帐。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="a5fbd-108">此功能将创建销售订单、发票和付款的负荷拆分到全天中完成，从而更够更清晰地了解绩效并且能够近乎实时地在帐簿中确认收入和付款。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="a5fbd-109">如何使用基于缓慢馈送的过帐</span><span class="sxs-lookup"><span data-stu-id="a5fbd-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="a5fbd-110">若要对零售交易记录启用基于缓慢馈送的过帐，请转到**系统管理 > 设置 > 许可证配置**，然后禁用**零售对帐单**密钥。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-110">To enable trickle feed-based posting of retail transactions, go to **System administration > Set up > License configuration** and disable the the **Retail statements** key.</span></span>

2. <span data-ttu-id="a5fbd-111">在同一页上，启用**零售对帐单（缓慢馈送）– 预览**许可证密钥。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-111">On the same page, enable the **Retail statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="a5fbd-112">启用此密钥时，请确保不存在等待过帐的待处理对帐单。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

> [!Important]
> <span data-ttu-id="a5fbd-113">在启用**零售对帐单（缓慢馈送）– 预览**许可证密钥之前，请确保不存在等待过帐的待处理对帐单。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-113">Before you enable the **Retail statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="a5fbd-114">当前对帐单文档将拆分为两种不同的类型，分别为交易记录对帐单和财务对帐单。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="a5fbd-115">交易记录对帐单将选取所有未过帐的和已验证的零售交易记录，并按照您配置的频率创建销售订单、销售发票、付款和折扣日记帐以及收入-支出交易记录。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-115">The transactional statement will pick up all unposted and validated retail transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="a5fbd-116">您应将此过程配置为以较高的频率运行，以便当通过 P 作业将零售交易记录上载到 Retail Headquarters 中时会创建文档。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-116">You should configure this process to run at a high frequency so that documents are created when the retail transactions are uploaded into Retail Headquarters through the P-job.</span></span> <span data-ttu-id="a5fbd-117">对于已创建销售订单和销售发票的交易记录对帐单，则无需配置**过帐库存**批处理作业。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="a5fbd-118">但是，您仍可以使用它来满足您可能具有的特定业务需求。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="a5fbd-119">财务对帐单设计为仅在一天结束时创建，并且仅支持**班次**的结帐方法。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="a5fbd-120">此对帐单仅限用于财务对帐，并且仅针对不同支付方式的计算金额与交易记录金额之间的差异金额而创建日记帐，以及针对其他现金管理交易记录创建日记帐。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="a5fbd-121">若要计算交易记录对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量计算交易记录对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-121">To calculate the transactional statement, click **Retail > Retail IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="a5fbd-122">若要批量过帐交易记录对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量过帐交易记录对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-122">To post the transactional statement statements in batch, click **Retail > Retail IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="a5fbd-123">若要计算财务对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量计算财务对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-123">To calculate the financial statement, click **Retail > Retail IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="a5fbd-124">若要批量过帐财务对帐单，请单击 **Retail > 零售 IT > POS 过帐 > 批量过帐财务对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-124">To post the financial statements in batch, click **Retail > Retail IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="a5fbd-125">此新功能中删除了菜单项 **Retail > 零售 IT > POS 过帐 > 批量计算对帐单**和 **Retail > 零售 IT > POS 过帐 > 批量过帐对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-125">The menu items **Retail > Retail IT > POS Posting > Calculate statements in batch** and **Retail > Retail IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="a5fbd-126">或者，可以手动创建交易记录对帐单和财务对帐单类型。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="a5fbd-127">转至 **Retail > 渠道 > 零售商店**，然后单击**零售对帐单**。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-127">Go to **Retail > Channels > Retail stores** and click **Retail statements**.</span></span> <span data-ttu-id="a5fbd-128">单击**新建**，然后选择您要创建的对帐单类型。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="a5fbd-129">**零售对帐单**页面上的字段和该页面的**对帐单组**下的操作将基于选定的对帐单类型显示相关的数据和操作。</span><span class="sxs-lookup"><span data-stu-id="a5fbd-129">Fields on the **Retail statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
