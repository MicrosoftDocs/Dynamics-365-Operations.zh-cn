---
title: 导入供应商目录
description: 此主题介绍供应商目录数据导入流程。
author: RichardLuan
manager: tfehr
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: riluan
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: f752e6c42653d7ac39e011e71d0d31f936996499
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260519"
---
# <a name="import-vendor-catalogs"></a><span data-ttu-id="7ace6-103">导入供应商目录</span><span class="sxs-lookup"><span data-stu-id="7ace6-103">Import vendor catalogs</span></span>

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a><span data-ttu-id="7ace6-104">供应商目录导入</span><span class="sxs-lookup"><span data-stu-id="7ace6-104">Vendor catalogs import</span></span>

<span data-ttu-id="7ace6-105">在 Dynamics 365 Supply Chain Management 中，采购专员可以创建和维护公司员工的目录以在订购供内部使用的物料和服务时使用。</span><span class="sxs-lookup"><span data-stu-id="7ace6-105">In Dynamics 365 Supply Chain Management, purchasing professionals can create and maintain catalogs for company employees to use when they order items and services for internal use.</span></span> <span data-ttu-id="7ace6-106">若要创建采购目录，您可以通过导入产品目录数据或通过将产品目录数据手动添加到基础产品，添加要向员工提供的物料和服务。</span><span class="sxs-lookup"><span data-stu-id="7ace6-106">To create a procurement catalog, you can add the items and services that you want to make available to employees, either by importing the product catalog data or by manually adding the product catalog data to the product master.</span></span> 

<span data-ttu-id="7ace6-107">可以上传客户从 Microsoft Dynamics 365 客户端提交的目录数据。</span><span class="sxs-lookup"><span data-stu-id="7ace6-107">You can upload catalog data submitted by a vendor from the Microsoft Dynamics 365 client.</span></span>

<span data-ttu-id="7ace6-108">在目录维护请求 (CMR) 文件的窗体中，供应商提交给您的产品数据必须是 XML 文件格式。</span><span class="sxs-lookup"><span data-stu-id="7ace6-108">The product data that a vendor submits to you, in the form of a catalog maintenance request (CMR) file, must be in XML file format.</span></span> <span data-ttu-id="7ace6-109">CMR 文件应包含供应商向贵公司提供的产品的详细信息。</span><span class="sxs-lookup"><span data-stu-id="7ace6-109">The CMR file should contain the details for the products that the vendor supplies to your company.</span></span>

## <a name="import-vendor-catalog-data"></a><span data-ttu-id="7ace6-110">导入供应商目录数据</span><span class="sxs-lookup"><span data-stu-id="7ace6-110">Import vendor catalog data</span></span>

<span data-ttu-id="7ace6-111">若要导入供应商目录数据，您必须完成以下任务：</span><span class="sxs-lookup"><span data-stu-id="7ace6-111">To import vendor catalog data, you must complete the following tasks:</span></span>

1. <span data-ttu-id="7ace6-112">在数据管理工作区（已在其中定义了数据映射规则）中设置一个项目。</span><span class="sxs-lookup"><span data-stu-id="7ace6-112">Set up a project in the Data management workspace where you have defined your data mapping rules.</span></span> <span data-ttu-id="7ace6-113">选择 **数据管理**，然后选择 **设置数据项目的角色**。</span><span class="sxs-lookup"><span data-stu-id="7ace6-113">Select **Data management** and then select **Set up roles for data projects**.</span></span>

2. <span data-ttu-id="7ace6-114">设置采购类别层次结构，并将您的供应商分配到采购类别。</span><span class="sxs-lookup"><span data-stu-id="7ace6-114">Set up a procurement category hierarchy, and assign your vendors to procurement categories.</span></span> <span data-ttu-id="7ace6-115">如果您使用了商品代码，则添加这些商品代码到采购类别中。</span><span class="sxs-lookup"><span data-stu-id="7ace6-115">If you use commodity codes, add the commodity codes to the procurement categories.</span></span> <span data-ttu-id="7ace6-116">有关设置采购类别层次结构的信息，请参阅[设置采购类别层次结构](../procurement/tasks/set-up-procurement-category-hierarchy.md)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-116">For information about setting up a procurement category hierarchy, see [Set up a procurement category hierarchy](../procurement/tasks/set-up-procurement-category-hierarchy.md).</span></span>

3. <span data-ttu-id="7ace6-117">配置目录导入的供应商。</span><span class="sxs-lookup"><span data-stu-id="7ace6-117">Configure the vendor for catalog import.</span></span> <span data-ttu-id="7ace6-118">选择供应商，然后选择 **采购**  >  **设置**  >  **配置目录导入的供应商**。</span><span class="sxs-lookup"><span data-stu-id="7ace6-118">Select a vendor, and then select **Procurement** > **Set up** > **Configure vendor for catalog import**.</span></span>

