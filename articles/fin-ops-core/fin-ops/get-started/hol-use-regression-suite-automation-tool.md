---
title: Regression Suite Automation Tool 使用教程
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
ms.openlocfilehash: cf3ca501efb4e540994b01e651eee5b8aab4ddbc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191078"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="5357b-104">Regression Suite Automation Tool 使用教程</span><span class="sxs-lookup"><span data-stu-id="5357b-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5357b-105">可使用 Internet 浏览器工具下载此页并以 pdf 格式保存。</span><span class="sxs-lookup"><span data-stu-id="5357b-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="5357b-106">本教程演练 Regression Suite Automation Tool (RSAT) 的部分高级功能，包括演示分配，还介绍策略和关键学习点。</span><span class="sxs-lookup"><span data-stu-id="5357b-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="5357b-107">RSAT/任务录制器的功能</span><span class="sxs-lookup"><span data-stu-id="5357b-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="5357b-108">验证字段值</span><span class="sxs-lookup"><span data-stu-id="5357b-108">Validate a field value</span></span>

<span data-ttu-id="5357b-109">有关此功能的信息，请参阅[创建具有验证功能的新任务录制](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)。</span><span class="sxs-lookup"><span data-stu-id="5357b-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="5357b-110">已保存变量</span><span class="sxs-lookup"><span data-stu-id="5357b-110">Saved variable</span></span>

<span data-ttu-id="5357b-111">有关此功能的信息，请参阅[修改现有任务录制以创建已保存变量](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)。</span><span class="sxs-lookup"><span data-stu-id="5357b-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="5357b-112">派生测试用例</span><span class="sxs-lookup"><span data-stu-id="5357b-112">Derived test case</span></span>

