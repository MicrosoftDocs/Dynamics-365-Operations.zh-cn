---
title: 使用 Regression Suite Automation Tool 教程
description: 本主题说明如何使用 Regression Suite Automation Tool (RSAT)。 其中介绍各种功能，并提供使用高级脚本的示例。
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070812"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="dddf8-104">Regression Suite Automation Tool 使用教程</span><span class="sxs-lookup"><span data-stu-id="dddf8-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="dddf8-105">可使用 Internet 浏览器工具下载此页并以 pdf 格式保存。</span><span class="sxs-lookup"><span data-stu-id="dddf8-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="dddf8-106">本教程演练 Regression Suite Automation Tool (RSAT) 的部分高级功能，包括演示分配，还介绍策略和关键学习点。</span><span class="sxs-lookup"><span data-stu-id="dddf8-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="dddf8-107">RSAT/任务录制器的功能</span><span class="sxs-lookup"><span data-stu-id="dddf8-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="dddf8-108">验证字段值</span><span class="sxs-lookup"><span data-stu-id="dddf8-108">Validate a field value</span></span>

<span data-ttu-id="dddf8-109">有关此功能的信息，请参阅[创建具有验证功能的新任务录制](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)。</span><span class="sxs-lookup"><span data-stu-id="dddf8-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="dddf8-110">已保存变量</span><span class="sxs-lookup"><span data-stu-id="dddf8-110">Saved variable</span></span>

<span data-ttu-id="dddf8-111">有关此功能的信息，请参阅[修改现有任务录制以创建已保存变量](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)。</span><span class="sxs-lookup"><span data-stu-id="dddf8-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="dddf8-112">派生测试用例</span><span class="sxs-lookup"><span data-stu-id="dddf8-112">Derived test case</span></span>

