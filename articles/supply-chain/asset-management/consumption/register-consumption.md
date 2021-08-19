---
title: 登记消耗
description: 本主题介绍如何在资产管理中登记消耗。
author: johanhoffmann
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderJournal, EntAssetWorkOrderAddSparePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 619da584ea37e80b1803ae5983e52e8ee4053f3751a8df75a8f5bc1ddf7e65d6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765565"
---
# <a name="register-consumption"></a>登记消耗

[!include [banner](../../includes/banner.md)]

 

为工作订单完成了维护作业之后，下一步是创建消耗登记和过帐日记帐。 可以为以下消耗类型创建登记：工时、物料和费用。 将在 **工作订单日记帐** 页面中登记和过帐不同消耗类型。 **资产管理** 中的日记帐设置用于在 **项目管理与核算** 模块中为工时、物料和费用分别创建和过帐日记帐。

有些情况下，您可能可以在工作订单中添加或删除预测行。 对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑日记帐行。 在[预测、工作订单和项目](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)中了解有关工作订单生命周期状态和相关的项目阶段的详细信息。

>[!NOTE]
>可以为工作订单生命周期状态设置日记帐自动过帐。 有关详细信息，请参阅[工作订单生命周期状态](../setup-for-work-orders/work-order-lifecycle-states.md)。

1. 单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 选择工作订单，然后单击 **日记帐**。

3. 单击 **从预测复制** 以传输可能与该工作订单关联的所有预测行。 可以选择要传输哪些消耗类型。

4. 如有必要，可通过单击 **添加行** 并在行中填写数据，在相关快速选项卡上添加更多消耗行。

5. 单击 **验证日记帐**，以便在过帐前验证日记帐行。

6. 单击 **日记帐过帐** 以过帐日记帐行。

7. 过帐消耗量日记帐后，您可以更新工作订单生命周期状态。 例如，要指示工作订单已完成，可以将生命周期状态更新为“已结束”。

    - 在 **工作订单日记帐** 页顶部的 **显示** 字段中，选择要查看哪些日记帐行：**所有**、**未过帐** 或 **已过帐**。 已过帐日记帐在 **已过帐** 复选框中具有选中标记。  
    - 在工作订单日记帐中创建物料行之后，将把与物料关联的产品维度和跟踪维度自动传输到这个日记帐行。  

下面的屏幕截图显示 **工作订单日记帐** 中工作订单的工时和物料登记的示例。

![图 1.](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>拆分具有多个工作订单作业的工作订单

如果工作订单中包含多个工作订单作业，则可使用 **拆分工时** 功能登记工时，这意味着可以将一个工时登记行平均分配给每个工作订单作业。

1. 单击 **资产管理** > **常用** > **工作订单** > **所有工作订单** 或 **有效工作订单**。

2. 选择工作订单，然后单击 **日记帐**。

3. 选择要拆分的工时登记行，然后单击 **拆分工时**。

4. 将在 **拆分工作订单维护作业的工时** 对话框的 **工人** 字段中自动显示已登录工人的姓名。 如果需要，可以选择其他工人。

5. 在 **类别** 字段中为工时登记选择类别。

6. 在 **工时** 字段中插入要拆分的工时数量。

    ![图 2.](media/02-consumption.png)

7. 单击 **确定**。

*示例：* 在下面的屏幕截图中，显示了其中包含三个工作订单作业的工作订单的日记帐行。 已拆分第一个行（其中包含三个工时），并为每个工作订单作业登记了一个工时。 创建这三个工时登记行之后，您可以决定如何处理原始工时登记行（此示例中为第一个行）。 可以将其保留原样或删除。 

![图 3.](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>消耗登记的财务维度

创建消耗登记时，将把与不同登记类型关联的财务维度按特定顺序添加到这些登记。 

- *工时和费用登记：* 首先添加来自日记帐标题的财务维度（如果有）。 接下来添加来自关联的工作订单项目的财务维度。 最后添加来自资源（工人） 的财务维度。

- *物料登记：* 首先添加来自日记帐标题的财务维度（如果有）。 然后添加来自关联的工作订单项目的财务维度。 接下来添加来自站点的财务维度。 最后添加来自物料 的财务维度。

>[!NOTE]
>对于所有三种登记类型，都将验证财务维度组合，并且无效组合将为空。 这是其他 Finance and Operations 应用的标准设置。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]