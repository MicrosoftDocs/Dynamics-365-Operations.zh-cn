---
title: 周期盘点示例场景
description: 本主题提供了一系列探索 Microsoft Dynamics 365 Supply Chain Management 的周期盘点功能的场景。
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 828954402d223c62f52d7a13fcc9efab84630c80
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261765"
---
# <a name="cycle-counting-example-scenarios"></a>周期盘点示例场景

[!include [banner](../includes/banner.md)]

本主题提供了一系列探索 Microsoft Dynamics 365 Supply Chain Management 的周期盘点功能的场景。 首先，它介绍了现有 Supply Chain Management 环境的要求。 然后，它说明了如何配置周期盘点并介绍了所有周期盘点阶段。 完成后，您应该对周期盘点有很好的了解，包括指导周期盘点、盲目周期盘点、现场周期盘点、周期盘点阈值和周期盘点计划。

## <a name="prerequisites"></a>先决条件

### <a name="make-demo-data-available"></a>提供演示数据

本主题中的每个场景引用为 Supply Chain Management 提供的标准演示数据中包含的值和记录。 如果要在完成场景时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人（公司）设置为 **USMF**。

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a>打开对 Warehouse Management 移动应用的支持

必须先在您的系统中添加对新 Warehouse Management 移动应用的支持，然后才能使用它。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*新仓库应用的用户设置、图标和步骤标题*

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a>为场景准备演示数据

按照以下步骤确认场景所需的所有演示数据在您系统中的 USMF 公司中可用。 创建任何缺失的记录或值。

1. 转到 **仓库管理 \> 设置 \> 工作人员**。
1. 在列表窗格中，选择 **Julia Funderburk**。
1. 在 **用户** 快速选项卡上，选择具有以下值的行。 如果没有现有行具有这些值，则创建它。

    - **用户 ID**：*61*
    - **用户名**：*WH61*
    - **默认仓库**：*61*
    - **菜单名称**：*主*

1. 在 **工作** 快速选项卡上，为用户 *61* 设置以下值（如果尚未设置）：

    - **为周期盘点主管**：*否*
    - **最大百分比限制**：*0*
    - **最大数量限制**：*0*
    - **最大值限制**：*0*

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作池**。
1. 工作池用于基于工作类型划分仓库工作（在这种情况下，为周期盘点工作）。 确保存在具有以下设置的记录：

    - **工作池 ID**：*CycleCount*
    - **描述**：*周期盘点*

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。
1. 在列表窗格中，选择名为 *周期盘点* 的记录。 如果没有现有记录具有此名称，则创建它。 确认或设置记录的以下值：

    - **菜单项名称**：*周期盘点*
    - **标题**：*周期盘点指导*
    - **模式：***工作*
    - **使用现有工作**：*是*
    - **导向方式**：*系统导向*（此值指示 Supply Chain Management 将向工作人员分配周期盘点工作 ID。）
    - **显示库存状态**：*是*

1. 在操作窗格上，选择 **周期盘点**。
1. 在 **移动设备周期盘点** 对话框中，确认或设置以下值：

    - **显示物料编号**：*是*
    - **显示牌照**：*是*
    - **尝试次数**：*1*

1. 选择 **确定** 关闭对话框。
1. 在列表窗格中，选择名为 *周期盘点盲目* 的记录。 如果没有现有记录具有此名称，则创建它。 确认或设置记录的以下值：

    - **菜单项名称**：*周期盘点盲目*
    - **标题**：*周期盘点盲目*
    - **模式：***工作*
    - **使用现有工作**：*是*
    - **导向方式**：*周期盘点分组*（此值指示工作人员可以对特定于库位、区域或工作池的周期盘点工作 ID 进行分组。）

1. 在操作窗格上，选择 **周期盘点**。
1. 在 **移动设备周期盘点** 对话框中，确认或设置以下值：

    - **显示物料编号**：*否*
    - **显示牌照**：*否*
    - **尝试次数**：*0*

