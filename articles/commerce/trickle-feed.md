---
title: 为零售商店交易记录创建基于缓慢馈送的订单
description: 本主题介绍如何为 Microsoft Dynamics 365 Commerce 中的商店交易记录创建基于缓慢馈送的订单。
author: josaw1
manager: AnnBe
ms.date: 06/08/2020
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
ms.openlocfilehash: 6e097ead7cacb3f71452323656546a4be661457f
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710275"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a><span data-ttu-id="e569b-103">为零售商店交易记录创建基于缓慢馈送的订单</span><span class="sxs-lookup"><span data-stu-id="e569b-103">Trickle feed-based order creation for retail store transactions</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e569b-104">在 Dynamics 365 Retail 10.0.4 及早期版本中，对账单过账是日结操作，于一天结束时在账簿中过账所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="e569b-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="e569b-105">大量的交易记录必须在有限的时间范围内处理，有时会导致加载、锁定和对帐单过帐失败。</span><span class="sxs-lookup"><span data-stu-id="e569b-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="e569b-106">零售商也无法全天在其帐簿中确认收入和付款。</span><span class="sxs-lookup"><span data-stu-id="e569b-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="e569b-107">通过 Retail 版本 10.0.5 中推出的、基于缓慢馈送的订单创建，可在全天中处理交易记录，并且在一天结束时仅处理支付方式和其他现金管理交易记录的财务对帐。</span><span class="sxs-lookup"><span data-stu-id="e569b-107">With trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="e569b-108">此功能将创建销售订单、发票和付款的负荷拆分到全天中完成，从而更够更清晰地了解绩效并且能够近乎实时地在帐簿中确认收入和付款。</span><span class="sxs-lookup"><span data-stu-id="e569b-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="e569b-109">如何使用基于缓慢馈送的过账</span><span class="sxs-lookup"><span data-stu-id="e569b-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="e569b-110">若要对交易记录启用基于缓慢馈送的过账，请转到**系统管理 > 设置 > 许可证配置**，然后禁用**对账单**密钥。</span><span class="sxs-lookup"><span data-stu-id="e569b-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="e569b-111">在同一页上，启用**对账单（缓慢馈送）– 预览**许可证密钥。</span><span class="sxs-lookup"><span data-stu-id="e569b-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="e569b-112">启用此密钥时，请确保不存在等待过账的待处理对账单。</span><span class="sxs-lookup"><span data-stu-id="e569b-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="e569b-113">在启用**对账单（缓慢馈送）– 预览**许可证密钥之前，请确保不存在等待过账的待处理对账单。</span><span class="sxs-lookup"><span data-stu-id="e569b-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="e569b-114">当前对帐单文档将拆分为两种不同的类型，分别为交易记录对帐单和财务对帐单。</span><span class="sxs-lookup"><span data-stu-id="e569b-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="e569b-115">交易记录对账单将选取所有未过账的和已验证的交易记录，并按照您配置的频率创建销售订单、销售账单、付款和折扣日记账以及收入-支出交易记录。</span><span class="sxs-lookup"><span data-stu-id="e569b-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="e569b-116">您应将此过程配置为以较高的频率运行，以便当通过 P 作业将交易记录上传到 Headquarters 中时会创建文档。</span><span class="sxs-lookup"><span data-stu-id="e569b-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="e569b-117">对于已创建销售订单和销售账单的交易记录对账单，则无需配置**过账库存**批处理作业。</span><span class="sxs-lookup"><span data-stu-id="e569b-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="e569b-118">但是，您仍可以使用它来满足您可能具有的特定业务需求。</span><span class="sxs-lookup"><span data-stu-id="e569b-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="e569b-119">财务对帐单设计为仅在一天结束时创建，并且仅支持**班次**的结帐方法。</span><span class="sxs-lookup"><span data-stu-id="e569b-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="e569b-120">此对账单仅限用于财务对账，并且仅针对不同支付方式的计算金额与交易记录金额之间的差异金额而创建日记账，以及针对其他现金管理交易记录创建日记账。</span><span class="sxs-lookup"><span data-stu-id="e569b-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="e569b-121">若要计算交易记录对账单，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算交易记录对账单**。</span><span class="sxs-lookup"><span data-stu-id="e569b-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="e569b-122">若要批量过账交易记录对账单，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量过账交易记录对账单**。</span><span class="sxs-lookup"><span data-stu-id="e569b-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="e569b-123">若要计算财务报表，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算财务报表**。</span><span class="sxs-lookup"><span data-stu-id="e569b-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="e569b-124">若要对财务报表进行批量过账，请单击 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 对财务报表进行批量过账**。</span><span class="sxs-lookup"><span data-stu-id="e569b-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="e569b-125">此新功能中删除了菜单项 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量计算对账单**和 **Retail 和 Commerce > Retail 和 Commerce IT > POS 过账 > 批量过账对账单**。</span><span class="sxs-lookup"><span data-stu-id="e569b-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="e569b-126">或者，可以手动创建交易记录对账单和财务报表类型。</span><span class="sxs-lookup"><span data-stu-id="e569b-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="e569b-127">转至 **Retail 和 Commerce > 渠道 > 商店**，然后单击**对账单**。</span><span class="sxs-lookup"><span data-stu-id="e569b-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="e569b-128">单击**新建**，然后选择您要创建的对账单类型。</span><span class="sxs-lookup"><span data-stu-id="e569b-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="e569b-129">**对账单**页面上的字段和该页面的**对账单组**下的操作将基于选定的对账单类型显示相关的数据和操作。</span><span class="sxs-lookup"><span data-stu-id="e569b-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
