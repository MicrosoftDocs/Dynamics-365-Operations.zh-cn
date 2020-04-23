---
title: 移动平均回退成本序列
description: 此主题介绍 Microsoft Dynamics 365 Supply Chain Management 中的移动平均回退成本计算顺序。
author: AndersGirke
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: b2172dfbec0a7f0fa25a081e4d92635a09f00e46
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261305"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="ef6c8-103">移动平均回退成本序列</span><span class="sxs-lookup"><span data-stu-id="ef6c8-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="ef6c8-104">库存成本的一种计算方法是使用_移动平均_。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="ef6c8-105">可以为每项库存物料最多关联三个成本值：</span><span class="sxs-lookup"><span data-stu-id="ef6c8-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="ef6c8-106">**最后发货** – 库存变负前分配的最后发货成本</span><span class="sxs-lookup"><span data-stu-id="ef6c8-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="ef6c8-107">**有效成本** – 成本计算版本中最后激活的成本</span><span class="sxs-lookup"><span data-stu-id="ef6c8-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="ef6c8-108">**物料价格** – 为发布的产品指定的成本</span><span class="sxs-lookup"><span data-stu-id="ef6c8-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="ef6c8-109">为了确定在移动平均计算中应该使用这些成本值中的哪一个，系统使用_回退成本序列_建立值的首选顺序。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="ef6c8-110">如果首选成本值不可用，系统将使用下一个首选值，依此类推。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="ef6c8-111">在 Microsoft Dynamics 365 Supply Chain Management 的早期版本中，系统使用固定回退成本序列（_最后发货 – 有效成本 – 物料价格_）。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="ef6c8-112">在版本 10.0.11 中，此序列仍然是默认序列。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="ef6c8-113">但是，也可以开启在三个可用回退成本序列中进行选择的功能。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="ef6c8-114">尤其可以将此功能用于定期使用负库存值的组织。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="ef6c8-115">若要为回退成本序列使用选择器，您（或管理员）必须使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)开启名称为_移动平均回退成本序列_的功能。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="ef6c8-116">若要选择移动平均回退成本计算序列，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="ef6c8-117">打开**参数**页面。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="ef6c8-118">在**库存会计**选项卡的**移动平均**部分中，将**回退成本序列**字段设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="ef6c8-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="ef6c8-119">**最后发货 – 有效成本 – 物料价格** – 此序列是默认序列。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="ef6c8-120">这是未开启_移动平均回退成本序列_功能时使用的同一个序列。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="ef6c8-121">**有效成本 - 上次发货**</span><span class="sxs-lookup"><span data-stu-id="ef6c8-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="ef6c8-122">**有效成本 – 物料价格** – 组织使用的业务流程中库存定期变负，并且同时交易量极高，组织可能会遇到性能问题。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="ef6c8-123">此设置有助于缓解这些性能问题。</span><span class="sxs-lookup"><span data-stu-id="ef6c8-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="ef6c8-124">![库存会计参数](media/inventory-accounting-parameters.png "库存会计参数")</span><span class="sxs-lookup"><span data-stu-id="ef6c8-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
