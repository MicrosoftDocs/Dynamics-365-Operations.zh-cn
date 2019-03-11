---
title: 周期盘点
description: 本文介绍如何使用仓库管理中提供的仓库解决方案使用周期盘点。 本文不适用于可用于库存管理的仓库解决方案。
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a76082a7aa375424e6f118744e2f63600a8cbda
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "323218"
---
# <a name="cycle-counting"></a>周期盘点

[!include [banner](../includes/banner.md)]

本文介绍如何使用仓库管理中提供的仓库解决方案使用周期盘点。 本文不适用于可用于库存管理的仓库解决方案。

周期盘点是用于审计现有库存项目的仓库流程。 周期盘点流程可以在三个步骤中介绍：

1.  **创建周期盘点工作** – 周期盘点工作可以是基于物料的临界值参数或通过周期盘点计划自动创建的。 或者，您可以通过在**按物料分类的周期盘点工作**页面或**按位置分类的周期盘点工作**页面中使用物料或仓库参数手动创建周期盘点计数工作。
2.  **处理周期盘点** – 在创建周期盘点工作之后，您通过盘点仓库库位的物料执行周期盘点，然后使用移动设备将结果输入到 Microsoft Dynamics 365 for Finance and Operations 中。 或者，您可以在不创建周期盘点的情况下在仓库场所盘点物料。 此过程被称为*现场周期盘点*。
3.  **解决周期盘点值中的差异** – 周期盘点之后，与盘点值有差异的任何物料必须在**所有工作**页中设定为**待核查**的工作状态。 您可以在**周期盘点工作待审阅**页上解决这些差异。

