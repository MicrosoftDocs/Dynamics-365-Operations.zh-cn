---
title: "需求预测设置"
description: "本主题介绍为准备需求预测您必须执行的设置任务。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 74d520199410711b80b750a12ee726633e09d01c
ms.contentlocale: zh-cn
ms.lasthandoff: 06/13/2017

---

# <a name="demand-forecasting-setup"></a>需求预测设置

[!include[banner](../includes/banner.md)]


本主题介绍为准备需求预测您必须执行的设置任务。  

这些设置任务包括设置以下数据和参数。

## <a name="item-allocation-key"></a>物料分配参数
只有当物料是物料分配参数的一部分时，为物料及其维度计算需求预测。 此规则强制对大量的物料进行分组，以便可以更快速创建需求预测。 在需求预测生成时，物料分配参数百分比被忽略。 预测只基于历史数据创建。 

如果物料分配参数在创建预测时使用，物料及其维度必须仅是这一个物料分配参数的一部分。 

若要向物料分配参数添加库存单位 (SKU)，请转到**主计划** &gt; **设置** &gt; **需求预测** &gt; **物料分配参数**。 使用**分配物料**页将物料分配到分配参数。

## <a name="intercompany-planning-groups"></a>内部公司计划组
需求预测会生成跨公司预测。 在 Microsoft Dynamics 365 for Finance and Operations 中，一起计划的公司会被分组到一个内部公司计划组。 若要根据公司指定应为需求预测考虑哪些物料分配参数，请将物料分配参数与相应的内部公司计划组成员关联，方式是转到**主计划** &gt; **设置** &gt;> **内部公司计划组**。 

默认情况下，如果未将任何物料分配参数分配给内部公司计划组成员，则针对分配给所有 Finance and Operations 公司所拥有所有物料分配参数的所有物料计算需求预测。 公司和物料分配参数的其他筛选选项在**生成统计基准预测**页可用。 

审查预测的物料的数量。 在您使用 Microsoft Azure 机器学习时，不必要的物料可能导致增加成本。

## <a name="demand-forecasting-parameters"></a>需求预测参数
若要设置需求预测参数，转到**主计划** &gt; **设置** &gt; **需求预测参数**。 由于需求预测跨公司运行，设置是全局的。 换言之，设置应用于所有公司。 

需求预测生成数量形式的预测。 因此，必须在**需求预测单位**字段中指定应用于表示数量的度量单位。 度量单位必须是唯一的，这有助于确保合并和百分比分配有意义。 有关合并和百分比分配的详细信息，请参阅[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)。 对于用于需求预测中包含的 SKU 的每个度量单位，请确保有针对该度量单位和一般预测度量单位的转换规则。 在预测生成运行时，不具有度量单位转换的物料列表被记录，以便您可以轻松地更正设置。 

需求预测可用于预测相关和不相关的需求。 例如，如果只选中**销售订单**复选框，并且如果为需求预测考虑的所有物料均为已售出的物料，则系统将计算不相关需求。 但是，重要子组件可以添加到物料分配参数并可以包括在需求预测中。 在这种情况下，如果选中**生产订单行**复选框，则计算相关的预测。 

在 Finance and Operations 中创建基准预测有两种方法。 您可以使用历史数据顶部的预测模型，也可以只是将历史数据复制到预测。 您可以通过**预测生成策略**字段选择这两种方式中的一个。 若要使用预测模型，则选择 **Azure 机器学习**。 

通过单击**需求预测参数**页左窗格中的**预测维度**，您还可以选择在生成需求预测时要使用的一组预测维度。 预测维度指示针对哪个详细级别定义预测。 公司、站点和物料分配参数是必需的预测维度，不过，您还可以在仓库、库存状态、客户组、客户帐户、国家/地区、州/省和物料及所有物料维度级别生成预测。 

您可以随时将预测维度添加到用于需求预测的维度列表。 您还可以从列表中删除预测维度。 但是，如果您添加或删除预测维度，手动调整将丢失。 

并非所有的物料都从需求预测角度具有相同的行为方式。 类似的物料可分组到一个物料分配参数中，并且诸如交易记录类型和预测方法设置等参数可按物料分配参数设置。 单击**需求预测参数**页左窗格中的**物料分配参数**。 

若要生成预测，Finance and Operations 使用机器学习 Web 服务。 若要连接到服务，如果您登录到 Microsoft Azure 机器学习工作室，则必须为 Finance and Operations 提供以下信息：

-   Web 服务应用程序编程接口 (API) 密钥
-   Web 服务终结点 URL
-   Azure 存储帐户名称
-   Azure 存储帐户密钥

**注意：**只有当您使用的是自定义存储帐户时才需要 Azure 存储帐户名称和密钥。 如果部署本地版本，必须在 Azure 有自定义存储帐户，以便机器学习服务可以访问历史数据。 

若要创建预测，可以通过使用机器学习工作室或 Finance and Operations 需求预测实验来部署您自己的服务。 有关将 Finance and Operations 需求预测实验部署为 Web 服务的说明，可在 Finance and Operations 中找到。 在**需求预测参数**页上，单击选项卡 **Azure 机器学习**。

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a>Finance and Operations 需求预测机器学习服务的设置
若要查看可为 Finance and Operations 需求预测服务配置的参数，请转到**主计划** &gt; **设置** &gt; **需求预测** &gt; **预测算法参数**。 **预测算法参数**页显示参数的默认值。 您可以在**需求预测参数**页覆盖这些参数。 使用**常规**选项卡全局覆盖参数，或使用**物料分配参数**选项卡依据物料分配参数来覆盖参数。 针对某个物料分配参数覆盖的参数只影响与该物料分配参数关联的物料的预测。

<a name="see-also"></a>请参阅
--------

[需求预测简介](introduction-demand-forecasting.md)

[生成统计基准预测](generate-statistical-baseline-forecast.md)

[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)




