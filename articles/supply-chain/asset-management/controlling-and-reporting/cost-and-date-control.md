---
title: 成本和日期控制
description: 本文介绍资产管理中的成本和日期控制。
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 643e5afda7d3abaff926e81ff75186ca195a8cb1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861027"
---
# <a name="cost-and-date-control"></a>成本和日期控制

[!include [banner](../../includes/banner.md)]

在资产管理中，可计算成本，以便获取资产、功能位置和工作订单的实际成本与预算成本的比较概览。 实际成本基于过帐的交易记录。

如果要将工作订单的计划开始日期和结束日期与实际开始日期和结束日期进行比较，也可以创建日期计算。

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>资产、功能位置和工作订单的成本控制

为资产、功能位置和工作订单创建的计算几乎相同。 唯一的区别是，对于资产和功能位置，还可以在计算中包括子资产和子位置。 日期是记录登记时的交易记录日期。

1. 单击 **资产管理** > **查询** > **资产** > **资产成本控制** 或 **功能位置成本控制**，或 **资产管理** > **查询** > **工作订单** > **工作订单成本控制**。

2. 在 **资产成本控制** / **功能位置成本控制** / **工作订单成本控制** 对话框中，选择要计算的时间范围。

3. 如果需要，选择计算中要包括的财务维度集。

4. 如果不希望显示包含零成本的结果，请在 **忽略零** 切换按钮上选择“是”。

5. 可使用 **级别** 字段指示要与功能位置有关的成本控制行的详细程度。 

    例如，如果在字段中插入数字“1”，并且采用了多级别功能位置层次结构，则将在最上级别显示某个功能位置的所有成本控制行，因此，可以从较低级别的功能位置叠加行中的工时。

    如果在 **级别** 字段中插入数字“0”，将看到详细结果，其中显示其关联的所有功能位置级别的所有成本控制行。

6. 如果要在计算中包括该列，请在 **显示未结承诺成本** 切换按钮上选择“是”。

7. 若要将与子资产关联的成本显示为单独行，请在 **包括子资产** 切换按钮上选择“是”。

8. 如果要限制搜索，可在 **要包括的记录** 快速选项卡上选择特定资产/功能位置/工作订单。

9. 单击 **确定** 开始计算。

    下图显示 **资产成本控制** 对话框的示例。

    ![“资产成本控制”对话框。](media/01-controlling-and-reporting.png)

10. 在 **资产成本控制** 页面上，单击 **分组依据** 按钮显示所需的计算详细程度。 将突出显示所选 **分组依据** 按钮。 单击按钮将其激活或停用。

## <a name="example-of-calculation-results-in-asset-cost-control"></a>资产成本控制中的计算结果示例

下面的屏幕截图显示 **资产成本控制** 中的计算结果的示例。

- **原始预算** 字段显示工作订单预测中的预算成本。 
- **承诺成本** 字段显示法人自行承诺支付的费用总额。 
- **未结承诺成本** 字段显示对要为您已订购或收到，但尚未付款的物料、工时和服务的付款承诺。 
- **实际成本** 字段显示过帐所有消耗登记之后的相关成本。

![“资产成本控制”中的计算结果的示例。](media/02-controlling-and-reporting.png)

另外一种创建成本计算的方法是在 **所有资产** 或 **有效资产** 中选择多个资产。 然后，单击 **常规** 选项卡上的 **成本控制** 按钮。在 **资产成本控制** 对话框中，将把所选资产自动插入到 **要包括的记录** 快速选项卡上的 **资产** 字段中。 单击 **确定**，然后将显示所选资产的成本计算。 可以在 **所有功能位置** 或 **有效功能位置** 中对功能位置执行同样的过程，也可以在 **所有工作订单** 或 **有效工作订单** 中对工作订单执行同样的过程。

## <a name="work-order-date-control"></a>工作订单日期控制

此页用于获取工作订单的预计开始日期和结束日期与实际开始日期和结束日期的比较概览。

1. 单击 **资产管理** > **查询** > **工作订单** > **工作订单日期控制**。

2. 单击 **计算**。

3. 在 **功能位置** 字段中选择一个功能位置。

4. 在 **开始日期** 和 **结束日期** 字段中插入要为其创建计算的范围。 将包括预计开始日期在该范围内的所有工作订单。

5. 单击 **确定**。

6. 单击 **分组依据** 按钮显示所需的计算详细程度。 将突出显示所选 **分组依据** 按钮。 单击按钮将其激活或停用。

## <a name="example-of-calculation-results-in-work-order-date-control"></a>工作订单日期控制中的计算结果示例

下面的屏幕截图显示 **工作订单日期控制** 中的计算结果的示例。

- **平均开始延迟** 字段显示工作订单的计划开始日期与实际开始日期之间的天数。 例如，如果实际开始日期在计划开始日期的两天前，则此字段中将显示“-2”。  
- **平均结束延迟** 字段显示工作订单的计划结束日期与实际结束日期之间的天数。 例如，如果实际结束日期在计划结束日期的三天后，则此字段中将显示“3”。  
- **发生次数** 字段显示工作订单的计划开始日期与实际开始日期之间和计划结束日期与实际结束日期之间发生偏差的次数。

![“工作订单日期控制”中的计算结果的示例。](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]