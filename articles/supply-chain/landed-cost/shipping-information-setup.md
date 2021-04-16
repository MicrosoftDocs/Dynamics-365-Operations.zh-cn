---
title: 装运信息设置
description: 本主题介绍如何为登陆成本模块设置装运信息。
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 74ac7e0eac545369eef1a48f0085c820a4728e75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833681"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="3134a-103">装运信息设置</span><span class="sxs-lookup"><span data-stu-id="3134a-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3134a-104">本主题介绍如何为 **登陆成本** 模块设置装运信息。</span><span class="sxs-lookup"><span data-stu-id="3134a-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="3134a-105">货物描述</span><span class="sxs-lookup"><span data-stu-id="3134a-105">Description of goods</span></span>

<span data-ttu-id="3134a-106">货物描述帮助确定货物的航行、装运集装箱或帐页以及其中的货物。</span><span class="sxs-lookup"><span data-stu-id="3134a-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="3134a-107">您可以在装运集装箱标头或帐页标头上选择货物描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="3134a-108">要使用货物描述，转到 **登陆成本 \> 装运信息设置 \> 货物描述**。</span><span class="sxs-lookup"><span data-stu-id="3134a-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="3134a-109">在那里，您可以查看、打开、创建和删除货物描述的记录。</span><span class="sxs-lookup"><span data-stu-id="3134a-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="3134a-110">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="3134a-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3134a-111">字段</span><span class="sxs-lookup"><span data-stu-id="3134a-111">Field</span></span> | <span data-ttu-id="3134a-112">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-112">Description</span></span> |
|---|---|
| <span data-ttu-id="3134a-113">货物描述</span><span class="sxs-lookup"><span data-stu-id="3134a-113">Description of goods</span></span> | <span data-ttu-id="3134a-114">为将使用此描述的货物类型输入唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="3134a-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="3134a-115">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-115">Description</span></span> | <span data-ttu-id="3134a-116">输入此类别中的货物类型的描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="3134a-117">船舶</span><span class="sxs-lookup"><span data-stu-id="3134a-117">Vessels</span></span>

<span data-ttu-id="3134a-118">船只是装运公司或代理使用的船舶或船只的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="3134a-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="3134a-119">创建航行时，必须始终为航行选择或输入船只。</span><span class="sxs-lookup"><span data-stu-id="3134a-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="3134a-120">如果您经常使用相同船只，那么可以通过为每个船只创建船只记录来更快、更轻松地创建新航行，从而允许用户从列表中选择船只，而不是每次都要手动输入名称或编号。</span><span class="sxs-lookup"><span data-stu-id="3134a-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="3134a-121">要使用船只，请转到 **登陆成本 \> 装运信息设置 \> 船只**。</span><span class="sxs-lookup"><span data-stu-id="3134a-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="3134a-122">在那里，您可以查看、打开、创建和删除船只的记录。</span><span class="sxs-lookup"><span data-stu-id="3134a-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="3134a-123">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="3134a-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3134a-124">字段</span><span class="sxs-lookup"><span data-stu-id="3134a-124">Field</span></span> | <span data-ttu-id="3134a-125">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-125">Description</span></span> |
|---|---|
| <span data-ttu-id="3134a-126">船舶</span><span class="sxs-lookup"><span data-stu-id="3134a-126">Vessel</span></span> | <span data-ttu-id="3134a-127">输入将用于在航行中运输货物的船的唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="3134a-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="3134a-128">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-128">Description</span></span> | <span data-ttu-id="3134a-129">输入船只的描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-129">Enter a description of the vessel.</span></span> <span data-ttu-id="3134a-130">通常，此描述确定船的名称以及装运公司/代理。</span><span class="sxs-lookup"><span data-stu-id="3134a-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="3134a-131">交货模式</span><span class="sxs-lookup"><span data-stu-id="3134a-131">Mode of delivery</span></span> | <span data-ttu-id="3134a-132">选择船只使用的交货方式（如 _空运_、_海运_ 或 _火车_）。</span><span class="sxs-lookup"><span data-stu-id="3134a-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="3134a-133">出口商</span><span class="sxs-lookup"><span data-stu-id="3134a-133">Exporters</span></span>

