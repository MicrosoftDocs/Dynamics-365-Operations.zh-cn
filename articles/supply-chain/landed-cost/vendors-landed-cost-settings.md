---
title: 为登陆成本添加了供应商设置
description: 本主题介绍在启用登陆成本模块时添加到现有“供应商”页的新字段。 您将使用这些字段设置要与登陆成本功能一起使用的供应商。
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 8cc0622cd761a671ebb88addc36b777cfefb7dc7
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500902"
---
# <a name="vendor-settings-added-for-landed-cost"></a><span data-ttu-id="3f9fc-104">为登陆成本添加了供应商设置</span><span class="sxs-lookup"><span data-stu-id="3f9fc-104">Vendor settings added for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3f9fc-105">启用 **登陆成本** 模块时，几个新字段将添加到现有的 **供应商** 页。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-105">When you enable the **Landed cost** module, several new fields are added to the existing **Vendors** page.</span></span> <span data-ttu-id="3f9fc-106">您将使用这些字段设置要与登陆成本功能一起使用的供应商。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-106">You use these fields to set up the vendors that you will use together with Landed cost features.</span></span>

<span data-ttu-id="3f9fc-107">要设置相关字段，转到 **采购 \> 供应商 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-107">To set the relevant fields, go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span> <span data-ttu-id="3f9fc-108">打开现有供应商，或创建一个新供应商，然后选择 **杂项详细信息** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-108">Open an existing vendor, or create a new vendor, and then select the **Miscellaneous details** FastTab.</span></span> <span data-ttu-id="3f9fc-109">**登陆成本** 模块添加的所有新字段都将显示在 **航行** 标题下。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-109">All the new fields that the **Landed cost** module adds appear under the **Voyages** heading.</span></span> <span data-ttu-id="3f9fc-110">下表介绍这些字段。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-110">The following table describes these fields.</span></span>

| <span data-ttu-id="3f9fc-111">字段</span><span class="sxs-lookup"><span data-stu-id="3f9fc-111">Field</span></span> | <span data-ttu-id="3f9fc-112">说明</span><span class="sxs-lookup"><span data-stu-id="3f9fc-112">Description</span></span> |
|---|---|
| <span data-ttu-id="3f9fc-113">装运类型</span><span class="sxs-lookup"><span data-stu-id="3f9fc-113">Shipping type</span></span> | <p><span data-ttu-id="3f9fc-114">选择与登陆成本相关的供应商角色：</span><span class="sxs-lookup"><span data-stu-id="3f9fc-114">Select the vendor's role in relation to Landed cost:</span></span></p><ul><li><span data-ttu-id="3f9fc-115">**无** – 供应商没有与登陆成本相关的特定角色。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-115">**None** – The vendor has no specific role that is related to Landed cost.</span></span> <span data-ttu-id="3f9fc-116">此值是默认设置，因为大多数供应商可能没有特定角色。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-116">This value is the default setting, because most vendors will probably have no specific role.</span></span></li><li><span data-ttu-id="3f9fc-117">**装运公司** – 供应商是装运公司。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-117">**Shipping company** – The vendor is a shipping company.</span></span> <span data-ttu-id="3f9fc-118">具有此装运类型的供应商可以在 **航行** 页上的 **装运公司** 字段中选择。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-118">Vendors that have this shipping type are available for selection in the **Shipping company** field on the **Voyages** page.</span></span></li><li><span data-ttu-id="3f9fc-119">**关税代理** – 供应商是关税代理。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-119">**Customs broker** – The vendor is a customs broker.</span></span> <span data-ttu-id="3f9fc-120">具有此装运类型的供应商可以在 **帐页** 页上的 **关税代理** 字段中选择。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-120">Vendors that have this shipping type are available for selection in the **Customs broker** field on the **Folios** page.</span></span></li><li><span data-ttu-id="3f9fc-121">**代理** – 供应商是代理。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-121">**Agent** – The vendor is an agent.</span></span> <span data-ttu-id="3f9fc-122">具有此装运类型的供应商可以在 **供应商** 和 **采购订单** 页上的 **代理** 字段中选择。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-122">Vendors that have this shipping type are available for selection in the **Agent** field on the **Vendors** and **Purchase orders** pages.</span></span></li></ul> |
| <span data-ttu-id="3f9fc-123">成本类型组</span><span class="sxs-lookup"><span data-stu-id="3f9fc-123">Cost type group</span></span> | <span data-ttu-id="3f9fc-124">将供应商分配到成本类型组，以选择[自动成本](auto-cost-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-124">Assign the vendor to a cost type group for the purpose of selecting [auto costs](auto-cost-setup.md).</span></span> |
| <span data-ttu-id="3f9fc-125">发运港口</span><span class="sxs-lookup"><span data-stu-id="3f9fc-125">From port</span></span> | <span data-ttu-id="3f9fc-126">选择航行的始发港口。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-126">Select the port of origin for the voyage.</span></span> |
| <span data-ttu-id="3f9fc-127">代理</span><span class="sxs-lookup"><span data-stu-id="3f9fc-127">Agent</span></span> | <span data-ttu-id="3f9fc-128">从供应商处进行采购时的默认代理。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-128">The default agent when purchases are made from the vendor.</span></span> |
| <span data-ttu-id="3f9fc-129">导入成本计算供应商</span><span class="sxs-lookup"><span data-stu-id="3f9fc-129">Import costing vendor</span></span> | <p><span data-ttu-id="3f9fc-130">指示供应商是否为登陆成本供应商。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-130">Indicate whether the vendor is a Landed cost vendor.</span></span></p><p><span data-ttu-id="3f9fc-131">**提示：** 您可以将此字段与记录级安全性一起使用，来限制创建航行时显示的采购订单。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-131">**Tip:** You can use this field together with record-level security to limit the purchase orders that are shown when a voyage is created.</span></span></p> |
| <span data-ttu-id="3f9fc-132">装运公司</span><span class="sxs-lookup"><span data-stu-id="3f9fc-132">Shipping company</span></span> | <span data-ttu-id="3f9fc-133">选择为供应商创建采购订单时使用的默认装运公司。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-133">Select the default shipping company that is used when purchase orders are created for the vendor.</span></span> |
| <span data-ttu-id="3f9fc-134">服务提供商</span><span class="sxs-lookup"><span data-stu-id="3f9fc-134">Services provider</span></span> | <span data-ttu-id="3f9fc-135">指示供应商是否是服务提供商。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-135">Indicate whether the vendor is services provider.</span></span> |
| <span data-ttu-id="3f9fc-136">超过/低于容差组</span><span class="sxs-lookup"><span data-stu-id="3f9fc-136">Over/Under tolerance group</span></span> | <span data-ttu-id="3f9fc-137">选择供应商的默认超过/低于容差组。</span><span class="sxs-lookup"><span data-stu-id="3f9fc-137">Select the default over/under tolerance group for the vendor.</span></span> |
