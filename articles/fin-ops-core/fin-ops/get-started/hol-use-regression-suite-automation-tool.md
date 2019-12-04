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
ms.openlocfilehash: 654685a382ca5f3f462ad8a9c506b51b52c3758c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811641"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool 使用教程

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 可使用 Internet 浏览器工具下载此页并以 pdf 格式保存。 

本教程演练 Regression Suite Automation Tool (RSAT) 的部分高级功能，包括演示分配，还介绍策略和关键学习点。

## <a name="features-of-rsattask-recorder"></a>RSAT/任务录制器的功能

### <a name="validate-a-field-value"></a>验证字段值

有关此功能的信息，请参阅[创建具有验证功能的新任务录制](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function)。

### <a name="saved-variable"></a>已保存变量

有关此功能的信息，请参阅[修改现有任务录制以创建已保存变量](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable)。

### <a name="derived-test-case"></a>派生测试用例

1. 打开 Regression Suite Automation Tool (RSAT)，然后选择您在[设置和安装 Regression Suite Automation Tool 教程](./hol-set-up-regression-suite-automation-tool.md)中创建的测试用例。
2. 选择**新建 \> 创建派生测试用例**。

    ![“新建”菜单上的“创建派生测试用例”命令](./media/use_rsa_tool_01.png)

