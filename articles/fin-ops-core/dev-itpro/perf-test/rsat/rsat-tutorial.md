---
title: Regression Suite Automation Tool 教程
description: 本主题说明如何使用 Regression Suite Automation Tool (RSAT)。 其中介绍各种功能，并提供使用高级脚本的示例。
author: robinarh
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: d70b2e7cf497fbf165a452f7977a14a98b9e1956e5a964d42c7bf8a6c3abe0bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714541"
---
# <a name="regression-suite-automation-tool-tutorial"></a>Regression Suite Automation Tool 教程

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> 可使用 Internet 浏览器工具下载此页并以 pdf 格式保存。

本教程演练 Regression Suite Automation Tool (RSAT) 的部分高级功能，包括演示分配，还介绍策略和关键学习点。

## <a name="notable-features-of-rsat-and-task-recorder"></a>值得注意的 RSAT 和任务录制器功能

### <a name="validate-a-field-value"></a>验证字段值

RSAT 允许您在测试用例中包含验证步骤，以验证期望值。 有关此功能的信息，请参阅文章[验证期望值](rsat-validate-expected.md)。

以下示例演示如何使用此功能来验证现有库存量是否超过 0（零）。

1. 在 **USMF** 公司的演示数据中，创建一个包含以下步骤的任务录制：

    1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
    2. 使用“快速筛选器”以查找记录。 例如，对 **物料编号** 字段使用值 **1000** 进行筛选。
    3. 选择 **现有库存量**。
    4. 使用“快速筛选器”以查找记录。 例如，对 **站点** 字段使用值 **1** 进行筛选。
    5. 在列表中，标记所选的行。
    6. 验证 **可用合计** 字段的值是否为 **411.0000000000000000**。

2. 将任务录制另存为 **开发人员录制**，并在 Azure Devops 中将其附加到测试用例中。
3. 将测试用例添加到测试计划，然后将测试用例加载到 RSAT 中。
4. 打开 Excel 参数文件，转到 **TestCaseSteps** 选项卡。
5. 要验证现有库存量是否总是大于 **0**，转到 **验证可用总计** 步骤，将值从 **411** 更改为 **0**。 将 **运算符** 字段的值从等号 (**=**) 更改为大于号 (**\>**)。
6. 保存并关闭 Excel 参数文件。
7. 选择 **上载** 将对 Excel 参数文件执行的更改保存到 Azure DevOps。

现在，如果库存中指定物料的 **可用合计** 字段的值大于 0（零），无论实际现有库存量值是多少，测试都将失败。

### <a name="saved-variables-and-chaining-of-test-cases"></a>保存的变量和链接测试用例

RSAT 的一项关键功能是链接测试用例，即一个测试将变量传递给其他测试这项功能。 有关详细信息，请参阅文章[复制变量以链接测试用例](rsat-chain-test-cases.md)。

### <a name="derived-test-case"></a>派生测试用例

RSAT 让您可以对多个测试用例使用同一个任务录制，从而可以使用不同数据配置运行一个任务。 有关详细信息，请参阅文章[派生测试用例](rsat-derived-test-cases.md)。

### <a name="validate-notifications-and-messages"></a>验证通知和消息

可使用此功能验证是否执行了某个操作。 例如，创建、估计，然后开始履行生产订单时，应用程序将显示“生产 - 开始”消息，通知您已开始履行生产订单。

![“生产 – 开始”通知。](./media/use_rsa_tool_05.png)

可通过 RSAT 验证此消息，方法是在相应录制的 Excel 参数文件的 **MessageValidation** 选项卡上输入消息文本。

![“消息验证”选项卡。](./media/use_rsa_tool_06.png)

运行测试用例之后，将把 Excel 参数文件中的消息与显示的消息进行比较。 如果这些消息不匹配，测试用例将失败。

> [!NOTE]
> 可在 Excel 参数文件中的 **MessageValidation** 选项卡上输入多条消息。 这些消息也可以是错误消息或警告消息，而不是参考消息。

