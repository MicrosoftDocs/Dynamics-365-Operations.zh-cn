---
title: 设置包含 TDS 分配的付款计划
description: 本主题说明如何设置包含从源扣缴税款 (TDS) 分配的付款计划。
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
ms.openlocfilehash: 47551f52f35fec5ae49d696e3f4027b7d2eb2e19
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023066"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a><span data-ttu-id="f270d-103">设置包含 TDS 分配的付款计划</span><span class="sxs-lookup"><span data-stu-id="f270d-103">Set up payment schedules with TDS allocation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f270d-104">本主题说明如何设置包含从源扣缴税款 (TDS) 分配的付款计划。</span><span class="sxs-lookup"><span data-stu-id="f270d-104">This topic explains how to set up payment schedules with Tax Deducted at Source (TDS) allocation.</span></span>

1. <span data-ttu-id="f270d-105">转到 **应付帐款 \> 付款设置 \> 付款计划**。</span><span class="sxs-lookup"><span data-stu-id="f270d-105">Go to **Accounts payable \> Payment setup \> Payment schedules**.</span></span>

    <span data-ttu-id="f270d-106">[![付款计划页面](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span><span class="sxs-lookup"><span data-stu-id="f270d-106">[![Payment schedules page](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)</span></span>

2. <span data-ttu-id="f270d-107">在操作窗格上，选择 **新建** 以创建付款计划，然后输入所需的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f270d-107">On the Action Pane, select **New** to create a payment schedule, and enter the required details.</span></span>
3. <span data-ttu-id="f270d-108">在 **分配** 字段中，选择要用于为付款计划分配付款的方法。</span><span class="sxs-lookup"><span data-stu-id="f270d-108">In the **Allocation** field, select the method to use to allocate the payment for the payment schedule:</span></span>

    - <span data-ttu-id="f270d-109">合计</span><span class="sxs-lookup"><span data-stu-id="f270d-109">Total</span></span>
    - <span data-ttu-id="f270d-110">固定金额</span><span class="sxs-lookup"><span data-stu-id="f270d-110">Fixed amount</span></span>
    - <span data-ttu-id="f270d-111">固定数量</span><span class="sxs-lookup"><span data-stu-id="f270d-111">Fixed quantity</span></span>
    - <span data-ttu-id="f270d-112">指定</span><span class="sxs-lookup"><span data-stu-id="f270d-112">Specified</span></span>

    <span data-ttu-id="f270d-113">**预缴税金分配** 字段显示付款计划的 TDS 分配方法。</span><span class="sxs-lookup"><span data-stu-id="f270d-113">The **Withholding tax allocation** field shows the TDS allocation method for the payment schedule.</span></span> <span data-ttu-id="f270d-114">如果在 **分配** 字段中选择 **合计**，**预缴税金分配** 字段将自动设置为 **合计**。</span><span class="sxs-lookup"><span data-stu-id="f270d-114">If you select **Total** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Total**.</span></span> <span data-ttu-id="f270d-115">如果在 **分配** 字段中选择 **固定金额**、**固定数量** 或 **指定**，**预缴税金分配** 字段将自动设置为 **按比例**。</span><span class="sxs-lookup"><span data-stu-id="f270d-115">If you select **Fixed amount**, **Fixed quantity**, or **Specified** in the **Allocation** field, the **Withholding tax allocation** field is automatically set to **Proportionally**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f270d-116">如果 **预缴税金分配** 字段设置为 **合计**，将基于包括 TDS 金额的总额计算分期付款。</span><span class="sxs-lookup"><span data-stu-id="f270d-116">If the **Withholding tax allocation** field is set to **Total**, the payment installments are calculated based on the gross amount, which includes the TDS amount.</span></span> <span data-ttu-id="f270d-117">如果 **预缴税金分配** 字段设置为 **按比例**，将基于扣除 TDS 金额后的净发票金额计算分期付款。</span><span class="sxs-lookup"><span data-stu-id="f270d-117">If the **Withholding tax allocation** field is set to **Proportionally**, the payment installments are calculated based on the net invoice amount after the TDS amount is deducted.</span></span>

4. <span data-ttu-id="f270d-118">输入其他所需的详细信息，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="f270d-118">Enter the other required details, and then close the page.</span></span>
