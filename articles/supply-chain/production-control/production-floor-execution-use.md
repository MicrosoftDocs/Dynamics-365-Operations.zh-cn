---
title: 工作人员如何使用生产车间执行界面
description: 本文从工作人员的角度介绍了如何使用生产车间执行界面。
author: johanhoffmann
ms.date: 01/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgProductionFloorExecution
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 876ee36c75a31ca89a9351d0ee1484e66076b6aa
ms.sourcegitcommit: 4abf9b375fed6885ea11a425c524958fea29c3b9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748705"
---
# <a name="how-workers-use-the-production-floor-execution-interface"></a>工作人员如何使用生产车间执行界面

[!include [banner](../includes/banner.md)]

生产车间执行界面针对触摸交互进行了优化。 它的设计提供了视觉对比，可以满足车间环境的可访问性要求。 它提供与作业卡设备相同的所有功能。 但是，它还允许从作业列表中并行启动多个作业。 （此功能也称为 *作业捆绑*。）此外，从作业列表中，工作人员可以打开在 Microsoft Dynamics 365 指南中创建的指南。 通过此方法，他们可以在 HoloLens 上获取视觉说明。

## <a name="sign-in-to-the-production-floor-execution-interface-as-a-worker"></a>以工作人员身份登录生产车间执行界面

在工作人员可以开始使用该设备之前，主管或技术人员必须准备该设备并在 Dynamics 365 Supply Chain Management 中打开正确的页面。 有关如何设置设备的详细信息，请参阅[设置设备以运行生产车间执行界面](production-floor-execution-setup.md)。

准备好设备后，设备上将显示登录页面。 此页面显示有关本地工作单元的作业状态的信息。 此信息会定期更新。 在该页面上，工作人员使用其锁屏提醒 ID 进行登录。 尽管工作人员不必具有 Supply Chain Management 的用户帐户，但他们必须具有可在登录时使用的 *时间登记工作人员* 帐户。

![生产车间执行界面登录页面。](media/pfei-sign-in-page.png "生产车间执行界面登录页面")

本文的其余各节介绍了工作人员如何与界面进行交互。

## <a name="all-jobs-tab"></a>所有作业选项卡

**所有作业** 选项卡提供了一个作业列表，显示状态为 *未开始*、*已停止* 或 *已开始* 的所有生产作业。 （此选项卡名称可以自定义，在您的系统中可能不同。）

![所有作业选项卡。](media/pfei-all-jobs-tab.png "所有作业选项卡")

作业列表具有以下列。 数字对应上一图中的数字。

1. **选择列** – 最左边的列使用复选标记指示工作人员已选择的作业。 工作人员可以同时在列表中选择多个作业。 若要在列表中选择所有作业，请选择列标题中的复选标记。 选择单个作业后，有关该作业的详细信息将显示在页面的下部。
1. **作业状态列** – 此列使用符号指示每个作业的状态。 此列中没有符号的作业的状态为 *未开始*。 绿色三角形指示状态为 *已开始*。 两个黄色竖线指示状态为 *已停止* 的作业。
1. **高优先级列** – 此列使用感叹号指示具有高优先级的作业。
1. **订单** – 此列显示作业的生产订单编号。
1. **描述** – 此列显示作业所属的工序的描述。
1. **已请求** – 此列显示作业计划生产的数量。
1. **已开始** – 此列显示作业已开始的数量。
1. **已完成** – 此列显示作业已完成的数量。
1. **已报废** – 此列显示作业已报废的数量。
1. **剩余** – 此列显示作业剩余完成的数量。

## <a name="active-jobs-tab"></a>活动作业选项卡

**活动作业** 选项卡显示登录工作人员已经开始的所有作业的列表。 （此选项卡名称可以自定义，在您的系统中可能不同。）

![活动作业选项卡。](media/pfei-active-jobs-tab.png "活动作业选项卡")

活动作业列表具有以下列：

- **选择列** – 最左边的列使用复选标记指示工作人员已选择的作业。 工作人员可以同时在列表中选择多个作业。 若要在列表中选择所有作业，请选择列标题中的复选标记。 选择单个作业后，有关该作业的详细信息将显示在页面的下部。
- **订单** – 此列显示作业的生产订单编号。
- **描述** – 此列显示作业所属的工序的描述。
- **已请求** – 此列显示作业计划生产的数量。
- **已开始** – 此列显示作业已开始的数量。
- **已完成** – 此列显示作业已完成的数量。
- **已报废** – 此列显示作业已报废的数量。
- **剩余** – 此列显示作业剩余完成的数量。

