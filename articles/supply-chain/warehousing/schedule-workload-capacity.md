---
title: "计划工作量产能"
description: "本主题介绍如何为一个仓库或全体仓库中的工作人员设置和计划工作量产能。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 69b9c5590e6f9311696bbbed2e63a6eeba2a90bf
ms.openlocfilehash: 1b93cfaf098b4cff3e72ee9bb599eadfdac2a9b9
ms.contentlocale: zh-cn
ms.lasthandoff: 05/03/2018

---

# <a name="schedule-workload-capacity"></a>计划工作量产能

[!include[banner](../includes/banner.md)]

您可以计划仓库的工作量产能，也可以预测单个仓库的工作人员当前和未来的工作量。 您可以为整个仓库计划工作量，或者为传入和传出工作量单独计划工作量。

若要预测所选仓库的工作量输出，主计划编制数据必须可用于这些仓库。 有关主计划的详细信息，请参阅[主计划](../master-planning/master-plans.md)。

## <a name="schedule-and-view-workloads-for-a-warehouse"></a>计划和查看仓库的工作量

若要为仓库计划工作量产能，您为一个或多个仓库创建工作量设置，然后将这些工作量设置与主计划相关联。 在工作量产能设置中，您可以为入货交易记录或出货交易记录定义重量或体积的限额。 您还可以为每个仓库创建多个设置，然后将设置与单独的主计划相关联。 例如，您可以使用此方法应对劳动力的季节性变化。

如果仓库的工作人员处理入货和出货工作量的交易记录，您可以配置仓库产能设置，以便在合并视图中计划工作量。

若要计划和查看仓库的工作量，必须完成以下任务：

1. 创建工作量产能设置并定义一个或多个仓库的产能限制。
2. 将工作量产能设置与主计划相关联，以便创建工作量预测并指定这些预测的适用时长。

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a>创建仓库的工作量产能设置

1. 选择**库存管理** \> **设置** \> **仓库监视** \> **工作量产能**。
2. 在“操作窗格”中，选择**新建**创建工作量产能设置。
3. 在**仓库**快速选项卡中，选择**新建**，然后输入有关行的值与仓库关联的产能负荷设置。
4. 如果**工作量产能**报表应在一个视图中显示入货交易记录和出货交易记录的总工作量，请选中**组合的入货和出货工作量**。
5. 在**交易记录类型**快速选项卡上，选择工作量限额要应用的入货和出货交易记录的类型。

    > [!NOTE]
    > 您必须为入货工作量和出货工作量选择至少一个交易记录类型。

#### <a name="define-limits-for-volume-or-weight"></a>定义体积或重量的限额

您可以为体积或重量设置限额，具体取决于仓库劳动力的相关限额。 您指定的限额包括在您可以在**工作量产能**报表中查看的工作量产能预测中。

若要预测有关物料的体积和数量的信息，必须为所有产品指定一个库存物料的标准体积和一个库存物料的重量。 **已发布产品详细信息**页**管理库存**快速选项卡上的以下字段组中提供了所需字段：

- 正在处理
- 物理维度
- 权重量化指标

如果此信息指定不正确，在生成**工作量产能**报表时，您将收到消息。 然后可以从该报告向下钻取到标识要预测未来工作量所需的缺失信息。

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a>与此主计划关联的工作量产能设置

1. 选择**库存管理** \> **定期任务** \> **计划工作量**。
2. 在**主计划**字段中，选择工作量预测使用的主计划。
3. 在**天数**字段中，指定工作量预测包含的天数。
4. 在**工作量**字段中，选择与工作量设置关联的主计划。

### <a name="view-workload-capacity"></a>查看工作负载产能

1. 选择**库存管理** \> **查询和报表** \> **实际库存报表** \> **工作量产能**。
2. 在**列数**字段中，指定显示在报表中列的数目。
3. 在**订单类型**字段中，选择**已计划并确认**、**已计划**或**已确认**，以便指示要对报表预测的订单类型。
4. 在**负载类型**字段中，选择一种负载类型以指定应预测体积还是重量的工作量产能。
5. 在**工作量产能**字段中，选择一种工作量产能设置。

