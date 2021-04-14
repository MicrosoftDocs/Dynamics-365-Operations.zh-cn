---
title: 使用 Regression Suite Automation Tool 的数据不可知测试
description: 此主题讨论有关使用 Regression Suite Automation Tool 的数据不可知测试的建议。
author: kfend
ms.date: 09/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2019-09-11
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 120a88790b7cdb6a8cfcf97cbafeced4685384f2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744655"
---
# <a name="data-agnostic-testing-using-the-regression-suite-automation-tool"></a><span data-ttu-id="b0069-103">使用 Regression Suite Automation Tool 的数据不可知测试</span><span class="sxs-lookup"><span data-stu-id="b0069-103">Data agnostic testing using the Regression Suite Automation Tool</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0069-104">由于 ERP 应用程序的功能验证不能是完整的数据不可知，测试有多个阶段和方法。</span><span class="sxs-lookup"><span data-stu-id="b0069-104">While the functional validation of an ERP application can’t be fully data agnostic, there are multiple phases and approaches for testing.</span></span> <span data-ttu-id="b0069-105">这些测试阶段包括：</span><span class="sxs-lookup"><span data-stu-id="b0069-105">These testing phases include:</span></span>  

- <span data-ttu-id="b0069-106">SysTest 框架</span><span class="sxs-lookup"><span data-stu-id="b0069-106">SysTest framework</span></span>
- <span data-ttu-id="b0069-107">ATL 框架</span><span class="sxs-lookup"><span data-stu-id="b0069-107">ATL frameowrk</span></span>
- <span data-ttu-id="b0069-108">Regression Suite Automation Tool (RSAT)</span><span class="sxs-lookup"><span data-stu-id="b0069-108">Regression Suite Automation Tool (RSAT)</span></span>

