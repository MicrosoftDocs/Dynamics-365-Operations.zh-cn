---
title: 使用 Regression Suite Automation Tool 教程
description: 本主题说明如何使用 Regression Suite Automation Tool (RSAT)。 其中介绍各种功能，并提供使用高级脚本的示例。
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 2d3dde69b102ce161e5c1f1dd393ffceca608bcb
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248728"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="96e36-104">Regression Suite Automation Tool 使用教程</span><span class="sxs-lookup"><span data-stu-id="96e36-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="96e36-105">可使用 Internet 浏览器工具下载此页并以 pdf 格式保存。</span><span class="sxs-lookup"><span data-stu-id="96e36-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="96e36-106">本教程演练 Regression Suite Automation Tool (RSAT) 的部分高级功能，包括演示分配，还介绍策略和关键学习点。</span><span class="sxs-lookup"><span data-stu-id="96e36-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="96e36-107">值得注意的 RSAT 和任务录制器功能</span><span class="sxs-lookup"><span data-stu-id="96e36-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="96e36-108">验证字段值</span><span class="sxs-lookup"><span data-stu-id="96e36-108">Validate a field value</span></span>

<span data-ttu-id="96e36-109">RSAT 允许您在测试用例中包含验证步骤，以验证期望值。</span><span class="sxs-lookup"><span data-stu-id="96e36-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="96e36-110">有关此功能的信息，请参阅文章[验证期望值](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md)。</span><span class="sxs-lookup"><span data-stu-id="96e36-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="96e36-111">以下示例演示如何使用此功能来验证现有库存量是否超过 0（零）。</span><span class="sxs-lookup"><span data-stu-id="96e36-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="96e36-112">在 **USMF** 公司的演示数据中，创建一个包含以下步骤的任务录制：</span><span class="sxs-lookup"><span data-stu-id="96e36-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="96e36-113">转到**产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="96e36-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="96e36-114">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="96e36-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="96e36-115">例如，对**物料编号**字段使用值 **1000** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="96e36-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="96e36-116">选择**现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="96e36-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="96e36-117">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="96e36-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="96e36-118">例如，对**站点**字段使用值 **1** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="96e36-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="96e36-119">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="96e36-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="96e36-120">验证**可用合计**字段的值是否为 **411.0000000000000000**。</span><span class="sxs-lookup"><span data-stu-id="96e36-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="96e36-121">保存任务录制，并在 Azure Devops 中将其附加到测试用例中。</span><span class="sxs-lookup"><span data-stu-id="96e36-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="96e36-122">将测试用例添加到测试计划，然后将测试用例加载到 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="96e36-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="96e36-123">打开 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-123">Open the Excel parameter file.</span></span> <span data-ttu-id="96e36-124">在 **InventOnhandItem** 选项卡上，将看到 **Validate InventOnhandItem** 部分，其中包含一个**运算符**字段。</span><span class="sxs-lookup"><span data-stu-id="96e36-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![“运算符”字段](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="96e36-126">若要验证现有库存量是否始终大于 0，请将**值**字段的值从 **411** 更改为 **0**，将**运算符**字段的值从等号 (**=**) 更改为大于符号 (**\>**)。</span><span class="sxs-lookup"><span data-stu-id="96e36-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![“值”和“运算符”字段的值已更改](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="96e36-128">保存并关闭 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="96e36-129">选择**上载**将对 Excel 参数文件执行的更改保存到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="96e36-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="96e36-130">现在，如果库存中指定物料的**可用合计**字段的值大于 0（零），无论实际现有库存量值是多少，测试都将失败。</span><span class="sxs-lookup"><span data-stu-id="96e36-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="96e36-131">保存的变量和链接测试用例</span><span class="sxs-lookup"><span data-stu-id="96e36-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="96e36-132">RSAT 的一项关键功能是链接测试用例，即一个测试将变量传递给其他测试这项功能。</span><span class="sxs-lookup"><span data-stu-id="96e36-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="96e36-133">有关详细信息，请参阅文章[复制变量以链接测试用例](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md)。</span><span class="sxs-lookup"><span data-stu-id="96e36-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="96e36-134">派生测试用例</span><span class="sxs-lookup"><span data-stu-id="96e36-134">Derived test case</span></span>

<span data-ttu-id="96e36-135">RSAT 让您可以对多个测试用例使用同一个任务录制，从而可以使用不同数据配置运行一个任务。</span><span class="sxs-lookup"><span data-stu-id="96e36-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="96e36-136">有关详细信息，请参阅文章[派生测试用例](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md)。</span><span class="sxs-lookup"><span data-stu-id="96e36-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="96e36-137">验证通知和消息</span><span class="sxs-lookup"><span data-stu-id="96e36-137">Validate notifications and messages</span></span>

<span data-ttu-id="96e36-138">可使用此功能验证是否执行了某个操作。</span><span class="sxs-lookup"><span data-stu-id="96e36-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="96e36-139">例如，创建、估计，然后开始履行生产订单时，应用程序将显示“生产 - 开始”消息，通知您已开始履行生产订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![“生产 – 开始”通知](./media/use_rsa_tool_05.png)

<span data-ttu-id="96e36-141">可通过 RSAT 验证此消息，方法是在相应录制的 Excel 参数文件的 **MessageValidation** 选项卡上输入消息文本。</span><span class="sxs-lookup"><span data-stu-id="96e36-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![“消息验证”选项卡](./media/use_rsa_tool_06.png)

<span data-ttu-id="96e36-143">运行测试用例之后，将把 Excel 参数文件中的消息与显示的消息进行比较。</span><span class="sxs-lookup"><span data-stu-id="96e36-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="96e36-144">如果这些消息不匹配，测试用例将失败。</span><span class="sxs-lookup"><span data-stu-id="96e36-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="96e36-145">可在 Excel 参数文件中的 **MessageValidation** 选项卡上输入多条消息。</span><span class="sxs-lookup"><span data-stu-id="96e36-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="96e36-146">这些消息也可以是错误消息或警告消息，而不是参考消息。</span><span class="sxs-lookup"><span data-stu-id="96e36-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="96e36-147">快照</span><span class="sxs-lookup"><span data-stu-id="96e36-147">Snapshot</span></span>

<span data-ttu-id="96e36-148">此功能用于拍摄任务录制期间执行的步骤的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="96e36-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="96e36-149">非常适合审核或调试用途。</span><span class="sxs-lookup"><span data-stu-id="96e36-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="96e36-150">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="96e36-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="96e36-151">运行测试用例时，RSAT 将在工作目录中测试用例的播放文件夹内生成步骤的快照（映像）。</span><span class="sxs-lookup"><span data-stu-id="96e36-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="96e36-152">如果使用的 RSAT 版本较低，将把这些映像保存到 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** 中，这是为运行的每个测试用例创建的单独文件夹。</span><span class="sxs-lookup"><span data-stu-id="96e36-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="96e36-153">赋值</span><span class="sxs-lookup"><span data-stu-id="96e36-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="96e36-154">应用场景</span><span class="sxs-lookup"><span data-stu-id="96e36-154">Scenario</span></span>

1. <span data-ttu-id="96e36-155">产品设计人员创建一个新发布的产品。</span><span class="sxs-lookup"><span data-stu-id="96e36-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="96e36-156">生产经理发起一个生产订单以将库存水平提升到两件。</span><span class="sxs-lookup"><span data-stu-id="96e36-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="96e36-157">制造将开始履行和终止生产订单，并验证现有数量是否为两件。</span><span class="sxs-lookup"><span data-stu-id="96e36-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="96e36-158">销售团队收到一个包含四件新产品的订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="96e36-159">因此，销售团队通过动态计划更新净需求。</span><span class="sxs-lookup"><span data-stu-id="96e36-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="96e36-160">因为没有更多产能，所以默认订单策略设置为“以买代造”。</span><span class="sxs-lookup"><span data-stu-id="96e36-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="96e36-161">因此，将创建一个计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="96e36-162">买方将添加一个供应商，确认计划采购订单，然后确认该采购订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="96e36-163">采购的货物到店时，商店操作员将搜索相关采购订单并收货。</span><span class="sxs-lookup"><span data-stu-id="96e36-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="96e36-164">因为订单现在已完成，所以可以针对销售订单拣货和为货物打包。</span><span class="sxs-lookup"><span data-stu-id="96e36-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="96e36-165">财务将过帐采购发票和销售发票。</span><span class="sxs-lookup"><span data-stu-id="96e36-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="96e36-166">下图显示此场景的流程。</span><span class="sxs-lookup"><span data-stu-id="96e36-166">The following illustration shows the flow for this scenario.</span></span>

![演示场景的流程](./media/use_rsa_tool_14.png)

<span data-ttu-id="96e36-168">下图显示该方案在业务流程建模器中的业务流程层次结构。</span><span class="sxs-lookup"><span data-stu-id="96e36-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![演示场景的业务流程](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="96e36-170">策略 – 关键学习点</span><span class="sxs-lookup"><span data-stu-id="96e36-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="96e36-171">数据</span><span class="sxs-lookup"><span data-stu-id="96e36-171">Data</span></span>

- <span data-ttu-id="96e36-172">确保您有代表数据卷（生产/黄金配置数据加迁移数据的副本）。</span><span class="sxs-lookup"><span data-stu-id="96e36-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="96e36-173">通过任务录制器生成新数据时，请创建与现有名称不冲突的测试名称（例如，使用 **RSATxxx** 之类前缀）。</span><span class="sxs-lookup"><span data-stu-id="96e36-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="96e36-174">使用 Azure 时间点还原在非一级环境中重新运行测试。</span><span class="sxs-lookup"><span data-stu-id="96e36-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="96e36-175">如果使用 Excel 函数 **RANDOM** 和 **NOW** 生成唯一组合，则工作量非常大。</span><span class="sxs-lookup"><span data-stu-id="96e36-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="96e36-176">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="96e36-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="96e36-177">任务录制器</span><span class="sxs-lookup"><span data-stu-id="96e36-177">Task recorder</span></span>

- <span data-ttu-id="96e36-178">开始录制前定义场景。</span><span class="sxs-lookup"><span data-stu-id="96e36-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="96e36-179">一个管理有方的项目已预定义了测试场景。</span><span class="sxs-lookup"><span data-stu-id="96e36-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="96e36-180">若要生成测试案例，请注意这些测试场景的结果可预测程度。</span><span class="sxs-lookup"><span data-stu-id="96e36-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="96e36-181">如果录制由不同角色执行，或者如果执行下一步之前需要等待或存在外部事件，请拆分录制。</span><span class="sxs-lookup"><span data-stu-id="96e36-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="96e36-182">请避免选择列表中的值。</span><span class="sxs-lookup"><span data-stu-id="96e36-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="96e36-183">而是改用文本格式，如 **FIFO**、**AudioRM** 和 **SiteWH**。</span><span class="sxs-lookup"><span data-stu-id="96e36-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="96e36-184">如果在列表中进行选择，则会录制值在列表中的位置，而不是录制值本身。</span><span class="sxs-lookup"><span data-stu-id="96e36-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="96e36-185">如果向该列表添加物料，值的位置可能会改变。</span><span class="sxs-lookup"><span data-stu-id="96e36-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="96e36-186">因此，录制将使用其他参数，并且可能会影响场景的其余部分。</span><span class="sxs-lookup"><span data-stu-id="96e36-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="96e36-187">请注意多用户行为。</span><span class="sxs-lookup"><span data-stu-id="96e36-187">Think about multi-user behavior.</span></span> <span data-ttu-id="96e36-188">例如，不要想当然地以为始终会自动选中新建的销售订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="96e36-189">请始终改用筛选器查找正确订单。</span><span class="sxs-lookup"><span data-stu-id="96e36-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="96e36-190">任务录制器中的复制功能用于保存新建产品的名称，以便在链式测试用例中使用。</span><span class="sxs-lookup"><span data-stu-id="96e36-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="96e36-191">任务录制器中的验证功能用于设置检查点来验证是否已正确运行了步骤。</span><span class="sxs-lookup"><span data-stu-id="96e36-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="96e36-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="96e36-192">RSAT</span></span>

- <span data-ttu-id="96e36-193">若要在另一个公司中运行测试，可以在 Excel 参数文件的**常规**选项卡上更改公司。</span><span class="sxs-lookup"><span data-stu-id="96e36-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="96e36-194">确保新选择的公司中有设置和数据。</span><span class="sxs-lookup"><span data-stu-id="96e36-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="96e36-195">可在 Excel 参数文件的**常规**选项卡上更改测试用户。</span><span class="sxs-lookup"><span data-stu-id="96e36-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="96e36-196">指定将运行测试用例的用户的电子邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="96e36-197">这样，就可以通过使用所指定用户的安全权限运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="96e36-198">若要在开始测试之前等待，可在 Excel 参数文件的**常规**选项卡上定义暂停。</span><span class="sxs-lookup"><span data-stu-id="96e36-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="96e36-199">可在批处理作业中使用此暂停（例如，如果必须向运行工作流，才能执行下一个步骤。）</span><span class="sxs-lookup"><span data-stu-id="96e36-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="96e36-200">高级脚本</span><span class="sxs-lookup"><span data-stu-id="96e36-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="96e36-201">CLI</span><span class="sxs-lookup"><span data-stu-id="96e36-201">CLI</span></span>

<span data-ttu-id="96e36-202">可以从**命令提示符** 或 **PowerShell** 窗口调用 RSAT。</span><span class="sxs-lookup"><span data-stu-id="96e36-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="96e36-203">请验证环境变量 **TestRoot** 是否设置为 RSAT 安装路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="96e36-204">（在 Microsoft Windows 中，打开**控制面板**，选择**系统和安全 \> 系统 \> 高级安全设置**，然后选择**环境变量**。）</span><span class="sxs-lookup"><span data-stu-id="96e36-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="96e36-205">以管理员身份打开**命令提示符**或 **PowerShell** 窗口。</span><span class="sxs-lookup"><span data-stu-id="96e36-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="96e36-206">浏览至 RSAT 安装目录。</span><span class="sxs-lookup"><span data-stu-id="96e36-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="96e36-207">列出所有命令。</span><span class="sxs-lookup"><span data-stu-id="96e36-207">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="96e36-208">?</span><span class="sxs-lookup"><span data-stu-id="96e36-208">?</span></span> 
<span data-ttu-id="96e36-209">显示有关所有可用命令及其参数的帮助。</span><span class="sxs-lookup"><span data-stu-id="96e36-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="96e36-210">可选参数</span><span class="sxs-lookup"><span data-stu-id="96e36-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="96e36-211">其中，``[command]`` 是下面指定的命令之一。</span><span class="sxs-lookup"><span data-stu-id="96e36-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="96e36-212">about</span><span class="sxs-lookup"><span data-stu-id="96e36-212">about</span></span>
<span data-ttu-id="96e36-213">显示当前版本。</span><span class="sxs-lookup"><span data-stu-id="96e36-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="96e36-214">cls</span><span class="sxs-lookup"><span data-stu-id="96e36-214">cls</span></span>
<span data-ttu-id="96e36-215">清除屏幕内容。</span><span class="sxs-lookup"><span data-stu-id="96e36-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="96e36-216">download</span><span class="sxs-lookup"><span data-stu-id="96e36-216">download</span></span>
<span data-ttu-id="96e36-217">将指定测试用例的附件下载到输出目录中。</span><span class="sxs-lookup"><span data-stu-id="96e36-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="96e36-218">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="96e36-219">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-220">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-220">Required parameters</span></span>
<span data-ttu-id="96e36-221">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="96e36-222">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="96e36-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="96e36-223">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-224">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="96e36-225">编辑</span><span class="sxs-lookup"><span data-stu-id="96e36-225">edit</span></span>
<span data-ttu-id="96e36-226">允许您在 Excel 程序中打开和编辑参数文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-227">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-227">Required parameters</span></span>
<span data-ttu-id="96e36-228">**``excel_file``** 必须包含现有 Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-229">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="96e36-230">generate</span><span class="sxs-lookup"><span data-stu-id="96e36-230">generate</span></span>
<span data-ttu-id="96e36-231">在输出目录中为指定的测试用例生成测试执行和参数文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="96e36-232">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="96e36-233">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-234">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-234">Required parameters</span></span>
<span data-ttu-id="96e36-235">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="96e36-236">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="96e36-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="96e36-237">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-238">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="96e36-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="96e36-239">generatederived</span></span>
<span data-ttu-id="96e36-240">生成派生自所提供测试用例的新测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="96e36-241">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="96e36-242">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-243">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-243">Required parameters</span></span>
<span data-ttu-id="96e36-244">**``parent_test_case_id``** 表示父测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="96e36-245">**``test_plan_id``** 表示测试计划 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="96e36-246">**``test_suite_id``** 表示测试套件 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-247">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="96e36-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="96e36-248">generatetestonly</span></span>
<span data-ttu-id="96e36-249">在输出目录中为指定的测试用例仅生成测试执行文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="96e36-250">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="96e36-251">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-252">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-252">Required parameters</span></span>
<span data-ttu-id="96e36-253">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="96e36-254">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="96e36-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="96e36-255">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-256">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="96e36-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="96e36-257">generatetestsuite</span></span>
<span data-ttu-id="96e36-258">在输出目录中为指定的套件生成所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="96e36-259">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="96e36-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="96e36-260">将列中的任何值用作 **test_suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-261">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-261">Required parameters</span></span>
<span data-ttu-id="96e36-262">**``test_suite_name``** 表示测试套件名称。</span><span class="sxs-lookup"><span data-stu-id="96e36-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="96e36-263">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="96e36-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="96e36-264">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-265">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="96e36-266">help</span><span class="sxs-lookup"><span data-stu-id="96e36-266">help</span></span>
<span data-ttu-id="96e36-267">与 [?](#section) 相同</span><span class="sxs-lookup"><span data-stu-id="96e36-267">Identical to the [?](#section)</span></span> <span data-ttu-id="96e36-268">命令</span><span class="sxs-lookup"><span data-stu-id="96e36-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="96e36-269">列表</span><span class="sxs-lookup"><span data-stu-id="96e36-269">list</span></span>
<span data-ttu-id="96e36-270">列出所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="96e36-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="96e36-271">listtestplans</span></span>
<span data-ttu-id="96e36-272">列出所有可用的测试计划。</span><span class="sxs-lookup"><span data-stu-id="96e36-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="96e36-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="96e36-273">listtestsuite</span></span>
<span data-ttu-id="96e36-274">列出指定测试套件的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="96e36-275">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="96e36-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="96e36-276">将第一列中的任何值用作 **suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-277">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-277">Required parameters</span></span>
<span data-ttu-id="96e36-278">**``suite_name``** 所需套件的名称。</span><span class="sxs-lookup"><span data-stu-id="96e36-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-279">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="96e36-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="96e36-280">listtestsuitenames</span></span>
<span data-ttu-id="96e36-281">列出所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="96e36-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="96e36-282">playback</span><span class="sxs-lookup"><span data-stu-id="96e36-282">playback</span></span>
<span data-ttu-id="96e36-283">使用 Excel 文件播放测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-284">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-284">Required parameters</span></span>
<span data-ttu-id="96e36-285">**``excel_file``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="96e36-286">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="96e36-287">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="96e36-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="96e36-288">playbackbyid</span></span>
<span data-ttu-id="96e36-289">一次播放多个测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="96e36-290">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="96e36-291">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-292">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-292">Required parameters</span></span>
<span data-ttu-id="96e36-293">**``test_case_id1``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="96e36-294">**``test_case_id2``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="96e36-295">**``test_case_idN``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="96e36-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="96e36-296">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="96e36-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="96e36-297">playbackmany</span></span>
<span data-ttu-id="96e36-298">使用 Excel 文件一次播放大量测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-299">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-299">Required parameters</span></span>
<span data-ttu-id="96e36-300">**``excel_file1``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="96e36-301">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-301">File must exist.</span></span>  
<span data-ttu-id="96e36-302">**``excel_file2``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="96e36-303">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-303">File must exist.</span></span>  
<span data-ttu-id="96e36-304">**``excel_fileN``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="96e36-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="96e36-305">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="96e36-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="96e36-306">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="96e36-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="96e36-307">playbacksuite</span></span>
<span data-ttu-id="96e36-308">播放指定测试套件中的所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="96e36-309">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="96e36-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="96e36-310">将第一列中的任何值用作 **suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-311">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-311">Required parameters</span></span>
<span data-ttu-id="96e36-312">**``suite_name``** 所需套件的名称。</span><span class="sxs-lookup"><span data-stu-id="96e36-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-313">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="96e36-314">quit</span><span class="sxs-lookup"><span data-stu-id="96e36-314">quit</span></span>
<span data-ttu-id="96e36-315">关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="96e36-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="96e36-316">upload</span><span class="sxs-lookup"><span data-stu-id="96e36-316">upload</span></span>
<span data-ttu-id="96e36-317">上载属于指定测试套件或测试用例的所有文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="96e36-318">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-318">Required parameters</span></span>
<span data-ttu-id="96e36-319">**``suite_name``** 将上载属于指定测试套件的所有文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="96e36-320">**``testcase_id``** 将上载属于指定测试用例的所有文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-321">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="96e36-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="96e36-322">uploadrecording</span></span>
<span data-ttu-id="96e36-323">仅上载属于指定测试用例的录制文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="96e36-324">必要参数</span><span class="sxs-lookup"><span data-stu-id="96e36-324">Required parameters</span></span>
<span data-ttu-id="96e36-325">**``testcase_id``** 将仅上载属于指定测试用例的录制文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="96e36-326">示例</span><span class="sxs-lookup"><span data-stu-id="96e36-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="96e36-327">usage</span><span class="sxs-lookup"><span data-stu-id="96e36-327">usage</span></span>
<span data-ttu-id="96e36-328">显示两种调用此应用程序的方法：一种使用默认设置文件，另一种提供设置文件。</span><span class="sxs-lookup"><span data-stu-id="96e36-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="96e36-329">Windows PowerShell 示例</span><span class="sxs-lookup"><span data-stu-id="96e36-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="96e36-330">下面的示例脚本出于演示目的按原样提供，不受 Microsoft 支持。</span><span class="sxs-lookup"><span data-stu-id="96e36-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="96e36-331">循环运行测试用例</span><span class="sxs-lookup"><span data-stu-id="96e36-331">Run a test case in a loop</span></span>

<span data-ttu-id="96e36-332">您有一个测试脚本用于创建新客户。</span><span class="sxs-lookup"><span data-stu-id="96e36-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="96e36-333">通过脚本，可以在运行每个迭代之前随机化以下数据来运行此测试用例。</span><span class="sxs-lookup"><span data-stu-id="96e36-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="96e36-334">客户 ID</span><span class="sxs-lookup"><span data-stu-id="96e36-334">Customer ID</span></span>
- <span data-ttu-id="96e36-335">客户名称</span><span class="sxs-lookup"><span data-stu-id="96e36-335">Customer name</span></span>
- <span data-ttu-id="96e36-336">客户地址</span><span class="sxs-lookup"><span data-stu-id="96e36-336">Customer address</span></span>

<span data-ttu-id="96e36-337">客户 ID 的格式为 *ATCUS\<number\>*，其中， \<number\> 是一个 **000000001** 与 **999999999** 之间的值。</span><span class="sxs-lookup"><span data-stu-id="96e36-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="96e36-338">以下示例使用一个参数 **start** 定义使用的第一个数字。</span><span class="sxs-lookup"><span data-stu-id="96e36-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="96e36-339">使用第二个参数 **nr** 定义必须创建的客户数量。</span><span class="sxs-lookup"><span data-stu-id="96e36-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="96e36-340">对于每个迭代，可使用 UpdateCustomer 函数更改 Excel 参数文件中的参数。</span><span class="sxs-lookup"><span data-stu-id="96e36-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="96e36-341">然后，在 RunTestCase 函数中调用 RSAT 命令行。</span><span class="sxs-lookup"><span data-stu-id="96e36-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="96e36-342">在管理模式下打开 Microsoft Windows PowerShell 集成脚本环境 (ISE)，然后将以下代码粘贴到名称为 **Untitled1.ps1** 的窗口中。</span><span class="sxs-lookup"><span data-stu-id="96e36-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="96e36-343">在 Microsoft Dynamics 365 中运行依赖数据的脚本</span><span class="sxs-lookup"><span data-stu-id="96e36-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="96e36-344">以下示例使用开放数据协议 (OData) 调用查找采购订单的订单状态。</span><span class="sxs-lookup"><span data-stu-id="96e36-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="96e36-345">例如，如果状态不是**已开票**，则可调用 RSAT 测试用例以过帐发票。</span><span class="sxs-lookup"><span data-stu-id="96e36-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
