---
title: 配置中国的税务集成
description: 本主题描述配置中国的税务集成的流程。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, VATInvoiceDescTable_CN, TaxProfileTable_CN
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265264
ms.assetid: e5dbbbe1-935f-4fb4-a014-447916051628
ms.search.region: China (PRC)
ms.author: leguo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 082b9b95af6b2c49627fd60382c9d726c22f1de2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175263"
---
# <a name="configure-tax-integration-for-china"></a><span data-ttu-id="e1275-103">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="e1275-103">Configure tax integration for China</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1275-104">本主题描述配置中国的税务集成的流程。</span><span class="sxs-lookup"><span data-stu-id="e1275-104">This topic describes the process for configuring tax integration for China.</span></span>

## <a name="prerequisites-for-dynamics-365-finance-version-100-and-later"></a><span data-ttu-id="e1275-105">Dynamics 365 Finance 版本 10.0 和更高版本的先决条件</span><span class="sxs-lookup"><span data-stu-id="e1275-105">Prerequisites for Dynamics 365 Finance version 10.0 and later</span></span>

<span data-ttu-id="e1275-106">要让系统生成此代码以充当导出的文件中的输出，必须按照以下任务的列出顺序完成这些任务。</span><span class="sxs-lookup"><span data-stu-id="e1275-106">To enable the system to generate this code as output in the exported file, you must complete the following tasks in the order in which they are listed.</span></span>

