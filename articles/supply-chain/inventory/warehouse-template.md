---
title: 使用仓库配置模板设置仓库
description: 此主题介绍如何使用仓库配置模板设置仓库。
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 66fdc26b0b967a04a3c6a6e3444e00b1372dc504
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204002"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="9163f-103">使用仓库配置模板设置仓库</span><span class="sxs-lookup"><span data-stu-id="9163f-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9163f-104">此主题介绍如何使用仓库配置模板设置仓库。</span><span class="sxs-lookup"><span data-stu-id="9163f-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="9163f-105">有多个预定义的配置模板可供使用。</span><span class="sxs-lookup"><span data-stu-id="9163f-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="9163f-106">有关如何使用这些模板的信息，请参阅[配置数据模板](../../dev-itpro/data-entities/configuration-data-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="9163f-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="9163f-107">配置模板可能有用的方案</span><span class="sxs-lookup"><span data-stu-id="9163f-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="9163f-108">配置模板在许多方案中都有用。</span><span class="sxs-lookup"><span data-stu-id="9163f-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="9163f-109">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="9163f-109">Here are some examples:</span></span>

- <span data-ttu-id="9163f-110">您完成了一个配置设置并在测试环境中进行了测试，您现在想要将该设置复制到生产环境。</span><span class="sxs-lookup"><span data-stu-id="9163f-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="9163f-111">您想要向多个法人推出该仓库设置或在相同法人中创建新的仓库。</span><span class="sxs-lookup"><span data-stu-id="9163f-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="9163f-112">您想要尽快为演示仓库功能做好准备。</span><span class="sxs-lookup"><span data-stu-id="9163f-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="9163f-113">您想要现有的物料和仓库使用仓库管理中的功能，而不是使用库存管理中的功能。</span><span class="sxs-lookup"><span data-stu-id="9163f-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="9163f-114">此主题主要介绍这些方案中的第一个方案。</span><span class="sxs-lookup"><span data-stu-id="9163f-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="9163f-115">它演示了您可以如何使用配置模板将测试环境中的配置设置复制到生产环境。</span><span class="sxs-lookup"><span data-stu-id="9163f-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="9163f-116">将测试环境中的配置设置复制到生产环境</span><span class="sxs-lookup"><span data-stu-id="9163f-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="9163f-117">在此方案中，测试环境中已经存在用于仓库和一些交易流程的配置设置。</span><span class="sxs-lookup"><span data-stu-id="9163f-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="9163f-118">您现在想要将仓库的配置设置从测试环境复制到生产环境。</span><span class="sxs-lookup"><span data-stu-id="9163f-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="9163f-119">重要的一点是在复制配置设置时包括其他相关设置数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="9163f-120">例如，您想要复制测试环境中的设置以设置产品。</span><span class="sxs-lookup"><span data-stu-id="9163f-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="9163f-121">但在创建该产品前，您不能设置产品的固定领料库位。</span><span class="sxs-lookup"><span data-stu-id="9163f-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="9163f-122">尽管单个配置模板不支持这种类型的依赖项，但存在支持它的默认数据模板。</span><span class="sxs-lookup"><span data-stu-id="9163f-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="9163f-123">您可以将这些默认数据模板轻松包括在配置流程中。</span><span class="sxs-lookup"><span data-stu-id="9163f-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="9163f-124">导出默认仓库模板</span><span class="sxs-lookup"><span data-stu-id="9163f-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="9163f-125">打开**数据管理**工作区。</span><span class="sxs-lookup"><span data-stu-id="9163f-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9163f-126">如果您是第一次使用此工作区，必须加载所有数据实体后才能继续。</span><span class="sxs-lookup"><span data-stu-id="9163f-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="9163f-127">选择**模板**磁贴，然后选择**加载默认模板**以加载默认模板。</span><span class="sxs-lookup"><span data-stu-id="9163f-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9163f-128">**加载默认模板**仅在**增强型**视图中可用。</span><span class="sxs-lookup"><span data-stu-id="9163f-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="9163f-129">选择**框架参数**，然后在**查看默认值**字段中选择**增强型视图**。</span><span class="sxs-lookup"><span data-stu-id="9163f-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="9163f-130">加载默认模板后，可以进行更改，使其满足您的业务要求。</span><span class="sxs-lookup"><span data-stu-id="9163f-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9163f-131">若要加载默认模板并导入模板，必须拥有系统管理员访问权限。</span><span class="sxs-lookup"><span data-stu-id="9163f-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="9163f-132">此要求有助于保证所有实体正确地加载到模板。</span><span class="sxs-lookup"><span data-stu-id="9163f-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="9163f-133">确保您所在的法人是您要从中导出公司特定数据的法人。</span><span class="sxs-lookup"><span data-stu-id="9163f-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="9163f-134">在该工作区中，选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="9163f-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="9163f-135">创建新的导出项目。</span><span class="sxs-lookup"><span data-stu-id="9163f-135">Create a new export project.</span></span>
7. <span data-ttu-id="9163f-136">选择 **+ 添加模板**，并找到 **400 - WMS** 默认仓库模板。</span><span class="sxs-lookup"><span data-stu-id="9163f-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="9163f-137">此模板添加用于仓库配置的数据实体。</span><span class="sxs-lookup"><span data-stu-id="9163f-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9163f-138">如果必须要筛选您正在导出的数据（例如，您只想要导出与特定仓库有关的数据），则必须评估每个数据实体并添加通过查询进行筛选。</span><span class="sxs-lookup"><span data-stu-id="9163f-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="9163f-139">或者可以导出所有数据，然后删除在目标文件中不需要的记录。</span><span class="sxs-lookup"><span data-stu-id="9163f-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="9163f-140">选择**导出**。</span><span class="sxs-lookup"><span data-stu-id="9163f-140">Select **Export**.</span></span> <span data-ttu-id="9163f-141">导出与项目中的所有数据实体有关的数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="9163f-142">您可以下载数据包的压缩文件。</span><span class="sxs-lookup"><span data-stu-id="9163f-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="9163f-143">此文件包含所选格式（例如，Excel 格式）的所有数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="9163f-144">正如前面所指出的，数据包文件中的一些记录可能必须进行更改，才能将其导入到生产环境。</span><span class="sxs-lookup"><span data-stu-id="9163f-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="9163f-145">如果更新记录，请确保不要更改文件名。</span><span class="sxs-lookup"><span data-stu-id="9163f-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="9163f-146">导入仓库配置设置</span><span class="sxs-lookup"><span data-stu-id="9163f-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="9163f-147">在目标环境中，请确保您所在的公司是您要将仓库数据导入其中的公司。</span><span class="sxs-lookup"><span data-stu-id="9163f-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9163f-148">在执行导入前，应确定任何数据依赖项。</span><span class="sxs-lookup"><span data-stu-id="9163f-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="9163f-149">例如，**仓库管理**模板包括命名为**仓库处置代码**的数据实体。</span><span class="sxs-lookup"><span data-stu-id="9163f-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="9163f-150">此实体包含与**处置代码**设置页（**仓库管理** > **设置** > **移动设备** > **处置代码**）有关的数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="9163f-151">如果现有设置已处理销售订单的退货流程，则**退货处置代码**字段包含值。</span><span class="sxs-lookup"><span data-stu-id="9163f-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="9163f-152">此字段中的处置代码与**处置代码**数据实体有关，是**销售和市场营销**模板的一部分。</span><span class="sxs-lookup"><span data-stu-id="9163f-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="9163f-153">如果来自**处置代码**数据实体的数据不在来自**仓库处置代码**字段的数据的前面导入，导入将失败。</span><span class="sxs-lookup"><span data-stu-id="9163f-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="9163f-154">在**数据管理**工作区中，选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="9163f-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="9163f-155">创建新的导入项目。</span><span class="sxs-lookup"><span data-stu-id="9163f-155">Create a new import project.</span></span>
4. <span data-ttu-id="9163f-156">选择 **+ 添加文件**，并上载数据包的压缩文件。</span><span class="sxs-lookup"><span data-stu-id="9163f-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="9163f-157">选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="9163f-157">Select **Import**.</span></span> <span data-ttu-id="9163f-158">在**增强型**视图中，可以使用**筛选器**选项快速获取在导入过程中可能发生的问题的概览。</span><span class="sxs-lookup"><span data-stu-id="9163f-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="9163f-159">**查看执行**日志提供与导入的各个数据实体有关的详细信息。</span><span class="sxs-lookup"><span data-stu-id="9163f-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="9163f-160">您可以使用暂存数据视图快速定位到目标数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="9163f-161">这样一来，您可以看到导入的数据在应用程序中的相关页面上的外观。</span><span class="sxs-lookup"><span data-stu-id="9163f-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="9163f-162">当您使用默认数据模板时，各数据实体的导入顺序采用预定义的方式，以帮助保证先导入所有依赖项数据。</span><span class="sxs-lookup"><span data-stu-id="9163f-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="9163f-163">如果自定义数据实体是项目的一部分，必须确保定义正确的顺序。</span><span class="sxs-lookup"><span data-stu-id="9163f-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="9163f-164">有关详细信息，请参阅[配置数据模板](../../dev-itpro/data-entities/configuration-data-templates.md)。</span><span class="sxs-lookup"><span data-stu-id="9163f-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

<span data-ttu-id="9163f-165">若要了解有关如何在同一个实例内使用仓库模板将仓库的配置从一家公司复制到新公司的详细信息，请观看 YouTube 上的这个 3 分钟的视频：[如何使用仓库模板复制 Finance and Operations 的配置](https://www.youtube.com/watch?v=K2WIfFlqJYs)。</span><span class="sxs-lookup"><span data-stu-id="9163f-165">To learn more about how to use warehouse template to copy the configuration of a warehouse from one company to a new company within the same instance, see this 3-minute video on YouTube about [how to use warehouse template to copy the configuration for Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).</span></span>

## <a name="related-topic"></a><span data-ttu-id="9163f-166">相关主题</span><span class="sxs-lookup"><span data-stu-id="9163f-166">Related topic</span></span>

[<span data-ttu-id="9163f-167">配置数据模板</span><span class="sxs-lookup"><span data-stu-id="9163f-167">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)
