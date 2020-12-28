---
title: 将固定资产与租赁关联
description: 本主题说明如何将现有固定资产与新租赁相关联。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440959"
---
# <a name="associate-fixed-assets-with-leases"></a><span data-ttu-id="28c5d-103">将固定资产与租赁关联</span><span class="sxs-lookup"><span data-stu-id="28c5d-103">Associate fixed assets with leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28c5d-104">本主题说明如何将现有固定资产与新租赁相关联。</span><span class="sxs-lookup"><span data-stu-id="28c5d-104">The topic explains how to associate an existing fixed asset with a new lease.</span></span> <span data-ttu-id="28c5d-105">将固定资产与租赁相关联时，初始确认时的使用权 (ROU) 资产价值将是固定资产的购置成本。</span><span class="sxs-lookup"><span data-stu-id="28c5d-105">When you associate a fixed asset with a lease, the right-of-use (ROU) asset value at initial recognition will be the acquisition cost of the fixed asset.</span></span>

<span data-ttu-id="28c5d-106">在将固定资产与租赁关联之前，必须在“固定资产”中为该固定资产创建一条记录。</span><span class="sxs-lookup"><span data-stu-id="28c5d-106">Before you can associate a fixed asset with a lease, you must create a record for the fixed asset in Fixed assets.</span></span> <span data-ttu-id="28c5d-107">然后，在 **租赁摘要** 页面上，您必须创建租赁并将资产链接到该租赁。</span><span class="sxs-lookup"><span data-stu-id="28c5d-107">Then, on the **Lease summary** page, you must create a lease and link the asset to that lease.</span></span>

1. <span data-ttu-id="28c5d-108">按照[添加或复制租赁](add-lease.md)中的步骤添加租赁。</span><span class="sxs-lookup"><span data-stu-id="28c5d-108">Add a lease by following the steps in [Add or copy leases](add-lease.md).</span></span> <span data-ttu-id="28c5d-109">在 **添加租赁** 页面的 **固定资产编号** 字段中，选择尚未购置的资产。</span><span class="sxs-lookup"><span data-stu-id="28c5d-109">On the **Add lease** page, in the **Fixed asset number** field, select the asset that hasn't yet been acquired.</span></span>
2. <span data-ttu-id="28c5d-110">选择 **帐簿**，然后确认付款计划。</span><span class="sxs-lookup"><span data-stu-id="28c5d-110">Select **Books**, and confirm the payment schedule.</span></span>
3. <span data-ttu-id="28c5d-111">选择 **初始确认**。</span><span class="sxs-lookup"><span data-stu-id="28c5d-111">Select **Initial recognition**.</span></span>
4. <span data-ttu-id="28c5d-112">选择 **资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="28c5d-112">Select **Asset leasing journal**.</span></span>

    <span data-ttu-id="28c5d-113">租赁的初始确认日记帐条目从固定资产中扣除通常从使用权资产科目中扣除的金额。</span><span class="sxs-lookup"><span data-stu-id="28c5d-113">The initial recognition journal entry for the lease debits the fixed asset for the amount that is usually debited to the ROU asset account.</span></span>

    <span data-ttu-id="28c5d-114">现在，您可以查看固定资产的交易类型和帐簿。</span><span class="sxs-lookup"><span data-stu-id="28c5d-114">You can now view the transaction type and book for the fixed asset.</span></span>

5. <span data-ttu-id="28c5d-115">选择 **日记帐详细信息**。</span><span class="sxs-lookup"><span data-stu-id="28c5d-115">Select **Journal details**.</span></span>
6. <span data-ttu-id="28c5d-116">选择 **行** 查看日记帐条目的各行。</span><span class="sxs-lookup"><span data-stu-id="28c5d-116">Select **Lines** to view the individual lines for the journal entry.</span></span>
7. <span data-ttu-id="28c5d-117">选择包含资产的日记帐行，然后选择 **固定资产** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="28c5d-117">Select the journal line that contains the asset, and then select the **Fixed Assets** tab.</span></span>

    <span data-ttu-id="28c5d-118">**固定资产** 选项卡显示交易类型和帐簿。</span><span class="sxs-lookup"><span data-stu-id="28c5d-118">The **Fixed assets** tab shows the transaction type and the book.</span></span> <span data-ttu-id="28c5d-119">默认情况下，**交易类型** 字段设置为 **购置**，**帐簿** 字段设置为固定资产的当前帐簿。</span><span class="sxs-lookup"><span data-stu-id="28c5d-119">By default, the **Transaction type** field is set to **Acquisition**, and the **Book** field is set to the current book for the fixed asset.</span></span>

<span data-ttu-id="28c5d-120">过帐初始确认日记帐条目后，该交易显示为固定资产的购置交易。</span><span class="sxs-lookup"><span data-stu-id="28c5d-120">After you post the initial recognition journal entry, the transaction appears as an acquisition transaction for the fixed asset.</span></span> <span data-ttu-id="28c5d-121">要查看交易表，请转到 **固定资产 \> 固定资产 \> 固定资产**，选择相应资产，然后选择 **估价**。</span><span class="sxs-lookup"><span data-stu-id="28c5d-121">To view the transaction table, go to **Fixed assets \> Fixed assets \> Fixed assets**, select the appropriate asset, and then select **Valuations**.</span></span> <span data-ttu-id="28c5d-122">您应该会看到初始确认日记帐条目已经为指定的固定资产创建了一笔购置交易。</span><span class="sxs-lookup"><span data-stu-id="28c5d-122">You should see that the initial recognition journal entry has created an acquisition transaction for the specified fixed asset.</span></span>

<span data-ttu-id="28c5d-123">现在可以使用固定资产中的标准折旧功能对固定资产进行折旧。</span><span class="sxs-lookup"><span data-stu-id="28c5d-123">The fixed asset can now be depreciated by using the standard depreciation functionality in Fixed assets.</span></span> <span data-ttu-id="28c5d-124">有关折旧的详细信息，请参阅[折旧法和惯例](../fixed-assets/depreciation-methods-conventions.md)。</span><span class="sxs-lookup"><span data-stu-id="28c5d-124">For more information about depreciation, see [Depreciation methods and conventions](../fixed-assets/depreciation-methods-conventions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="28c5d-125">如果您将固定资产与租赁关联，“资产租赁”中将禁用 **资产折旧** 和 **租赁减损** 按钮。</span><span class="sxs-lookup"><span data-stu-id="28c5d-125">If you associate a fixed asset with a lease, the **Asset depreciation** and **Lease impairment** buttons are disabled in Asset leasing.</span></span> <span data-ttu-id="28c5d-126">您可以从“固定资产”查看资产折旧和租赁减损交易。</span><span class="sxs-lookup"><span data-stu-id="28c5d-126">You can view asset depreciation and lease impairment transactions from Fixed assets.</span></span> <span data-ttu-id="28c5d-127">还将禁用 **资产交易** 按钮，该按钮用于打开一个查询窗体。</span><span class="sxs-lookup"><span data-stu-id="28c5d-127">The **Asset transactions** button, which opens an inquiry form is also disabled.</span></span> <span data-ttu-id="28c5d-128">您也可以在“固定资产”中打开 **资产交易** 查询窗体。</span><span class="sxs-lookup"><span data-stu-id="28c5d-128">You can also open the **Asset transactions** inquiry form in Fixed assets.</span></span>  