| <span data-ttu-id="e1275-107">必备项</span><span class="sxs-lookup"><span data-stu-id="e1275-107">Prerequisite</span></span> | <span data-ttu-id="e1275-108">说明</span><span class="sxs-lookup"><span data-stu-id="e1275-108">Description</span></span> | <span data-ttu-id="e1275-109">更多信息</span><span class="sxs-lookup"><span data-stu-id="e1275-109">More information</span></span> |
|------------|-------------|------------------------|
| <span data-ttu-id="e1275-110">设置产品分类的层次结构。</span><span class="sxs-lookup"><span data-stu-id="e1275-110">Set up a hierarchy for product classification.</span></span> | <span data-ttu-id="e1275-111">必须为货物和服务的分配设置类别层次结构，还必须将产品物料（货物或服务）与类别节点关联。</span><span class="sxs-lookup"><span data-stu-id="e1275-111">You must set up a category hierarchy for the classification of goods and services, and you must relate product items (goods or services) with category nodes.</span></span> <span data-ttu-id="e1275-112">通过使用此功能，可以设置公司中需要的所有层次结构。</span><span class="sxs-lookup"><span data-stu-id="e1275-112">By using this functionality, you can set up any hierarchy that is required in a company.</span></span> | [<span data-ttu-id="e1275-113">创建产品分类的层次结构</span><span class="sxs-lookup"><span data-stu-id="e1275-113">Create a hierarchy of product classification</span></span>](../../supply-chain/pim/tasks/create-hierarchy-product-classification.md) |
| <span data-ttu-id="e1275-114">为税务集成模板分配新层次结构。</span><span class="sxs-lookup"><span data-stu-id="e1275-114">Assign the new hierarchy to a tax integration profile.</span></span> | <span data-ttu-id="e1275-115">转到**应收帐款 &gt; 税务集成 &gt; 税务集成模板**，然后在**商品代码层次结构**字段中选择新类别。</span><span class="sxs-lookup"><span data-stu-id="e1275-115">Go to **Accounts receivable &gt; Tax integration &gt; Tax integration profiles**, and then, in the **Commodity code hierarchy** field, select the new category.</span></span> | |
| <span data-ttu-id="e1275-116">选择发票行的商品代码。</span><span class="sxs-lookup"><span data-stu-id="e1275-116">Select a commodity code for invoice lines.</span></span> | <span data-ttu-id="e1275-117">对于与产品物料无关的发票行（如普通发票行和项目发票行），或基于工时、支出和费用日记帐创建的发票行，可在**税务集成模板**页面中设置默认商品代码。</span><span class="sxs-lookup"><span data-stu-id="e1275-117">For invoice lines that aren't related to product items (such as free text invoice lines and project invoice lines), or invoice lines that are created based on hour, expense, and fee journals, you can set up a default commodity code on the **Tax integration profiles** page.</span></span> | |
| <span data-ttu-id="e1275-118">标识用于导入文件的模型映射。</span><span class="sxs-lookup"><span data-stu-id="e1275-118">Identify the model mapping to use for import files.</span></span> | <span data-ttu-id="e1275-119">转到**应收帐款 &gt; 定期任务 &gt; 增值税发票金税集成**，然后选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="e1275-119">Go to **Accounts receivable &gt; Periodic tasks &gt; VAT invoice integration**, and then select **Import**.</span></span> <span data-ttu-id="e1275-120">为来自其中一个提供商（Aisino 或 BaiWang）的导入文件选择模型映射，具体取决于公司将导出的发票与哪个提供商的软件集成。</span><span class="sxs-lookup"><span data-stu-id="e1275-120">Select the model mapping for the import file from one of the providers (Aisino or BaiWang), depending on which provider's software the company integrates exported invoices with.</span></span> <span data-ttu-id="e1275-121">此项选择应仅进行一次。</span><span class="sxs-lookup"><span data-stu-id="e1275-121">This selection should be made only one time.</span></span> <span data-ttu-id="e1275-122">（系统将保存选择的值。）</span><span class="sxs-lookup"><span data-stu-id="e1275-122">(The system saves the selected value.)</span></span><ul><li><span data-ttu-id="e1275-123">若要导入文本文件（\<file name\>\_invoicing result.TXT），请将**导入 BaiWang TXT 文件**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e1275-123">To import a text file (\<file name\>\_invoicing result.TXT), set the **Import BaiWang TXT file** option to **Yes**.</span></span> <span data-ttu-id="e1275-124">然后，在**模型映射**字段中，选择 **BaiWang – txt 文件映射**。</span><span class="sxs-lookup"><span data-stu-id="e1275-124">Then, in the **Model mapping** field, select **BaiWang – txt file mapping**.</span></span></li><li><span data-ttu-id="e1275-125">要导入来自 Aisino 的文本文件或来自 BaiWang 的 XML 文件（从 BaiWang 软件导出的文件），请将**导入 BaiWang txt 文件**选项设置为**否**。</span><span class="sxs-lookup"><span data-stu-id="e1275-125">To import a text file from Aisino or an XML file from BaiWang (exported files from BaiWang software), set the **Import BaiWang txt file** option to **No**.</span></span> <span data-ttu-id="e1275-126">然后，在**模型映射**字段中，选择 **Aisino 或 BaiWang – xml 文件映射**。</span><span class="sxs-lookup"><span data-stu-id="e1275-126">Then, in the **Model mapping** field, select **Aisino or BaiWang – xml file mapping**.</span></span></li></ul> | |
| <span data-ttu-id="e1275-127">从 Microsoft Dynamics Lifecycle Services (LCS) 导入配置。</span><span class="sxs-lookup"><span data-stu-id="e1275-127">Import configurations from Microsoft Dynamics Lifecycle Services (LCS).</span></span> | <span data-ttu-id="e1275-128">对于与 Aisino 软件的集成，必须从 LCS 导入以下配置：</span><span class="sxs-lookup"><span data-stu-id="e1275-128">For integration with Aisino software, you must import the following configurations from LCS:</span></span><ul><li><span data-ttu-id="e1275-129">GoldenTax 模型</span><span class="sxs-lookup"><span data-stu-id="e1275-129">GoldenTax model</span></span></li><li><span data-ttu-id="e1275-130">GST 导出模型映射 (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-130">GST Export model mapping (CN)</span></span></li><li><span data-ttu-id="e1275-131">GTS 导出格式 (Aisino) (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-131">GTS Export format (Aisino) (CN)</span></span></li><li><span data-ttu-id="e1275-132">GTS 导入模型映射 (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-132">GTS Import model mapping (CN)</span></span></li><li><span data-ttu-id="e1275-133">GTS 导入格式 (Aisino) (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-133">GTS Import format (Aisino) (CN)</span></span></li></ul><span data-ttu-id="e1275-134">对于与 BaiWang 软件的集成，必须从 LCS 导入以下配置：</span><span class="sxs-lookup"><span data-stu-id="e1275-134">For integration with BaiWang software, you must import the following configurations from LCS:</span></span><ul><li><span data-ttu-id="e1275-135">GoldenTax 模型</span><span class="sxs-lookup"><span data-stu-id="e1275-135">GoldenTax model</span></span></li><li><span data-ttu-id="e1275-136">GST 导出模型映射 (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-136">GST Export model mapping (CN)</span></span></li><li><span data-ttu-id="e1275-137">GTS 导入模型映射 (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-137">GTS Import model mapping (CN)</span></span></li><li><span data-ttu-id="e1275-138">GTS 导出格式 (BaiWang) (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-138">GTS Export format (BaiWang) (CN)</span></span></li><li><span data-ttu-id="e1275-139">GTS 导入格式 (BaiWang)-txt) (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-139">GTS Import format (BaiWang)-txt) (CN)</span></span></li><li><span data-ttu-id="e1275-140">GTS 导入格式 (BaiWang)-xml) (CN)</span><span class="sxs-lookup"><span data-stu-id="e1275-140">GTS Import format (BaiWang-xml) (CN)</span></span></li></ul> | [<span data-ttu-id="e1275-141">从 Lifecycle Services 下载电子申报配置</span><span class="sxs-lookup"><span data-stu-id="e1275-141">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) |

> [!NOTE]
> <span data-ttu-id="e1275-142">可将作为导入后的响应收到的文本文件导入 BaiWang 软件。</span><span class="sxs-lookup"><span data-stu-id="e1275-142">You can import a text file that is received as a response after import to BaiWang software.</span></span> <span data-ttu-id="e1275-143">也可以导入从 BaiWang 软件导出的 XML 文件。</span><span class="sxs-lookup"><span data-stu-id="e1275-143">Alternatively, you can import XML files that are exported from BaiWang software.</span></span>

## <a name="configure-tax-integration-for-china"></a><span data-ttu-id="e1275-144">配置中国的税务集成</span><span class="sxs-lookup"><span data-stu-id="e1275-144">Configure tax integration for China</span></span>

<span data-ttu-id="e1275-145">必须先开启，才能配置税务集成。</span><span class="sxs-lookup"><span data-stu-id="e1275-145">Before you can configure tax integration, you must turn it on.</span></span> <span data-ttu-id="e1275-146">转到**应收帐款 \> 设置 \> 应收帐款参数**，然后在**分类帐和销售税** 选项卡的**常规**快速选项卡上，将**与税收系统集成** 选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="e1275-146">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**, and then, on the **Ledger and sales tax** tab, on the **General** FastTab, set the **Integration with tax system** option to **Yes**.</span></span>

<span data-ttu-id="e1275-147">若要配置中国的税收集成，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e1275-147">To configure tax integration for China, follow these steps.</span></span>

1. <span data-ttu-id="e1275-148">在**增值税发票描述**页中，创建新的增值税（VAT）发票描述。</span><span class="sxs-lookup"><span data-stu-id="e1275-148">On the **VAT invoice description** page, create a new value-added tax (VAT) invoice description.</span></span> <span data-ttu-id="e1275-149">例如，可能必须设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e1275-149">For example, you might have to set the following values:</span></span>

    - <span data-ttu-id="e1275-150">**增值税发票描述 ID：** InvoiceDescID01</span><span class="sxs-lookup"><span data-stu-id="e1275-150">**VAT invoice description ID:** InvoiceDescID01</span></span>
    - <span data-ttu-id="e1275-151">**描述：** 设备</span><span class="sxs-lookup"><span data-stu-id="e1275-151">**Description:** 设备</span></span>
    - <span data-ttu-id="e1275-152">**单位：** 箱</span><span class="sxs-lookup"><span data-stu-id="e1275-152">**Unit:** Box</span></span>

2. <span data-ttu-id="e1275-153">在**税务集成模板**页中，创建一个新税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="e1275-153">On the **Tax integration profiles** page, create a new tax integration profile.</span></span> <span data-ttu-id="e1275-154">可以设置导入或导出发票时使用的税务集成模板。</span><span class="sxs-lookup"><span data-stu-id="e1275-154">You can set up tax integration profiles that are used when invoices are imported or exported.</span></span> <span data-ttu-id="e1275-155">在税务集成模板中，可以指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="e1275-155">In the tax integration profile, you can specify the following information:</span></span>

    - <span data-ttu-id="e1275-156">增值税代码</span><span class="sxs-lookup"><span data-stu-id="e1275-156">Sales tax code</span></span>
    - <span data-ttu-id="e1275-157">最大发票金额</span><span class="sxs-lookup"><span data-stu-id="e1275-157">Maximum invoice amount</span></span>
    - <span data-ttu-id="e1275-158">金税发票的默认描述和单位</span><span class="sxs-lookup"><span data-stu-id="e1275-158">Default description and unit for the golden tax invoice</span></span>

    <span data-ttu-id="e1275-159">也可以指定是否应包含普通增值税发票。</span><span class="sxs-lookup"><span data-stu-id="e1275-159">You can also specify whether non-deductible VAT invoices should be included.</span></span>

<span data-ttu-id="e1275-160">下图显示了税务集成流程。</span><span class="sxs-lookup"><span data-stu-id="e1275-160">The following illustration shows the tax integration process.</span></span>

<span data-ttu-id="e1275-161">[![税务集成流程](./media/ic666469.gif)](./media/ic666469.gif)</span><span class="sxs-lookup"><span data-stu-id="e1275-161">[![Tax integration process](./media/ic666469.gif)](./media/ic666469.gif)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1275-162">其他资源</span><span class="sxs-lookup"><span data-stu-id="e1275-162">Additional resources</span></span>

- <span data-ttu-id="e1275-163">[导入中国金税数据实体](apac-chn-import-golden-tax-data-entity.md)（不适用于 Microsoft Dynamics 365 for Finance and Operations 版本 10.0 \[2019 年四月\]及更高版本）</span><span class="sxs-lookup"><span data-stu-id="e1275-163">[Import the Chinese Golden Tax data entity](apac-chn-import-golden-tax-data-entity.md) (Not applicable for Microsoft Dynamics 365 for Finance and Operations version 10.0 \[April 2019\] and later)</span></span>
- [<span data-ttu-id="e1275-164">增值税客户发票的中国税务集成修改常见问题</span><span class="sxs-lookup"><span data-stu-id="e1275-164">Chinese tax integration modification for VAT customer invoices FAQ</span></span>](apac-chn-tax-integration-vat-customer-invoices.md)
- [<span data-ttu-id="e1275-165">设置中国的基本税务集成模板</span><span class="sxs-lookup"><span data-stu-id="e1275-165">Set up basic tax integration profile for China</span></span>](./tasks/set-up-basic-tax-integration-profile-china.md)
