---
title: "需求预测设置"
description: "本主题介绍为准备需求预测您必须执行的设置任务。"
author: roxanadiaconu
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 905794e39933c9788a7ff5247807baf0ebb807d8
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="demand-forecasting-setup"></a><span data-ttu-id="f8991-103">需求预测设置</span><span class="sxs-lookup"><span data-stu-id="f8991-103">Demand forecasting setup</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f8991-104">本主题介绍为准备需求预测您必须执行的设置任务。</span><span class="sxs-lookup"><span data-stu-id="f8991-104">This topic describes the setup tasks that you must perform to prepare for demand forecasting.</span></span>  

<span data-ttu-id="f8991-105">这些设置任务包括设置以下数据和参数。</span><span class="sxs-lookup"><span data-stu-id="f8991-105">The setup tasks include setting up the following data and parameters.</span></span>

## <a name="item-allocation-key"></a><span data-ttu-id="f8991-106">物料分配参数</span><span class="sxs-lookup"><span data-stu-id="f8991-106">Item allocation key</span></span>
<span data-ttu-id="f8991-107">只有当物料是物料分配参数的一部分时，为物料及其维度计算需求预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-107">A demand forecast is calculated for an item and its dimensions only if the item is part of an item allocation key.</span></span> <span data-ttu-id="f8991-108">此规则强制对大量的物料进行分组，以便可以更快速创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-108">This rule is enforced to group large numbers of items, so that demand forecasts can be created more quickly.</span></span> <span data-ttu-id="f8991-109">在需求预测生成时，物料分配参数百分比被忽略。</span><span class="sxs-lookup"><span data-stu-id="f8991-109">The item allocation key percentage is ignored when demand forecasts are generated.</span></span> <span data-ttu-id="f8991-110">预测只基于历史数据创建。</span><span class="sxs-lookup"><span data-stu-id="f8991-110">Forecasts are created based on historical data only.</span></span> 

<span data-ttu-id="f8991-111">如果物料分配参数在创建预测时使用，物料及其维度必须仅是这一个物料分配参数的一部分。</span><span class="sxs-lookup"><span data-stu-id="f8991-111">An item and its dimensions must be part of only one item allocation key if the item allocation key is used during forecast creation.</span></span> 

<span data-ttu-id="f8991-112">若要向物料分配参数添加库存单位 (SKU)，请转到**主计划** &gt; **设置** &gt; **需求预测** &gt; **物料分配参数**。</span><span class="sxs-lookup"><span data-stu-id="f8991-112">To add a stock keeping unit (SKU) to an item allocation key, go to **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Item allocation keys**.</span></span> <span data-ttu-id="f8991-113">使用**分配物料**页将物料分配到分配参数。</span><span class="sxs-lookup"><span data-stu-id="f8991-113">Use the **Assign items** page to assign an item to an allocation key.</span></span>

## <a name="intercompany-planning-groups"></a><span data-ttu-id="f8991-114">内部公司计划组</span><span class="sxs-lookup"><span data-stu-id="f8991-114">Intercompany planning groups</span></span>
<span data-ttu-id="f8991-115">需求预测会生成跨公司预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-115">Demand forecasting generates cross-company forecasts.</span></span> <span data-ttu-id="f8991-116">在 Microsoft Dynamics 365 for Finance and Operations 中，一起计划的公司会被分组到一个内部公司计划组。</span><span class="sxs-lookup"><span data-stu-id="f8991-116">In Microsoft Dynamics 365 for Finance and Operations, companies that are planned together are grouped into one intercompany planning group.</span></span> <span data-ttu-id="f8991-117">若要根据公司指定应为需求预测考虑哪些物料分配参数，请将物料分配参数与相应的内部公司计划组成员关联，方式是转到**主计划** &gt; **设置** &gt;> **内部公司计划组**。</span><span class="sxs-lookup"><span data-stu-id="f8991-117">To specify, per company, which item allocation keys should be considered for demand forecasting, associate an item allocation key with the intercompany planning group member by going to **Master planning** &gt; **Setup** &gt; **Intercompany planning groups**.</span></span> 

<span data-ttu-id="f8991-118">默认情况下，如果未将任何物料分配参数分配给内部公司计划组成员，则针对分配给所有 Finance and Operations 公司所拥有所有物料分配参数的所有物料计算需求预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-118">By default, if no item allocation keys are assigned to intercompany planning group members, a demand forecast is calculated for all items that are assigned to all item allocation keys from all Finance and Operations companies.</span></span> <span data-ttu-id="f8991-119">公司和物料分配参数的其他筛选选项在**生成统计基准预测**页可用。</span><span class="sxs-lookup"><span data-stu-id="f8991-119">Additional filtering options for companies and item allocation keys are available on the **Generate statistical baseline forecast** page.</span></span> 