1. 选择 **确定** 关闭对话框。
1. 在列表窗格中，选择名为 *现场盘点* 的记录。 如果没有现有记录具有此名称，则创建它。 确认或设置记录的以下值：

    - **菜单项名称**：*现场盘点*
    - **标题**：*现场盘点*
    - **模式：***工作*
    - **使用现有工作**：*否*
    - **工作创建流程**：*现场周期盘点*（此值指示工作人员可以随时盘点一个仓库库位中的物料，而无需创建周期盘点工作。 若要在库位中执行现场周期盘点，工作人员输入库位 ID。）

1. 转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。
1. 在列表窗格中，选择名为 *库存* 的记录。 如果没有现有记录具有此名称，则创建它。 确认以下周期盘点菜单项显示在 **菜单结构** 列中：

    - 周期盘点
    - 周期盘点盲目
    - 现场盘点

1. 转到 **仓库管理 \> 设置 \> 仓库管理参数**。
1. 在 **周期盘点** 选项卡上，设置以下值：

    - **默认周期盘点调整类型**：*周期盘点*（此字段指定完成周期盘点时过帐的日记帐类型。）
    - **默认周期盘点工作类 ID**：*CCount*（此字段指定用于周期盘点的工作类。）
    - **默认周期盘点工作优先级**：*50*（此字段设置周期盘点工作相对于仓库中其他类型工作的优先级。 通过输入小于为其他类型工作输入的数量的数字，提升周期盘点工作的优先级。）

1. 转到 **仓库管理 \> 设置 \> 库存 \> 调整类型**。
1. **调整类型** 页面允许您为可能发生的不同调入和调出创建代码。 确认存在具有以下设置的记录：

    - **库存调整类型**：*周期盘点*
    - **描述**：*周期盘点*
    - **名称**：*ICnt*

1. 转到 **仓库管理 \> 设置 \> 仓库设置 \> 仓库**。
1. 在列表窗格中，选择仓库 *61*。 如果没有现有记录具有此名称，则创建它。
1. 在 **仓库** 快速选项卡上，设置以下值：

    - **使用仓库管理流程**：*是*（此值为仓库管理流程启用仓库。）
    - **允许在周期盘点期间移动牌照**：*是*（此值使工作人员可以在周期盘点期间移动牌照。）

## <a name="scenario-1-guided-cycle-counting"></a>场景 1：指导周期盘点

您必须创建一些工作，才能进行指导周期盘点。 此工作将指导整个仓库中不同库位的分配人员完成在工作中设置的盘点。

### <a name="create-cycle-counting-work-for-scenario-1"></a>为场景 1 创建周期盘点工作

按照以下步骤为仓库 *61* 中的物料库位 *01A02R2S2B* (BULK-06) 创建周期盘点工作。

1. 转到 **仓库管理 \> 周期盘点 \> 按库位分类的周期盘点工作**。
1. 在 **按库位创建周期盘点工作** 对话框中，将 **工作池 ID** 字段设置为 *CycleCount*。
1. 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 在查询编辑器对话框中的 **范围** 选项卡上，按照以下步骤操作：

    - 对于 **字段** 字段设置为 *仓库* 的行，将 **条件** 字段设置为 *61*。
    - 对于 **字段** 字段设置为 *库位* 的行，将 **条件** 字段设置为 *01A02R2S2B*。

1. 选择 **确定** 关闭查询编辑器对话框。
1. 选择 **确定** 以关闭 **按库位创建周期盘点工作** 对话框。

    完成工作创建流程后，操作中心中会显示一条消息。

1. 转到 **仓库管理 \> 工作 \> 工作详细信息**。
1. 通过在 **工作池 ID** 列上设置筛选器以查找值为 *CycleCount* 的记录，找到最新创建的工作。

### <a name="do-cycle-counting-work-for-scenario-1"></a>为场景 1 执行周期盘点工作

创建周期盘点工作后，您通过盘点仓库库位中的物料，然后使用移动设备在 Supply Chain Management 中输入结果来执行工作。 按照以下步骤在 Warehouse Management 移动应用中执行周期盘点工作。