## <a name="my-jobs-tab"></a>“我的作业”选项卡

**我的作业** 选项卡让工作人员可以轻松查看专门分配给他们的所有未开始和未完成的作业。 在有时或总是将工作分配给特定工作人员（人工资源）而不是其他类型的资源（如机器）的公司中，它很有用。

计划系统会自动将每个生产作业分配给特定的资源记录，每个资源记录都有一个类型（如机器或人）。 当您将员工设置为生产工作人员时，您可以将工作人员帐户与唯一的人工资源记录相关联。

**我的作业** 选项卡会列出已分配给已登录工作人员的人工资源记录的所有未开始和未完成的作业（如果有工作人员已登录）。 它永远不会列出已分配给机器或其他类型资源的作业，即使已登录的工作人员已开始处理这些作业。

要查看已由已登录工作人员开始的所有作业，不论每个作业所分配的资源类型如何，使用 **活动作业** 选项卡。要查看与本地作业筛选器的配置匹配的所有未完成的作业，无论工作人员或开始状态如何，使用 **所有作业** 选项卡。

![“我的作业”选项卡。](media/pfei-my-jobs-tab.png "“我的作业”选项卡")

## <a name="my-machine-tab"></a>“我的机器”选项卡

**我的机器** 选项卡让工作人员可以在 **所有作业** 选项卡上设置的筛选器中选择连接到机器资源的资产。然后，工作人员可以通过读取最多四个所选计数器的值以及最近的维护请求和登记的停机时间列表来查看所选资产的状态和运行状况。 工作人员还可以请求对所选资产进行维护，并登记和编辑机器停机时间。 （此选项卡名称可以自定义，在您的系统中可能不同。）

![“我的机器”选项卡。](media/pfei-my-machine-tab.png "“我的机器”选项卡")

**我的机器** 选项卡包含以下列。 数字对应上一图中的数字。

1. **机器资产** – 选择要跟踪的机器资产。开始键入名称来从匹配资产的列表中选择，或选择放大镜图标从与作业列表的筛选器内与资源关联的所有资产的列表中选择。

    > [!NOTE]
    > Supply Chain Management 用户可以使用 **所有资产** 页（在 **固定资产** 选项卡上，使用 **资源** 下拉列表）为每个资产分配资源。 有关详细信息，请参阅[创建资产](../asset-management/objects/create-an-object.md)。

1. **设置** – 选择齿轮图标打开一个对话框，您可以在其中选择要查看所选机器资产的计数器。 这些计数器的值显示在 **资产管理** 选项卡的顶部。**设置** 菜单（如以下屏幕截图所示）让您最多可以启用四个计数器。 对于要启用的每个计数器，请使用磁贴顶部的查找字段来选择计数器。 查找字段在 **资产管理** 页顶部列出与所选资产相关的所有计数器。 设置每个计数器来监视计数器的 **聚合** 值或最新的 **实际** 值。 例如，如果您设置一个计数器来跟踪机器运行了几个小时，则应将其设置为 **聚合**。 如果设置计数器来测量最新更新的温度或压力，则应将其设置为 **实际**。 选择 **确定** 保存设置并关闭对话框。

    ![“我的机器”选项卡设置。](media/pfei-my-machine-tab-settings.png "“我的机器”选项卡设置")

1. **请求维护** – 选择此按钮将打开一个对话框，您可以在其中创建维护请求。 您可以提供描述和注释。 请求将引起 Supply Chain Management 用户的注意，然后用户可以将维护请求转换为维护工作订单。
1. **登记停机时间** – 选择此按钮将打开一个对话框，您可以在其中登记机器停机时间。 您可以选择原因码并输入停机时间的日期/时间跨度。 机器停机时间登记用于计算机器资产的效率。
1. **查看或编辑** – 选择此按钮将打开一个对话框，您可以在其中编辑或查看现有停机时间记录。

## <a name="starting-and-completing-production-jobs"></a>开始和完成生产作业

工作人员通过在 **所有作业** 选项卡上选择作业，然后选择 **开始作业** 以打开 **开始作业** 对话框来开始生产作业。

![开始作业对话框。](media/pfei-start-job-dialog.png "开始作业对话框")

工作人员使用 **开始作业** 对话框确认生产数量，然后开始作业。 工作人员可以通过选择 **数量** 字段，然后使用出现的数字键盘来调整数量。 然后，工作人员选择 **开始** 以开始处理作业。 **开始作业** 对话框将关闭，作业将添加到 **活动作业** 选项卡。