### <a name="snapshot"></a>快照

此功能用于拍摄任务录制期间执行的步骤的屏幕快照。 非常适合审核或调试用途。

- 若要使用此功能，请打开 RSAT 安装文件夹（如 **C:\\Program Files (x86)\\Regression Suite Automation Tool**）下的 **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** 文件，然后将以下元素的值从 **false** 更改为 **true**。

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

运行测试用例时，RSAT 将在工作目录中测试用例的播放文件夹内生成步骤的快照（映像）。 如果使用的 RSAT 版本较低，将把这些映像保存到 **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** 中，这是为运行的每个测试用例创建的单独文件夹。

## <a name="assignment"></a>赋值

### <a name="scenario"></a>应用场景

1. 产品设计人员创建一个新发布的产品。
2. 生产经理发起一个生产订单以将库存水平提升到两件。
3. 制造将开始履行和终止生产订单，并验证现有数量是否为两件。
4. 销售团队收到一个包含四件新产品的订单。 因此，销售团队通过动态计划更新净需求。 因为没有更多产能，所以默认订单策略设置为“以买代造”。 因此，将创建一个计划采购订单。
5. 买方将添加一个供应商，确认计划采购订单，然后确认该采购订单。
6. 采购的货物到店时，商店操作员将搜索相关采购订单并收货。 因为订单现在已完成，所以可以针对销售订单拣货和为货物打包。
7. 财务将过帐采购发票和销售发票。

下图显示此场景的流程。

![演示场景的流。](./media/use_rsa_tool_14.png)

下图显示该方案在业务流程建模器中的业务流程层次结构。