1. 以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。 对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。 （USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）
1. 在主菜单上，选择 **库存**。
1. 在 **库存** 菜单上，选择 **周期盘点指导**。
1. 选择 **数量** 字段，使用数字键盘输入 *9*，然后选择 **确定**（复选标记按钮）。
1. 系统希望您为该物料、库位和牌照输入 10 件的盘点数量。 因此，系统将要求您重新盘点。 选择 **数量** 字段，再次使用数字键盘输入 *9*，然后选择 **确定**（复选标记按钮）。 在第二次尝试时，您的盘点将被接受。

    > [!NOTE]
    > 当系统检测到预期的现有数量与您输入的数量之间存在差异时，它会要求您执行第二次盘点，因为 **周期盘点指导** 移动设备菜单项的 **尝试次数** 字段设置为 *1*。 您将导向到特定物料编号和牌照编号，因为移动设备菜单项的 **显示物料编号** 选项和 **显示牌照** 选项都设置为 *是*。

1. 选择 **确定**（复选标记按钮）。

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a>审查场景 1 的周期盘点差异

按照以下步骤审查周期盘点差异。

1. 返回到 Supply Chain Management。
1. 转到 **仓库管理 \> 工作 \> 工作详细信息**。
1. 查找并选择您之前查看的周期盘点工作。 （例如，在 **工作池 ID** 列上设置筛选器以查找值为 *CycleCount* 的记录。）请注意，此工作的 **工作状态** 字段现在设置为 *待审查*。

    > [!NOTE]
    > 对于用于执行盘点工作的工作用户帐户，**周期盘点主管** 选项设置为 *否*，**最大百分比限制**、**最大数量限制** 和 **最大值限制** 字段都设置为 *0*（零）。 因此，此用户报告的所有盘点差异都必须手动批准，并且相关工作的 **工作状态** 字段设置为 *待审查*。 如果盘点的值在偏差限制范围内（如 **工作用户** 页面上的 **最大百分比限制** 或 **最大数量限制** 字段所指定），或者如果用户的 **周期盘点主管** 选项已设置为 *是*，则工作会自动关闭。

1. 在操作窗格上的 **工作** 选项卡上，选择 **周期盘点**。
1. 在操作窗格上，选择 **接受盘点**。

    使用标准盘点日记帐过帐差异，并创建新的工作订单。

1. 在 **周期盘点交易** 页面上的操作窗格上，选择 **派生工作** 以查找已为批准的差异创建的工作。

## <a name="scenario-2-blind-cycle-counting"></a>场景 2：盲目周期盘点

此场景要求已在您的系统中完成场景 1。

### <a name="create-cycle-counting-work-for-scenario-2"></a>为场景 2 创建周期盘点工作

您必须创建一些工作，才能进行盲目周期盘点。 按照以下步骤为仓库 *61* 中的物料库位 *01A02R2S2B* (BULK-06) 创建周期盘点工作。

1. 转到 **仓库管理 \> 周期盘点 \> 按物料分类的周期盘点工作**。
1. 在 **按物料创建周期盘点工作** 对话框中，将 **工作池 ID** 字段设置为 *CycleCount*。
1. 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的三个行：

    - 行 1：

        - **表：***物料*
        - **字段：***物料编号*
        - **条件：** *L0101*

    - 行 2：

        - **表**：*库存维度*
        - **字段**：*仓库*
        - **条件**：*61*

    - 行 3：

        - **表**：*库存维度*
        - **字段**：*货位*
        - **条件：** *01A02R2S2B*

1. 选择 **确定** 关闭查询编辑器对话框。
1. 选择 **确定** 以关闭 **按物料创建周期盘点工作** 对话框。

    完成工作创建流程后，您将收到一条信息性消息。

### <a name="do-cycle-counting-work-for-scenario-2"></a>为场景 2 执行周期盘点工作

创建周期盘点工作后，按照以下步骤在 Warehouse Management 移动应用中执行工作。