工作人员可以开始处于任何状态的作业。 当工作人员开始状态为 *未开始* 的作业时，**开始作业** 对话框中的 **数量** 字段最初显示完整数量。 当工作人员开始状态为 *已开始* 或 *已停止* 的作业时，**数量** 字段最初显示剩余数量。

## <a name="reporting-good-quantities"></a>报告完好数量

当工作人员完成或部分完成作业时，他们可以通过在 **活动作业** 选项卡上选择作业，然后选择 **报告进度** 来报告已生产的完好数量。 然后，在 **报告进度** 对话框中，工作人员使用数字键盘输入完好数量。 默认情况下，该数量为空白。 输入数量后，工作人员可以将作业状态更新为 *进行中*、*已停止* 或 *已完成*。

![报表进度对话框。](media/pfei-report-progress-dialog.png "报告进度对话框")

## <a name="reporting-good-quantities-on-batch-orders-that-have-co-products-and-by-products"></a>报告具有联产品和副产品的批次订单的完好数量

工作人员可以使用生产车间执行界面报告批次订单的进度。 此报告包括联产品和副产品报告。

有些制造商，尤其是加工行业的制造商，使用批次订单来管理他们的生产流程。 批次订单根据配方创建，这些配方可以定义为将联产品和副产品作为输出。 报告有关这些批次订单的反馈后，必须在配方物料上以及联产品和副产品上登记输出金额。

当工作人员完成或部分完成批次订单上的作业时，他们可以报告定义为订单输出的每个产品的完好或报废数量。 定义为批次订单输出的产品可以是 *配方*、*联产品* 或 *副产品* 类型。

要报告产品的完好数量，工作人员在 **活动作业** 选项卡上选择一个作业，然后选择 **报告进度**。

然后，在 **报告进度** 对话框中，工作人员可以在定义为要报告的批次订单输出的产品中进行选择。 工作人员可以在列表中选择一个或多个产品，然后选择 **报告进度**。 对于每个产品，默认情况下数量为空，工作人员可以使用数字键盘输入数量。 工作人员可以使用 **上一个** 和 **下一个** 按钮在所选产品之间移动。 为每个产品输入数量后，工作人员可以将作业状态更新为 *进行中*、*已停止* 或 *已完成*。

![报告联产品和副产品。](media/report-co-by-products.png "报告联产品和副产品")

### <a name="reporting-on-batch-orders-for-planning-items"></a>报告计划物料的批次订单

当工作人员完成计划物料的批次订单的作业时，他们将仅报告联产品和副产品的数量，因为计划物料不包含 *配方* 类型的物料。

### <a name="reporting-co-product-variation"></a>报告联产品变体

如果从 **联产品变体** 选项设置为 *是* 的配方版本创建批次订单，工作人员可以报告不属于批次订单定义一部分的联产品。 此功能用于生产流程中可能发生意外产品输出的场景。

在这种情况下，工作人员可以通过在报表进度对话框中选择 **联产品变体** 来指定要报告的联产品和数量。 然后，工作人员可以在定义为联产品的所有已发布产品中进行选择。

### <a name="reporting-catch-weight-items"></a>报告实际称重物料

工作人员可以使用生产车间执行界面报告为实际称重物料创建的批次订单的进度。 批次订单是从配方创建的，配方可以定义为将实际称重物料作为配方物料、联产品和副产品。 另外还可以定义一个配方，使其具有针对实际称重定义的成分的配方行。 实际称重物料使用两种度量单位来跟踪库存：实际称重数量和库存数量。 例如，在食品行业，可以将盒装肉定义为一个实际称重物料，其中实际称重数量用于跟踪盒数，库存数量用于跟踪盒重量。

## <a name="reporting-scrap"></a>报告废料

当工作人员完成或部分完成作业时，他们可以通过在 **活动作业** 选项卡上选择作业，然后选择 **报告废料** 来报告废料。 然后，在 **报告废料** 对话框中，工作人员使用数字键盘输入废料数量。 工作人员还将选择原因（*无*、*机器*、*操作员* 或 *材料*）。

![报表废料对话框。](media/pfei-report-scrap-dialog.png "报告废料对话框")

## <a name="adjust-material-consumption-and-make-material-reservations"></a>调整物料消耗量并进行物料预留

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