<span data-ttu-id="b0069-109">[![测试分类金字塔](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span><span class="sxs-lookup"><span data-stu-id="b0069-109">[![Test classification pyramid](./media/rsat-data-agnostic-testing-01.PNG)](./media/rsat-data-agnostic-testing-01.PNG)</span></span>

## <a name="overview"></a><span data-ttu-id="b0069-110">概览</span><span class="sxs-lookup"><span data-stu-id="b0069-110">Overview</span></span>
-   <span data-ttu-id="b0069-111">**SysTest 框架** – SysTest 框架可以可靠地用于编写单元测试。</span><span class="sxs-lookup"><span data-stu-id="b0069-111">**SysTest framework** – The SysTest framework is reliable for writing unit tests.</span></span> <span data-ttu-id="b0069-112">因为单元测试通常测试方法或功能，所以始终应该数据不可知，并且仅依赖在测试中提供的输入数据。</span><span class="sxs-lookup"><span data-stu-id="b0069-112">Because unit tests are generally testing a method or function, they should always be data agnostic and dependent only on the input data that is provided as part of the test.</span></span>
-   <span data-ttu-id="b0069-113">**ATL 框架** – Microsoft 有一个 ATL 框架，该框架是 SysTest 框架的精华，可以更简单、更可靠地编写功能测试。</span><span class="sxs-lookup"><span data-stu-id="b0069-113">**ATL framework** – Microsoft has an ATL framework that is an abstraction on the SysTest framework and makes functional test writing much more simple and reliable.</span></span> <span data-ttu-id="b0069-114">应该使用此框架编写组件测试或简单集成测试。</span><span class="sxs-lookup"><span data-stu-id="b0069-114">This framework should be used for writing component tests or simple integration tests.</span></span>
-   <span data-ttu-id="b0069-115">**RSAT** – RSAT 用于集成测试和业务周期测试。</span><span class="sxs-lookup"><span data-stu-id="b0069-115">**RSAT** – The RSAT is used for integration tests and business cycle tests.</span></span> <span data-ttu-id="b0069-116">业务周期测试也称为重复验证测试，依赖于现有数据。</span><span class="sxs-lookup"><span data-stu-id="b0069-116">The business cycle tests, also called the regression validation tests, are dependent on existing data.</span></span> <span data-ttu-id="b0069-117">但是，如果考虑更多因素，这些测试可能变得数据不可知。</span><span class="sxs-lookup"><span data-stu-id="b0069-117">However, these tests can become data agnostic if you consider additional factors.</span></span> 

    - <span data-ttu-id="b0069-118">o 在单元测试和组件测试为低级别且可能完全不可知（不依赖于现有数据集）的情况下，业务周期或回归验证测试依赖于某些现有数据。</span><span class="sxs-lookup"><span data-stu-id="b0069-118">o Where unit tests and component tests are low level and can fully be data agnostic (not dependent on existing dataset), the business cycle or regression validation tests are dependent on some existing data.</span></span> <span data-ttu-id="b0069-119">此数据中包括设置、配置设置（参数）和主数据（客户、供应商、物料等），但是不能包含交易记录数据。</span><span class="sxs-lookup"><span data-stu-id="b0069-119">This data includes setup, configuration settings (parameters), and master data (customer, vendors, items, etc.), but never transaction data.</span></span> <span data-ttu-id="b0069-120">确保在最终测试中还原测试期间更改了的其中任何数据。</span><span class="sxs-lookup"><span data-stu-id="b0069-120">Make sure that during the test, if any of these are being changed, that they are reverted back as part of the final test.</span></span>
    - <span data-ttu-id="b0069-121">根据特定条件选择主数据，而不是选择特定记录。</span><span class="sxs-lookup"><span data-stu-id="b0069-121">Select master data based on certain criteria instead of selecting a particular record.</span></span> <span data-ttu-id="b0069-122">例如，如果要根据物料的维度值和存货可用性选择物料，请使用这些值筛选产品列表，选择第一个物料，然后复制要用于将来测试的编号。</span><span class="sxs-lookup"><span data-stu-id="b0069-122">For example, if you want to select an item based on its dimension values and stock availability, filter the product list with those values, select the first item, and copy the number to be used for future tests.</span></span> <span data-ttu-id="b0069-123">如果是客户、供应商或物料之类简单主数据行，则可在自动化期间创建，并通过链接在将来的测试中使用。</span><span class="sxs-lookup"><span data-stu-id="b0069-123">If it’s a simple master data line such as customer, vendor, or item, it can be created as part of the automation and used in future tests through chaining.</span></span> 
    - <span data-ttu-id="b0069-124">o 通过编号规则或通过使用 Microsoft Excel 函数（如 =TEXT(NOW(),"yyyymmddhhmm")）输入唯一标识符，如发票编号。</span><span class="sxs-lookup"><span data-stu-id="b0069-124">o Enter the unique identifiers, such as invoice numbers, through the number sequence or by using Microsoft Excel functions such as =TEXT(NOW(),"yyyymmddhhmm").</span></span> <span data-ttu-id="b0069-125">此函数每分钟提供一个唯一编号，这样您就可以跟踪执行的操作。</span><span class="sxs-lookup"><span data-stu-id="b0069-125">This function will provide a unique number every minute, which allows you to track when the action happened.</span></span> <span data-ttu-id="b0069-126">可将其用于变量，如产品收据编号和供应商发票编号。</span><span class="sxs-lookup"><span data-stu-id="b0069-126">This can be used for variables such as product receipt numbers and vendor invoice numbers.</span></span> <span data-ttu-id="b0069-127">这些测试将重复使用同一个数据库，无需进行任何还原。</span><span class="sxs-lookup"><span data-stu-id="b0069-127">These tests continue to work on the same database again and again, without requiring any restoration.</span></span>
    - <span data-ttu-id="b0069-128">请始终将环境的 **编辑模式** 设置为 **读取** 或 **编辑** 来充当第一个测试案例，因为默认选项为 **自动**。**自动** 选项始终使用前一个设置，可能导致不可靠的测试。</span><span class="sxs-lookup"><span data-stu-id="b0069-128">Always set the **Edit mode** of the environment to **Read** or **Edit** as the first test case because the default option is **Auto**. The **Auto** options always uses the previous setting and can cause unreliable tests.</span></span> 
 
    <span data-ttu-id="b0069-129">[![“选项”页“性能”选项卡](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span><span class="sxs-lookup"><span data-stu-id="b0069-129">[![Options page, Performance tab](./media/rsat-data-agnostic-testing-02.PNG)](./media/rsat-data-agnostic-testing-02.PNG)</span></span>
 
    - <span data-ttu-id="b0069-130">仅在筛选了特定交易记录后才验证，而不是进行常规验证。</span><span class="sxs-lookup"><span data-stu-id="b0069-130">Only validate after you filter on a particular transaction instead of generic validation.</span></span> <span data-ttu-id="b0069-131">例如，对于记录数量，筛选交易记录编号或交易记录日期，以便验证中排除其他所有交易记录。</span><span class="sxs-lookup"><span data-stu-id="b0069-131">For example, for the number of records, filter for the transaction number or the transaction date so that the validation excludes all other transactions.</span></span> 
    - <span data-ttu-id="b0069-132">如果检查客户余额或预算检查，请首先保存值，然后添加交易记录值以验证预期结果，而不是验证固定预期值。</span><span class="sxs-lookup"><span data-stu-id="b0069-132">If you are checking a customer balance or budget check, save the value first and then add your transaction value to validate the expected result instead of validating a fixed expected value.</span></span> 
 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]