1. 以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。 对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。 （USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）
1. 在主菜单上，选择 **库存**。
1. 在 **库存** 菜单上，选择 **周期盘点盲目**。
1. 选择 **区域 ID** 字段，输入 *BULK06*，然后选择 **确定**（复选标记按钮）。
1. 选择 **物料** 字段，输入 *L0101*，然后选择 **确定**（复选标记按钮）。
1. 选择 **牌照** 字段，输入 *LP\_BULK\_06\_01*，然后选择 **确定**（复选标记按钮）。
1. 选择 **数量** 字段，输入 *10*，然后选择 **确定**（复选标记按钮）。

    > [!NOTE]
    > 即使系统检测到预期的现有数量与您扫描的数量之间存在差异，但它不会要求您执行第二次盘点，因为 **周期盘点盲目** 移动设备菜单项的 **尝试次数** 字段设置为 *0*（零）。 系统要求您扫描物料编号和牌照，因为移动设备菜单项的 **显示物料编号** 选项和 **显示牌照** 选项都设置为 *否*。

1. 选择 **确定**（复选标记按钮）。

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a>审查场景 2 的周期盘点差异

按照以下步骤审查周期盘点差异。

1. 返回到 Supply Chain Management。
1. 转到 **仓库管理 \> 常用 \> 工作 \> 周期盘点工作待审查**。
1. 在操作窗格上的 **工作** 选项卡上，选择 **周期盘点**。
1. 在操作窗格上，选择 **拒绝盘点**。

    由于盘点差异遭拒绝，因此关闭工作。

## <a name="scenario-3-spot-cycle-counting"></a>场景 3：现场周期盘点

现有记录表明物料 *L0101* 在库位 *01A02R2S2B* 有现有数量。 仓库工作人员在库位 *01A02R2S1B* 处。 虽然此库位应该为空，但它已满。 因此，仓库工作人员会立即对该库位进行现场盘点。

### <a name="do-cycle-counting-work-for-scenario-3"></a>为场景 3 执行周期盘点工作

按照以下步骤在 Warehouse Management 移动应用中执行周期盘点工作。

1. 以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。 对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。 （USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）
1. 在主菜单上，选择 **库存**。
1. 在 **库存** 菜单上，选择 **现场盘点**。
1. 选择 **库位** 字段，输入 *01A02R2S1B*，然后选择 **确定**（复选标记按钮）。

    系统检测到在 Supply Chain Management 中该库位为空。

1. 选择 **添加牌照或物料**。
1. 选择 **物料** 字段，输入 *L0101*，然后选择 **确定**（复选标记按钮）。
1. 选择 **牌照** 字段，输入 *LP\_BULK\_06\_01*，然后选择 **确定**（复选标记按钮）。
1. 选择 **数量** 字段，输入 *9*，然后选择 **确定**（复选标记按钮）。

    因为系统检测到指定的牌照已在 Supply Chain Management 中的另一个库位可用，因此该牌照将移动到当前库位。 因此，系统会要求您确认移动。

1. 选择 **确定**（复选标记按钮）。

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a>审查场景 3 的周期盘点差异

按照以下步骤审查盘点结果。

1. 返回到 Supply Chain Management。
1. 转到 **仓库管理 \> 常用 \> 工作详细信息**。
1. 选中网格顶部的 **显示已关闭** 复选框。
1. 将 **工作订单类型** 列的筛选器设置为 *库存移动*。

    系统自动将此盘点检测为库存移动。 允许此移动，因为在 **仓库** 页面上，仓库 *61* 的 **允许在周期盘点期间移动牌照** 选项设置为 *是*。

## <a name="scenario-4-define-cycle-count-thresholds"></a>场景 4：定义周期盘点阈值

创建周期盘点工作的一种方法是使用阈值。 周期盘点阈值指示库存物料的数量或百分比限制。 当达到阈值时，会自动创建周期盘点工作。

例如，一个库位的周期盘点阈值是 40，而物料数量是 60。 在一次销售订单交易期间，有 25 个物料被从该场所领取并被放置在暂放库位。 因为新的物料数量 35 低于临界值，将自动为该库位创建周期盘点工作。