工作人员可以调整每个生产作业的物料消耗量。 此功能用于生产作业消耗的实际物料数量大于或小于计划数量的场景。 因此，必须对其进行调整以保持最新的库存水平。

工作人员还可以对物料的批处理和序列号进行预留。 此功能用于工作人员必须手动指定已消耗的物料批处理或序列号以满足物料可追溯性要求的场景。

工作人员可以通过选择 **调整物料** 来指定要调整的数量。 此按钮在以下位置可用：

- 在 **报告废料** 对话框中
- 在 **报告进度** 对话框中
- 在右侧的工具栏上

### <a name="adjust-material-consumption-from-the-report-scrap-and-report-progress-dialog-boxes"></a>从“报告废料”和“报告进度”对话框调整物料消耗

工作人员在 **报告进度** 或 **报告废料** 对话框中输入要报告的数量后，**调整物料** 按钮将可用。 当用户选择此按钮时，将显示 **调整物料** 对话框。 此对话框将在报告作业的完好或报废数量时列出计划消耗的物料。

此对话框中的列表显示以下信息：

- **产品编号** – 基础产品和产品变型。
- **产品名称** – 产品的名称。
- **建议量** – 在报告作业的指定数量的进度或废料时将消耗的估计物料数量。
- **消耗量** – 在报告作业的指定数量的进度或废料时将消耗的实际物料数量。
- **已预留** – 已在库存中实际预留的物料数量。
- **单位** – 物料清单 (BOM) 单位。

对话框右侧显示以下信息：

- **产品编号** – 基础产品和产品变型。
- **估计** – 估计消耗的数量。
- **已开始** – 生产作业中已开始的数量。
- **剩余数量** – 在估计数量中，剩余的待消耗的数量。
- **已发放数量** – 已消耗的数量。

可以执行以下操作：

- 工作人员可以通过选择 **调整消耗** 指定要针对物料调整的数量。 数量确认后，**消耗量** 列中的数量会更新为调整后的数量。
- 当工作人员选择 **调整材料** 时，将创建生产领料单日记帐。 此日记帐包含与 **调整物料** 列表相同的物料和数量。
- 当工作人员在 **调整物料** 对话框中调整数量时，相应日记帐行上的 **建议量** 字段将更新为相同数量。 如果工作人员在 **调整物料** 对话框中选择 **取消**，领料单将被删除。
- 如果工作人员选择 **确定**，领料单将不会被删除。 它会在 **报告废料** 或 **报告进度** 对话框中报告作业时进行过帐。
- 如果工作人员在 **报告进度** 或 **报告废料** 对话框中选择 **取消**，领料单将被删除。

### <a name="adjust-material-from-the-primary-or-secondary-toolbar"></a>调整主工具栏或辅助工具栏中的材料

**调整物料** 按钮可以配置为显示在主工具栏或辅助工具栏上。 （有关详细信息，请参阅 [设计生产车间执行界面](production-floor-execution-tabs.md)。）工作人员可以为正在进行的生产作业选择 **调整物料**。 在这种情况下，将出现 **调整物料** 对话框，工作人员可以在其中进行所需的调整。 对话框打开后，将为生产订单创建包含调整后数量的行的生产领料单。 如果工人选择 **立即过帐**，调整将被确认，领料单将过帐。 如果工人选择 **取消**，领料单将被删除，不做任何调整。

### <a name="adjust-material-consumption-for-catch-weight-items"></a>调整实际称重物料的物料消耗量

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]
<!-- KFM: preview until further notice -->

可以调整实际称重物料的物料消耗量的工作人员。 此功能用于生产作业消耗的实际称重物料的实际数量大于或小于计划数量的场景。 因此，必须对其进行调整以保持最新的库存水平。 当工作人员调整实际称重物料的消耗量时，他们可以调整实际称重数量和库存数量。 例如，如果一项生产作业计划消耗五个估计每箱重量为 2 公斤的箱子，工作人员可以同时调整要消耗的箱子数量和箱子的重量。 系统将验证箱子的指定重量是否在已发布产品上定义的最小和最大阈值范围内。

### <a name="reserve-materials"></a>预留物料

在 **调整物料** 对话框中，工作人员可以通过选择 **预留物料** 来进行物料预留并进行调整。 出现的 **预留物料** 对话框显示每个存储和跟踪维度的物料的实际可用库存。

如果为仓库管理流程 (WMS) 启用了物料，列表将仅显示物料的生产输入位置的实际可用库存。 生产输入位置在计划生产作业的资源上定义。 如果物料编号受批处理或序列号控制，将显示实际可用的批处理和序列号的完整列表。 要指定要预留的数量，工作人员可以选择 **预留物料**。 要删除现有预留，工作人员可以选择 **删除预留**。

