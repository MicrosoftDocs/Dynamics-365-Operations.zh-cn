---
title: 为每个法人设置 ER 格式的参数
description: 本主题说明如何为每个法人设置电子报告 (ER) 格式的参数。
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: ca837026f18034cddb34d7a2d5a62002ed69106a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042749"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="9daf6-103">为每个法人设置 ER 格式的参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9daf6-104">先决条件</span><span class="sxs-lookup"><span data-stu-id="9daf6-104">Prerequisites</span></span>

<span data-ttu-id="9daf6-105">要完成这些步骤，您必须首先完成[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="9daf6-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="9daf6-106">若要完成本主题中的示例，您必须具有以下角色之一的 Microsoft Dynamics 365 Finance (Finance) 访问权限：</span><span class="sxs-lookup"><span data-stu-id="9daf6-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="9daf6-107">电子申报开发人员</span><span class="sxs-lookup"><span data-stu-id="9daf6-107">Electronic reporting developer</span></span>
- <span data-ttu-id="9daf6-108">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="9daf6-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="9daf6-109">系统管理员</span><span class="sxs-lookup"><span data-stu-id="9daf6-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="9daf6-110">导入 ER 配置</span><span class="sxs-lookup"><span data-stu-id="9daf6-110">Import ER configurations</span></span>

1.  <span data-ttu-id="9daf6-111">登录您的环境。</span><span class="sxs-lookup"><span data-stu-id="9daf6-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="9daf6-112">在默认仪表板中，选择**电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="9daf6-113">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="9daf6-114">在完成[配置 ER 格式以使用每个法人指定的参数](er-app-specific-parameters-configure-format.md)主题中的步骤时，将您从 Regulatory Configuration Services (RCS) 导出的配置导入到 Finance 的当前实例。</span><span class="sxs-lookup"><span data-stu-id="9daf6-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="9daf6-115">对于每个电子报告 (ER) 配置，请按照以下顺序执行以下步骤：数据模型、模型映射和格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="9daf6-116">选择**交易 \> 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="9daf6-117">选择**浏览**以 XML 格式选择所需 ER 配置的文件。</span><span class="sxs-lookup"><span data-stu-id="9daf6-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="9daf6-118">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-118">Select **OK**.</span></span>
    
    <span data-ttu-id="9daf6-119">下图显示了完成后必须具有的配置。</span><span class="sxs-lookup"><span data-stu-id="9daf6-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER 配置页](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="9daf6-121">为 DEMF 公司设置参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="9daf6-122">您可以使用 ER 框架为 ER 格式设置特定于应用程序的参数。</span><span class="sxs-lookup"><span data-stu-id="9daf6-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="9daf6-123">选择 **DEMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="9daf6-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="9daf6-124">在配置树中，选择**用于了解如何查找 LE 数据的格式**格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="9daf6-125">在操作窗格的**配置**选项卡的**应用程序特定参数**组中，选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="9daf6-127">在**应用程序特定参数**页面上，您可以为**用于了解如何查找 LE 数据的格式**格式的**选择器**数据源配置规则。</span><span class="sxs-lookup"><span data-stu-id="9daf6-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="9daf6-128">如果基本 ER 格式将包含多个**查找**类型的数据源，则必须先在**查找**快速选项卡上选择所需的数据源，然后才能开始为数据源配置规则集。</span><span class="sxs-lookup"><span data-stu-id="9daf6-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="9daf6-129">对于每个数据源，您可以为所选 ER 格式的每个版本配置单独的规则。</span><span class="sxs-lookup"><span data-stu-id="9daf6-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="9daf6-130">在基本 ER 格式的选定版本中可用的所有查找数据源的全部规则构成了 ER 格式的特定于应用程序的参数。</span><span class="sxs-lookup"><span data-stu-id="9daf6-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="9daf6-131">选择 ER 格式的版本 **1.1.1**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="9daf6-132">在**条件**快速选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="9daf6-133">在新记录的**代码**字段中，选择下拉箭头以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9daf6-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="9daf6-134">查找显示可供选择的税码列表。</span><span class="sxs-lookup"><span data-stu-id="9daf6-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="9daf6-135">此列表由在基本 ER 格式中配置的 **Model.Data.Tax** 数据源返回。</span><span class="sxs-lookup"><span data-stu-id="9daf6-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="9daf6-136">由于此数据源包含**名称**字段，因此每个税码的名称将显示在查找中。</span><span class="sxs-lookup"><span data-stu-id="9daf6-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="9daf6-138">选择 **VAT19** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="9daf6-139">在新记录的**查找结果**字段中，选择下拉箭头以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9daf6-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="9daf6-140">查找显示 TaxationLevel 格式枚举的值列表供选择。</span><span class="sxs-lookup"><span data-stu-id="9daf6-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="9daf6-141">请注意，如果选择德语作为用来登录的用户的首选语言，则查找中值的标签将以德语显示，前提是它们已在基本 ER 格式中进行翻译。</span><span class="sxs-lookup"><span data-stu-id="9daf6-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="9daf6-142">此外，如果查找数据源的标签已翻译，该标签将以用户的首选语言显示在**查找**选项卡上。</span><span class="sxs-lookup"><span data-stu-id="9daf6-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="9daf6-144">选择**正常税收**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="9daf6-145">通过添加此记录，您可以定义以下规则：每当请求**选择器**查找数据源，并且将 **VAT19** 税码作为参数传递时，**正常税收**将返回为请求的征税级别。</span><span class="sxs-lookup"><span data-stu-id="9daf6-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="9daf6-146">选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-147">在**代码**字段中，选择 **InVAT19** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="9daf6-148">在**查找结果**字段中，选择**正常税收**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="9daf6-149">再次选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-150">在**代码**字段中，选择 **VAT7** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="9daf6-151">在**查找结果**字段中，选择**减税**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="9daf6-152">再次选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-153">在**代码**字段中，选择 **InVAT7** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="9daf6-154">在**查找结果**字段中，选择**减税**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="9daf6-155">再次选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-156">在**代码**字段中，选择 **THIRD** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="9daf6-157">在**查找结果**字段中，选择**免税**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="9daf6-158">再次选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-159">在**代码**字段中，选择 **InVAT0** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="9daf6-160">在**查找结果**字段中，选择**免税**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="9daf6-161">再次选择**添加**，然后按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9daf6-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="9daf6-162">在**代码**字段中，选择**\*非空\*** 选项。</span><span class="sxs-lookup"><span data-stu-id="9daf6-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="9daf6-163">在**查找结果**字段中，选择**其他**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="9daf6-164">通过添加最后这个记录，您可以定义以下规则：每当作为参数传递的税码不满足任何先前的规则时，查找数据源将返回**其他**作为请求的征税级别。</span><span class="sxs-lookup"><span data-stu-id="9daf6-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="9daf6-166">在**状态**字段中，选择**已完成**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="9daf6-167">当您运行状态为**已完成**或**共享**的 ER 格式版本时，这组规则必须处于**已完成**状态。</span><span class="sxs-lookup"><span data-stu-id="9daf6-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="9daf6-168">否则，当运行**选择器**查找数据源时，如果尝试从此组规则加载数据，则基本 ER 格式的执行将被中断。</span><span class="sxs-lookup"><span data-stu-id="9daf6-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="9daf6-169">当您运行状态为**草稿**的 ER 格式版本时，基本 ER 格式可以访问这组规则，不管其状态如何。</span><span class="sxs-lookup"><span data-stu-id="9daf6-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="9daf6-170">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-170">Select **Save**.</span></span>
18. <span data-ttu-id="9daf6-171">关闭**应用程序特定参数**页面。</span><span class="sxs-lookup"><span data-stu-id="9daf6-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="9daf6-172">在 DEMF 公司中运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="9daf6-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="9daf6-173">在配置树中，选择**用于了解如何查找 LE 数据的格式**格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="9daf6-174">在操作窗格上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="9daf6-175">在显示的对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="9daf6-176">下载生成的报表并将其存储在本地。</span><span class="sxs-lookup"><span data-stu-id="9daf6-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="9daf6-177">在生成的报表中，注意 **InVAT7** 税码的汇总已进入**减税**级别，**VAT19** 和 **InVA19** 税码的汇总已进入**正常**级别。</span><span class="sxs-lookup"><span data-stu-id="9daf6-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="9daf6-178">此行为由依赖于法人的一组规则中的配置确定。</span><span class="sxs-lookup"><span data-stu-id="9daf6-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="9daf6-179">转到**税金 \> 间接税 \> 销售税 \> 销售税代码**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="9daf6-180">选择 **InVAT7** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="9daf6-181">在操作窗格的**销售税代码**选项卡上的**查询**组中，选择**已过帐的销售税**以查看有关每个税码的税金值和所应用税率的信息。</span><span class="sxs-lookup"><span data-stu-id="9daf6-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![已过帐的销售税页面](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="9daf6-183">关闭“已过帐的销售税”页。</span><span class="sxs-lookup"><span data-stu-id="9daf6-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="9daf6-184">为 USMF 公司设置参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="9daf6-185">选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="9daf6-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="9daf6-186">转到**组织管理 \> 电子申报 \> 配置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="9daf6-187">在配置树中，展开**用于了解参数化调用的数据模型**项，展开**用于了解参数化调用的格式**项，然后选择**用于了解如何查找 LE 数据的格式**格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="9daf6-188">在操作窗格的**配置**选项卡的**应用程序特定参数**组中，选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="9daf6-189">选择所选 ER 格式的版本 **1.1.1**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="9daf6-190">在**条件**快速选项卡上，选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="9daf6-191">在新记录的**代码**字段中，选择下拉箭头以打开查找。</span><span class="sxs-lookup"><span data-stu-id="9daf6-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="9daf6-192">现在，查找将显示 **USMF** 公司税务的税码列表供选择。</span><span class="sxs-lookup"><span data-stu-id="9daf6-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="9daf6-194">选择 **EXEMPT** 税码。</span><span class="sxs-lookup"><span data-stu-id="9daf6-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="9daf6-195">在新记录的**查找结果**字段中，选择**免税**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-195">In the **Lookup resul**t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="9daf6-196">再次选择**添加**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-196">Select **Add** again.</span></span>
11. <span data-ttu-id="9daf6-197">在新记录的**代码**字段中，选择**\*非空\*** 选项。</span><span class="sxs-lookup"><span data-stu-id="9daf6-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="9daf6-198">在新记录的**查找结果**字段中，选择**正常税收**值。</span><span class="sxs-lookup"><span data-stu-id="9daf6-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="9daf6-199">在**状态**字段中，选择**已完成**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="9daf6-200">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-200">Select **Save**.</span></span>

    ![ER 应用程序特定参数页面](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="9daf6-202">关闭**应用程序特定参数**页面。</span><span class="sxs-lookup"><span data-stu-id="9daf6-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="9daf6-203">在 USMF 公司中运行 ER 格式</span><span class="sxs-lookup"><span data-stu-id="9daf6-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="9daf6-204">在配置树中，选择**用于了解如何查找 LE 数据的格式**格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="9daf6-205">在操作窗格上，选择**运行**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="9daf6-206">在显示的对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="9daf6-207">下载生成的报表并将其存储在本地。</span><span class="sxs-lookup"><span data-stu-id="9daf6-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="9daf6-208">在生成的报表中，注意您现在已将相同的 ER 格式重复用于其他法人，但未对 ER 格式进行任何调整。</span><span class="sxs-lookup"><span data-stu-id="9daf6-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="9daf6-209">重用依赖于法人的参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="9daf6-210">导出参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-210">Export parameters</span></span>

1.  <span data-ttu-id="9daf6-211">转到**组织管理 \> 工作区 \> 电子申报**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="9daf6-212">选择**申报配置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="9daf6-213">在配置树中，选择**用于了解如何查找 LE 数据的格式**格式。</span><span class="sxs-lookup"><span data-stu-id="9daf6-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="9daf6-214">在操作窗格的**配置**选项卡的**应用程序特定参数**组中，选择**设置**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="9daf6-215">选择 ER 格式的版本 **1.1.1**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="9daf6-216">在操作窗格上，选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="9daf6-217">下载生成的文件并将其存储在本地。</span><span class="sxs-lookup"><span data-stu-id="9daf6-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="9daf6-218">现在，配置的一组特定于应用程序的参数已导出为 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="9daf6-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="9daf6-219">导入参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-219">Import parameters</span></span>

1.  <span data-ttu-id="9daf6-220">选择 ER 格式的版本 **1.1.2**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="9daf6-221">在操作窗格上，选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="9daf6-222">选择**是**以确认您要为此格式版本覆盖现有的特定于应用程序的参数。</span><span class="sxs-lookup"><span data-stu-id="9daf6-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="9daf6-223">选择**浏览**查找包含导出的版本 **1.1.1** 的应用程序特定参数的文件。</span><span class="sxs-lookup"><span data-stu-id="9daf6-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="9daf6-224">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="9daf6-224">Select **OK**.</span></span>

    <span data-ttu-id="9daf6-225">ER 格式的版本 **1.1.2** 现在具有与您最初为版本 **1.1.1** 版本配置的应用程序特定参数相同的参数。</span><span class="sxs-lookup"><span data-stu-id="9daf6-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="9daf6-226">请注意，ER 格式的特定于应用程序的参数依赖于法人。</span><span class="sxs-lookup"><span data-stu-id="9daf6-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="9daf6-227">要重用为另一个法人中的一个法人配置的应用程序特定参数，必须在登录第一个法人时将其导出，然后在登录另一个法人后将其导入。</span><span class="sxs-lookup"><span data-stu-id="9daf6-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="9daf6-228">您还可以使用此方法将最初在一个 Finance 实例中配置的与 ER 格式相关的特定于应用程序的参数转移到另一个 Finance 实例。</span><span class="sxs-lookup"><span data-stu-id="9daf6-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="9daf6-229">请注意，如果您为 ER 格式的一个版本配置了特定于应用程序的参数，并将同一格式的更高版本导入当前的 Finance 实例，则现有的特定于应用程序的参数将不会应用于导入的版本。</span><span class="sxs-lookup"><span data-stu-id="9daf6-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="9daf6-230">还应注意，当选择要导入的文件时，该文件中特定于应用程序的参数的结构将与为导入选择的 ER 格式中的**查找**类型的相应数据源的结构进行比较。</span><span class="sxs-lookup"><span data-stu-id="9daf6-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="9daf6-231">当每个特定于应用程序的参数的结构与为导入选择的 ER 格式的相应数据源的结构匹配时，将完成导入。</span><span class="sxs-lookup"><span data-stu-id="9daf6-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="9daf6-232">如果结构不匹配，则会收到一条警告消息，指示无法完成导入。</span><span class="sxs-lookup"><span data-stu-id="9daf6-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="9daf6-233">如果您强制完成导入，将清除所选 ER 格式的现有的特定于应用程序的参数，您必须从头开始进行设置。</span><span class="sxs-lookup"><span data-stu-id="9daf6-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="9daf6-234">特定于应用程序的参数和 ER 格式之间的关系</span><span class="sxs-lookup"><span data-stu-id="9daf6-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="9daf6-235">ER 格式与其特定于应用程序的参数之间的关系由 ER 格式不依赖于实例的唯一标识代码建立。</span><span class="sxs-lookup"><span data-stu-id="9daf6-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="9daf6-236">因此，当您从 Finance 中删除 ER 格式时，为 ER 格式配置的特定于应用程序的参数将保留在 Finance 的当前实例中。</span><span class="sxs-lookup"><span data-stu-id="9daf6-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="9daf6-237">只要将基本 ER 格式重新导入到此 Finance 实例中，就可以访问它们。</span><span class="sxs-lookup"><span data-stu-id="9daf6-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="9daf6-238">通过使用 ER 框架访问特定于应用程序的参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="9daf6-239">在前面的示例中，您已经通过使用 ER 框架访问了 ER 格式的特定于应用程序的参数。</span><span class="sxs-lookup"><span data-stu-id="9daf6-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="9daf6-240">这种方法不允许您限制对特定 ER 格式的应用程序特定参数的访问。</span><span class="sxs-lookup"><span data-stu-id="9daf6-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="9daf6-241">如果您必须应用此类限制，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="9daf6-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="9daf6-242">重用现有的 **ERSolutionAppSpecificParametersDesigner** 菜单项，或实现自己的 **ERSolutionAppSpecificParametersDesigner** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="9daf6-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual studio 页面](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="9daf6-244">按以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="9daf6-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="9daf6-245">创建一个新的菜单项按钮，并将其**数据源**属性设置为 **ERSolutionTable**，通过此方式将其链接到 **ERSolutionTable** 表中的相应记录。</span><span class="sxs-lookup"><span data-stu-id="9daf6-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual studio 页面](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="9daf6-247">创建一个简单的按钮，并覆盖**单击**方法，如以下示例所示。</span><span class="sxs-lookup"><span data-stu-id="9daf6-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="9daf6-248">通过使用此方法，您可以指定唯一的解决方案 ID（通过 **GUID** 值定义），以允许仅访问特定 ER 格式的应用程序特定参数以及从其派生的后代副本。</span><span class="sxs-lookup"><span data-stu-id="9daf6-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="9daf6-249">其他资源</span><span class="sxs-lookup"><span data-stu-id="9daf6-249">Additional resources</span></span>

[<span data-ttu-id="9daf6-250">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="9daf6-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="9daf6-251">配置 ER 格式以使用每个法人指定的参数</span><span class="sxs-lookup"><span data-stu-id="9daf6-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