4. <span data-ttu-id="7ace6-119">配置目录导入的工作流。</span><span class="sxs-lookup"><span data-stu-id="7ace6-119">Configure workflow for catalog import.</span></span> <span data-ttu-id="7ace6-120">创建一个 CMR 文件模板，然后将其与供应商共享。</span><span class="sxs-lookup"><span data-stu-id="7ace6-120">Create a CMR file template and share this with your vendor.</span></span>

5. <span data-ttu-id="7ace6-121">选择 **采购** \> **通用** \> **目录** \> **供应商目录** 以创建供应商目录。</span><span class="sxs-lookup"><span data-stu-id="7ace6-121">Select **Procurement and sourcing** \> **Common** \> **Catalogs** \> **Vendor catalogs** to create a vendor catalog.</span></span> <span data-ttu-id="7ace6-122">在此目录中对您从供应商处接收的目录维护请求 (CMR) 文件进行分组。</span><span class="sxs-lookup"><span data-stu-id="7ace6-122">The catalog maintenance request (CMR) files that you receive from your vendor are grouped in this catalog.</span></span> 

6. <span data-ttu-id="7ace6-123">上载 CMR 文件。</span><span class="sxs-lookup"><span data-stu-id="7ace6-123">Upload the CMR file.</span></span>

7. <span data-ttu-id="7ace6-124">复查、审核或拒绝供应商目录中的产品。</span><span class="sxs-lookup"><span data-stu-id="7ace6-124">Review, approve, or reject the products in the vendor catalog.</span></span> <span data-ttu-id="7ace6-125">将把这些产品自动映射到采购类别。</span><span class="sxs-lookup"><span data-stu-id="7ace6-125">The products are automatically mapped to the procurement categories.</span></span> 

<span data-ttu-id="7ace6-126">将已审核的产品添加到基础产品，并将它们发放给所选的法人。</span><span class="sxs-lookup"><span data-stu-id="7ace6-126">Approved products are added to the product master and are released to the selected legal entities.</span></span> <span data-ttu-id="7ace6-127">只有已审核的产品能添加到采购目录。</span><span class="sxs-lookup"><span data-stu-id="7ace6-127">Only approved products can be added to the procurement catalog.</span></span>

## <a name="generate-a-catalog-import-file-template"></a><span data-ttu-id="7ace6-128">生成目录导入文件模板</span><span class="sxs-lookup"><span data-stu-id="7ace6-128">Generate a catalog import file template</span></span>

<span data-ttu-id="7ace6-129">目录导入文件模板是您用于为供应商产品创建的 CMR 文件的 XSD 文件。</span><span class="sxs-lookup"><span data-stu-id="7ace6-129">The catalog import file template is an XSD file that you use to create a CMR file for a vendor's products.</span></span> <span data-ttu-id="7ace6-130">您可以使用 CMR 文件创建新的目录，替换现有目录或修改现有的目录。</span><span class="sxs-lookup"><span data-stu-id="7ace6-130">You can use the CMR file to create a new catalog, replace an existing catalog, or modify an existing catalog.</span></span>

1. <span data-ttu-id="7ace6-131">选择 **采购** \> **目录** \> **供应商目录**，然后双击要使用的目录。</span><span class="sxs-lookup"><span data-stu-id="7ace6-131">Select **Procurement and sourcing** \> **Catalogs** \> **Vendor  catalogs** and double-click the catalog that you want  to work with.</span></span>

2. <span data-ttu-id="7ace6-132">下载一个当前目录导入模板（XSD 文件）。</span><span class="sxs-lookup"><span data-stu-id="7ace6-132">Download a current catalog import template (XSD file).</span></span> <span data-ttu-id="7ace6-133">在 **更新目录** 页 **操作窗格** 上 **目录** 选项卡的 **相关信息** 组中，单击 **生成目录模板**，然后选择 **采购类别**。</span><span class="sxs-lookup"><span data-stu-id="7ace6-133">On the **Update catalog** page, on the **Action Pane**, on the **Catalogs** tab, in the **Related information** group, click **Generate catalog template** and select **Procurement category**.</span></span>

    - <span data-ttu-id="7ace6-134">可使用 **采购类别** 选项生成包括供应商授权提供产品的采购类别的目录模板。</span><span class="sxs-lookup"><span data-stu-id="7ace6-134">With the **Procurement category** option you can generate a catalog template that includes the procurement categories in which the vendor is authorized to provide products.</span></span>

3. <span data-ttu-id="7ace6-135">在 **另存为** 对话框中，选择要存储目录文件模板和保存该文件的位置。</span><span class="sxs-lookup"><span data-stu-id="7ace6-135">In the **Save as** dialog box, select the location where you want to store the catalog file template and save the file.</span></span>

<span data-ttu-id="7ace6-136">有关更多信息和示例，请参阅以下博客文章：[Dynamics AX 中的供应商目录](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/)。</span><span class="sxs-lookup"><span data-stu-id="7ace6-136">For more information and for examples, refer to this blog post: [Vendor catalogs in Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]