---
title: 维护预测
description: 本主题介绍资产管理中的维护预测。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a1596b283c3eaffca25ff7f03c722a2bcce109fb
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626285"
---
# <a name="maintenance-forecasts"></a>维护预测

[!include [banner](../../includes/banner.md)]



创建工作订单时，将创建具有相关的资产和维护作业类型的工作订单作业。 如果选择包含维护预测的维护作业类型，将把这些预测自动复制到工作订单。

您可能可以将预测行添加到工作订单中或从工作订单中删除它们。 对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑预测行。 有关工作订单生命周期状态和相关的项目阶段的详细信息，请参阅[预测、工作订单和项目](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md)。

1. 选择**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。

2. 在列表中选择工作订单，然后在“操作窗格”> **工作订单**选项卡 > **项目**组中，选择**预测**。 **工作订单维护预测**页面将显示来自为工作订单作业选择的维护作业类型的预测行。


## <a name="add-an-hours-forecast-to-a-work-order"></a>向工作订单添加工时预测

1. 在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。

2. 在**工时**快速选项卡上，选择**添加**创建新行。

3. 在**类别**字段中选择一个类别。

4. 在**工时**字段中，输入预测工时的数量。

5. 在**行属性**字段中选择应该对行使用的费用类型。


## <a name="add-an-items-forecast-to-a-work-order"></a>向工作订单添加物料预测

有三种向工作订单维护预测添加物料的方法。 可以为备件列表或资产物料清单 (BOM) 中不包含的物料（备件）创建行，可以从已核准的备件列表选择备件，或从资产物料清单选择物料。

- 在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。

- 在**物料**快速选项卡上，使用适当的方法将物料添加到维护预测中。

要为备件列表或资产物料清单中不包含的备件创建行，请按照以下步骤操作：

1. 选择**添加**。
2. 在**物料编号**字段中，选择物料。
3. 在**销售数量**字段中输入数量。
4. 在**单位**字段中，选择数量的度量单位。
5. 在**成本价**和**货币**字段中，输入相应值。
6. 在**行属性**字段中，选择一个行属性。
7. 要更改物料行中显示的维度的列表，请选择**库存** > **显示维度**，选择维度，然后将**保存设置**选项设置为**是**。

要从已审核的备件列表添加备件，请按照下列步骤操作：

1. 选择**添加备件**。
2. 选择备件，然后根据需要编辑相关信息。
3. 选择**确定**。

要从资产物料清单添加物料，请按照以下步骤操作：

1. 选择**添加 BOM 物料**。
2. 选择物料，然后根据需要编辑相关信息。
3. 选择**确定**。

若要获取显示所选行上的物料在资产管理中在何处用于资产、维护作业类型默认值、备件和工作订单的概览，请选择**物料使用位置**。 有关此概览的详细信息，请参阅[物料的使用位置](../controlling-and-reporting/item-where-used.md)。


## <a name="add-an-expense-forecast-to-a-work-order"></a>向工作订单添加费用预测

1. 在**工作订单维护预测**页面上，选择要添加预测的工作订单作业。

2. 在**费用**快速选项卡上，选择**添加**创建行。

3. 在**类别**字段中选择一个类别。

4. 在**数量**字段中输入数量。

5. 在**成本价**、**销售币种**和**销售价**字段中，输入相应的值。

6. 在**行属性**字段中选择应该对行使用的费用类型。

>[!NOTE]
>**维护预测总计**快速选项卡在每个快速选项卡上显示为所选工作订单作业和为工作订单创建的行的数量的概览。 另外还显示工作订单作业的和工作订单的预测工时总计。

下图显示**工作订单维护预测**页面的示例。

![图 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>自动更新工作订单预测

如果在 Microsoft Dynamics 365 for Finance and Operations 的其他模块中更新了工时成本、物料成本和费用，资产管理中的工作订单预测可以自动更新以反映这些更改。 此功能帮助确保工作订单预测中始终使用最新成本价。 您还可以对[维护作业类型预测](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)进行类似更新。

1. 选择**资产管理** > **定期** > **预测** > **更新工作订单预测**。

2. 根据需要，可以在**更新工作订单预测**对话框中，在**要包括的记录**快速选项卡上，添加有关特定工作订单或工作订单作业的选项。 单击**筛选器**进行相关选择。

3. 在**在后台运行**快速选项卡上，可根据需要将自动更新设置为批处理作业。

4. 选择**确定**开始进行预测更新。


下图显示**更新工作订单预测**对话框的示例。

![图 2](media/07-work-orders.png)
