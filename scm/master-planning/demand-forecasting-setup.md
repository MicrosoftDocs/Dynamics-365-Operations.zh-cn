---
title: "需求预测设置"
description: "本主题介绍为准备需求预测您必须执行的设置任务。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>需求预测设置

本主题介绍为准备需求预测您必须执行的设置任务。  

这些设置任务包括设置以下数据和参数。

## <a name="item-allocation-key"></a>物料分配参数
只有当物料是物料分配参数的一部分时，为物料及其维度计算需求预测。 此规则已执行组大量物料，因此，预测需求可以快速创建。 在需求预测生成时，忽略百分比物料分配参数。 预测只基于历史数据创建。 

如果物料分配参数在创建预测时使用，物料及其维度必须仅是这一个物料分配参数的一部分。 

要添加到库存单位 (SKU) 物料分配参数，请转到**主计划** &gt; ** ** &gt; **设置需求预测** &gt; ** **物料分配参数。 使用**分配物料**页将物料分配到分配参数。

## <a name="intercompany-planning-groups"></a>内部公司计划组
需求预测会生成跨公司预测。 在工序的 Microsoft Dynamics 365 中，公司分组到一起计划的一个内部公司计划组。 对于每个公司，应指定要为需求预测，考虑哪些物料分配参数，请将物料分配参数。内部公司计划组成员。至的**主计划** &gt; ** ** &gt; **设置内部公司计划**组。 

默认情况下，如果分配参数，物料未分配给内部公司计划组成员，需求预测用于所有分配给从 Dynamics 365 的所有物料分配参数。工序公司的所有物料计算。 公司和物料分配参数的其他筛选选项在**生成统计基准预测**页可用。 

审查预测的物料的数量。 在您使用 Microsoft Azure 机器学习时，不必要的物料可能导致增加成本。

## <a name="demand-forecasting-parameters"></a>需求预测参数
若要设置需求预测参数，请转到**主计划** &gt; **设置** &gt; ** **需求预测参数。 由于需求预测跨公司运行，设置是全局的。 换言之，设置应用于所有公司。 

需求预测生成数量形式的预测。 因此，必须在**需求预测单位**字段中指定应用于表示数量的度量单位。 度量单位必须是唯一的，这有助于确保合并和百分比分配有意义。 有关合并和百分比分配的详细信息，请参阅[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)。 对于用于需求预测中包含的 SKU 的每个度量单位，请确保有针对该度量单位和一般预测度量单位的转换规则。 在预测生成运行时，不具有度量单位转换的物料列表被记录，以便您可以轻松地更正设置。 

需求预测可用于预测相关和不相关的需求。 例如，如果只选中**销售订单**复选框，并且如果为需求预测考虑的所有物料均为已售出的物料，则系统将计算不相关需求。 但是，重要子组件可以添加到物料分配参数并可以包括在需求预测中。 在这种情况下，如果选中**生产订单行**复选框，则计算相关的预测。 

在创建工序的 Dynamics 的基线两种方法预测的 365。 您可以使用历史数据顶部的预测模型，也可以只是将历史数据复制到预测。 您可以通过**预测生成策略**字段选择这两种方式中的一个。 若要使用预测模型，则选择 **Azure 机器学习**。 

通过单击**需求预测参数**页左窗格中的**预测维度**，您还可以选择在生成需求预测时要使用的一组预测维度。 预测维度指示针对哪个详细级别定义预测。 公司、站点和物料分配参数是必需的预测维度，不过，您还可以在仓库、库存状态、客户组、客户帐户、国家/地区、州/省和物料及所有物料维度级别生成预测。 

您可以随时将预测维度添加到用于需求预测的维度列表。 您还可以从列表中删除预测维度。 但是，如果您添加或删除预测维度，手动调整将丢失。 

并非所有的物料都从需求预测角度具有相同的行为方式。 类似的物料可分组到一个物料分配参数中，并且诸如交易记录类型和预测方法设置等参数可按物料分配参数设置。 单击**需求预测参数**页左窗格中的**物料分配参数**。 

若要生成预测，工序的 Dynamics 365 使用一个机器学习 Web 服务。 则登录到 Microsoft Azure 机器学习工作室，要连接到服务，则必须为此工序 Dynamics 365 提供以下信息：

-   Web 服务应用程序编程接口 (API) 密钥
-   Web 服务终结点 URL
-   Azure 存储帐户名称
-   Azure 存储帐户密钥

**注意：**只有当您使用的是自定义存储帐户时才需要 Azure 存储帐户名称和密钥。 如果您部署本地版本，您必须在 Azure 的自定义存储帐户，因此，机器学习可以访问服务历史数据。 

若要创建需求预测，您可以部署您的服务通过使用机器学习工作室或工序需求预测测试的 Dynamics 365。 因为工序的 Web 服务是可用，Dynamics 365 部署的 Dynamics 365 演示工序的测试需求预测。 在**需求预测参数**页上，单击选项卡 **Azure 机器学习**。

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Dynamics 365 设置工序的机器学习预测需求的服务
若要查看可以为工序需求预测的 Dynamics 服务的 365 Configuration Key，请转到**主计划** &gt; ** ** &gt; **设置需求预测** &gt; **算法**预测参数。 **算法预测参数**页面查看参数的默认值。 **可以覆盖在需求预测参数**页面的这些参数。 使用**常规**选项卡全局覆盖参数，或使用**物料分配参数**选项卡依据物料分配参数来覆盖参数。 针对某个物料分配参数覆盖的参数只影响与该物料分配参数关联的物料的预测。

<a name="see-also"></a>请参阅
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