有关如何设置生产输入位置的详细信息，请参阅以下博客文章：[设置生产输入位置](/archive/blogs/axmfg/deliver-picked-materials-to-the-locations-where-the-materials-are-consumed-by-operations-in-production)。

> [!NOTE]
> 工作人员在 **预留物料** 对话框中进行的预留，在工作人员在 **报告进度** 或 **报告废料** 对话框中选择 **取消** 时仍会保留。
>
> 无法调整实际称重物料的预留。

## <a name="completing-a-job-and-starting-a-new-job"></a>完成作业并开始新作业

通常，工作人员通过在 **活动作业** 选项卡上选择一个或多个当前作业，然后选择 **报告进度** 来完成作业。 然后，他们输入已生产的数量（完好数量）并将状态设置为 *完成*。 如果选择了多个作业，则工作人员将使用 **上一个** 和 **下一个** 按钮来进行切换。 若要开始新作业，工作人员在 **所有作业** 选项卡上选择它，然后选择 **开始作业**。

工作人员也可以在上一个作业仍处于打开状态时开始新作业。 同样，工作人员在 **所有作业** 选项卡上选择新作业，然后选择 **开始作业**。 但是，在这种情况下，**开始作业** 对话框将通知工作人员他们当前正在处理一个作业，因此他们必须在开始新作业之前停止或完成该作业。

## <a name="working-on-multiple-jobs-in-parallel"></a>并行处理多个作业

一个工作人员可以同时（即并行）处理多个作业。 在这种情况下，该工作人员正在处理的作业集称为 *作业捆绑*。 工作人员可以将新作业添加到捆绑中，或完成捆绑中的一个或多个作业。 以下两种场景显示了工作人员如何并行处理作业。

### <a name="scenario-1-a-worker-who-has-no-active-jobs-wants-to-start-two-jobs-and-work-on-them-in-parallel"></a>场景 1：没有活动作业的工作人员想要开始两个作业并且并行处理它们

工作人员在 **所有作业** 选项卡上选择两个作业，然后选择 **开始作业**。 **开始作业** 对话框显示这两个选定的作业，工作人员可以在每个作业上调整要开始的数量。 然后，工作人员确认对话框并可以开始这两个作业。

### <a name="scenario-2-a-worker-who-has-two-active-jobs-that-are-in-progress-wants-to-start-a-third-job-and-work-on-it-in-parallel-with-the-other-two"></a>场景 2：有两个正在进行的活动作业的工作人员想要开始第三个作业并且与其他两个作业并行处理它

工作人员在 **所有作业** 选项卡上选择第三个作业，然后选择 **捆绑**。 在 **捆绑** 对话框中，工作人员可以调整要开始的数量。 然后，工作人员通过选择 **捆绑** 确认对话框。

## <a name="working-on-indirect-activities"></a>处理间接活动

间接活动是与生产订单不直接相关的活动。 间接活动可以灵活定义，如[设置考勤管理的间接活动](/dynamicsax-2012/appuser-itpro/set-up-indirect-activities-for-time-and-attendance)中所述。

例如，Contoso 的车间工作人员 Shannon 想要参加公司会议，而会议被认为是间接活动。 以下两种场景之一适用：

- **Shannon 正在处理一个或多个活动作业。** Shannon 选择 **活动**，确定活动（会议）并确认她的选择。 显示的消息通知她，她有正在进行的作业。 从该消息中，Shannon 可以选择在参加会议之前完成或停止她正在处理的作业。
- **Shannon 没有任何活动作业。** Shannon 选择 **活动**，确定活动（会议），确认她的选择。 现在，她已登记参加会议。

在这两种场景下，在 Shannon 确认选择后，她都会进入登录页面或等待她确认已从间接活动中返回的页面。 显示的页面取决于生产车间执行界面的配置。 （有关详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。）

## <a name="registering-breaks"></a>登记工间休息

工作人员可以登记工间休息。 工间休息可以灵活定义，如[基于登记付薪](pay-based-on-registrations.md)中所述。

工作人员通过选择 **工间休息**，然后选择表示工间休息类型（例如午餐）的卡片来登记工间休息。 在工作人员确认选择后，设备将显示登录页面或等待工作人员确认他们已从工间休息返回的页面。 显示的页面取决于生产车间执行界面的配置。 （有关详细信息，请参阅[配置生产车间执行界面](production-floor-execution-configure.md)。）

