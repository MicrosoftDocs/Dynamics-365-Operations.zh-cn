---
title: 固定资产购置过帐帐户
description: 本文说明如何为购置资产设置总帐过帐科目。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ac1580e33197c0cd8a82f34804d4639945d861
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548615"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="c2428-103">固定资产购置过帐帐户</span><span class="sxs-lookup"><span data-stu-id="c2428-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2428-104">本文说明如何为购置资产设置总帐过帐科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="c2428-105">用于过帐固定资产购置的帐户根据用于购置资产的方法而变。</span><span class="sxs-lookup"><span data-stu-id="c2428-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="c2428-106">在“固定资产过帐模板”页上，在“会计科目”选项卡上，选择“购置”和“购置调整”以设置要过帐到分类帐的固定资产科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="c2428-107">在日志中和采购订单上，“会计科目”通常是资产负债表科目，在其中将借记新固定资产的购置价格。</span><span class="sxs-lookup"><span data-stu-id="c2428-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="c2428-108">此科目不会显示在日志中并且无法在交易记录中被替换。</span><span class="sxs-lookup"><span data-stu-id="c2428-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="c2428-109">“对方科目”也是资产负债表科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="c2428-110">在一般日志和固定资产日志中，此科目通常将是用于支付资产购置费用的银行帐户。</span><span class="sxs-lookup"><span data-stu-id="c2428-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="c2428-111">对方科目是在日志中建议的默认科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="c2428-112">如果该固定资产从供应商处购买，则可以在日志中将其更改为从会计科目表到供应商帐户的任何其他科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="c2428-113">当应付账款中的发票日记帐或采购订单用于固定资产购置时，固定资产交易记录的对方科目由为该交易记录选择的供应商帐户所替代。</span><span class="sxs-lookup"><span data-stu-id="c2428-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="c2428-114">对于在“总帐”中使用“库存转为固定资产日记帐”过帐的购置，固定资产不是从外部购买的，而是从公司自己的库存转移的。</span><span class="sxs-lookup"><span data-stu-id="c2428-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="c2428-115">因此，对方科目是库存管理中的库存物料的发货科目。</span><span class="sxs-lookup"><span data-stu-id="c2428-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="c2428-116">有关详细信息，请参阅[通过采购购置资产](acquire-assets-procurement.md)。</span><span class="sxs-lookup"><span data-stu-id="c2428-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>



