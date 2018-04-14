--- 
title: "定义财务维度"
description: "此任务指南演示如何添加实体支持的财务维度和自定义的财务维度。"
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7ea96953d07b4025f294a07040ea9d8b1db87945
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="define-financial-dimensions"></a><span data-ttu-id="1470f-103">定义财务维度</span><span class="sxs-lookup"><span data-stu-id="1470f-103">Define financial dimensions</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1470f-104">此任务指南演示如何添加实体支持的财务维度和自定义的财务维度。</span><span class="sxs-lookup"><span data-stu-id="1470f-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="1470f-105">此指南使用演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="1470f-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="1470f-106">创建实体支持的财务维度</span><span class="sxs-lookup"><span data-stu-id="1470f-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="1470f-107">转到“总帐”>“会计科目表”>“维度”>“财务维度”。</span><span class="sxs-lookup"><span data-stu-id="1470f-107">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="1470f-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1470f-108">Click New.</span></span>
3. <span data-ttu-id="1470f-109">在“源用户值”字段中，选择系统中定义的实体作为财务维度的基础。</span><span class="sxs-lookup"><span data-stu-id="1470f-109">In the User values from field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="1470f-110">在“维度名称”字段中，输入描述财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="1470f-110">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="1470f-111">该名称可与系统定义的实体名称不同，但不能含有空格或特殊字符。</span><span class="sxs-lookup"><span data-stu-id="1470f-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>  
5. <span data-ttu-id="1470f-112">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1470f-112">Click Activate.</span></span>
    * <span data-ttu-id="1470f-113">“启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。</span><span class="sxs-lookup"><span data-stu-id="1470f-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1470f-114">在启用财务维度前，您可以输入维度值，但是财务维度在启用后才能使用。</span><span class="sxs-lookup"><span data-stu-id="1470f-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="1470f-115">在启用消息上，单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="1470f-115">Click Close on the activation message.</span></span>
7. <span data-ttu-id="1470f-116">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1470f-116">Click Activate.</span></span>
    * <span data-ttu-id="1470f-117">维度启用可安排在特定日期和时间批量运行。</span><span class="sxs-lookup"><span data-stu-id="1470f-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="1470f-118">单击“维度值”。</span><span class="sxs-lookup"><span data-stu-id="1470f-118">Click Dimension values.</span></span>
    * <span data-ttu-id="1470f-119">一些维度值是公司特定的。</span><span class="sxs-lookup"><span data-stu-id="1470f-119">Some dimension values are company specific.</span></span> <span data-ttu-id="1470f-120">您可以通过验证公司名称是否在维度值列表中来验证是否是特定于公司的维度值。</span><span class="sxs-lookup"><span data-stu-id="1470f-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="1470f-121">创建自定义的财务维度</span><span class="sxs-lookup"><span data-stu-id="1470f-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="1470f-122">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1470f-122">Close the page.</span></span>
2. <span data-ttu-id="1470f-123">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1470f-123">Click New.</span></span>
3. <span data-ttu-id="1470f-124">在“使用以下来源中的值”字段中，选择 <Custom dimension>。</span><span class="sxs-lookup"><span data-stu-id="1470f-124">In the Use values from field, select <Custom dimension>.</span></span>
4. <span data-ttu-id="1470f-125">在“维度名称”字段中，输入描述财务维度的值。</span><span class="sxs-lookup"><span data-stu-id="1470f-125">In the Dimension name field, type a value to describe the financial dimension.</span></span>
    * <span data-ttu-id="1470f-126">名称不能含有空格或特殊字符。</span><span class="sxs-lookup"><span data-stu-id="1470f-126">The name cannot contain spaces or special characters.</span></span>  
    * <span data-ttu-id="1470f-127">您还可以指定科目掩码以限制您为维度值输入的金额和信息类型。</span><span class="sxs-lookup"><span data-stu-id="1470f-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    * <span data-ttu-id="1470f-128">您可以输入保持不变的每个维度值的信息，例如的字符的字母或连字符。</span><span class="sxs-lookup"><span data-stu-id="1470f-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="1470f-129">还可以输入数字标志 (#) 和和符号 (&) 作为每次要更改的字母和数字的占位符创建维度值。</span><span class="sxs-lookup"><span data-stu-id="1470f-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="1470f-130">使用一个数字标志 (#) 作为编号占位符和符号 (&) 作为信函的占位符。</span><span class="sxs-lookup"><span data-stu-id="1470f-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="1470f-131">示例：若要限制维度值为字母 CC 和三个数字，您要输入 CC-### 作为格式掩码。</span><span class="sxs-lookup"><span data-stu-id="1470f-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="1470f-132">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1470f-132">Click Activate.</span></span>
    * <span data-ttu-id="1470f-133">“启用财务维度”更新带有财务维度名称的表格，并移除已删除的维度。</span><span class="sxs-lookup"><span data-stu-id="1470f-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="1470f-134">在启用财务维度前，您可以输入维度值，但是财务维度在启用后才能使用。</span><span class="sxs-lookup"><span data-stu-id="1470f-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="1470f-135">单击“启用”。</span><span class="sxs-lookup"><span data-stu-id="1470f-135">Click Activate.</span></span>
    * <span data-ttu-id="1470f-136">维度启用可安排在特定日期和时间批量运行。</span><span class="sxs-lookup"><span data-stu-id="1470f-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
7. <span data-ttu-id="1470f-137">单击“维度值”。</span><span class="sxs-lookup"><span data-stu-id="1470f-137">Click Dimension values.</span></span>
8. <span data-ttu-id="1470f-138">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="1470f-138">Click New.</span></span>
9. <span data-ttu-id="1470f-139">在“维度值”字段中，输入描述财务维度值的名称。</span><span class="sxs-lookup"><span data-stu-id="1470f-139">In the Dimension value field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="1470f-140">在“描述”字段中，输入描述您的财务维度值的描述。</span><span class="sxs-lookup"><span data-stu-id="1470f-140">In the Description field, type a description that describes your financial dimension value.</span></span>


