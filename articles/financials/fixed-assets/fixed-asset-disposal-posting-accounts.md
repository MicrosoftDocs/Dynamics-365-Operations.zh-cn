---
title: "固定资产处置过帐科目"
description: "本主题说明如何为处理资产设置总帐过帐科目。"
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a8e00c00b0cb7058858fde3774941911ce20fb6f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="5c2a7-103">固定资产处置过帐科目</span><span class="sxs-lookup"><span data-stu-id="5c2a7-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c2a7-104">本主题说明如何为处理资产设置总帐过帐科目。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="5c2a7-105">在“固定资产过帐模板”页，在“会计科目”快速选项卡上，选择“处置 - 销售和处置 - 报废”以设置过帐到分类帐。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="5c2a7-106">对于这两种交易记录类型，为固定资产的处置价值贷记会计科目。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="5c2a7-107">贷项将过帐到对方科目；例如，可以是银行帐户。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="5c2a7-108">如果向客户销售某一固定资产，则使用该客户的帐户，来代替对方科目。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="5c2a7-109">单击“处置”，然后单击“销售”或“报废”，然后设置详细帐户来冲销固定资产的帐面净值。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="5c2a7-110">您还可以在“处置参数”页的“过帐值”和“销售价值类型”字段中输入信息。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="5c2a7-111">低价值池中某一资产的处置交易记录将只按已处置金额减少低价值池的帐面净值。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="5c2a7-112">但是，当某一资产的销售额大于低价值池的帐面净值时，帐面净值将被减少到零。</span><span class="sxs-lookup"><span data-stu-id="5c2a7-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>






