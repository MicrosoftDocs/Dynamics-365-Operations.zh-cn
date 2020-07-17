---
title: 在仓库应用中配置应用字段名
description: 此主题介绍如何在 Dynamics 365 Supply Chain Management 中定义和配置仓库应用程序字段名和优先级。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a4cfe62aa50c423adfd116a81d7962c30b25fcf
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530481"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a><span data-ttu-id="d3cc3-103">在仓库应用中配置应用字段名</span><span class="sxs-lookup"><span data-stu-id="d3cc3-103">Configure app field names in the warehouse app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3cc3-104">此主题介绍如何在 Dynamics 365 Supply Chain Management 中定义和配置仓库应用程序字段名和优先级。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-104">This topic describes how to define and configure warehouse app field names and priorities in Dynamics 365 Supply Chain Management.</span></span> 

> [!NOTE]
> <span data-ttu-id="d3cc3-105">本主题适用于仓库管理中的功能。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="d3cc3-106">它不适用于库存管理中的功能。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="d3cc3-107">Warehousing 是可用于执行仓库任务的应用程序。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-107">Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="d3cc3-108">可定义和配置此应用程序中使用的字段名，以及配置应该为字段名分配的优先级。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="d3cc3-109">此主题说明如何在 Warehousing 中定义、配置和使用这些仓库应用程序字段名和优先级。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Warehousing.</span></span> <span data-ttu-id="d3cc3-110">有关如何配置与 Warehousing 之间的连接的详细信息，请参阅教程[安装和配置仓库应用概览](install-configure-warehousing-app.md)。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-110">For detailed information about how to configure the connection to FWarehousing, refer to the tutorial [Install and configure the warehouse app overview](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="d3cc3-111">配置仓库应用程序字段名</span><span class="sxs-lookup"><span data-stu-id="d3cc3-111">Configure warehouse app field names</span></span>

<span data-ttu-id="d3cc3-112">在移动设备上使用 Warehousing 时，可在**仓库应用字段名**页面中配置应如何在设备上显示元数据。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-112">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="d3cc3-113">在新公司中，选择**创建默认设置**以生成将在仓库移动设备工作流中使用的所有字段名，然后为其分配首选输入模式和输入类型。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-113">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="d3cc3-114">生成所有字段名之后，可以选择以下输入选项。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3cc3-115">选项</span><span class="sxs-lookup"><span data-stu-id="d3cc3-115">Option</span></span></th>
<th><span data-ttu-id="d3cc3-116">说明</span><span class="sxs-lookup"><span data-stu-id="d3cc3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3cc3-117">首选输入类型</span><span class="sxs-lookup"><span data-stu-id="d3cc3-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="d3cc3-118">此选项定义应如何为所选字段名显示扫描字段或手动输入的输入字段。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="d3cc3-119">这对根据条码是否用于字段来区分字段十分有用。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="d3cc3-120"><strong>注释：</strong>对于首选输入模式设置为<strong>扫描</strong>的字段名，如果条码不可识别或已损坏，则可手动输入信息。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3cc3-121">输入类型</span><span class="sxs-lookup"><span data-stu-id="d3cc3-121">Input type</span></span></td>
<td><span data-ttu-id="d3cc3-122">此选项定义应对所选字段名使用哪种输入类型。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="d3cc3-123">有四个选项：</span><span class="sxs-lookup"><span data-stu-id="d3cc3-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="d3cc3-124"><strong>选择</strong> - 包含可供选择的选项的列表。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="d3cc3-125">使用此选项选择的字段名不可编辑。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="d3cc3-126"><strong>日期</strong> - 指定为日期的字段名将显示带标签的日期格式。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="d3cc3-127">这将帮助仓库工作人员了解要使用哪种格式输入日期。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="d3cc3-128">使用此选项选择的字段名不可编辑。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="d3cc3-129"><strong>字母</strong> - 如果选择此选项，在应用程序中手动输入信息时，将使用设备键盘。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="d3cc3-130">可根据所用设备更改键盘体验。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="d3cc3-131"><strong>数字</strong> - 对于仅使用数字输入的字段名，可选择此选项以显示带输入字段的自定义数字键盘，而不是设备键盘。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="d3cc3-132">配置仓库应用字段优先级</span><span class="sxs-lookup"><span data-stu-id="d3cc3-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="d3cc3-133">在**仓库应用字段优先级**页面中，可将字段名放入不同优先级组。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="d3cc3-134">这样就可以定义当仓库工作人员使用此应用程序执行任务时，应在主任务页面中显示哪些信息。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="d3cc3-135">如果单击**创建默认设置**，将生成一组默认优先级组。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="d3cc3-136">可以根据需要创建任意数量的优先级组，但是任务页面中将仅显示三个优先级组。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="d3cc3-137">当系统向该应用程序发送元数据时，将根据每个字段的优先级组为字段分配一个相对优先级，并且该应用程序将在任务页面中显示元数据中包含的前三个优先级组。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-137">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="d3cc3-138">将在第二详细信息页面中显示其余过剩元数据。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="d3cc3-139">下表显示五个优先级组的示例。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d3cc3-140">优先级组</span><span class="sxs-lookup"><span data-stu-id="d3cc3-140">Priority group</span></span></th>
<th><span data-ttu-id="d3cc3-141">已分配字段</span><span class="sxs-lookup"><span data-stu-id="d3cc3-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="d3cc3-142">优先级 10</span><span class="sxs-lookup"><span data-stu-id="d3cc3-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="d3cc3-143">项目</span><span class="sxs-lookup"><span data-stu-id="d3cc3-143">Item</span></span></li>
<li><span data-ttu-id="d3cc3-144">数量</span><span class="sxs-lookup"><span data-stu-id="d3cc3-144">Quantity</span></span></li>
<li><span data-ttu-id="d3cc3-145">度量单位</span><span class="sxs-lookup"><span data-stu-id="d3cc3-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="d3cc3-146">优先级 20</span><span class="sxs-lookup"><span data-stu-id="d3cc3-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="d3cc3-147">群集职位</span><span class="sxs-lookup"><span data-stu-id="d3cc3-147">Cluster position</span></span></li>
<li><span data-ttu-id="d3cc3-148">群集</span><span class="sxs-lookup"><span data-stu-id="d3cc3-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="d3cc3-149">优先级 30</span><span class="sxs-lookup"><span data-stu-id="d3cc3-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="d3cc3-150">物料描述</span><span class="sxs-lookup"><span data-stu-id="d3cc3-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="d3cc3-151">优先级 40</span><span class="sxs-lookup"><span data-stu-id="d3cc3-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="d3cc3-152">配置</span><span class="sxs-lookup"><span data-stu-id="d3cc3-152">Configuration</span></span></li>
<li><span data-ttu-id="d3cc3-153">颜色</span><span class="sxs-lookup"><span data-stu-id="d3cc3-153">Color</span></span></li>
<li><span data-ttu-id="d3cc3-154">尺寸</span><span class="sxs-lookup"><span data-stu-id="d3cc3-154">Size</span></span></li>
<li><span data-ttu-id="d3cc3-155">样式</span><span class="sxs-lookup"><span data-stu-id="d3cc3-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="d3cc3-156">优先级 50</span><span class="sxs-lookup"><span data-stu-id="d3cc3-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="d3cc3-157">货位</span><span class="sxs-lookup"><span data-stu-id="d3cc3-157">Location</span></span></li>
<li><span data-ttu-id="d3cc3-158">牌照</span><span class="sxs-lookup"><span data-stu-id="d3cc3-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3cc3-159">例如，当仓库工作人员在移动设备上执行任务时，如果应用程序中将显示的元数据包含以下字段：</span><span class="sxs-lookup"><span data-stu-id="d3cc3-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="d3cc3-160">项目</span><span class="sxs-lookup"><span data-stu-id="d3cc3-160">Item</span></span>
-   <span data-ttu-id="d3cc3-161">数量</span><span class="sxs-lookup"><span data-stu-id="d3cc3-161">Quantity</span></span>
-   <span data-ttu-id="d3cc3-162">度量单位</span><span class="sxs-lookup"><span data-stu-id="d3cc3-162">Unit of measure</span></span>
-   <span data-ttu-id="d3cc3-163">物料描述</span><span class="sxs-lookup"><span data-stu-id="d3cc3-163">Item description</span></span>
-   <span data-ttu-id="d3cc3-164">尺寸和位置</span><span class="sxs-lookup"><span data-stu-id="d3cc3-164">Size and Location</span></span>

<span data-ttu-id="d3cc3-165">将根据上表中设置的仓库应用程序字段优先级，在任务页面中显示以下 3 行信息：</span><span class="sxs-lookup"><span data-stu-id="d3cc3-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="d3cc3-166">第 1 行：物料、数量、度量单位</span><span class="sxs-lookup"><span data-stu-id="d3cc3-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="d3cc3-167">第 2 行：物料描述</span><span class="sxs-lookup"><span data-stu-id="d3cc3-167">Row 2: Item description</span></span>
-   <span data-ttu-id="d3cc3-168">第 3 行：尺寸</span><span class="sxs-lookup"><span data-stu-id="d3cc3-168">Row 3: Size</span></span>

<span data-ttu-id="d3cc3-169">其余元数据（如位置）将不在任务页面中显示，但是将在详细信息页面中显示。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="d3cc3-170">若要详细了解和查看用户界面的示例，请参阅博客文章[介绍 Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)。</span><span class="sxs-lookup"><span data-stu-id="d3cc3-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="d3cc3-171">其他资源</span><span class="sxs-lookup"><span data-stu-id="d3cc3-171">Additional resources</span></span>
--------

[<span data-ttu-id="d3cc3-172">安装和配置仓库应用概览</span><span class="sxs-lookup"><span data-stu-id="d3cc3-172">Install and configure the warehouse app overview</span></span>](install-configure-warehousing-app.md)