![演示场景的业务流程。](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a>策略 – 关键学习点

### <a name="data"></a>数据

- 确保您有代表数据卷（生产/黄金配置数据加迁移数据的副本）。
- 通过任务录制器生成新数据时，请创建与现有名称不冲突的测试名称（例如，使用 **RSATxxx** 之类前缀）。
- 使用 Azure 时间点还原在非一级环境中重新运行测试。
- 如果使用 Excel 函数 **RANDOM** 和 **NOW** 生成唯一组合，则工作量非常大。 下面是一个示例。

    ```Excel
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

- 若要在另一个公司中运行测试，可以在 Excel 参数文件的 **常规** 选项卡上更改公司。 确保新选择的公司中有设置和数据。
- 可在 Excel 参数文件的 **常规** 选项卡上更改测试用户。 指定将运行测试用例的用户的电子邮件 ID。 这样，就可以通过使用所指定用户的安全权限运行测试用例。
- 若要在开始测试之前等待，可在 Excel 参数文件的 **常规** 选项卡上定义暂停。 可在批处理作业中使用此暂停（例如，如果必须向运行工作流，才能执行下一个步骤。）

## <a name="advanced-scripting"></a>高级脚本

### <a name="cli"></a>CLI

可以从 **命令提示符** 或 **PowerShell** 窗口调用 RSAT。

> [!NOTE]
> 请验证环境变量 **TestRoot** 是否设置为 RSAT 安装路径。 （在 Microsoft Windows 中，打开 **控制面板**，选择 **系统和安全 \> 系统 \> 高级安全设置**，然后选择 **环境变量**。）

1. 以管理员身份打开 **命令提示符** 或 **PowerShell** 窗口。
2. 浏览至 RSAT 安装目录。

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. 列出所有命令。

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

#### <a name=""></a>?

显示有关所有可用命令及其参数的帮助。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="-optional-parameters"></a>?：可选参数

`command`：其中，``[command]`` 是下面指定的命令之一。

#### <a name="about"></a>关于

显示当前版本。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a>cls

清除屏幕内容。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**

#### <a name="download"></a>download

将指定测试用例的附件下载到输出目录中。
可使用 ``list`` 命令获取所有可用的测试用例。 将第一列的任何值用作 **test_case_id** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="download-required-parameters"></a>download：必需参数

+ `test_case_id`：表示测试用例 ID。
+ `output_dir`：表示输出目录。 该目录必须存在。

##### <a name="download-examples"></a>download：示例

`download 123 c:\temp\rsat`

`download 765 c:\rsat\last`

#### <a name="edit"></a>编辑

允许您在 Excel 程序中打开和编辑参数文件。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="edit-required-parameters"></a>edit：必需参数

+ `excel_file`：必须包含现有 Excel 文件的完整路径。

##### <a name="edit-examples"></a>edit：示例

`edit c:\RSAT\TestCase_123_Base.xlsx`

`edit e:\temp\TestCase_456_Base.xlsx`

#### <a name="generate"></a>generate

在输出目录中为指定的测试用例生成测试执行和参数文件。 可使用 ``list`` 命令获取所有可用的测试用例。 将第一列的任何值用作 **test_case_id** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="generate-required-parameters"></a>generate：必需参数

+ `test_case_id`：表示测试用例 ID。
+ `output_dir`：表示输出目录。 该目录必须存在。

##### <a name="generate-examples"></a>generate：示例

`generate 123 c:\temp\rsat`

`generate 765 c:\rsat\last`

#### <a name="generatederived"></a>generatederived

生成派生自所提供测试用例的新测试用例。 可使用 ``list`` 命令获取所有可用的测试用例。 将第一列的任何值用作 **test_case_id** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="generatederived-required-parameters"></a>generatederived：必需参数

+ `parent_test_case_id`：表示父测试用例 ID。
+ `test_plan_id`：表示测试计划 ID。
+ `test_suite_id`：表示测试套件 ID。

##### <a name="generatederived-examples"></a>generatederived：示例

`generatederived 123 8901 678`

#### <a name="generatetestonly"></a>generatetestonly

在输出目录中为指定的测试用例仅生成测试执行文件。 可使用 ``list`` 命令获取所有可用的测试用例。 将第一列的任何值用作 **test_case_id** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="generatetestonly-required-parameters"></a>generatetestonly：必需参数

+ `test_case_id`：表示测试用例 ID。
+ `output_dir`：表示输出目录。 该目录必须存在。

##### <a name="generatetestonly-examples"></a>generatetestonly：示例

`generatetestonly 123 c:\temp\rsat`

`generatetestonly 765 c:\rsat\last`

#### <a name="generatetestsuite"></a>generatetestsuite

在输出目录中为指定的套件生成所有测试用例。 可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。 将列中的任何值用作 **test_suite_name** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="generatetestsuite-required-parameters"></a>generatetestsuite：必需参数

+ `test_suite_name`：表示测试套件名称。
+ `output_dir`：表示输出目录。 该目录必须存在。

##### <a name="generatetestsuite-examples"></a>generatetestsuite：示例

`generatetestsuite Tests c:\temp\rsat`

`generatetestsuite Purchase c:\rsat\last`

#### <a name="help"></a>help

与 [?](#section) 命令相同。

#### <a name="list"></a>列表

列出所有可用的测试用例。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**

#### <a name="listtestplans"></a>listtestplans

列出所有可用的测试计划。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**

#### <a name="listtestsuite"></a>listtestsuite

列出指定测试套件的测试用例。 可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。 将第一列中的任何值用作 **suite_name** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="listtestsuite-required-parameters"></a>listtestsuite：必需参数

+ `suite_name`：所需套件的名称。

##### <a name="listtestsuite-examples"></a>listtestsuite：示例

`listtestsuite "sample suite name"`

`listtestsuite NameOfTheSuite`

#### <a name="listtestsuitenames"></a>listtestsuitenames

列出所有可用的测试套件。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**

#### <a name="playback"></a>playback

使用 Excel 文件播放测试用例。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="playback-required-parameters"></a>playback：必需参数

+ `excel_file`：Excel 文件的完整路径。 文件必须存在。

##### <a name="playback-examples"></a>playback：示例

`playback c:\RSAT\TestCaseParameters\sample1.xlsx`

`playback e:\temp\test.xlsx`

#### <a name="playbackbyid"></a>playbackbyid

一次播放多个测试用例。 可使用 ``list`` 命令获取所有可用的测试用例。 将第一列的任何值用作 **test_case_id** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="playbackbyid-required-parameters"></a>playbackbyid：必需参数

+ `test_case_id1`：现有测试用例的 ID。
+ `test_case_id2`：现有测试用例的 ID。
+ `test_case_idN`：现有测试用例的 ID。

##### <a name="playbackbyid-examples"></a>playbackbyid：示例

`playbackbyid 878`

`playbackbyid 2345 667 135`

#### <a name="playbackmany"></a>playbackmany

使用 Excel 文件一次播放大量测试用例。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="playbackmany-required-parameters"></a>playbackmany：必需参数

+ `excel_file1`：Excel 文件的完整路径。 文件必须存在。
+ `excel_file2`：Excel 文件的完整路径。 文件必须存在。
+ `excel_fileN`：Excel 文件的完整路径。 文件必须存在。

##### <a name="playbackmany-examples"></a>playbackmany：示例

`playbackmany c:\RSAT\TestCaseParameters\param1.xlsx`

`playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx`

#### <a name="playbacksuite"></a>playbacksuite

播放指定测试套件中的所有测试用例。
可使用 ``listtestsuitenames`` 命令获取所有可用的测试套件。 将第一列中的任何值用作 **suite_name** 参数。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="playbacksuite-required-parameters"></a>playbacksuite：必需参数

+ `suite_name`：所需套件的名称。

##### <a name="playbacksuite-examples"></a>playbacksuite：示例

`playbacksuite suiteName`

`playbacksuite sample_suite`

#### <a name="quit"></a>quit

关闭应用程序。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**

#### <a name="upload"></a>upload

上载属于指定测试套件或测试用例的所有文件。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="upload-required-parameters"></a>upload：必需参数

+ `suite_name`：将上载属于指定测试套件的所有文件。
+ `testcase_id`：将上载属于指定测试用例的所有文件。

##### <a name="upload-examples"></a>upload：示例

`upload sample_suite`

`upload 123`

`upload 123 456`

#### <a name="uploadrecording"></a>uploadrecording

仅上载属于指定测试用例的录制文件。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="uploadrecording-required-parameters"></a>uploadrecording：必需参数

+ `testcase_id`：将仅上载属于指定测试用例的录制文件。

##### <a name="uploadrecording-examples"></a>uploadrecording：示例

`uploadrecording 123`

`uploadrecording 123 456`

#### <a name="usage"></a>usage

显示两种调用此应用程序的方法：一种使用默认设置文件，另一种提供设置文件。

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**

### <a name="windows-powershell-examples"></a>Windows PowerShell 示例

#### <a name="run-a-test-case-in-a-loop"></a>循环运行测试用例

您有一个测试脚本用于创建新客户。 通过脚本，可以在运行每个迭代之前随机化以下数据来运行此测试用例。

- 客户 ID
- 客户名称
- 客户地址

客户 ID 的格式为 *ATCUS\<number\>*，其中，\<number\> 是一个 **000000001** 与 **999999999** 之间的值。

以下示例使用一个参数 **start** 定义使用的第一个数字。 使用第二个参数 **nr** 定义必须创建的客户数量。 对于每个迭代，可使用 UpdateCustomer 函数更改 Excel 参数文件中的参数。 然后，在 RunTestCase 函数中调用 RSAT 命令行。

在管理模式下打开 Microsoft Windows PowerShell 集成脚本环境 (ISE)，然后将以下代码粘贴到名称为 **Untitled1.ps1** 的窗口中。

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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a>在 Microsoft Dynamics 365 中运行依赖数据的脚本

以下示例使用开放数据协议 (OData) 调用查找采购订单的订单状态。 例如，如果状态不是 **已开票**，则可调用 RSAT 测试用例以过帐发票。

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]