下图显示了周期盘点流程。 ![周期盘点流程](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>周期盘点先决条件
下表显示必须先就绪然后才能开始使用周期盘点。
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>先决条件</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>物料</td>
<td>物料必须在仓库管理流程中启用。</td>
</tr>
<tr class="even">
<td>仓库</td>
<td>仓库必须在仓库管理流程中启用。 要在仓库管理流程中启用仓库，请在<strong>仓库</strong>页中，选择仓库，然后选中<strong>使用仓库管理流程</strong>选项。 若要在周期盘点期间使工作人员能够移动栈板，在<strong>仓库管理</strong>快速选项卡上，选中<strong>允许在周期盘点期间移动托盘</strong>选项。</td>
</tr>
<tr class="odd">
<td>工作池</td>
<td>可选：基于工作类型创建工作池来划分仓库工作（在这种情况下，周期盘点执行）。</td>
</tr>
<tr class="even">
<td>位置</td>
<td>在场所中启用周期盘点。 若要为仓库库位启用周期盘点，在<strong>位置配置文件</strong>页中，选择<strong>允许周期盘点</strong>选项。</td>
</tr>
<tr class="odd">
<td>仓库管理参数</td>
<td>为周期盘点设置参数。 在<strong>仓库管理参数</strong>页中，为周期盘点指定默认调整类型代码、工作类 ID 和工作优先级。</td>
</tr>
<tr class="even">
<td>移动设备</td>
<td><ul>
<li>为<strong>移动设备菜单项</strong>页中以下方法中的一个创建一个菜单项：
<ul>
<li>用户指导的周期盘点</li>
<li>系统指导的周期盘点</li>
<li>周期盘点分组</li>
<li>现货周期盘点</li>
</ul>
</li>
<li>设置移动设备的菜单。</li>
<li>创建一个工作用户帐户并向工作用户 ID 分配一个移动设备菜单。</li>
</ul></td>
</tr>
<tr class="odd">
<td>相关设置任务</td>
<td>为一个仓库场所设置一个周期盘点计划</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>自动创建周期盘点工作
有两种方法可以计划工作周期工作的重复创建：设置周期盘点阈值或设置周期盘点计划。

-   周期盘点阈值指示库存物料的数量或百分比限制。 当达到周期盘点阈值时，会自动创建周期盘点工作。
-   周期盘点计划通过批处理作业立即或定期创建周期盘点工作。 当创建周期盘点工作时，盘点工作行包含有关要盘点的库位的信息。 不会锁定与此位置相关联的现有库存，因此它可用于预留和传出处理，即使存在未结的盘点工作。

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>基于物料临界值参数创建周期盘点工作

当物料数量减少至低于库位中某个特定的临界值，可以创建周期盘点工作。 例如，当一个库位的周期盘点临界数量是 40，而物料数量为 60。 在一次销售订单交易期间，有 25 个物料被从该场所领取并被放置在暂放库位。 因为新的物料数量 35 低于临界值，将自动为该库位创建周期盘点工作。

### <a name="schedule-cycle-counting-work"></a>计划周期盘点工作

您可以计划周期盘点计划以立即或定期创建周期盘点工作。 通过设置周期盘点计划，您可以控制为其创建周期盘点工作的工作池，为不同库位的物料创建的周期盘点的最大数，以及仓库库位再次盘点前的天数。 例如，物料可在仓库中的三个库位可用；并且，周期盘点的最大数设置为 **2**。 在这种情况下，在您运行周期盘点计划时，会为存放物料的两个库位创建两个周期盘点。 作为另一个示例，您将周期盘点之间的天数设置为 **5**。 在这种情况下，周期盘点工作每五天创建一次。 但是，如果在第三天处理周期盘点工作，则下一个周期盘点工作将在处理完最后的周期盘点之后的第五天被创建，即第八天。

## <a name="create-cycle-counting-work-manually"></a>手动创建周期工作
若要手动创建周期盘点工作，则可以使用 **按物料分类的周期盘点工作**或**按位置分类的周期盘点工作**页。 您可以指定创建的周期盘点的最大数量。 例如，如果仓库经理指定该值为 **5**，那么将为五个场所创建周期盘点工作，即使该物料存放于 10 个不同的场所。 您还可以选择一个将所创建的周期盘点工作 ID 分配至的工作池 ID。 当一个工作池 ID 被处理用于周期盘点，分配至此工作池的周期盘点工作 ID 被处理为一个组。

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>使用移动设备执行周期盘点
使用移动设备上的 Finance and Operations 可以有几种方法处理周期盘点工作：

-   **用户导向** – 工作人员可以指定处于**未结**状态的周期盘点工作 ID。
-   **系统导向** – Finance and Operations 分配一个周期盘点工作 ID 给工作人员。
-   **周期盘点分组** – 工作人员可以对特定场所、地带或工作池的特定的周期盘点工作 ID 进行分组。
-   **现场周期盘点** – 工作人员可以随时盘点一个仓库库位中的物料，而无需创建周期盘点工作。 若要在库位中执行现场周期盘点，工人人员输入库位 ID。

以下示例显示您如何通过使用移动设备来执行现场周期盘点。 工作人员看到的说明因设备而异，具体取决于现场周期盘点菜单项的设置。

1.  在移动设备上，选择处理现场周期盘点的菜单项。
2.  登记要为其执行现场周期盘点的库位。
3.  登记并确认物料编号和已盘点的物料数量。 **注意：** 根据在**工作人员**页中设置的参数，周期盘点工作的状态在**所有工作**页中更新至**待审核**或**已关闭**。
4.  可选择：为该库位中的剩余物料重复步骤 3，并确认没有更多的物料以供盘点。

## <a name="resolve-cycle-counting-differences"></a>解决周期盘点差异
如果一个工作用户 ID 的**为周期盘点主管**选项设置为**否**，那么以下情况会发生周期盘点差异：

-   盘点的结果值不在**工作用户**页中的**最大百分比限制**或**最大数量限制**字段中指定的偏差范围内。 例如，某场所中现有库存数量为 50，而该工作用户的偏差限制为 10。 如果该工作用户输入的值不介于 40 和 60 之间，就会发生差异。
-   盘点结果值与现有库存数量不同，且没有设置偏差限制。

您可以调整盘点结果值的差异，然后在**待审阅的周期盘点**页上接受该盘点结果值。 您可以在**按库位显示的现有量**页中验证修改后的物料数量的盘点。 如果差异未被批准则盘点结果值将被拒绝。

## <a name="additional-resources"></a>其他资源
[为仓库工作配置移动设备](configure-mobile-devices-warehouse.md)



