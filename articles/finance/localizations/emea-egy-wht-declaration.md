---
title: 埃及预缴税金申报
description: 本主题说明如何配置和生成埃及预缴税金申报。
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e0d13a2de9acaa8b1c896e130b4dabb222e45dcb
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881414"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="14fbe-103">埃及预缴税金申报 (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="14fbe-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="14fbe-104">概览</span><span class="sxs-lookup"><span data-stu-id="14fbe-104">Overview</span></span>
<span data-ttu-id="14fbe-105">本主题说明如何为埃及中的法人创建和生成预缴税金申报以及预缴税金申报表 41 和 11</span><span class="sxs-lookup"><span data-stu-id="14fbe-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="14fbe-106">所有埃及实体都必须准备表格 41，该表格概括了从本地供应商和服务提供商处保留的所有税款。</span><span class="sxs-lookup"><span data-stu-id="14fbe-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="14fbe-107">除表格 41 外，还必须生成表格 11 来详细说明从外国供应商处征收的所有保留税。</span><span class="sxs-lookup"><span data-stu-id="14fbe-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="14fbe-108">Dynamics 365 Finance 中的 **预缴税金申报** 报表包括以下报告：</span><span class="sxs-lookup"><span data-stu-id="14fbe-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="14fbe-109">申报单编号</span><span class="sxs-lookup"><span data-stu-id="14fbe-109">Declaration form No.</span></span> <span data-ttu-id="14fbe-110">41</span><span class="sxs-lookup"><span data-stu-id="14fbe-110">41</span></span>
- <span data-ttu-id="14fbe-111">申报单编号</span><span class="sxs-lookup"><span data-stu-id="14fbe-111">Declaration form No.</span></span> <span data-ttu-id="14fbe-112">11</span><span class="sxs-lookup"><span data-stu-id="14fbe-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="14fbe-113">先决条件</span><span class="sxs-lookup"><span data-stu-id="14fbe-113">Prerequisites</span></span>
<span data-ttu-id="14fbe-114">法人的主地址必须在埃及。</span><span class="sxs-lookup"><span data-stu-id="14fbe-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="14fbe-115">在 **功能管理** 工作区中，必须启用以下功能：</span><span class="sxs-lookup"><span data-stu-id="14fbe-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="14fbe-116">**全球预缴税金**</span><span class="sxs-lookup"><span data-stu-id="14fbe-116">**Global withholding tax**</span></span>

