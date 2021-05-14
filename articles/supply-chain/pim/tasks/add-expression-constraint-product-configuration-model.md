---
title: 将表达式约束添加到产品配置模型
description: 该过程显示如何添加新的约束表达式到产品配置模型。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920873"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="a13e3-103">将表达式约束添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="a13e3-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a13e3-104">该过程显示如何添加新的约束表达式到产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="a13e3-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="a13e3-105">它显示，如果用户选择为金属的前格栅，应该如何授权必须应用于扬声器的护角。</span><span class="sxs-lookup"><span data-stu-id="a13e3-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="a13e3-106">该过程使用演示公司 USMF 的高端扬声器组件。</span><span class="sxs-lookup"><span data-stu-id="a13e3-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="a13e3-107">创建一个表达式约束</span><span class="sxs-lookup"><span data-stu-id="a13e3-107">Create an expression constraint</span></span>

1. <span data-ttu-id="a13e3-108">转到 **产品信息管理 \> 产品 \> 产品配置模型**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="a13e3-109">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a13e3-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a13e3-110">此示例使用高端扬声器模型。</span><span class="sxs-lookup"><span data-stu-id="a13e3-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="a13e3-111">在列表中，选择所选择行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a13e3-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="a13e3-112">展开 **约束** 部分。</span><span class="sxs-lookup"><span data-stu-id="a13e3-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="a13e3-113">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-113">Select **Add**.</span></span>
7. <span data-ttu-id="a13e3-114">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-114">Select **Create**.</span></span>
8. <span data-ttu-id="a13e3-115">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a13e3-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="a13e3-116">输入表达式</span><span class="sxs-lookup"><span data-stu-id="a13e3-116">Enter expression</span></span>

1. <span data-ttu-id="a13e3-117">选择 **编辑表达式**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="a13e3-118">如果您解锁此阶段任务记录的用户界面，您可以使用 IntelliSense 和符号列表，以构建约束表达式。</span><span class="sxs-lookup"><span data-stu-id="a13e3-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="a13e3-119">在 **ConstraintBody** 字段中，输入“Implies[FrontGrill=="Metal", CornerProtection]”。</span><span class="sxs-lookup"><span data-stu-id="a13e3-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="a13e3-120">此表达逻辑表明：如果“前格栅”为金属，则必须选择护角选项。</span><span class="sxs-lookup"><span data-stu-id="a13e3-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="a13e3-121">选择 **验证**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-121">Select **Validate**.</span></span>
    * <span data-ttu-id="a13e3-122">核实功能通过约束表达式运行并检查语法错误。</span><span class="sxs-lookup"><span data-stu-id="a13e3-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="a13e3-123">选择 **关闭**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-123">Select **Close**.</span></span>
5. <span data-ttu-id="a13e3-124">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a13e3-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]