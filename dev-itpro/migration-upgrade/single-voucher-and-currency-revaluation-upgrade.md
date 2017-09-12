---
title: "单个凭证和货币重估升级"
description: "某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收帐款或应付帐款外币重估流程。 此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 13ad43cc77731727525aae1edc4d405c166acbc1
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a><span data-ttu-id="9bfc6-104">单个凭证和货币重估升级</span><span class="sxs-lookup"><span data-stu-id="9bfc6-104">Single voucher and currency revaluation upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9bfc6-105">某些组织输入的日记帐中包含有多位客户或供应商的单一凭证，并且还运行应收帐款或应付帐款外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="9bfc6-106">此主题描述这些组织在升级到 Microsoft Dynamics 365 for Operations 版本 1611 时应执行的步骤。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="9bfc6-107">升级到 Microsoft Dynamics 365 for Operations 版本 1611 时，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="9bfc6-108">升级到 Dynamics 365 for Operations 之前，请为应收帐款和应付帐款运行外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-108">Before you upgrade to Dynamics 365 for Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="9bfc6-109">将**方法**字段设置为**发票日期**。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="9bfc6-110">将创建一条重估交易记录，用于冲销上一笔外币重估。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="9bfc6-111">因此，将以原始会计币种计算这笔未结交易记录的价值。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="9bfc6-112">升级到 Dynamics 365 for Operations 版本 1611。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-112">Upgrade to Dynamics 365 for Operations version 1611.</span></span>
3.  <span data-ttu-id="9bfc6-113">再次运行应付帐款和应收帐款外币重估流程。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="9bfc6-114">此时，将**方法**字段设置为**标准**。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="9bfc6-115">将根据当前汇率创建一条新的重估交易记录。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="9bfc6-116">此交易记录记录或有利润/损失和正确的汇总会计科目。</span><span class="sxs-lookup"><span data-stu-id="9bfc6-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>