1. <span data-ttu-id="5357b-113">打开 Regression Suite Automation Tool (RSAT)，然后选择您在[设置和安装 Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md) 中创建的测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="5357b-114">选择**新建 \> 创建派生测试用例**。</span><span class="sxs-lookup"><span data-stu-id="5357b-114">Select **New \> Create derived test case**.</span></span>

    ![“新建”菜单上的“创建派生测试用例”命令](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="5357b-116">您将收到一条消息，说明将为当前测试套件中选择的每个测试用例创建一个派生测试用例，以及每个派生测试用例将有自己的 Excel 参数文件副本。</span><span class="sxs-lookup"><span data-stu-id="5357b-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5357b-117">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="5357b-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5357b-118">运行派生测试用例时，其使用自己的父测试用例的任务录制和自己的 Excel 参数文件副本。</span><span class="sxs-lookup"><span data-stu-id="5357b-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="5357b-119">因此，可以使用不同参数运行同一个测试，不必维护多个任务录制。</span><span class="sxs-lookup"><span data-stu-id="5357b-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="5357b-120">派生测试用例不必与其父测试用例属于同一个测试套件。</span><span class="sxs-lookup"><span data-stu-id="5357b-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![消息框](./media/use_rsa_tool_02.png)

    <span data-ttu-id="5357b-122">将创建两个额外的测试用例，并且为其选中**是否派生?** 复选框。</span><span class="sxs-lookup"><span data-stu-id="5357b-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![已创建派生测试用例](./media/use_rsa_tool_03.png)

    <span data-ttu-id="5357b-124">将在 Azure DevOps 中创建一个派生测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="5357b-125">这是**创建新产品**测试用例的子项，并带有特殊关键字标记：**RSAT:DerivedTestSteps**。</span><span class="sxs-lookup"><span data-stu-id="5357b-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="5357b-126">还会将这些测试用例自动添加到 Azure DevOps 中的测试计划。</span><span class="sxs-lookup"><span data-stu-id="5357b-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![RSAT:DerivedTestSteps 关键字](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="5357b-128">如果因为任何原因导致创建的派生测试用例的顺序不正确，请转到 Azure DevOps 并为测试套件中的测试用例重新排序，以便 RSAT 按正确顺序运行这些测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="5357b-129">选择派生测试用例，然后选择**编辑**打开相应 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="5357b-130">按照编辑父文件的方式编辑这些 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="5357b-131">换句话说，确保设置产品 ID，以便自动生成。</span><span class="sxs-lookup"><span data-stu-id="5357b-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="5357b-132">同时确保将已保存变量复制到相关字段。</span><span class="sxs-lookup"><span data-stu-id="5357b-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="5357b-133">在两个 Excel 参数文件的**常规**选项卡上，将**公司**字段的值更新为 **USSI**，以便对非父测试用例法人运行派生测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="5357b-134">若要对特定用户（或与特定用户关联的角色）运行测试用例，可以更新**测试用户**字段的值。</span><span class="sxs-lookup"><span data-stu-id="5357b-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="5357b-135">选择**运行**，并且验证是否同时在 USMF 法人和 USSI 法人中创建了产品。</span><span class="sxs-lookup"><span data-stu-id="5357b-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="5357b-136">验证通知</span><span class="sxs-lookup"><span data-stu-id="5357b-136">Validate notifications</span></span>

<span data-ttu-id="5357b-137">可使用此功能验证是否执行了某个操作。</span><span class="sxs-lookup"><span data-stu-id="5357b-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="5357b-138">例如，创建、估计，然后开始履行生产订单时，应用程序将显示“生产 - 开始”消息，通知您已开始履行生产订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![“生产 – 开始”通知](./media/use_rsa_tool_05.png)

<span data-ttu-id="5357b-140">可通过 RSAT 验证此消息，方法是在相应录制的 Excel 参数文件的 **MessageValidation** 选项卡上输入消息文本。</span><span class="sxs-lookup"><span data-stu-id="5357b-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![“消息验证”选项卡](./media/use_rsa_tool_06.png)

<span data-ttu-id="5357b-142">运行测试用例之后，将把 Excel 参数文件中的消息与显示的消息进行比较。</span><span class="sxs-lookup"><span data-stu-id="5357b-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="5357b-143">如果这些消息不匹配，测试用例将失败。</span><span class="sxs-lookup"><span data-stu-id="5357b-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="5357b-144">可在 Excel 参数文件中的 **MessageValidation** 选项卡上输入多条消息。</span><span class="sxs-lookup"><span data-stu-id="5357b-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="5357b-145">这些消息也可以是错误消息或警告消息，而不是参考消息。</span><span class="sxs-lookup"><span data-stu-id="5357b-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="5357b-146">使用运算符验证值</span><span class="sxs-lookup"><span data-stu-id="5357b-146">Validate values by using operators</span></span>

<span data-ttu-id="5357b-147">在 RSAT 早期版本中，仅当控制值等于预期值时，才可以验证值。</span><span class="sxs-lookup"><span data-stu-id="5357b-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="5357b-148">新功能则允许您验证某个变量是否不等于、小于或大于指定值。</span><span class="sxs-lookup"><span data-stu-id="5357b-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="5357b-149">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="5357b-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="5357b-150">在 Excel 参数文件中，将显示一个新的**运算符**字段。</span><span class="sxs-lookup"><span data-stu-id="5357b-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5357b-151">如果已经在使用 RSAT 早期版本，则必须生成新的 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![“运算符”字段](./media/use_rsa_tool_07.png)

<span data-ttu-id="5357b-153">以下示例演示如何使用此功能来验证现有库存量是否超过 0（零）。</span><span class="sxs-lookup"><span data-stu-id="5357b-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="5357b-154">在 **USMF** 公司的演示数据中，创建一个包含以下步骤的任务录制：</span><span class="sxs-lookup"><span data-stu-id="5357b-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="5357b-155">转到**产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="5357b-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="5357b-156">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="5357b-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5357b-157">例如，对**物料编号**字段使用值 **1000** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="5357b-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="5357b-158">选择**现有库存量**。</span><span class="sxs-lookup"><span data-stu-id="5357b-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="5357b-159">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="5357b-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="5357b-160">例如，对**站点**字段使用值 **1** 进行筛选。</span><span class="sxs-lookup"><span data-stu-id="5357b-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="5357b-161">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="5357b-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="5357b-162">验证**可用合计**字段的值是否为 **411.0000000000000000**。</span><span class="sxs-lookup"><span data-stu-id="5357b-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="5357b-163">将任务录制保存到 LCS 中的 BPM 库，然后同步到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="5357b-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="5357b-164">将测试用例添加到测试计划，然后将测试用例加载到 RSAT 中。</span><span class="sxs-lookup"><span data-stu-id="5357b-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="5357b-165">打开 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-165">Open the Excel parameter file.</span></span> <span data-ttu-id="5357b-166">在 **InventOnhandItem** 选项卡上，将看到 **Validate InventOnhandItem** 部分，其中包含一个**运算符**字段。</span><span class="sxs-lookup"><span data-stu-id="5357b-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![“运算符”字段](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="5357b-168">若要验证现有库存量是否始终大于 0，请将**值**字段的值从 **411** 更改为 **0**，将**运算符**字段的值从等号 (**=**) 更改为大于符号 (**\>**)。</span><span class="sxs-lookup"><span data-stu-id="5357b-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![“值”和“运算符”字段的值已更改](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="5357b-170">保存并关闭 Excel 参数文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="5357b-171">选择**上载**将对 Excel 参数文件执行的更改保存到 Azure DevOps。</span><span class="sxs-lookup"><span data-stu-id="5357b-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="5357b-172">现在，如果库存中指定物料的**可用合计**字段的值大于 0（零），无论实际现有库存量值是多少，测试都将失败。</span><span class="sxs-lookup"><span data-stu-id="5357b-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="5357b-173">生成器日志</span><span class="sxs-lookup"><span data-stu-id="5357b-173">Generator logs</span></span>

<span data-ttu-id="5357b-174">此功能将创建一个文件夹，其中包含已运行的测试用例的日志。</span><span class="sxs-lookup"><span data-stu-id="5357b-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="5357b-175">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="5357b-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="5357b-176">运行测试用例之后，可以在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs** 下找到日志文件。</span><span class="sxs-lookup"><span data-stu-id="5357b-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![GeneratorLogs 文件夹](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="5357b-178">如果更改 .config 文件中的值之前已有测试用例，则生成新的测试执行文件之前，不会为这些测试用例生成日志。</span><span class="sxs-lookup"><span data-stu-id="5357b-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![“新建”菜单上的“仅生成测试执行文件”命令](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="5357b-180">快照</span><span class="sxs-lookup"><span data-stu-id="5357b-180">Snapshot</span></span>

<span data-ttu-id="5357b-181">此功能用于拍摄任务录制期间执行的步骤的屏幕快照。</span><span class="sxs-lookup"><span data-stu-id="5357b-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="5357b-182">若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素的值从 **false** 更改为 **true**。</span><span class="sxs-lookup"><span data-stu-id="5357b-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="5357b-183">将在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** 下为运行的每个测试用例创建一个单独的文件夹。</span><span class="sxs-lookup"><span data-stu-id="5357b-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![测试用例的快照文件夹](./media/use_rsa_tool_12.png)

<span data-ttu-id="5357b-185">在这些文件夹的每一个中，都可以找到运行测试用例期间执行的步骤的快照。</span><span class="sxs-lookup"><span data-stu-id="5357b-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![快照文件](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="5357b-187">赋值</span><span class="sxs-lookup"><span data-stu-id="5357b-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="5357b-188">方案</span><span class="sxs-lookup"><span data-stu-id="5357b-188">Scenario</span></span>

1. <span data-ttu-id="5357b-189">产品设计人员创建一个新发布的产品。</span><span class="sxs-lookup"><span data-stu-id="5357b-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="5357b-190">生产经理发起一个生产订单以将库存水平提升到两件。</span><span class="sxs-lookup"><span data-stu-id="5357b-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="5357b-191">制造将开始履行和终止生产订单，并验证现有数量是否为两件。</span><span class="sxs-lookup"><span data-stu-id="5357b-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="5357b-192">销售团队收到一个包含四件新产品的订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="5357b-193">因此，销售团队通过动态计划更新净需求。</span><span class="sxs-lookup"><span data-stu-id="5357b-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="5357b-194">因为没有更多产能，所以默认订单策略设置为“以买代造”。</span><span class="sxs-lookup"><span data-stu-id="5357b-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="5357b-195">因此，将创建一个计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="5357b-196">买方将添加一个供应商，确认计划采购订单，然后确认该采购订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="5357b-197">采购的货物到店时，商店操作员将搜索相关采购订单并收货。</span><span class="sxs-lookup"><span data-stu-id="5357b-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="5357b-198">因为订单现在已完成，所以可以针对销售订单拣货和为货物打包。</span><span class="sxs-lookup"><span data-stu-id="5357b-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="5357b-199">财务将过帐采购发票和销售发票。</span><span class="sxs-lookup"><span data-stu-id="5357b-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="5357b-200">下图显示此场景的流程。</span><span class="sxs-lookup"><span data-stu-id="5357b-200">The following illustration shows the flow for this scenario.</span></span>

![演示场景的流程](./media/use_rsa_tool_14.png)

<span data-ttu-id="5357b-202">下图显示此场景在 RSAT 中的业务流程。</span><span class="sxs-lookup"><span data-stu-id="5357b-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![演示场景的业务流程](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="5357b-204">策略 – 关键学习点</span><span class="sxs-lookup"><span data-stu-id="5357b-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="5357b-205">数据</span><span class="sxs-lookup"><span data-stu-id="5357b-205">Data</span></span>

- <span data-ttu-id="5357b-206">确保您有代表数据卷（生产/黄金配置数据加迁移数据的副本）。</span><span class="sxs-lookup"><span data-stu-id="5357b-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="5357b-207">通过任务录制器生成新数据时，请创建与现有名称不冲突的测试名称（例如，使用 **RSATxxx** 之类前缀）。</span><span class="sxs-lookup"><span data-stu-id="5357b-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="5357b-208">使用 Azure 时间点还原在非一级环境中重新运行测试。</span><span class="sxs-lookup"><span data-stu-id="5357b-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="5357b-209">如果使用 Excel 函数 **RANDOM** 和 **NOW** 生成唯一组合，则工作量非常大。</span><span class="sxs-lookup"><span data-stu-id="5357b-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="5357b-210">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="5357b-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="5357b-211">任务录制器</span><span class="sxs-lookup"><span data-stu-id="5357b-211">Task recorder</span></span>

- <span data-ttu-id="5357b-212">开始录制前定义场景。</span><span class="sxs-lookup"><span data-stu-id="5357b-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="5357b-213">一个管理有方的项目已预定义了测试场景。</span><span class="sxs-lookup"><span data-stu-id="5357b-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="5357b-214">若要生成测试案例，请注意这些测试场景的结果可预测程度。</span><span class="sxs-lookup"><span data-stu-id="5357b-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="5357b-215">如果录制由不同角色执行，或者如果执行下一步之前需要等待或存在外部事件，请拆分录制。</span><span class="sxs-lookup"><span data-stu-id="5357b-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="5357b-216">请避免选择列表中的值。</span><span class="sxs-lookup"><span data-stu-id="5357b-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="5357b-217">而是改用文本格式，如 **FIFO**、**AudioRM** 和 **SiteWH**。</span><span class="sxs-lookup"><span data-stu-id="5357b-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="5357b-218">如果在列表中进行选择，则会录制值在列表中的位置，而不是录制值本身。</span><span class="sxs-lookup"><span data-stu-id="5357b-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="5357b-219">如果向该列表添加物料，值的位置可能会改变。</span><span class="sxs-lookup"><span data-stu-id="5357b-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="5357b-220">因此，录制将使用其他参数，并且可能会影响场景的其余部分。</span><span class="sxs-lookup"><span data-stu-id="5357b-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="5357b-221">请注意多用户行为。</span><span class="sxs-lookup"><span data-stu-id="5357b-221">Think about multi-user behavior.</span></span> <span data-ttu-id="5357b-222">例如，不要想当然地以为始终会自动选中新建的销售订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="5357b-223">请始终改用筛选器查找正确订单。</span><span class="sxs-lookup"><span data-stu-id="5357b-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="5357b-224">任务录制器中的复制功能用于保存新建产品的名称，以便在链式测试用例中使用。</span><span class="sxs-lookup"><span data-stu-id="5357b-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="5357b-225">任务录制器中的验证功能用于设置检查点来验证是否已正确运行了步骤。</span><span class="sxs-lookup"><span data-stu-id="5357b-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="5357b-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="5357b-226">RSAT</span></span>

- <span data-ttu-id="5357b-227">若要在另一个公司中运行测试，可以在 Excel 参数文件的**常规**选项卡上更改公司。</span><span class="sxs-lookup"><span data-stu-id="5357b-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5357b-228">确保新选择的公司中有设置和数据。</span><span class="sxs-lookup"><span data-stu-id="5357b-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="5357b-229">可在 Excel 参数文件的**常规**选项卡上更改测试用户。</span><span class="sxs-lookup"><span data-stu-id="5357b-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5357b-230">指定将运行测试用例的用户的电子邮件 ID。</span><span class="sxs-lookup"><span data-stu-id="5357b-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="5357b-231">这样，就可以通过使用所指定用户的安全权限运行测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="5357b-232">若要在开始测试之前等待，可在 Excel 参数文件的**常规**选项卡上定义暂停。</span><span class="sxs-lookup"><span data-stu-id="5357b-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="5357b-233">可在批处理作业中使用此暂停（例如，如果必须向运行工作流，才能执行下一个步骤。）</span><span class="sxs-lookup"><span data-stu-id="5357b-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="5357b-234">高级脚本</span><span class="sxs-lookup"><span data-stu-id="5357b-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="5357b-235">命令行</span><span class="sxs-lookup"><span data-stu-id="5357b-235">Command line</span></span>

<span data-ttu-id="5357b-236">可以从**命令提示符**窗口调用 RSAT。</span><span class="sxs-lookup"><span data-stu-id="5357b-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="5357b-237">请验证环境变量 **TestRoot** 是否设置为 RSAT 安装路径。</span><span class="sxs-lookup"><span data-stu-id="5357b-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="5357b-238">（在 Microsoft Windows 中，打开**控制面板**，选择**系统和安全 \> 系统 \> 高级安全设置**，然后选择**环境变量**。）</span><span class="sxs-lookup"><span data-stu-id="5357b-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="5357b-239">以管理员身份打开**命令提示符**窗口。</span><span class="sxs-lookup"><span data-stu-id="5357b-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="5357b-240">从安装目录运行工具。</span><span class="sxs-lookup"><span data-stu-id="5357b-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="5357b-241">列出所有命令。</span><span class="sxs-lookup"><span data-stu-id="5357b-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="5357b-242">Windows PowerShell 示例</span><span class="sxs-lookup"><span data-stu-id="5357b-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="5357b-243">循环运行测试用例</span><span class="sxs-lookup"><span data-stu-id="5357b-243">Run a test case in a loop</span></span>

<span data-ttu-id="5357b-244">您有一个测试脚本用于创建新客户。</span><span class="sxs-lookup"><span data-stu-id="5357b-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="5357b-245">通过脚本，可以在运行每个迭代之前随机化以下数据来运行此测试用例。</span><span class="sxs-lookup"><span data-stu-id="5357b-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="5357b-246">客户 ID</span><span class="sxs-lookup"><span data-stu-id="5357b-246">Customer ID</span></span>
- <span data-ttu-id="5357b-247">客户名称</span><span class="sxs-lookup"><span data-stu-id="5357b-247">Customer name</span></span>
- <span data-ttu-id="5357b-248">客户地址</span><span class="sxs-lookup"><span data-stu-id="5357b-248">Customer address</span></span>

<span data-ttu-id="5357b-249">客户 ID 的格式为 *ATCUS\<number\>*，其中， \<number\> 是一个 **000000001** 与 **999999999** 之间的值。</span><span class="sxs-lookup"><span data-stu-id="5357b-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="5357b-250">以下示例使用一个参数 **start** 定义使用的第一个数字。</span><span class="sxs-lookup"><span data-stu-id="5357b-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="5357b-251">使用第二个参数 **nr** 定义必须创建的客户数量。</span><span class="sxs-lookup"><span data-stu-id="5357b-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="5357b-252">对于每个迭代，可使用 UpdateCustomer 函数更改 Excel 参数文件中的参数。</span><span class="sxs-lookup"><span data-stu-id="5357b-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="5357b-253">然后，在 RunTestCase 函数中调用 RSAT 命令行。</span><span class="sxs-lookup"><span data-stu-id="5357b-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="5357b-254">在管理模式下打开 Microsoft Windows PowerShell 集成脚本环境 (ISE)，然后将以下代码粘贴到名称为 **Untitled1.ps1** 的窗口中。</span><span class="sxs-lookup"><span data-stu-id="5357b-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="5357b-255">在 Microsoft Dynamics 365 中运行依赖数据的脚本</span><span class="sxs-lookup"><span data-stu-id="5357b-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="5357b-256">以下示例使用开放数据协议 (OData) 调用查找采购订单的订单状态。</span><span class="sxs-lookup"><span data-stu-id="5357b-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="5357b-257">例如，如果状态不是**已开票**，则可调用 RSAT 测试用例以过帐发票。</span><span class="sxs-lookup"><span data-stu-id="5357b-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
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