<span data-ttu-id="f8991-120">审查预测的物料的数量。</span><span class="sxs-lookup"><span data-stu-id="f8991-120">Review the number of items that are forecasted.</span></span> <span data-ttu-id="f8991-121">在您使用 Microsoft Azure 机器学习时，不必要的物料可能导致增加成本。</span><span class="sxs-lookup"><span data-stu-id="f8991-121">Unnecessary items might cause increased costs when you use Microsoft Azure Machine Learning.</span></span>

## <a name="demand-forecasting-parameters"></a><span data-ttu-id="f8991-122">需求预测参数</span><span class="sxs-lookup"><span data-stu-id="f8991-122">Demand forecasting parameters</span></span>
<span data-ttu-id="f8991-123">若要设置需求预测参数，转到**主计划** &gt; **设置** &gt; **需求预测参数**。</span><span class="sxs-lookup"><span data-stu-id="f8991-123">To set up demand forecasting parameters, go to **Master planning** &gt; **Setup** &gt; **Demand forecasting parameters**.</span></span> <span data-ttu-id="f8991-124">由于需求预测跨公司运行，设置是全局的。</span><span class="sxs-lookup"><span data-stu-id="f8991-124">Because demand forecasting runs cross-company, the setup is global.</span></span> <span data-ttu-id="f8991-125">换言之，设置应用于所有公司。</span><span class="sxs-lookup"><span data-stu-id="f8991-125">In other words, the setup applies to all companies.</span></span> 

<span data-ttu-id="f8991-126">需求预测生成数量形式的预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-126">Demand forecasting generates the forecast in quantities.</span></span> <span data-ttu-id="f8991-127">因此，必须在**需求预测单位**字段中指定应用于表示数量的度量单位。</span><span class="sxs-lookup"><span data-stu-id="f8991-127">Therefore, the unit of measure that the quantity should be expressed in must be specified in the **Demand forecast unit** field.</span></span> <span data-ttu-id="f8991-128">度量单位必须是唯一的，这有助于确保合并和百分比分配有意义。</span><span class="sxs-lookup"><span data-stu-id="f8991-128">The unit of measure must be unique, to help guarantee that the aggregation and percentage distribution make sense.</span></span> <span data-ttu-id="f8991-129">有关合并和百分比分配的详细信息，请参阅[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)。</span><span class="sxs-lookup"><span data-stu-id="f8991-129">For more information about aggregation and percentage distribution, see [Make manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md).</span></span> <span data-ttu-id="f8991-130">对于用于需求预测中包含的 SKU 的每个度量单位，请确保有针对该度量单位和一般预测度量单位的转换规则。</span><span class="sxs-lookup"><span data-stu-id="f8991-130">For every unit of measure that is used for SKUs that are included in demand forecasting, make sure that there is a conversion rule for the unit of measure and the general forecasting unit of measure.</span></span> <span data-ttu-id="f8991-131">在预测生成运行时，不具有度量单位转换的物料列表被记录，以便您可以轻松地更正设置。</span><span class="sxs-lookup"><span data-stu-id="f8991-131">When forecast generation is run, the list of items that don't have a unit of measure conversion is logged, so that you can easily correct the setup.</span></span> 

<span data-ttu-id="f8991-132">需求预测可用于预测相关和不相关的需求。</span><span class="sxs-lookup"><span data-stu-id="f8991-132">Demand forecasting can be used to forecast both dependent and independent demand.</span></span> <span data-ttu-id="f8991-133">例如，如果只选中**销售订单**复选框，并且如果为需求预测考虑的所有物料均为已售出的物料，则系统将计算不相关需求。</span><span class="sxs-lookup"><span data-stu-id="f8991-133">For example, if only the **Sales order** check box is selected, and if all the items that are considered for demand forecasting are items that are sold, the system calculates independent demand.</span></span> <span data-ttu-id="f8991-134">但是，重要子组件可以添加到物料分配参数并可以包括在需求预测中。</span><span class="sxs-lookup"><span data-stu-id="f8991-134">However, critical subcomponents can be added to item allocation keys and included in demand forecasting.</span></span> <span data-ttu-id="f8991-135">在这种情况下，如果选中**生产订单行**复选框，则计算相关的预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-135">In this case, if the **Production line** check box is selected, a dependent forecast is calculated.</span></span> 

