---
title: 您无法从预测行中删除仓库需求预测维度
description: 您无法从预测行中删除仓库需求预测维度。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026306"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="7ab58-103">您无法从预测行中删除仓库需求预测维度</span><span class="sxs-lookup"><span data-stu-id="7ab58-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="7ab58-104">知识库编号：4614408</span><span class="sxs-lookup"><span data-stu-id="7ab58-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="7ab58-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="7ab58-105">Symptoms</span></span>

<span data-ttu-id="7ab58-106">当未在 **需求预测参数** 页的 **预测维度** 选项卡上分配 **仓库** 维度时，会发生此问题。</span><span class="sxs-lookup"><span data-stu-id="7ab58-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="7ab58-107">不过，**仓库** 列在 **需求预测** 页显示（**主计划 \> 预测 \> 手动预测实体 \> 需求预测行**）。</span><span class="sxs-lookup"><span data-stu-id="7ab58-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="7ab58-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="7ab58-108">Resolution</span></span>

<span data-ttu-id="7ab58-109">**需求预测参数** 页的 **预测维度** 选项卡上的设置不会影响 **需求预测** 页。</span><span class="sxs-lookup"><span data-stu-id="7ab58-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="7ab58-110">它们控制在调整后的需求预测中生成和显示的基准预测。</span><span class="sxs-lookup"><span data-stu-id="7ab58-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="7ab58-111">但是，它们不控制“实际”需求预测所需的维度。</span><span class="sxs-lookup"><span data-stu-id="7ab58-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="7ab58-112">通过对 **调整后的需求预测** 页上显示的记录授权，您可以将它们转换为预测模型的“实际”预测条目。</span><span class="sxs-lookup"><span data-stu-id="7ab58-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="7ab58-113">然后可以将该模型用于主计划。</span><span class="sxs-lookup"><span data-stu-id="7ab58-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="7ab58-114">在 **需求预测** 页上，需求预测行上显示的“实际”预测的维度是库存维度的一部分。</span><span class="sxs-lookup"><span data-stu-id="7ab58-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="7ab58-115">（此行为类似于销售订单行的行为。）如果未将系统设置为将 **仓库** 用作必需的库存维度，您可以自定义此页面来隐藏列。</span><span class="sxs-lookup"><span data-stu-id="7ab58-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
