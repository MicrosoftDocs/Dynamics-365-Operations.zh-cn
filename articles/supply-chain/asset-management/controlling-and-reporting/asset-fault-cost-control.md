---
title: 资产故障成本控制
description: 本主题介绍资产管理中的资产故障成本控制。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCostControlFault
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 44b101c3b386c3edd8aec4c44e8ee834519718ec
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811174"
---
# <a name="asset-fault-cost-control"></a><span data-ttu-id="775ff-103">资产故障成本控制</span><span class="sxs-lookup"><span data-stu-id="775ff-103">Asset fault cost control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="775ff-104">在资产管理中，可计算资产故障登记的成本，以便获取实际成本与预算成本的比较概览。</span><span class="sxs-lookup"><span data-stu-id="775ff-104">In Asset Management, you can calculate costs on asset fault registrations to get an overview of actual costs compared to budget costs.</span></span> <span data-ttu-id="775ff-105">实际成本基于过帐的交易记录。</span><span class="sxs-lookup"><span data-stu-id="775ff-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="775ff-106">日期是记录故障特征时的故障日期。</span><span class="sxs-lookup"><span data-stu-id="775ff-106">The date is the fault date on which the symptom was recorded.</span></span>

1. <span data-ttu-id="775ff-107">单击 **资产管理** > **查询** > **资产故障** > **资产故障成本控制**。</span><span class="sxs-lookup"><span data-stu-id="775ff-107">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault cost control**.</span></span>

2. <span data-ttu-id="775ff-108">在 **资产故障成本控制** 对话框中，选择计算中要包括的财务维度集（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="775ff-108">In the **Asset fault cost control** dialog, select a financial dimension set to be included in the calculation, if required.</span></span>

4. <span data-ttu-id="775ff-109">如果不希望显示包含零成本的结果，请在 **忽略零** 切换按钮上选择“是”。</span><span class="sxs-lookup"><span data-stu-id="775ff-109">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="775ff-110">可使用 **级别** 字段指示要与功能位置有关的成本控制行的详细程度。</span><span class="sxs-lookup"><span data-stu-id="775ff-110">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="775ff-111">例如，如果在字段中插入数字“1”，并且采用了多级别功能位置结构，则将在最上级别显示某个功能位置的所有资产故障成本控制行，因此，可以从较低级别的功能位置叠加行中的工时。</span><span class="sxs-lookup"><span data-stu-id="775ff-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="775ff-112">如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有资产故障成本控制行。</span><span class="sxs-lookup"><span data-stu-id="775ff-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault cost control lines on all the functional location levels to which they are related.</span></span>

6. <span data-ttu-id="775ff-113">如果要限制搜索，可在 **要包括的记录** 快速选项卡上选择特定资产、故障日期和故障成因。</span><span class="sxs-lookup"><span data-stu-id="775ff-113">If you want to limit the search, you can select specific assets, fault dates, and fault causes on the **Records to include** FastTab.</span></span>

7. <span data-ttu-id="775ff-114">单击 **确定** 开始计算。</span><span class="sxs-lookup"><span data-stu-id="775ff-114">Click **OK** to start the calculation.</span></span>

8. <span data-ttu-id="775ff-115">单击 **分组依据** 按钮显示所需的计算详细程度。</span><span class="sxs-lookup"><span data-stu-id="775ff-115">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="775ff-116">将突出显示所选 **分组依据** 按钮。</span><span class="sxs-lookup"><span data-stu-id="775ff-116">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="775ff-117">单击按钮将其激活或停用。</span><span class="sxs-lookup"><span data-stu-id="775ff-117">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="775ff-118">示例</span><span class="sxs-lookup"><span data-stu-id="775ff-118">Example</span></span>

<span data-ttu-id="775ff-119">此示例显示资产故障成本控制计算。</span><span class="sxs-lookup"><span data-stu-id="775ff-119">This example shows an asset fault cost control calculation.</span></span>

- <span data-ttu-id="775ff-120">**原始预算** 字段显示工作订单预测中的预算成本。</span><span class="sxs-lookup"><span data-stu-id="775ff-120">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="775ff-121">**实际成本** 字段显示工作订单中的已过帐成本。</span><span class="sxs-lookup"><span data-stu-id="775ff-121">The **Actual cost** field shows posted costs on work orders.</span></span> 
- <span data-ttu-id="775ff-122">**承诺成本** 字段显示在与工作订单关联时，公司承诺的总成本。</span><span class="sxs-lookup"><span data-stu-id="775ff-122">The **Committed cost** field shows total costs that your company is committed to in relation to work orders.</span></span>

    ![图 1](media/05-controlling-and-reporting.png)

<span data-ttu-id="775ff-124">有关如何设置故障的信息，请参阅[故障管理](../setup-for-work-orders/fault-management.md)主题。</span><span class="sxs-lookup"><span data-stu-id="775ff-124">For information about how to set up faults, see the [Fault management](../setup-for-work-orders/fault-management.md) topic.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]