<span data-ttu-id="f8991-136">在 Finance and Operations 中创建基准预测有两种方法。</span><span class="sxs-lookup"><span data-stu-id="f8991-136">There are two methods for creating a baseline forecast in Finance and Operations.</span></span> <span data-ttu-id="f8991-137">您可以使用历史数据顶部的预测模型，也可以只是将历史数据复制到预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-137">You can use forecasting models on top of historical data, or you can just copy over the historical data to the forecast.</span></span> <span data-ttu-id="f8991-138">您可以通过**预测生成策略**字段选择这两种方式中的一个。</span><span class="sxs-lookup"><span data-stu-id="f8991-138">The **Forecast generation strategy** field lets you select between these two methods.</span></span> <span data-ttu-id="f8991-139">若要使用预测模型，则选择 **Azure 机器学习**。</span><span class="sxs-lookup"><span data-stu-id="f8991-139">To use forecast models, select **Azure Machine Learning**.</span></span> 

<span data-ttu-id="f8991-140">通过单击**需求预测参数**页左窗格中的**预测维度**，您还可以选择在生成需求预测时要使用的一组预测维度。</span><span class="sxs-lookup"><span data-stu-id="f8991-140">By clicking **Forecast dimensions** in the left pane of the **Demand forecasting parameters** page, you can also select the set of forecast dimensions to use when the demand forecast is generated.</span></span> <span data-ttu-id="f8991-141">预测维度指示针对哪个详细级别定义预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-141">A forecast dimension indicates the level of detail that the forecast is defined for.</span></span> <span data-ttu-id="f8991-142">公司、站点和物料分配参数是必需的预测维度，不过，您还可以在仓库、库存状态、客户组、客户帐户、国家/地区、州/省和物料及所有物料维度级别生成预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-142">Company, site, and item allocation key are mandatory forecast dimensions, but you can also generate forecasts at the warehouse, inventory status, customer group, customer account, country/region, state, and item plus all item dimension levels.</span></span> 

<span data-ttu-id="f8991-143">您可以随时将预测维度添加到用于需求预测的维度列表。</span><span class="sxs-lookup"><span data-stu-id="f8991-143">At any point, you can add forecast dimensions to the list of dimensions that are used for demand forecasting.</span></span> <span data-ttu-id="f8991-144">您还可以从列表中删除预测维度。</span><span class="sxs-lookup"><span data-stu-id="f8991-144">You can also remove forecast dimensions from the list.</span></span> <span data-ttu-id="f8991-145">但是，如果您添加或删除预测维度，手动调整将丢失。</span><span class="sxs-lookup"><span data-stu-id="f8991-145">However, manual adjustments are lost if you add or remove a forecast dimension.</span></span> 

<span data-ttu-id="f8991-146">并非所有的物料都从需求预测角度具有相同的行为方式。</span><span class="sxs-lookup"><span data-stu-id="f8991-146">Not all items behave in the same manner from a demand forecasting perspective.</span></span> <span data-ttu-id="f8991-147">类似的物料可分组到一个物料分配参数中，并且诸如交易记录类型和预测方法设置等参数可按物料分配参数设置。</span><span class="sxs-lookup"><span data-stu-id="f8991-147">Similar items can be grouped in one item allocation key, and parameters such as transaction types and forecast method settings can be set per item allocation key.</span></span> <span data-ttu-id="f8991-148">单击**需求预测参数**页左窗格中的**物料分配参数**。</span><span class="sxs-lookup"><span data-stu-id="f8991-148">Click **Item allocation keys** in the left pane of the **Demand forecasting parameters** page.</span></span> 

<span data-ttu-id="f8991-149">若要生成预测，Finance and Operations 使用机器学习 Web 服务。</span><span class="sxs-lookup"><span data-stu-id="f8991-149">To generate the forecast, Finance and Operations uses a Machine Learning web service.</span></span> <span data-ttu-id="f8991-150">若要连接到服务，如果您登录到 Microsoft Azure 机器学习工作室，则必须为 Finance and Operations 提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="f8991-150">To connect to the service, you must provide Finance and Operations the following information if you sign in to Microsoft Azure Machine Learning Studio:</span></span>