## <a name="view-the-my-day-dialog"></a>查看“我的一天”对话框

**我的一天** 对话框为工作人员提供了登记和余额的概览。 此对话框分为以下三个部分：

- 主部分列出当前工作人员在所选日期进行的登记。 它将打开并显示当天的登记，还会提供一个日期选取器，使工作人员可以查看其他天。
- **上次计算的每日余额** 部分显示工作人员的带薪时间、带薪加班、缺勤和带薪缺勤的当前余额。 这些值基于审核过程中计算的登记。
- **余额** 部分概述了所选登记类别（如休假、标准时间和加班）的定义期间内的余额。 这些余额基于在 **考勤管理** 模块中设置统计余额的方式。 有关其设置方式的详细信息，请参阅[在生产车间执行界面中显示休假余额](production-floor-execution-payroll-stats.md)。

管理员可以将 **我的一天** 按钮放在每个相关选项卡的工具栏上，从而将此功能添加到界面，如[设计生产车间执行界面中所述](production-floor-execution-tabs.md)。

## <a name="working-in-teams"></a>在团队中工作

在将多个工作人员分配到同一个生产作业时，他们可以组成一个团队。 团队可以指定一个工作人员作为指导员。 那么剩下的工作人员会自动成为该指导员的助手。 对于所生成的团队，只有指导员必须登记作业状态。 时间记录适用于所有团队成员。

### <a name="prerequisites"></a>先决条件

若要使用团队，管理员必须在生产车间执行界面的 **所有作业** 选项卡上针对主要工具栏启用 **助手** 操作。 有关说明，请参阅[设计生产车间执行界面](production-floor-execution-tabs.md)。

### <a name="form-a-new-team-that-has-a-pilot-and-an-assistant"></a>组成一个具有指导员和助手的新团队

工作人员可以在 **所有作业** 选项卡上选择 **助手** 来登记为助手。然后，在显示的 **选择要提供帮助的员工** 对话框中，工作人员可以在积极从事工作的工作人员列表中选择指导员。 在工作人员确认其选择后，他们将成为所选工作人员的助手，所选工作人员会成为新团队的指导员。

### <a name="assign-a-new-pilot-to-an-existing-team"></a>将新指导员分配到现有团队

当团队想要选择新指导员时，当前指导员必须指定团队中的另一名工作人员作为新指导员。 要指定新指导员，当前指导员应在 **所有作业** 选项卡上选择 **助手**。然后，在显示的 **更改指导员** 对话框中，指导员可以在已在团队中的工作人员列表中选择新的指导员。 在当前指导员确认其选择后，他们将完全从团队中删除。 但是，他们可以根据需要重新加入团队。

### <a name="assistant-clocks-out"></a>助手下班打卡

当一名担任助手的工作人员下班打卡时，他们就会离开团队。 如果 **永久团队** 和 **在上班打卡时重新启动** 选项设置为 *是*，则下班打卡的工作人员将在下次上班打卡时自动重新加入团队。 您可以在 **考勤管理参数** 页面的 **常规** 选项卡上找到这些选项。

## <a name="opening-instructions"></a>打开说明

工作人员可以通过选择 **说明** 打开附加到作业的文档。 仅在文档与主数据中的作业相关联时，**说明** 按钮才可用。 例如，将为工作人员提供附加到 Supply Chain Management 中 **已发布产品** 页面上的产品的文档，以在工作车间执行界面中打开。

## <a name="opening-mixed-reality-guides-for-hololens"></a>打开 HoloLens 的混合现实指南

[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) 可以通过提供使用混合现实的实践学习来帮助工作人员执行作业。 您可以定义通过分步说明指导工作人员使用他们所需的工具和零件的标准化流程，并展示如何在实际工作中使用这些工具。 下面是流程的概述。

1. 每当工作人员在车间执行界面中打开作业列表时，该界面将为显示的作业找到所有相关的指南。
1. 工作人员选择 **指南** 以查看指南列表。
1. 工作人员在列表中选择相关的指南。
1. 车间执行界面显示所选指南的 QR 码。
1. 工作人员使用 HoloLens 并浏览 QR 码以开始使用指南。
1. 工作人员通过指南工作以了解任务。

有关如何创建、分配和使用 HoloLens 指南的详细信息，请参阅[为生产中的工作人员提供混合现实指南](instruction-guides-in-production-overview.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
