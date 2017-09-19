--- 
title: "将表达式约束添加到产品配置模型"
description: "该过程显示如何添加新的约束表达式到产品配置模型。"
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8db46c5b8361c96745b440c0d0684e18c06a6c6f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="15d7e-103">将表达式约束添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="15d7e-103">Add an expression constraint to a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="15d7e-104">该过程显示如何添加新的约束表达式到产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="15d7e-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="15d7e-105">它显示，如果用户选择为金属的前格栅，应该如何授权必须应用于扬声器的护角。</span><span class="sxs-lookup"><span data-stu-id="15d7e-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="15d7e-106">该过程使用演示公司 USMF 的高端扬声器组件。</span><span class="sxs-lookup"><span data-stu-id="15d7e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="15d7e-107">创建一个表达式约束</span><span class="sxs-lookup"><span data-stu-id="15d7e-107">Create an expression constraint</span></span>
1. <span data-ttu-id="15d7e-108">单击“产品变型模型定义”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="15d7e-109">单击“产品配置模型”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="15d7e-110">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="15d7e-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="15d7e-111">此示例使用高端扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="15d7e-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="15d7e-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="15d7e-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="15d7e-113">展开“约束”部分。</span><span class="sxs-lookup"><span data-stu-id="15d7e-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="15d7e-114">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-114">Click Add.</span></span>
7. <span data-ttu-id="15d7e-115">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-115">Click Create.</span></span>
8. <span data-ttu-id="15d7e-116">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="15d7e-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="15d7e-117">输入表达式</span><span class="sxs-lookup"><span data-stu-id="15d7e-117">Enter expression</span></span>
1. <span data-ttu-id="15d7e-118">单击“编辑表达式”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-118">Click Edit expression.</span></span>
    * <span data-ttu-id="15d7e-119">如果您解锁此阶段任务记录的用户界面，您可以使用 IntelliSense 和符号列表，以构建约束表达式。</span><span class="sxs-lookup"><span data-stu-id="15d7e-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="15d7e-120">在“约束体”字段中，输入“提示[前格栅==“金属”，护角]”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="15d7e-121">此表达逻辑表明：如果“前格栅”为金属，则必须选择护角选项。</span><span class="sxs-lookup"><span data-stu-id="15d7e-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="15d7e-122">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-122">Click Validate.</span></span>
    * <span data-ttu-id="15d7e-123">核实功能通过约束表达式运行并检查语法错误。</span><span class="sxs-lookup"><span data-stu-id="15d7e-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="15d7e-124">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-124">Click Close.</span></span>
5. <span data-ttu-id="15d7e-125">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="15d7e-125">Click OK.</span></span>

