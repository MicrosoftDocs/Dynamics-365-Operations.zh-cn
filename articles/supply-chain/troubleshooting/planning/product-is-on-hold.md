---
title: 产品因交易而暂停
description: 在确认计划订单后，您将收到一条错误消息，指示物料因交易而暂停。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6654e6437a088218db116b955631be4c7e62de5f
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301271"
---
# <a name="product-is-on-hold-for-transactions"></a><span data-ttu-id="f11c9-103">产品因交易而暂停</span><span class="sxs-lookup"><span data-stu-id="f11c9-103">Product is on hold for transactions</span></span>

<span data-ttu-id="f11c9-104">错误代码：SYS13295</span><span class="sxs-lookup"><span data-stu-id="f11c9-104">Error code: SYS13295</span></span>

## <a name="symptoms"></a><span data-ttu-id="f11c9-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="f11c9-105">Symptoms</span></span>

<span data-ttu-id="f11c9-106">在确定计划订单后，您将收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="f11c9-106">After you firm planned orders, you receive the following error message:</span></span>

> <span data-ttu-id="f11c9-107">物料 %1 正在等待用于 %2 中的交易记录。</span><span class="sxs-lookup"><span data-stu-id="f11c9-107">Item %1 is on hold for transactions in %2.</span></span>

## <a name="cause"></a><span data-ttu-id="f11c9-108">原因</span><span class="sxs-lookup"><span data-stu-id="f11c9-108">Cause</span></span>

<span data-ttu-id="f11c9-109">在描述锁定的物料时，系统可交换使用术语 *已锁定*、*已停止* 和 *暂停*。</span><span class="sxs-lookup"><span data-stu-id="f11c9-109">When describing blocked items, system uses the terms *blocked*, *stopped*, and *on hold* interchangeably.</span></span> <span data-ttu-id="f11c9-110">此错误意味着物料在其默认订单设置中设置为 **已停止**。</span><span class="sxs-lookup"><span data-stu-id="f11c9-110">This error means that the item is set as **Stopped** in its default order settings.</span></span>

<span data-ttu-id="f11c9-111">如果物料已锁定，并且您将其添加到采购订单或销售订单行，您将收到一条警告消息。</span><span class="sxs-lookup"><span data-stu-id="f11c9-111">If an item is blocked, and you add it to a purchase order or sales order line, you receive a warning message.</span></span> <span data-ttu-id="f11c9-112">当物料已锁定时，将不能修改与采购订单或销售订单行相关的库存交易（例如，当过帐装箱单或发票时）。</span><span class="sxs-lookup"><span data-stu-id="f11c9-112">When an item is blocked, inventory transactions that are related to the purchase order or sales order line can't be modified (for example, when you post a packing slip or an invoice).</span></span> <span data-ttu-id="f11c9-113">您可以锁定已采购物料并同时出售此物料。</span><span class="sxs-lookup"><span data-stu-id="f11c9-113">You can block a purchased item, and, at the same time, sell the item.</span></span> <span data-ttu-id="f11c9-114">在这种情况下，在采购订单上选中 **已停止** 复选框，但未在库存或销售订单上锁定物料。</span><span class="sxs-lookup"><span data-stu-id="f11c9-114">In this case, the **Stopped** check box is selected on a purchase order, but the item isn't blocked in inventory or on a sales order.</span></span>

<span data-ttu-id="f11c9-115">以下是一些可能导致物料编号锁定而无法出售的条件：</span><span class="sxs-lookup"><span data-stu-id="f11c9-115">Here are some of the conditions that can cause an item number to be blocked from being sold:</span></span>

- <span data-ttu-id="f11c9-116">物料仍在开发或制造中。</span><span class="sxs-lookup"><span data-stu-id="f11c9-116">The item is still under development or manufacture.</span></span> <span data-ttu-id="f11c9-117">因此，您不希望将其出售或预留。</span><span class="sxs-lookup"><span data-stu-id="f11c9-117">Therefore, you don't want it to be sold or reserved.</span></span>
- <span data-ttu-id="f11c9-118">您收到了许多有缺陷的物料，必须更正缺陷才能出售物料。</span><span class="sxs-lookup"><span data-stu-id="f11c9-118">You've received many defective items, and the defects must be corrected before the item can be sold.</span></span>

<span data-ttu-id="f11c9-119">在这种情况下，您可以锁定此物料，直到解决问题。</span><span class="sxs-lookup"><span data-stu-id="f11c9-119">In cases of this type, you can block the item until the issue is resolved.</span></span>

<span data-ttu-id="f11c9-120">如果物料已锁定，并且您创建一个退货单行，您将收到一条消息。</span><span class="sxs-lookup"><span data-stu-id="f11c9-120">If an item is blocked, and you create a return order line, you receive a message.</span></span> <span data-ttu-id="f11c9-121">您不能锁定一系列物料或一批物料。</span><span class="sxs-lookup"><span data-stu-id="f11c9-121">You can't block a series or a lot of an item.</span></span> <span data-ttu-id="f11c9-122">如果必须锁定部分物料，可以通过移动库存或锁定该期间物料的全部存货来锁定它们。</span><span class="sxs-lookup"><span data-stu-id="f11c9-122">If parts of an item must be blocked, you can block them by moving inventory or by blocking the full stock of the item for that period.</span></span>

## <a name="resolution"></a><span data-ttu-id="f11c9-123">解决方法</span><span class="sxs-lookup"><span data-stu-id="f11c9-123">Resolution</span></span>

- <span data-ttu-id="f11c9-124">打开物料的 **默认订单设置** 页面，并清除 **已停止** 复选框。</span><span class="sxs-lookup"><span data-stu-id="f11c9-124">Open the **Default order settings** page for the item, and clear the **Stopped** checkbox.</span></span>