-   <span data-ttu-id="f8991-151">Web 服务应用程序编程接口 (API) 密钥</span><span class="sxs-lookup"><span data-stu-id="f8991-151">Web service application programming interface (API) key</span></span>
-   <span data-ttu-id="f8991-152">Web 服务终结点 URL</span><span class="sxs-lookup"><span data-stu-id="f8991-152">Web service endpoint URL</span></span>
-   <span data-ttu-id="f8991-153">Azure 存储帐户名称</span><span class="sxs-lookup"><span data-stu-id="f8991-153">Azure storage account name</span></span>
-   <span data-ttu-id="f8991-154">Azure 存储帐户密钥</span><span class="sxs-lookup"><span data-stu-id="f8991-154">Azure storage account key</span></span>

<span data-ttu-id="f8991-155">**注意：**只有当您使用的是自定义存储帐户时才需要 Azure 存储帐户名称和密钥。</span><span class="sxs-lookup"><span data-stu-id="f8991-155">**Note:** The Azure storage account name and key are required only if you use a custom storage account.</span></span> <span data-ttu-id="f8991-156">如果部署本地版本，必须在 Azure 有自定义存储帐户，以便机器学习服务可以访问历史数据。</span><span class="sxs-lookup"><span data-stu-id="f8991-156">If you deploy the on-premises version, you must have a custom storage account on Azure, so that the Machine Learning service can access the historical data.</span></span> 

<span data-ttu-id="f8991-157">若要创建预测，可以通过使用机器学习工作室或 Finance and Operations 需求预测实验来部署您自己的服务。</span><span class="sxs-lookup"><span data-stu-id="f8991-157">To create demand predictions, you can deploy your own service by using Machine Learning Studio or the Finance and Operations demand forecasting experiments.</span></span> <span data-ttu-id="f8991-158">有关将 Finance and Operations 需求预测实验部署为 Web 服务的说明，可在 Finance and Operations 中找到。</span><span class="sxs-lookup"><span data-stu-id="f8991-158">Instructions for deploying the Finance and Operations demand forecasting experiments as a web service are available Finance and Operations.</span></span> <span data-ttu-id="f8991-159">在**需求预测参数**页上，单击选项卡 **Azure 机器学习**。</span><span class="sxs-lookup"><span data-stu-id="f8991-159">On the **Demand forecasting parameters** page, click the **Azure Machine Learning** tab.</span></span>

## <a name="settings-for-the-finance-and-operations-demand-forecasting-machine-learning-service"></a><span data-ttu-id="f8991-160">Finance and Operations 需求预测机器学习服务的设置</span><span class="sxs-lookup"><span data-stu-id="f8991-160">Settings for the Finance and Operations demand forecasting machine learning service</span></span>
<span data-ttu-id="f8991-161">若要查看可为 Finance and Operations 需求预测服务配置的参数，请转到**主计划** &gt; **设置** &gt; **需求预测** &gt; **预测算法参数**。</span><span class="sxs-lookup"><span data-stu-id="f8991-161">To view the parameters that can be configured for the Finance and Operations demand forecasting service, go to **Master Planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Forecasting algorithm parameters**.</span></span> <span data-ttu-id="f8991-162">**预测算法参数**页显示参数的默认值。</span><span class="sxs-lookup"><span data-stu-id="f8991-162">The **Forecasting algorithm parameters** page shows the default values for the parameters.</span></span> <span data-ttu-id="f8991-163">您可以在**需求预测参数**页覆盖这些参数。</span><span class="sxs-lookup"><span data-stu-id="f8991-163">You can overwrite these parameters on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="f8991-164">使用**常规**选项卡全局覆盖参数，或使用**物料分配参数**选项卡依据物料分配参数来覆盖参数。</span><span class="sxs-lookup"><span data-stu-id="f8991-164">Use the **General** tab to overwrite the parameters globally, or use the **Item allocation keys** tab to overwrite the parameters per item allocation key.</span></span> <span data-ttu-id="f8991-165">针对某个物料分配参数覆盖的参数只影响与该物料分配参数关联的物料的预测。</span><span class="sxs-lookup"><span data-stu-id="f8991-165">Parameters that are overwritten for an item allocation key affect only the forecast of items that are associated with that item allocation key.</span></span>

<a name="see-also"></a><span data-ttu-id="f8991-166">请参阅</span><span class="sxs-lookup"><span data-stu-id="f8991-166">See also</span></span>
--------

[<span data-ttu-id="f8991-167">需求预测简介</span><span class="sxs-lookup"><span data-stu-id="f8991-167">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="f8991-168">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="f8991-168">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

[<span data-ttu-id="f8991-169">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="f8991-169">Making manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)