<span data-ttu-id="3134a-134">每个出口商记录确定可以定义为航行的供应商的供应商或出口商。</span><span class="sxs-lookup"><span data-stu-id="3134a-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="3134a-135">出口商可以与航行关联，并可以用于报告。</span><span class="sxs-lookup"><span data-stu-id="3134a-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="3134a-136">要使用出口商，请转到 **登陆成本 \> 装运信息设置 \> 出口商**。</span><span class="sxs-lookup"><span data-stu-id="3134a-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="3134a-137">在那里，您可以查看、打开、创建和删除出口商的记录。</span><span class="sxs-lookup"><span data-stu-id="3134a-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="3134a-138">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="3134a-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3134a-139">字段</span><span class="sxs-lookup"><span data-stu-id="3134a-139">Field</span></span> | <span data-ttu-id="3134a-140">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-140">Description</span></span> |
|---|---|
| <span data-ttu-id="3134a-141">出口商</span><span class="sxs-lookup"><span data-stu-id="3134a-141">Exporter</span></span> | <span data-ttu-id="3134a-142">输入在航行中运输的货物出口商的唯一标识名称/编号。</span><span class="sxs-lookup"><span data-stu-id="3134a-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="3134a-143">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-143">Description</span></span> | <span data-ttu-id="3134a-144">输入出口商的描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-144">Enter a description of the exporter.</span></span> <span data-ttu-id="3134a-145">通常，此描述确定装运公司/代理的完整名称。</span><span class="sxs-lookup"><span data-stu-id="3134a-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="3134a-146">商品代码</span><span class="sxs-lookup"><span data-stu-id="3134a-146">Commodity codes</span></span>

<span data-ttu-id="3134a-147">您将使用商品代码来帮助海关查验和计算航行中货物的关税税率。</span><span class="sxs-lookup"><span data-stu-id="3134a-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="3134a-148">您可以在 **已发布产品** 页选择商品代码。</span><span class="sxs-lookup"><span data-stu-id="3134a-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="3134a-149">要使用商品代码，请转到 **登陆成本 \> 装运信息设置 \> 商品代码**。</span><span class="sxs-lookup"><span data-stu-id="3134a-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="3134a-150">在那里，您可以查看、打开、创建和删除商品代码的记录。</span><span class="sxs-lookup"><span data-stu-id="3134a-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="3134a-151">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="3134a-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3134a-152">字段</span><span class="sxs-lookup"><span data-stu-id="3134a-152">Field</span></span> | <span data-ttu-id="3134a-153">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-153">Description</span></span> |
|---|---|
| <span data-ttu-id="3134a-154">商品代码</span><span class="sxs-lookup"><span data-stu-id="3134a-154">Commodity code</span></span> | <span data-ttu-id="3134a-155">为此商品类型输入唯一代码。</span><span class="sxs-lookup"><span data-stu-id="3134a-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="3134a-156">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-156">Description</span></span> | <span data-ttu-id="3134a-157">输入商品类型的描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="3134a-158">海关描述</span><span class="sxs-lookup"><span data-stu-id="3134a-158">Customs description</span></span>

<span data-ttu-id="3134a-159">海关描述帮助出于海关目的识别货物。</span><span class="sxs-lookup"><span data-stu-id="3134a-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="3134a-160">您可以在 **已发布产品** 页或采购订单行上选择海关描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="3134a-161">要使用海关描述，转到 **登陆成本 \> 装运信息设置 \> 海关描述**。</span><span class="sxs-lookup"><span data-stu-id="3134a-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="3134a-162">在那里，您可以查看、打开、创建和删除海关描述的记录。</span><span class="sxs-lookup"><span data-stu-id="3134a-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="3134a-163">下表说明了可用于每个记录的字段。</span><span class="sxs-lookup"><span data-stu-id="3134a-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="3134a-164">字段</span><span class="sxs-lookup"><span data-stu-id="3134a-164">Field</span></span> | <span data-ttu-id="3134a-165">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-165">Description</span></span> |
|---|---|
| <span data-ttu-id="3134a-166">海关描述</span><span class="sxs-lookup"><span data-stu-id="3134a-166">Customs description</span></span> | <span data-ttu-id="3134a-167">为此海关分类类型输入唯一代码。</span><span class="sxs-lookup"><span data-stu-id="3134a-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="3134a-168">通常，此代码将是关税主管机构为货物的描述和性质提供的官方描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="3134a-169">说明</span><span class="sxs-lookup"><span data-stu-id="3134a-169">Description</span></span> | <span data-ttu-id="3134a-170">输入海关分类的描述。</span><span class="sxs-lookup"><span data-stu-id="3134a-170">Enter a description of the customs classification.</span></span> |
