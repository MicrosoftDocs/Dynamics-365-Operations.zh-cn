---
title: 维护预测
description: 本主题介绍资产管理中的维护预测。
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024491"
---
# <a name="maintenance-forecasts"></a>维护预测

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


创建工作订单时，将创建与资产和维护作业类型关联的工作订单作业。 如果选择其中包含维护预测的维护作业类型，将把这些预测自动复制到工作订单。

您可能可以在工作订单中添加或删除预测行。 对工作订单生命周期状态、关联的项目类型和与项目类型关联的阶段规则的设置决定是否可以添加或编辑预测行。 

1. 单击**资产管理** > **常用** > **工作订单** > **所有工作订单**或**有效工作订单**。

2. 在列表中选择工作订单，然后单击**预测**。 在**工作订单维护预测**中，将显示来自为工作订单作业选择的维护作业类型的预测行。


## <a name="add-hours-forecast-to-a-work-order"></a>向工作订单添加工时预测

1. 选择要向其添加预测的工作订单作业。

2. 在**工时**快速选项卡上，单击**添加**创建新行。

3. 在**类别**字段中选择一个类别。

4. 在**工时**字段中插入预测工时的数量。

5. 在**行属性**字段中选择要对行使用的费用类型。


## <a name="add-items-forecast-to-a-work-order"></a>向工作订单添加物料预测

可以通过三种方法向工作订单维护预测添加物料：可以为备件列表做资产 BOM 中不包含的物料（即备件）创建行，可以从已核准的部件列表选择备件，还可以从资产 BOM 选择物料。

1. 选择要向其添加预测的工作订单作业。

2. 选择**物料**快速选项卡。

3. 选择**添加**为部件列表或资产 BOM 列表中不包含的备件创建新行。

4. 在**物料编号**字段中选择物料。

5. 在**销售数量**字段中插入数量，然后在**单位**字段中选择数量单位。

6. 在相关字段中插入成本价和币种，然后选择**行属性**。

7. 如果要更改物料行中显示的维度的列表，请单击**库存** > **显示维度**，选择维度，然后在**保存设置**切换按钮上选择“是”。

8. 如果要向维护预测添加已核准的备件，请单击**添加备件**，选择备件，需要时编辑相关信息，然后单击**确定**。

9. 如果要向预测添加资产 BOM 物料，请单击**添加 BOM 物料**，选择物料，需要时编辑相关信息，然后单击**确定**。

10. 如果要在资产管理中获取有关在与资产、维护作业类型默认、备件和工作订单关联时，所选行中的物料的使用位置的概览，请选择**物料使用位置**。 



## <a name="add-expense-forecast-to-a-work-order"></a>向工作订单添加费用预测

1. 本主题介绍如何向工作订单添加费用预测。 在窗体的左侧，选择要向其添加预测的工作订单作业。

2. 选择**费用**快速选项卡。

3. 单击**添加**创建新行。

4. 在**类别**字段中选择一个类别。

5. 在**数量**字段中插入数量。

6. 在相关字段中插入成本价、销售币种和销售价。

7. 在**行属性**字段中选择要对行使用的费用类型。

>[!NOTE]
>在**维护预测总计**快速选项卡上的每个选项卡中，可查看为所选工作订单作业和为工作订单创建的行的数量。 还可以查看工作订单作业的和工作订单的预测工时之和。

![图 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>自动更新工作订单预测

在资产管理中，可自动更新对已在其他模块中更新了的有关工时成本、物料成本和费用的工作订单预测的所有更改。 这是为了确保工作订单预测中始终使用最新成本价。 还可以对[维护作业类型预测](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)进行类似更新。

1. 单击**资产管理** > **定期** > **预测** > **更新工作订单预测**。

2. 如果需要，可以在**更新工作订单预测**下拉对话框中添加有关特定工作订单或工作订单作业的选项。 单击**筛选**创建这些选项。

3. 如果需要，可以在**在后台运行**快速选项卡上将自动更新设置为批处理作业。

4. 单击**确定**开始进行预测更新。


![图 2](media/07-work-orders.png)