按照以下步骤设置周期盘点阈值。

1. 转到 **仓库管理 \> 设置 \> 周期盘点 \> 周期盘点阈值**。
1. 在操作窗格上，选择 **新建** 创建阈值，并为其设置以下值：

    - **周期盘点阈值 ID**：*L0101*
    - **描述**：*阈值 L0101*
    - **阈值数量**：*2*
    - **单位：** *ea*
    - **基于百分比的产能阈值**：*0.00*
    - **周期盘点阈值类型**：*数量*
    - **立即处理周期盘点**：*是*
    - **周期盘点之间的天数**：*1*
    - **工作池 ID**：*CycleCount*

1. 在操作窗格上，选择 **选择物料**。
1. 在查询编辑器对话框中的 **范围** 选项卡上，找到 **字段** 字段设置为 *物料编号* 的行。 将该行的 **条件** 字段设置为 *L0101*。
1. 选择 **确定** 关闭查询编辑器对话框。

    现在，您已为物料 *L0101* 定义了周期盘点阈值。

现在，如果现有数量小于 2，并且如果任何库位的最后一个周期盘点的日期不是今天，将在该库位为物料 *L0101* 创建周期盘点。

## <a name="scenario-5-define-cycle-count-plans"></a>场景 5：定义周期盘点计划

周期盘点计划可让您自动创建周期盘点工作。 您可以使用特定的物料和库位查询来设置每个周期盘点计划。 当批处理作业运行时，它将为所有与物料和库位条件匹配的库位（最多为计划指定的最大盘点数）创建周期盘点工作。 当创建周期盘点工作时，盘点工作行包含有关必须盘点的库位的信息。 与该库位关联的现有库存不会受阻止。 因此，即使存在未结盘点工作，它也可用于预留和出站处理。

按照以下步骤设置周期盘点计划。

1. 转到 **仓库管理 \> 设置 \> 周期盘点 \> 周期盘点计划**。
1. 在操作窗格上，选择 **新建** 以向网格添加一行，然后为其设置以下值：

    - **周期盘点计划 ID**：*BULK06*
    - **描述**：*BULK06 的库位盘点*
    - **工作池 ID**：*CycleCount*
    - **周期盘点的最大数量**：*10*
    - **周期盘点之间的天数**：*10*
    - **空库位**：*排除空库位*
    - **工作模板**：将此字段保留为空。

1. 在操作窗格上，选择 **选择库位**。
1. 将显示标准查询编辑器对话框。 在 **范围** 选项卡上，添加一行，然后为其设置以下值：

    - **表：** *位置*
    - **字段：** *区域 ID*
    - **条件：** *BULK06*

1. 选择 **确定** 关闭查询编辑器对话框。
1. 在操作窗格上，选择 **处理周期盘点计划**。
1. 在 **周期盘点计划** 对话框中，在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。
1. 选择 **定期**。
1. 在 **定义定期** 对话框中，设置批处理作业，以便它立即开始，每分钟运行一次，并且没有结束日期。
1. 选择 **确定** 以关闭 **定义定期** 对话框。
1. 选择 **确定** 以关闭 **周期盘点计划** 对话框。

    将显示一条消息，通知您作业已添加到批处理队列。

1. 转到 **仓库管理 \> 常用 \> 周期盘点计划**。 该计划立即开始并创建盘点工作。 由于盘点工作尚未完成，因此 **状态** 字段设置为 *进行中*。 一分钟后，**总周期盘点** 列中的值更改为 *1*。

    > [!NOTE]
    > 如果自上次周期盘点以来的天数小于您为周期盘点计划的 **周期盘点之间的天数** 字段设置的值，将不会创建周期盘点工作。 例如，如果 **周期盘点之间的天数** 字段设置为 *5*，则周期盘点工作每五天创建一次。 但是，如果在第三天处理周期盘点工作，则下一个周期盘点工作将在处理完最后的周期盘点之后的第五天被创建，即第八天。

1. 在操作窗格上，选择 **工作** 以查看创建的盘点工作。