1. <span data-ttu-id="dddf8-113">打开 Regression Suite Automation Tool (RSAT)，然后选择您在[设置和安装 Regression Suite Automation Tool 教程](./hol-set-up-regression-suite-automation-tool.md)中创建的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="dddf8-114">选择**新建 \> 创建派生测试用例**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-114">Select **New \> Create derived test case**.</span></span>

    ![“新建”菜单上的“创建派生测试用例”命令](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="dddf8-116">您将收到一条消息，说明将为当前测试套件中选择的每个测试用例创建一个派生测试用例，以及每个派生测试用例将有自己的 Excel 参数文件副本。</span><span class="sxs-lookup"><span data-stu-id="dddf8-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="dddf8-117">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dddf8-118">运行派生测试用例时，其使用自己的父测试用例的任务录制和自己的 Excel 参数文件副本。</span><span class="sxs-lookup"><span data-stu-id="dddf8-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="dddf8-119">因此，可以使用不同参数运行同一个测试，不必维护多个任务录制。</span><span class="sxs-lookup"><span data-stu-id="dddf8-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="dddf8-120">派生测试用例不必与其父测试用例属于同一个测试套件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![消息框](./media/use_rsa_tool_02.png)

    <span data-ttu-id="dddf8-122">将创建两个额外的测试用例，并且为其选中**是否派生?** 复选框。</span><span class="sxs-lookup"><span data-stu-id="dddf8-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![已创建派生测试用例](./media/use_rsa_tool_03.png)

    <span data-ttu-id="dddf8-124">将在 Azure DevOps 中创建一个派生测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="dddf8-125">这是**创建新产品**测试用例的子项，并带有特殊关键字标记：**RSAT:DerivedTestSteps**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="dddf8-126">还会将这些测试用例自动添加到 Azure DevOps 中的测试计划。</span><span class="sxs-lookup"><span data-stu-id="dddf8-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT:DerivedTestSteps 关键字](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="dddf8-128">如果因为任何原因导致创建的派生测试用例的顺序不正确，请转到 Azure DevOps 并为测试套件中的测试用例重新排序，以便 RSAT 按正确顺序运行这些测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="dddf8-129">选择派生测试用例，然后选择**编辑**打开相应 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="dddf8-130">按照编辑父文件的方式编辑这些 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="dddf8-131">换句话说，确保设置产品 ID，以便自动生成。</span><span class="sxs-lookup"><span data-stu-id="dddf8-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="dddf8-132">同时确保将已保存变量复制到相关字段。</span><span class="sxs-lookup"><span data-stu-id="dddf8-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="dddf8-133">在两个 Excel 参数文件的**常规**选项卡上，将**公司**字段的值更新为 **USSI**，以便对非父测试用例法人运行派生测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="dddf8-134">若要对特定用户（或与特定用户关联的角色）运行测试用例，可以更新**测试用户**字段的值。</span><span class="sxs-lookup"><span data-stu-id="dddf8-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="dddf8-135">选择**运行**，并且验证是否同时在 USMF 法人和 USSI 法人中创建了产品。</span><span class="sxs-lookup"><span data-stu-id="dddf8-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="dddf8-136">验证通知</span><span class="sxs-lookup"><span data-stu-id="dddf8-136">Validate notifications</span></span>

<span data-ttu-id="dddf8-137">可使用此功能验证是否执行了某个操作。</span><span class="sxs-lookup"><span data-stu-id="dddf8-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="dddf8-138">例如，创建、估计，然后开始履行生产订单时，应用程序将显示“生产 - 开始”消息，通知您已开始履行生产订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![“生产 – 开始”通知](./media/use_rsa_tool_05.png)

<span data-ttu-id="dddf8-140">可通过 RSAT 验证此消息，方法是在相应录制的 Excel 参数文件的 **MessageValidation** 选项卡上输入消息文本。</span><span class="sxs-lookup"><span data-stu-id="dddf8-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![“消息验证”选项卡](./media/use_rsa_tool_06.png)

<span data-ttu-id="dddf8-142">运行测试用例之后，将把 Excel 参数文件中的消息与显示的消息进行比较。</span><span class="sxs-lookup"><span data-stu-id="dddf8-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="dddf8-143">如果这些消息不匹配，测试用例将失败。</span><span class="sxs-lookup"><span data-stu-id="dddf8-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="dddf8-144">可在 Excel 参数文件中的 **MessageValidation** 选项卡上输入多条消息。</span><span class="sxs-lookup"><span data-stu-id="dddf8-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="dddf8-145">这些消息也可以是错误消息或警告消息，而不是参考消息。</span><span class="sxs-lookup"><span data-stu-id="dddf8-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="dddf8-146">使用运算符验证值</span><span class="sxs-lookup"><span data-stu-id="dddf8-146">Validate values by using operators</span></span>

<span data-ttu-id="dddf8-147">在 RSAT 早期版本中，仅当控制值等于预期值时，才可以验证值。</span><span class="sxs-lookup"><span data-stu-id="dddf8-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="dddf8-148">新功能则允许您验证某个变量是否不等于、小于或大于指定值。</span><span class="sxs-lookup"><span data-stu-id="dddf8-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="dddf8-149">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="dddf8-150">在 Excel 参数文件中，将显示一个新的**运算符**字段。</span><span class="sxs-lookup"><span data-stu-id="dddf8-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dddf8-151">如果已经在使用 RSAT 早期版本，则必须生成新的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![“运算符”字段](./media/use_rsa_tool_07.png)

<span data-ttu-id="dddf8-153">以下示例演示如何使用此功能来验证现有库存量是否超过 0（零）。</span><span class="sxs-lookup"><span data-stu-id="dddf8-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="dddf8-154">在 **USMF** 公司的演示数据中，创建一个包含以下步骤的任务录制：</span><span class="sxs-lookup"><span data-stu-id="dddf8-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="dddf8-155">转到**产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="dddf8-156">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dddf8-157">例如，对**物料编号**字段使用值 **1000** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="dddf8-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="dddf8-158">选择**现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="dddf8-159">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dddf8-160">例如，对**站点**字段使用值 **1** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="dddf8-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="dddf8-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="dddf8-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="dddf8-162">验证**可用合计**字段的值是否为 **411.0000000000000000**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="dddf8-163">将任务录制保存到 LCS 中的 BPM 库，然后同步到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="dddf8-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="dddf8-164">将测试用例添加到测试计划，然后将测试用例加载到 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="dddf8-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="dddf8-165">打开 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-165">Open the Excel parameter file.</span></span> <span data-ttu-id="dddf8-166">在 **InventOnhandItem** 选项卡上，将看到 **Validate InventOnhandItem** 部分，其中包含一个**运算符**字段。</span><span class="sxs-lookup"><span data-stu-id="dddf8-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![“运算符”字段](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="dddf8-168">若要验证现有库存量是否始终大于 0，请将**值**字段的值从 **411** 更改为 **0**，将**运算符**字段的值从等号 (**=**) 更改为大于符号 (**\>**)。</span><span class="sxs-lookup"><span data-stu-id="dddf8-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![“值”和“运算符”字段的值已更改](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="dddf8-170">保存并关闭 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="dddf8-171">选择**上载**将对 Excel 参数文件执行的更改保存到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="dddf8-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="dddf8-172">现在，如果库存中指定物料的**可用合计**字段的值大于 0（零），无论实际现有库存量值是多少，测试都将失败。</span><span class="sxs-lookup"><span data-stu-id="dddf8-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="dddf8-173">生成器日志</span><span class="sxs-lookup"><span data-stu-id="dddf8-173">Generator logs</span></span>

<span data-ttu-id="dddf8-174">此功能将创建一个文件夹，其中包含已运行的测试用例的日志。</span><span class="sxs-lookup"><span data-stu-id="dddf8-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="dddf8-175">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="dddf8-176">运行测试用例之后，可以在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs** 下找到日志文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs 文件夹](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="dddf8-178">如果更改 .config 文件中的值之前已有测试用例，则生成新的测试执行文件之前，不会为这些测试用例生成日志。</span><span class="sxs-lookup"><span data-stu-id="dddf8-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![“新建”菜单上的“仅生成测试执行文件”命令](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="dddf8-180">快照</span><span class="sxs-lookup"><span data-stu-id="dddf8-180">Snapshot</span></span>

<span data-ttu-id="dddf8-181">此功能用于拍摄任务录制期间执行的步骤的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="dddf8-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="dddf8-182">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="dddf8-183">将在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** 下为运行的每个测试用例创建一个单独的文件夹。</span><span class="sxs-lookup"><span data-stu-id="dddf8-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![测试用例的快照文件夹](./media/use_rsa_tool_12.png)

<span data-ttu-id="dddf8-185">在这些文件夹的每一个中，都可以找到运行测试用例期间执行的步骤的快照。</span><span class="sxs-lookup"><span data-stu-id="dddf8-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![快照文件](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="dddf8-187">赋值</span><span class="sxs-lookup"><span data-stu-id="dddf8-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="dddf8-188">方案</span><span class="sxs-lookup"><span data-stu-id="dddf8-188">Scenario</span></span>

1. <span data-ttu-id="dddf8-189">产品设计人员创建一个新发布的产品。</span><span class="sxs-lookup"><span data-stu-id="dddf8-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="dddf8-190">生产经理发起一个生产订单以将库存水平提升到两件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="dddf8-191">制造将开始履行和终止生产订单，并验证现有数量是否为两件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="dddf8-192">销售团队收到一个包含四件新产品的订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="dddf8-193">因此，销售团队通过动态计划更新净需求。</span><span class="sxs-lookup"><span data-stu-id="dddf8-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="dddf8-194">因为没有更多产能，所以默认订单策略设置为“以买代造”。</span><span class="sxs-lookup"><span data-stu-id="dddf8-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="dddf8-195">因此，将创建一个计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="dddf8-196">买方将添加一个供应商，确认计划采购订单，然后确认该采购订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="dddf8-197">采购的货物到店时，商店操作员将搜索相关采购订单并收货。</span><span class="sxs-lookup"><span data-stu-id="dddf8-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="dddf8-198">因为订单现在已完成，所以可以针对销售订单拣货和为货物打包。</span><span class="sxs-lookup"><span data-stu-id="dddf8-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="dddf8-199">财务将过帐采购发票和销售发票。</span><span class="sxs-lookup"><span data-stu-id="dddf8-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="dddf8-200">下图显示此场景的流程。</span><span class="sxs-lookup"><span data-stu-id="dddf8-200">The following illustration shows the flow for this scenario.</span></span>

![演示场景的流程](./media/use_rsa_tool_14.png)

<span data-ttu-id="dddf8-202">下图显示此场景在 RSAT 中的业务流程。</span><span class="sxs-lookup"><span data-stu-id="dddf8-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![演示场景的业务流程](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="dddf8-204">策略 – 关键学习点</span><span class="sxs-lookup"><span data-stu-id="dddf8-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="dddf8-205">数据</span><span class="sxs-lookup"><span data-stu-id="dddf8-205">Data</span></span>

- <span data-ttu-id="dddf8-206">确保您有代表数据卷（生产/黄金配置数据加迁移数据的副本）。</span><span class="sxs-lookup"><span data-stu-id="dddf8-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="dddf8-207">通过任务录制器生成新数据时，请创建与现有名称不冲突的测试名称（例如，使用 **RSATxxx** 之类前缀）。</span><span class="sxs-lookup"><span data-stu-id="dddf8-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="dddf8-208">使用 Azure 时间点还原在非一级环境中重新运行测试。</span><span class="sxs-lookup"><span data-stu-id="dddf8-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="dddf8-209">如果使用 Excel 函数 **RANDOM** 和 **NOW** 生成唯一组合，则工作量非常大。</span><span class="sxs-lookup"><span data-stu-id="dddf8-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="dddf8-210">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="dddf8-211">任务录制器</span><span class="sxs-lookup"><span data-stu-id="dddf8-211">Task recorder</span></span>

- <span data-ttu-id="dddf8-212">开始录制前定义场景。</span><span class="sxs-lookup"><span data-stu-id="dddf8-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="dddf8-213">一个管理有方的项目已预定义了测试场景。</span><span class="sxs-lookup"><span data-stu-id="dddf8-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="dddf8-214">若要生成测试案例，请注意这些测试场景的结果可预测程度。</span><span class="sxs-lookup"><span data-stu-id="dddf8-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="dddf8-215">如果录制由不同角色执行，或者如果执行下一步之前需要等待或存在外部事件，请拆分录制。</span><span class="sxs-lookup"><span data-stu-id="dddf8-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="dddf8-216">请避免选择列表中的值。</span><span class="sxs-lookup"><span data-stu-id="dddf8-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="dddf8-217">而是改用文本格式，如 **FIFO**、**AudioRM** 和 **SiteWH**。</span><span class="sxs-lookup"><span data-stu-id="dddf8-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="dddf8-218">如果在列表中进行选择，则会录制值在列表中的位置，而不是录制值本身。</span><span class="sxs-lookup"><span data-stu-id="dddf8-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="dddf8-219">如果向该列表添加物料，值的位置可能会改变。</span><span class="sxs-lookup"><span data-stu-id="dddf8-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="dddf8-220">因此，录制将使用其他参数，并且可能会影响场景的其余部分。</span><span class="sxs-lookup"><span data-stu-id="dddf8-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="dddf8-221">请注意多用户行为。</span><span class="sxs-lookup"><span data-stu-id="dddf8-221">Think about multi-user behavior.</span></span> <span data-ttu-id="dddf8-222">例如，不要想当然地以为始终会自动选中新建的销售订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="dddf8-223">请始终改用筛选器查找正确订单。</span><span class="sxs-lookup"><span data-stu-id="dddf8-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="dddf8-224">任务录制器中的复制功能用于保存新建产品的名称，以便在链式测试用例中使用。</span><span class="sxs-lookup"><span data-stu-id="dddf8-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="dddf8-225">任务录制器中的验证功能用于设置检查点来验证是否已正确运行了步骤。</span><span class="sxs-lookup"><span data-stu-id="dddf8-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="dddf8-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="dddf8-226">RSAT</span></span>

- <span data-ttu-id="dddf8-227">若要在另一个公司中运行测试，可以在 Excel 参数文件的**常规**选项卡上更改公司。</span><span class="sxs-lookup"><span data-stu-id="dddf8-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="dddf8-228">确保新选择的公司中有设置和数据。</span><span class="sxs-lookup"><span data-stu-id="dddf8-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="dddf8-229">可在 Excel 参数文件的**常规**选项卡上更改测试用户。</span><span class="sxs-lookup"><span data-stu-id="dddf8-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="dddf8-230">指定将运行测试用例的用户的电子邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="dddf8-231">这样，就可以通过使用所指定用户的安全权限运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="dddf8-232">若要在开始测试之前等待，可在 Excel 参数文件的**常规**选项卡上定义暂停。</span><span class="sxs-lookup"><span data-stu-id="dddf8-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="dddf8-233">可在批处理作业中使用此暂停（例如，如果必须向运行工作流，才能执行下一个步骤。）</span><span class="sxs-lookup"><span data-stu-id="dddf8-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="dddf8-234">高级脚本</span><span class="sxs-lookup"><span data-stu-id="dddf8-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="dddf8-235">CLI</span><span class="sxs-lookup"><span data-stu-id="dddf8-235">CLI</span></span>

<span data-ttu-id="dddf8-236">可以从**命令提示符** 或 **PowerShell** 窗口调用 RSAT。</span><span class="sxs-lookup"><span data-stu-id="dddf8-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="dddf8-237">请验证环境变量 **TestRoot** 是否设置为 RSAT 安装路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="dddf8-238">（在 Microsoft Windows 中，打开**控制面板**，选择**系统和安全 \> 系统 \> 高级安全设置**，然后选择**环境变量**。）</span><span class="sxs-lookup"><span data-stu-id="dddf8-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="dddf8-239">以管理员身份打开**命令提示符**或 **PowerShell** 窗口。</span><span class="sxs-lookup"><span data-stu-id="dddf8-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="dddf8-240">浏览至 RSAT 安装目录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="dddf8-241">列出所有命令。</span><span class="sxs-lookup"><span data-stu-id="dddf8-241">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="dddf8-242">?</span><span class="sxs-lookup"><span data-stu-id="dddf8-242">?</span></span> 
<span data-ttu-id="dddf8-243">显示有关所有可用命令及其参数的帮助。</span><span class="sxs-lookup"><span data-stu-id="dddf8-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="dddf8-244">可选参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="dddf8-245">其中，``[command]`` 是下面指定的命令之一。</span><span class="sxs-lookup"><span data-stu-id="dddf8-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="dddf8-246">about</span><span class="sxs-lookup"><span data-stu-id="dddf8-246">about</span></span>
<span data-ttu-id="dddf8-247">显示当前版本。</span><span class="sxs-lookup"><span data-stu-id="dddf8-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="dddf8-248">cls</span><span class="sxs-lookup"><span data-stu-id="dddf8-248">cls</span></span>
<span data-ttu-id="dddf8-249">清除屏幕内容。</span><span class="sxs-lookup"><span data-stu-id="dddf8-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="dddf8-250">download</span><span class="sxs-lookup"><span data-stu-id="dddf8-250">download</span></span>
<span data-ttu-id="dddf8-251">将指定测试用例的附件下载到输出目录中。</span><span class="sxs-lookup"><span data-stu-id="dddf8-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="dddf8-252">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="dddf8-253">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-254">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-254">Required parameters</span></span>
<span data-ttu-id="dddf8-255">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="dddf8-256">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="dddf8-257">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-258">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="dddf8-259">编辑</span><span class="sxs-lookup"><span data-stu-id="dddf8-259">edit</span></span>
<span data-ttu-id="dddf8-260">允许您在 Excel 程序中打开和编辑参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-261">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-261">Required parameters</span></span>
<span data-ttu-id="dddf8-262">**``excel_file``** 必须包含现有 Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-263">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="dddf8-264">generate</span><span class="sxs-lookup"><span data-stu-id="dddf8-264">generate</span></span>
<span data-ttu-id="dddf8-265">在输出目录中为指定的测试用例生成测试执行和参数文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="dddf8-266">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="dddf8-267">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-268">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-268">Required parameters</span></span>
<span data-ttu-id="dddf8-269">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="dddf8-270">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="dddf8-271">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-272">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="dddf8-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="dddf8-273">generatederived</span></span>
<span data-ttu-id="dddf8-274">生成派生自所提供测试用例的新测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="dddf8-275">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="dddf8-276">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-277">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-277">Required parameters</span></span>
<span data-ttu-id="dddf8-278">**``parent_test_case_id``** 表示父测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="dddf8-279">**``test_plan_id``** 表示测试计划 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="dddf8-280">**``test_suite_id``** 表示测试套件 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-281">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="dddf8-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="dddf8-282">generatetestonly</span></span>
<span data-ttu-id="dddf8-283">在输出目录中为指定的测试用例仅生成测试执行文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="dddf8-284">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="dddf8-285">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-286">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-286">Required parameters</span></span>
<span data-ttu-id="dddf8-287">**``test_case_id``** 表示测试用例 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="dddf8-288">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="dddf8-289">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-290">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="dddf8-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="dddf8-291">generatetestsuite</span></span>
<span data-ttu-id="dddf8-292">在输出目录中为指定的套件生成所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="dddf8-293">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="dddf8-294">将列中的任何值用作 **test_suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-295">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-295">Required parameters</span></span>
<span data-ttu-id="dddf8-296">**``test_suite_name``** 表示测试套件名称。</span><span class="sxs-lookup"><span data-stu-id="dddf8-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="dddf8-297">**``output_dir``** 表示输出目录。</span><span class="sxs-lookup"><span data-stu-id="dddf8-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="dddf8-298">该目录必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-299">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="dddf8-300">help</span><span class="sxs-lookup"><span data-stu-id="dddf8-300">help</span></span>
<span data-ttu-id="dddf8-301">与 [?](####?) 相同</span><span class="sxs-lookup"><span data-stu-id="dddf8-301">Identical to the [?](####?)</span></span> <span data-ttu-id="dddf8-302">命令</span><span class="sxs-lookup"><span data-stu-id="dddf8-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="dddf8-303">列表</span><span class="sxs-lookup"><span data-stu-id="dddf8-303">list</span></span>
<span data-ttu-id="dddf8-304">列出所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="dddf8-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="dddf8-305">listtestplans</span></span>
<span data-ttu-id="dddf8-306">列出所有可用的测试计划。</span><span class="sxs-lookup"><span data-stu-id="dddf8-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="dddf8-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="dddf8-307">listtestsuite</span></span>
<span data-ttu-id="dddf8-308">列出指定测试套件的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="dddf8-309">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="dddf8-310">将第一列中的任何值用作 **suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-311">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-311">Required parameters</span></span>
<span data-ttu-id="dddf8-312">**``suite_name``** 所需套件的名称。</span><span class="sxs-lookup"><span data-stu-id="dddf8-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-313">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="dddf8-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="dddf8-314">listtestsuitenames</span></span>
<span data-ttu-id="dddf8-315">列出所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="dddf8-316">playback</span><span class="sxs-lookup"><span data-stu-id="dddf8-316">playback</span></span>
<span data-ttu-id="dddf8-317">使用 Excel 文件播放测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-318">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-318">Required parameters</span></span>
<span data-ttu-id="dddf8-319">**``excel_file``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="dddf8-320">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="dddf8-321">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="dddf8-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="dddf8-322">playbackbyid</span></span>
<span data-ttu-id="dddf8-323">一次播放多个测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="dddf8-324">可使用 ``list`` 命令获取所有可用的测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="dddf8-325">将第一列的任何值用作 **test_case_id** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-326">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-326">Required parameters</span></span>
<span data-ttu-id="dddf8-327">**``test_case_id1``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="dddf8-328">**``test_case_id2``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="dddf8-329">**``test_case_idN``** 现有测试用例的 ID。</span><span class="sxs-lookup"><span data-stu-id="dddf8-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="dddf8-330">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="dddf8-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="dddf8-331">playbackmany</span></span>
<span data-ttu-id="dddf8-332">使用 Excel 文件一次播放大量测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-333">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-333">Required parameters</span></span>
<span data-ttu-id="dddf8-334">**``excel_file1``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="dddf8-335">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-335">File must exist.</span></span>  
<span data-ttu-id="dddf8-336">**``excel_file2``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="dddf8-337">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-337">File must exist.</span></span>  
<span data-ttu-id="dddf8-338">**``excel_fileN``** Excel 文件的完整路径。</span><span class="sxs-lookup"><span data-stu-id="dddf8-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="dddf8-339">文件必须存在。</span><span class="sxs-lookup"><span data-stu-id="dddf8-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="dddf8-340">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="dddf8-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="dddf8-341">playbacksuite</span></span>
<span data-ttu-id="dddf8-342">播放指定测试套件中的所有测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="dddf8-343">可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="dddf8-344">将第一列中的任何值用作 **suite_name** 参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-345">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-345">Required parameters</span></span>
<span data-ttu-id="dddf8-346">**``suite_name``** 所需套件的名称。</span><span class="sxs-lookup"><span data-stu-id="dddf8-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-347">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="dddf8-348">quit</span><span class="sxs-lookup"><span data-stu-id="dddf8-348">quit</span></span>
<span data-ttu-id="dddf8-349">关闭应用程序。</span><span class="sxs-lookup"><span data-stu-id="dddf8-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="dddf8-350">upload</span><span class="sxs-lookup"><span data-stu-id="dddf8-350">upload</span></span>
<span data-ttu-id="dddf8-351">上载属于指定测试套件或测试用例的所有文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="dddf8-352">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-352">Required parameters</span></span>
<span data-ttu-id="dddf8-353">**``suite_name``** 将上载属于指定测试套件的所有文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="dddf8-354">**``testcase_id``** 将上载属于指定测试用例的所有文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-355">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="dddf8-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="dddf8-356">uploadrecording</span></span>
<span data-ttu-id="dddf8-357">仅上载属于指定测试用例的录制文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="dddf8-358">必要参数</span><span class="sxs-lookup"><span data-stu-id="dddf8-358">Required parameters</span></span>
<span data-ttu-id="dddf8-359">**``testcase_id``** 将仅上载属于指定测试用例的录制文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="dddf8-360">示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="dddf8-361">usage</span><span class="sxs-lookup"><span data-stu-id="dddf8-361">usage</span></span>
<span data-ttu-id="dddf8-362">显示两种调用此应用程序的方法：一种使用默认设置文件，另一种提供设置文件。</span><span class="sxs-lookup"><span data-stu-id="dddf8-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="dddf8-363">Windows PowerShell 示例</span><span class="sxs-lookup"><span data-stu-id="dddf8-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="dddf8-364">循环运行测试用例</span><span class="sxs-lookup"><span data-stu-id="dddf8-364">Run a test case in a loop</span></span>

<span data-ttu-id="dddf8-365">您有一个测试脚本用于创建新客户。</span><span class="sxs-lookup"><span data-stu-id="dddf8-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="dddf8-366">通过脚本，可以在运行每个迭代之前随机化以下数据来运行此测试用例。</span><span class="sxs-lookup"><span data-stu-id="dddf8-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="dddf8-367">客户 ID</span><span class="sxs-lookup"><span data-stu-id="dddf8-367">Customer ID</span></span>
- <span data-ttu-id="dddf8-368">客户名称</span><span class="sxs-lookup"><span data-stu-id="dddf8-368">Customer name</span></span>
- <span data-ttu-id="dddf8-369">客户地址</span><span class="sxs-lookup"><span data-stu-id="dddf8-369">Customer address</span></span>

<span data-ttu-id="dddf8-370">客户 ID 的格式为 *ATCUS\<number\>*，其中， \<number\> 是一个 **000000001** 与 **999999999** 之间的值。</span><span class="sxs-lookup"><span data-stu-id="dddf8-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="dddf8-371">以下示例使用一个参数 **start** 定义使用的第一个数字。</span><span class="sxs-lookup"><span data-stu-id="dddf8-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="dddf8-372">使用第二个参数 **nr** 定义必须创建的客户数量。</span><span class="sxs-lookup"><span data-stu-id="dddf8-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="dddf8-373">对于每个迭代，可使用 UpdateCustomer 函数更改 Excel 参数文件中的参数。</span><span class="sxs-lookup"><span data-stu-id="dddf8-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="dddf8-374">然后，在 RunTestCase 函数中调用 RSAT 命令行。</span><span class="sxs-lookup"><span data-stu-id="dddf8-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="dddf8-375">在管理模式下打开 Microsoft Windows PowerShell 集成脚本环境 (ISE)，然后将以下代码粘贴到名称为 **Untitled1.ps1** 的窗口中。</span><span class="sxs-lookup"><span data-stu-id="dddf8-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="dddf8-376">在 Microsoft Dynamics 365 中运行依赖数据的脚本</span><span class="sxs-lookup"><span data-stu-id="dddf8-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="dddf8-377">以下示例使用开放数据协议 (OData) 调用查找采购订单的订单状态。</span><span class="sxs-lookup"><span data-stu-id="dddf8-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="dddf8-378">例如，如果状态不是**已开票**，则可调用 RSAT 测试用例以过帐发票。</span><span class="sxs-lookup"><span data-stu-id="dddf8-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