3. 您将收到一条消息，说明将为当前测试套件中选择的每个测试用例创建一个派生测试用例，以及每个派生测试用例将有自己的 Excel 参数文件副本。 选择**确定**。

    > [!NOTE]
    > 运行派生测试用例时，其使用自己的父测试用例的任务录制和自己的 Excel 参数文件副本。 因此，可以使用不同参数运行同一个测试，不必维护多个任务录制。 派生测试用例不必与其父测试用例属于同一个测试套件。

    ![消息框](./media/use_rsa_tool_02.png)

    将创建两个额外的测试用例，并且为其选中**是否派生?** 复选框。

    ![已创建派生测试用例](./media/use_rsa_tool_03.png)

    将在 Azure DevOps 中创建一个派生测试用例。 这是**创建新产品**测试用例的子项，并带有特殊关键字标记：**RSAT:DerivedTestSteps**。 还会将这些测试用例自动添加到 Azure DevOps 中的测试计划。

    ![RSAT:DerivedTestSteps 关键字](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > 如果因为任何原因导致创建的派生测试用例的顺序不正确，请转到 Azure DevOps 并为测试套件中的测试用例重新排序，以便 RSAT 按正确顺序运行这些测试用例。

4. 选择派生测试用例，然后选择**编辑**打开相应 Excel 参数文件。
5. 按照编辑父文件的方式编辑这些 Excel 参数文件。 换句话说，确保设置产品 ID，以便自动生成。 同时确保将已保存变量复制到相关字段。
6. 在两个 Excel 参数文件的**常规**选项卡上，将**公司**字段的值更新为 **USSI**，以便对非父测试用例法人运行派生测试用例。 若要对特定用户（或与特定用户关联的角色）运行测试用例，可以更新**测试用户**字段的值。
7. 选择**运行**，并且验证是否同时在 USMF 法人和 USSI 法人中创建了产品。

### <a name="validate-notifications"></a>验证通知

可使用此功能验证是否执行了某个操作。 例如，创建、估计，然后开始履行生产订单时，应用程序将显示“生产 - 开始”消息，通知您已开始履行生产订单。

![“生产 – 开始”通知](./media/use_rsa_tool_05.png)

可通过 RSAT 验证此消息，方法是在相应录制的 Excel 参数文件的 **MessageValidation** 选项卡上输入消息文本。

![“消息验证”选项卡](./media/use_rsa_tool_06.png)

运行测试用例之后，将把 Excel 参数文件中的消息与显示的消息进行比较。 如果这些消息不匹配，测试用例将失败。

> [!NOTE]
> 可在 Excel 参数文件中的 **MessageValidation** 选项卡上输入多条消息。 这些消息也可以是错误消息或警告消息，而不是参考消息。

### <a name="validate-values-by-using-operators"></a>使用运算符验证值

在 RSAT 早期版本中，仅当控制值等于预期值时，才可以验证值。 新功能则允许您验证某个变量是否不等于、小于或大于指定值。

- 若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    在 Excel 参数文件中，将显示一个新的**运算符**字段。

    > [!NOTE]
    > 如果已经在使用 RSAT 早期版本，则必须生成新的 Excel 参数文件。

    ![“运算符”字段](./media/use_rsa_tool_07.png)

以下示例演示如何使用此功能来验证现有库存量是否超过 0（零）。

1. 在 **USMF** 公司的演示数据中，创建一个包含以下步骤的任务录制：

    1. 转到**产品信息管理 \> 产品 \> 已发布产品**。
    2. 使用“快速筛选器”以查找记录。 例如，对**物料编号**字段使用值 **1000** 进行筛选。
    3. 选择**现有库存量**。
    4. 使用“快速筛选器”以查找记录。 例如，对**站点**字段使用值 **1** 进行筛选。
    5. 在列表中，标记所选的行。
    6. 验证**可用合计**字段的值是否为 **411.0000000000000000**。

2. 将任务录制保存到 LCS 中的 BPM 库，然后同步到 Azure DevOps。
3. 将测试用例添加到测试计划，然后将测试用例加载到 RSAT 中。
4. 打开 Excel 参数文件。 在 **InventOnhandItem** 选项卡上，将看到 **Validate InventOnhandItem** 部分，其中包含一个**运算符**字段。

    ![“运算符”字段](./media/use_rsa_tool_08.png)

5. 若要验证现有库存量是否始终大于 0，请将**值**字段的值从 **411** 更改为 **0**，将**运算符**字段的值从等号 (**=**) 更改为大于符号 (**\>**)。

    ![“值”和“运算符”字段的值已更改](./media/use_rsa_tool_09.png)

6. 保存并关闭 Excel 参数文件。
7. 选择**上载**将对 Excel 参数文件执行的更改保存到 Azure DevOps。

现在，如果库存中指定物料的**可用合计**字段的值大于 0（零），无论实际现有库存量值是多少，测试都将失败。

### <a name="generator-logs"></a>生成器日志

此功能将创建一个文件夹，其中包含已运行的测试用例的日志。

- 若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素中的值从 **false** 更改为 **true**。

    ```
    <add key="LogGeneration" value="false" />
    ```

运行测试用例之后，可以在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs** 下找到日志文件。

![GeneratorLogs 文件夹](./media/use_rsa_tool_10.png)

> [!NOTE]
> 如果更改 .config 文件中的值之前已有测试用例，则生成新的测试执行文件之前，不会为这些测试用例生成日志。
> 
> ![“新建”菜单上的“仅生成测试执行文件”命令](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a>快照

此功能用于拍摄任务录制期间执行的步骤的屏幕快照。

- 若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素的值从 **false** 更改为 **true**。

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

将在 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** 下为运行的每个测试用例创建一个单独的文件夹。

![测试用例的快照文件夹](./media/use_rsa_tool_12.png)

在这些文件夹的每一个中，都可以找到运行测试用例期间执行的步骤的快照。

![快照文件](./media/use_rsa_tool_13.png)

## <a name="assignment"></a>赋值

### <a name="scenario"></a>方案

1. 产品设计人员创建一个新发布的产品。
2. 生产经理发起一个生产订单以将库存水平提升到两件。
3. 制造将开始履行和终止生产订单，并验证现有数量是否为两件。
4. 销售团队收到一个包含四件新产品的订单。 因此，销售团队通过动态计划更新净需求。 因为没有更多产能，所以默认订单策略设置为“以买代造”。 因此，将创建一个计划采购订单。
5. 买方将添加一个供应商，确认计划采购订单，然后确认该采购订单。
6. 采购的货物到店时，商店操作员将搜索相关采购订单并收货。 因为订单现在已完成，所以可以针对销售订单拣货和为货物打包。
7. 财务将过帐采购发票和销售发票。

下图显示此场景的流程。

![演示场景的流程](./media/use_rsa_tool_14.png)

下图显示此场景在 RSAT 中的业务流程。

![演示场景的业务流程](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>策略 – 关键学习点

### <a name="data"></a>数据

- 确保您有代表数据卷（生产/黄金配置数据加迁移数据的副本）。
- 通过任务录制器生成新数据时，请创建与现有名称不冲突的测试名称（例如，使用 **RSATxxx** 之类前缀）。
- 使用 Azure 时间点还原在非一级环境中重新运行测试。
- 如果使用 Excel 函数 **RANDOM** 和 **NOW** 生成唯一组合，则工作量非常大。 下面是一个示例。

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a>任务录制器

- 开始录制前定义场景。 一个管理有方的项目已预定义了测试场景。 若要生成测试案例，请注意这些测试场景的结果可预测程度。
- 如果录制由不同角色执行，或者如果执行下一步之前需要等待或存在外部事件，请拆分录制。
- 请避免选择列表中的值。 而是改用文本格式，如 **FIFO**、**AudioRM** 和 **SiteWH**。 如果在列表中进行选择，则会录制值在列表中的位置，而不是录制值本身。 如果向该列表添加物料，值的位置可能会改变。 因此，录制将使用其他参数，并且可能会影响场景的其余部分。
- 请注意多用户行为。 例如，不要想当然地以为始终会自动选中新建的销售订单。 请始终改用筛选器查找正确订单。
- 任务录制器中的复制功能用于保存新建产品的名称，以便在链式测试用例中使用。
- 任务录制器中的验证功能用于设置检查点来验证是否已正确运行了步骤。

### <a name="rsat"></a>RSAT

- 若要在另一个公司中运行测试，可以在 Excel 参数文件的**常规**选项卡上更改公司。 确保新选择的公司中有设置和数据。
- 可在 Excel 参数文件的**常规**选项卡上更改测试用户。 指定将运行测试用例的用户的电子邮件 ID。 这样，就可以通过使用所指定用户的安全权限运行测试用例。
- 若要在开始测试之前等待，可在 Excel 参数文件的**常规**选项卡上定义暂停。 可在批处理作业中使用此暂停（例如，如果必须向运行工作流，才能执行下一个步骤。）

## <a name="advanced-scripting"></a>高级脚本

### <a name="command-line"></a>命令行

可以从**命令提示符**窗口调用 RSAT。

> [!NOTE]
> 请验证环境变量 **TestRoot** 是否设置为 RSAT 安装路径。 （在 Microsoft Windows 中，打开**控制面板**，选择**系统和安全 \> 系统 \> 高级安全设置**，然后选择**环境变量**。）

1. 以管理员身份打开**命令提示符**窗口。
2. 从安装目录运行工具。

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. 列出所有命令。

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

### <a name="windows-powershell-examples"></a>Windows PowerShell 示例

#### <a name="run-a-test-case-in-a-loop"></a>循环运行测试用例

您有一个测试脚本用于创建新客户。 通过脚本，可以在运行每个迭代之前随机化以下数据来运行此测试用例。

- 客户 ID
- 客户名称
- 客户地址

客户 ID 的格式为 *ATCUS\<number\>*，其中， \<number\> 是一个 **000000001** 与 **999999999** 之间的值。

以下示例使用一个参数 **start** 定义使用的第一个数字。 使用第二个参数 **nr** 定义必须创建的客户数量。 对于每个迭代，可使用 UpdateCustomer 函数更改 Excel 参数文件中的参数。 然后，在 RunTestCase 函数中调用 RSAT 命令行。

在管理模式下打开 Microsoft Windows PowerShell 集成脚本环境 (ISE)，然后将以下代码粘贴到名称为 **Untitled1.ps1** 的窗口中。

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>在 Microsoft Dynamics 365 中运行依赖数据的脚本

以下示例使用开放数据协议 (OData) 调用查找采购订单的订单状态。 例如，如果状态不是**已开票**，则可调用 RSAT 测试用例以过帐发票。

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
