---
title: 供应商代码未针对特定产品和日期授权
description: 当您尝试确认计划订单或向采购订单添加一行时，将收到一条错误消息，指示供应商代码未针对产品和日期授权。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294023"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="f55fc-103">供应商代码未针对特定产品和日期授权</span><span class="sxs-lookup"><span data-stu-id="f55fc-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="f55fc-104">错误代码：SYP4881415</span><span class="sxs-lookup"><span data-stu-id="f55fc-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="f55fc-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f55fc-105">Symptoms</span></span>

<span data-ttu-id="f55fc-106">当您尝试确认计划订单或向采购订单添加一行时，将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="f55fc-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="f55fc-107">供应商代码 %1 未针对 %3 上的 %2 授权。</span><span class="sxs-lookup"><span data-stu-id="f55fc-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="f55fc-108">原因</span><span class="sxs-lookup"><span data-stu-id="f55fc-108">Cause</span></span>

<span data-ttu-id="f55fc-109">发生错误的原因是指定产品的 **核准供应商检查方法** 字段设置为 *仅警告* 或 *不允许*，并且供应商当前未授权供应该产品。</span><span class="sxs-lookup"><span data-stu-id="f55fc-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="f55fc-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="f55fc-110">Resolution</span></span>

<span data-ttu-id="f55fc-111">若要解决此问题，请禁用相关产品的供应商检查或审核供应商。</span><span class="sxs-lookup"><span data-stu-id="f55fc-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="f55fc-112">若要禁用产品的供应商检查，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f55fc-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="f55fc-113">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="f55fc-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f55fc-114">打开相关产品。</span><span class="sxs-lookup"><span data-stu-id="f55fc-114">Open the relevant product.</span></span>
1. <span data-ttu-id="f55fc-115">在 **购买** 快速选项卡上，将 **核准供应商检查方法** 字段设置为除 *仅警告* 或 *不允许* 以外的值。</span><span class="sxs-lookup"><span data-stu-id="f55fc-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="f55fc-116">若要审核产品的供应商，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f55fc-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="f55fc-117">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="f55fc-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f55fc-118">打开相关物料。</span><span class="sxs-lookup"><span data-stu-id="f55fc-118">Open the relevant item.</span></span>
1. <span data-ttu-id="f55fc-119">在操作窗格上的 **购买** 选项卡上，在 **核准供应商** 组中，选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="f55fc-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="f55fc-120">在 **核准供应商** 列表页面上，向网格添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="f55fc-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="f55fc-121">**供应商** – 选择要为当前产品审核的供应商。</span><span class="sxs-lookup"><span data-stu-id="f55fc-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="f55fc-122">**生效日期** – 选择供应商获得批准的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="f55fc-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="f55fc-123">**到期日期** – 选择供应商获得批准的最后一个日期。</span><span class="sxs-lookup"><span data-stu-id="f55fc-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="f55fc-124">有关详细信息，请参阅[审核特定产品的供应商](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md)。</span><span class="sxs-lookup"><span data-stu-id="f55fc-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>
