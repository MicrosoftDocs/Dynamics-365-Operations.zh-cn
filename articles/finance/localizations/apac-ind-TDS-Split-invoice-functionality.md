---
title: 拆分发票功能
description: 本主题介绍了按交货地址和税务帐号 (TAN) 拆分发票的设置和功能。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023063"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="d5dfd-103">拆分发票功能</span><span class="sxs-lookup"><span data-stu-id="d5dfd-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5dfd-104">本主题介绍了按交货地址和税务帐号 (TAN) 拆分发票的设置和功能。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="d5dfd-105">在 **应付帐款参数** 页面的 **常规** 选项卡上，选中 **产品收据** 或 **发票** 复选框以过帐和拆分在 **采购订单** 页面上具有不同交货地址和 TAN 的产品收据或发票。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="d5dfd-106">然后，按交货地址和 TAN 拆分已过帐的发票。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="d5dfd-107">在 **汇总更新** 选项卡上，在 **拆分依据** 快速选项卡的 **交货信息** 行中，将 **确认**、**领料单**、**装箱单** 或 **发票** 选项设置为 **是**，以过帐和拆分在 **销售订单** 页面上为不同的发票行定义不同的交货地址和 TAN 的确认、领料单、装箱单或发票。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="d5dfd-108">依次按交货地址和 TAN 拆分发票。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="d5dfd-109">如果 **交货信息** 的选项均为设置为 **是**，该发票作为单个发票过帐。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="d5dfd-110">不会进行发票拆分。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="d5dfd-111">若要拆分和过帐发票行具有不同交货地址和 TAN 的装箱单，必须将 **交货信息** 的 **装箱单** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="d5dfd-112">若要拆分和过帐发票行具有不同交货地址和 TAN 的发票，必须将 **交货信息** 的 **发票** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="d5dfd-113">若要过帐发票行具有不同交货地址，但具有相同 TAN 的发票，必须将 **交货信息** 的 **发票** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="d5dfd-114">按交货地址拆分发票。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="d5dfd-115">示例</span><span class="sxs-lookup"><span data-stu-id="d5dfd-115">Example</span></span>

<span data-ttu-id="d5dfd-116">在此示例中，在 **应付帐款参数** 页面的 **汇总更新** 选项卡上，将 **交货信息** 的 **发票** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="d5dfd-117">过帐在行上对交货地址和 TAN 具有以下设置的采购发票：</span><span class="sxs-lookup"><span data-stu-id="d5dfd-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="d5dfd-118">**物料行 1：** 交货地址 1，TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="d5dfd-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="d5dfd-119">**物料行 2：** 交货地址 1，TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="d5dfd-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="d5dfd-120">**物料行 3：** 交货地址 2，TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="d5dfd-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="d5dfd-121">**物料行 4：** 交货地址 3，TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="d5dfd-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="d5dfd-122">在此情况下，原始发票将拆分为两个发票，并通过以下方式过帐：</span><span class="sxs-lookup"><span data-stu-id="d5dfd-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="d5dfd-123">针对物料行 1 和物料行 2 过帐发票 1，因为这两行具有相同的交货地址和 TAN。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="d5dfd-124">针对物料行 3 过帐发票 2。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="d5dfd-125">针对物料行 4 过帐发票 3。</span><span class="sxs-lookup"><span data-stu-id="d5dfd-125">Invoice 3 is posted for item line 4.</span></span>
