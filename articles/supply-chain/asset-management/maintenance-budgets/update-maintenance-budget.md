---
title: 更新维护预算
description: 本主题说明如何在资产管理中更新维护预算。
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e43abd4644eec8c91606ec48bbecf30f12600856
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423061"
---
# <a name="update-maintenance-budgets"></a>更新维护预算

[!include [banner](../../includes/banner.md)]

 

**维护预算行** 页显示已经为 **维护预算** 页中选择的预算创建的所有预算行。 （有关详细信息，请参阅[创建维护预算](create-maintenance-budget.md)。）核准维护预算之前，可重新计算和调整维护预算行。 预算期间过去，并且已经在资产管理中过帐了成本之后，还可以使用实际成本更新预算行。

## <a name="recalculate-a-maintenance-budget"></a>重新计算维护预算

可以在 **维护预算行** 页中重新计算维护预算。 重新计算维护预算时，将删除现有预算行，并完成新计算。

1. 在 **维护预算行** 页上，选择 **重新计算**。
2. 在 **重新计算预算** 对话框中，对新计算进行必需的更改，然后选择 **确定**。

将根据您设置的值创建新预算行。

## <a name="adjust-budget-lines"></a>调整预算行

您可以调整与预算成本关联的所选行，而不是重新计算整个维护预算。

1. 在 **维护预算行** 页上，选择要更新其预算成本的行。
2. 选择 **调整**。
3. 若要向所选行添加金额，请选中 **添加成本** 复选框，然后在 **添加值** 字段中输入值。
4. 若要将所选预算行的预算成本乘以系数，请选中 **乘以成本** 复选框，然后在 **乘以值** 字段中输入系数。

    例如，如果在 **乘以值** 字段中输入 **1.2**，则所选行的预算成本增加 20%。 如果输入 **0.7**，则所选行的预算成本减少 30%。

5. 选择 **确定**。

将根据在步骤 3 或 4 中设置的值更新所选预算行。

## <a name="update-actual-costs"></a>更新实际成本

预算行的日期过去，并且已经在资产管理中过帐了实际成本之后，可以更新维护预算的实际成本。

1. 在 **维护预算行** 页上，选择 **更新成本**。
2. 在 **计算实际成本** 对话框中，选择 **确定**。

如果已过帐实际成本，将更新预算行的 **实际成本** 字段。 如果在创建预算之后创建了新的资产类型，并且如果已经对为其创建了工作订单且为其过帐了关联的成本的资产使用了这些资产类型，可能会生成新预算行。 新预算行仅显示实际成本，因为没有为其计算任何预算成本。

> [!NOTE]
> 若要查看拆分为预防性成本、纠正成本和投资成本的实际成本的概览，可以在 **资产成本控制** 页中为相同期间执行计算。 

## <a name="manually-add-budget-lines"></a>手动添加预算行

在 **维护预算行** 页中，可通过选择 **新建**，然后行中进行选择，手动添加新的预算行。 下面是这种方法可能有用的情况的一些示例：

- 您知道某些资产的整修正处于规划阶段，但是尚未在资产管理中创建关联的作业。 但是，您希望维护预算中包括这些作业的预算成本。
- 在您创建维护预算之后已创建了新的资产或资产类型，但是尚未为这些资产或资产类型设置维护计划。 但是，您希望维护预算中包括这些资产类型的预算成本。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]