<span data-ttu-id="14fbe-117">有关如何启用功能的详细信息，请参阅[功能管理概述。](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="14fbe-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="14fbe-118">转到 **税** > **设置** > **参数** > **总帐参数**，然后在 **预缴税金** 选项卡上，将 **启用全球预缴税金** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="14fbe-119">在 **电子报告** 工作区中，从存储库中导入以下电子报告格式：</span><span class="sxs-lookup"><span data-stu-id="14fbe-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="14fbe-120">WHT 申报 Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="14fbe-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="14fbe-121">上面的格式基于 **税申报模型** 并使用 **税申报模型映射**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="14fbe-122">系统将自动导入此附加配置。</span><span class="sxs-lookup"><span data-stu-id="14fbe-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="14fbe-123">有关如何导入电子报告配置的更多信息，请参见[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)。</span><span class="sxs-lookup"><span data-stu-id="14fbe-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="14fbe-124">下载电子报告配置</span><span class="sxs-lookup"><span data-stu-id="14fbe-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="14fbe-125">埃及 WHT 申报表的实施基于电子报告 (ER) 配置。</span><span class="sxs-lookup"><span data-stu-id="14fbe-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="14fbe-126">有关可配置报告的功能和概念的更多信息，请参见[电子报告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md)。</span><span class="sxs-lookup"><span data-stu-id="14fbe-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="14fbe-127">对于生产和用户验收测试 (UAT) 环境，请按照[从 Lifecycle Services 下载电子报告配置](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)主题中的说明进行操作。</span><span class="sxs-lookup"><span data-stu-id="14fbe-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="14fbe-128">要在埃及法人中生成预缴税申报，您需要上传以下配置：</span><span class="sxs-lookup"><span data-stu-id="14fbe-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="14fbe-129">Tax declaration model.version.82.xml 或更高版本</span><span class="sxs-lookup"><span data-stu-id="14fbe-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="14fbe-130">Tax declaration model mapping.version.82.133.xml 或更高版本</span><span class="sxs-lookup"><span data-stu-id="14fbe-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="14fbe-131">WHT Declaration Excel (EG).version.82.21 或更高版本</span><span class="sxs-lookup"><span data-stu-id="14fbe-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="14fbe-132">从 Lifecycle Services (LCS) 或全局存储库下载完 ER 配置后，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="14fbe-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="14fbe-133">转到 **电子申报** 工作区中，并选择 **报告配置** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="14fbe-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="14fbe-134">在 **配置** 页上的“操作”窗格中，选择 **交换 > 从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="14fbe-135">按照先前项目符号中列出的顺序上传所有文件。</span><span class="sxs-lookup"><span data-stu-id="14fbe-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="14fbe-136">在上传所有配置之后，配置树应该会出现在 Finance 中。</span><span class="sxs-lookup"><span data-stu-id="14fbe-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="14fbe-137">设置特定于应用程序的参数</span><span class="sxs-lookup"><span data-stu-id="14fbe-137">Set up application-specific parameters</span></span>

<span data-ttu-id="14fbe-138">特定于应用程序的参数选项允许用户根据 **预扣税项目组** 配置或查找定义中建立的其他标准来建立以下相关标准：如何在生成的报告的每一行中分类和计算税收交易。</span><span class="sxs-lookup"><span data-stu-id="14fbe-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="14fbe-139">预缴税申报表 41 包含一个特定的列，在该列中，必须根据名为 **折扣代码类型** 的税务主管机构对预缴税金交易进行分类。</span><span class="sxs-lookup"><span data-stu-id="14fbe-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="14fbe-140">在过帐交易时，不要将这些新分类作为新录入数据包括在内，而是要根据 **配置** > **设置特定于应用程序的参数** > **设置** 中引入的不同查找来确定分类，以满足埃及预缴税报告的要求。</span><span class="sxs-lookup"><span data-stu-id="14fbe-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="14fbe-141">以下配置用于在预缴税申报表 41 报告中对交易进行分类：</span><span class="sxs-lookup"><span data-stu-id="14fbe-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="14fbe-142">**DiscountTaxTypeLookup** -> 第 18 列</span><span class="sxs-lookup"><span data-stu-id="14fbe-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="14fbe-143">完成以下步骤以设置用于生成 WHT 申报和相关帐簿报告的不同查找。</span><span class="sxs-lookup"><span data-stu-id="14fbe-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="14fbe-144">在 **电子报告** 工作区中，选择 **配置** > **设置**，以设置规则来识别在 WHT 申报报表中如何对交易进行分类。</span><span class="sxs-lookup"><span data-stu-id="14fbe-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="14fbe-145">选择当前版本，然后在 **查询** 快速选项卡上选择查找名称。</span><span class="sxs-lookup"><span data-stu-id="14fbe-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="14fbe-146">例如，**DiscountTaxTypeLookup**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="14fbe-147">此查找标识了税务机关要求的折扣类型的列表。</span><span class="sxs-lookup"><span data-stu-id="14fbe-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="14fbe-148">在 **条件** 快速选项卡上，选择 **添加**，并在 **查询结果** 列内的新行中，选择代表 **第 18 列** 中的类别的相关行。</span><span class="sxs-lookup"><span data-stu-id="14fbe-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="14fbe-149">在 **预扣税项目组** 列中，选择用于识别分类的相关代码。</span><span class="sxs-lookup"><span data-stu-id="14fbe-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="14fbe-150">例如，**允许的折扣**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="14fbe-151">对所有可用的查找重复步骤 3 和 4。</span><span class="sxs-lookup"><span data-stu-id="14fbe-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="14fbe-152">再次选择 **添加**，以包含最终记录行，并在 **查询结果** 列中，选择 **不适用**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="14fbe-153">在其余列中，选择 **非空**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="14fbe-154">设置总帐参数</span><span class="sxs-lookup"><span data-stu-id="14fbe-154">Set up General ledger parameters</span></span>

<span data-ttu-id="14fbe-155">要在 Microsoft Excel 中生成 WHT 申报表报告，请在 **总帐参数** 页上定义 ER 格式。</span><span class="sxs-lookup"><span data-stu-id="14fbe-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="14fbe-156">转到 **税** > **设置** > **总帐参数**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="14fbe-157">在 **预扣税** 选项卡上的 **WHT 申报格式映射** 字段中，选择 **WHT 申报 Excel (EG)**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="14fbe-158">如果您将该字段留空，则标准销售税报告将以 SSRS 格式生成。</span><span class="sxs-lookup"><span data-stu-id="14fbe-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![申报表](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="14fbe-160">生成预扣税申报表</span><span class="sxs-lookup"><span data-stu-id="14fbe-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="14fbe-161">针对特定时期准备和提交预扣税申报表的过程基于在结算和过帐纳税作业期间过帐的预扣税交易。</span><span class="sxs-lookup"><span data-stu-id="14fbe-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="14fbe-162">有关全球预缴税金的更多信息，请参见[全球预缴税金](../general-ledger/global-withholding-tax-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="14fbe-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="14fbe-163">完成以下步骤以生成纳税申报报表：</span><span class="sxs-lookup"><span data-stu-id="14fbe-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="14fbe-164">转到 **税** > **申报** > **预缴税金**> \**预缴税金付款*。</span><span class="sxs-lookup"><span data-stu-id="14fbe-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="14fbe-165">选择结算期，然后选择报告的开始日期。</span><span class="sxs-lookup"><span data-stu-id="14fbe-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="14fbe-166">输入交易日期，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="14fbe-167">在打开的对话框中，选择一种或多种表单类型：**表单编号 41**、**表单编号 11** 或 **无**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="14fbe-168">如果选择 **无**，将生成标准报告。</span><span class="sxs-lookup"><span data-stu-id="14fbe-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="14fbe-169">选择语言。</span><span class="sxs-lookup"><span data-stu-id="14fbe-169">Select the language.</span></span> <span data-ttu-id="14fbe-170">所有报告均翻译成 **en-us** 和 **ar-eg**。</span><span class="sxs-lookup"><span data-stu-id="14fbe-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="14fbe-171">输入将要支付税款的银行的分支机构和名称。</span><span class="sxs-lookup"><span data-stu-id="14fbe-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="14fbe-172">选择业务类型，然后输入支票和单据编号。</span><span class="sxs-lookup"><span data-stu-id="14fbe-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="14fbe-173">输入实体类型。</span><span class="sxs-lookup"><span data-stu-id="14fbe-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="14fbe-174">输入为分配表单而注册的人员的姓名，然后选择 **确定** 以确认生成报告。</span><span class="sxs-lookup"><span data-stu-id="14fbe-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
