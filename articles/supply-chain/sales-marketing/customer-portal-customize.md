---
title: 自定义和使用客户门户
description: 本主题说明将客户门户添加到系统后如何对其进行自定义。
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7849f354817f189bf7c844bbe2944f94c8fffe83
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527355"
---
# <a name="customize-and-use-the-customer-portal"></a><span data-ttu-id="7b72f-103">自定义和使用客户门户</span><span class="sxs-lookup"><span data-stu-id="7b72f-103">Customize and use the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7b72f-104">本主题介绍客户门户中现成可用的不同页面。</span><span class="sxs-lookup"><span data-stu-id="7b72f-104">This topic describes the different pages that available in the Customer portal out of the box.</span></span> <span data-ttu-id="7b72f-105">说明了页面的功能以及如何自定义页面。</span><span class="sxs-lookup"><span data-stu-id="7b72f-105">It explains what the pages do and how you can customize them.</span></span>

<span data-ttu-id="7b72f-106">客户门户提供了一些现成的网页和操作。</span><span class="sxs-lookup"><span data-stu-id="7b72f-106">The Customer portal offers a few webpages and actions out of the box.</span></span> <span data-ttu-id="7b72f-107">以下站点地图提供了这些网页和操作以及可以执行这些操作的角色的概览。</span><span class="sxs-lookup"><span data-stu-id="7b72f-107">The following site map provides an overview of those webpages and actions, and the roles that can perform the actions.</span></span>

<span data-ttu-id="7b72f-108">![客户门户站点地图](media/customer-portal-site-map.png "客户门户站点地图")</span><span class="sxs-lookup"><span data-stu-id="7b72f-108">![Customer portal site map](media/customer-portal-site-map.png "Customer portal site map")</span></span>

## <a name="typical-customizations"></a><span data-ttu-id="7b72f-109">典型自定义</span><span class="sxs-lookup"><span data-stu-id="7b72f-109">Typical customizations</span></span>

<span data-ttu-id="7b72f-110">以下主题将帮助您学习有关 Power Apps 门户以及如何定制这些门户的基础知识：</span><span class="sxs-lookup"><span data-stu-id="7b72f-110">The following topics will help you learn the basics about Power Apps portals and how you can customize portals:</span></span>

- <span data-ttu-id="7b72f-111">[使用模板](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – 本主题概括介绍 Power Apps 门户的工作原理以及如何对门户进行简单的自定义。</span><span class="sxs-lookup"><span data-stu-id="7b72f-111">[Work with templates](https://docs.microsoft.com/powerapps/maker/portals/work-with-templates) – This topic provides a general overview of how Power Apps portals works and how you can do simple customizations of portals.</span></span>
- <span data-ttu-id="7b72f-112">[管理门户内容](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – 本主题说明如何管理和自定义您在门户中显示的内容。</span><span class="sxs-lookup"><span data-stu-id="7b72f-112">[Manage portal content](https://docs.microsoft.com/dynamics365/portals/manage-portal-content) – This topic explains how you can manage and customize the content that you surface in your portal.</span></span>
- <span data-ttu-id="7b72f-113">[编辑 CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – 本主题帮助您对门户的用户界面 (UI) 进行更复杂的自定义。</span><span class="sxs-lookup"><span data-stu-id="7b72f-113">[Edit CSS](https://docs.microsoft.com/powerapps/maker/portals/edit-css) – This topic helps you make more complex customizations to the user interface (UI) of your portal.</span></span>
- <span data-ttu-id="7b72f-114">[为您的门户创建主题](https://docs.microsoft.com/dynamics365/portals/create-theme) – 本主题帮助您为门户创建 UI 主题。</span><span class="sxs-lookup"><span data-stu-id="7b72f-114">[Create a theme for your portal](https://docs.microsoft.com/dynamics365/portals/create-theme) – This topic helps you create a UI theme for your portal.</span></span>
- <span data-ttu-id="7b72f-115">[轻松创建和公开门户内容](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – 本主题帮助您管理用于门户的基础数据和实体。</span><span class="sxs-lookup"><span data-stu-id="7b72f-115">[Create and expose portal content easily](https://docs.microsoft.com/dynamics365/portals/create-expose-portal-content) – This topic helps you manage the underlying data and entities that you use for your portal.</span></span>
- <span data-ttu-id="7b72f-116">[配置要在门户上使用的联系人](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – 本主题说明如何创建和自定义用户角色，以及 Power Apps 门户中的安全性和身份验证如何运行。</span><span class="sxs-lookup"><span data-stu-id="7b72f-116">[Configure a contact for use on a portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) – This topic explains how to create and customize user roles, and how security and authentication work in Power Apps portals.</span></span>
- <span data-ttu-id="7b72f-117">[在门户上配置实体窗体和 Web 窗体的注释](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – 本主题说明如何向门户添加文档和其他存储。</span><span class="sxs-lookup"><span data-stu-id="7b72f-117">[Configure notes for entity forms and web forms on portals](https://docs.microsoft.com/powerapps/maker/portals/configure-notes) – This topic explains how to add documents and additional storage to your portal.</span></span>
- <span data-ttu-id="7b72f-118">[门户网站的错误处理](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – 本主题说明如何查看门户错误日志并将其存储在您的 Microsoft Azure Blob 存储帐户中。</span><span class="sxs-lookup"><span data-stu-id="7b72f-118">[Error handling for portal website](https://docs.microsoft.com/powerapps/maker/portals/admin/view-portal-error-log) – This topic explains how to view portal error logs and store them in your Microsoft Azure Blob storage account.</span></span>

## <a name="customize-the-order-creation-process"></a><span data-ttu-id="7b72f-119">自定义订单创建流程</span><span class="sxs-lookup"><span data-stu-id="7b72f-119">Customize the order creation process</span></span>

<span data-ttu-id="7b72f-120">当用户使用客户门户提交订单时，订单将自动同步到相应的 Dynamics 365 Supply Chain Management 环境。</span><span class="sxs-lookup"><span data-stu-id="7b72f-120">When a user submits an order by using the Customer portal, the order is automatically synced to the corresponding Dynamics 365 Supply Chain Management environment.</span></span> <span data-ttu-id="7b72f-121">由于用户是外部客户，因此有意向他/她隐藏了一些必需的信息。</span><span class="sxs-lookup"><span data-stu-id="7b72f-121">Because the user is an external customer, some required information is intentionally hidden from him or her.</span></span> <span data-ttu-id="7b72f-122">表单提交后，这些信息会自动填写。</span><span class="sxs-lookup"><span data-stu-id="7b72f-122">This information will automatically be filled in when the form is submitted.</span></span>

<span data-ttu-id="7b72f-123">本节说明应该如何设置联系人以避免错误。</span><span class="sxs-lookup"><span data-stu-id="7b72f-123">This section shows how you should set up contacts to avoid errors.</span></span> <span data-ttu-id="7b72f-124">其中说明了自动设置的字段以及如何在必要时修改这些字段的值。</span><span class="sxs-lookup"><span data-stu-id="7b72f-124">It explains fields that are automatically set and how you can modify the value of those fields if you must.</span></span>

### <a name="the-out-of-box-order-creation-process"></a><span data-ttu-id="7b72f-125">现成的订单创建流程</span><span class="sxs-lookup"><span data-stu-id="7b72f-125">The out-of-box order creation process</span></span>

<span data-ttu-id="7b72f-126">以下是从客户门户提交订单的标准步骤。</span><span class="sxs-lookup"><span data-stu-id="7b72f-126">Here are the standard steps for submitting an order from the Customer portal.</span></span>

1. <span data-ttu-id="7b72f-127">在主页上，选择 **创建订单** 磁贴打开 **创建订单** 向导。</span><span class="sxs-lookup"><span data-stu-id="7b72f-127">On the home page, select the **Create order** tile to open the **Create Order** wizard.</span></span>
1. <span data-ttu-id="7b72f-128">在 **订单信息** 页面上，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="7b72f-128">On the **Order Information** page, set the following fields:</span></span>

    - <span data-ttu-id="7b72f-129">**请求收货日期** – 指定交货日期。</span><span class="sxs-lookup"><span data-stu-id="7b72f-129">**Requested receipt date** – Specify the date of delivery.</span></span>
    - <span data-ttu-id="7b72f-130">**交货地址** – 输入应该交付订单的地址。</span><span class="sxs-lookup"><span data-stu-id="7b72f-130">**Delivery address** – Enter the address that the order should be delivered to.</span></span>
    - <span data-ttu-id="7b72f-131">**公司** – 选择客户公司的名称。</span><span class="sxs-lookup"><span data-stu-id="7b72f-131">**Company** – Select the name of the customer company.</span></span> <span data-ttu-id="7b72f-132">此字段将为非管理员用户自动设置。</span><span class="sxs-lookup"><span data-stu-id="7b72f-132">This field is automatically set for non-admin users.</span></span>
    - <span data-ttu-id="7b72f-133">**申请编号** – 输入订单的申请编号。</span><span class="sxs-lookup"><span data-stu-id="7b72f-133">**Requisition number** – Enter the requisition number of the order.</span></span> <span data-ttu-id="7b72f-134">此字段不是必填项。</span><span class="sxs-lookup"><span data-stu-id="7b72f-134">This field isn't required.</span></span>
    - <span data-ttu-id="7b72f-135">**运达国家/地区** – 输入物料将送达的国家或地区。</span><span class="sxs-lookup"><span data-stu-id="7b72f-135">**Ship to country/region** – Enter the country or region that the items will be delivered to.</span></span> <span data-ttu-id="7b72f-136">此字段将为非管理员用户自动设置。</span><span class="sxs-lookup"><span data-stu-id="7b72f-136">This field is automatically set for non-admin users.</span></span>

    <span data-ttu-id="7b72f-137">![订单信息页面](media/customer-portal-order-information.png "“订单信息”页面")</span><span class="sxs-lookup"><span data-stu-id="7b72f-137">![Order Information page](media/customer-portal-order-information.png "Order Information page")</span></span>

1. <span data-ttu-id="7b72f-138">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="7b72f-138">Select **Next**.</span></span>
1. <span data-ttu-id="7b72f-139">在 **物料** 页上，选择 **添加物料**。</span><span class="sxs-lookup"><span data-stu-id="7b72f-139">On the **Items** page, select **Add Item**.</span></span>

    <span data-ttu-id="7b72f-140">![“物料”页面](media/customer-portal-items.png "“物料”页面")</span><span class="sxs-lookup"><span data-stu-id="7b72f-140">![Items page](media/customer-portal-items.png "Items page")</span></span>

1. <span data-ttu-id="7b72f-141">在 **物料信息** 对话框中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="7b72f-141">In the **Item Information** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="7b72f-142">**产品名称** – 查找并选择要添加到订单中的产品。</span><span class="sxs-lookup"><span data-stu-id="7b72f-142">**Product Name** – Find and select a product to add to the order.</span></span>
    - <span data-ttu-id="7b72f-143">**数量** – 输入所选产品的数量。</span><span class="sxs-lookup"><span data-stu-id="7b72f-143">**Quantity** – Enter the quantity of the selected product.</span></span>
    - <span data-ttu-id="7b72f-144">**单位** – 指定度量单位（例如，**个**、**公斤** 或 **箱**）。</span><span class="sxs-lookup"><span data-stu-id="7b72f-144">**Unit** – Specify the unit of measure (for example, **ea.**, **kgs**, or **box**).</span></span>
    - <span data-ttu-id="7b72f-145">**估计净额** – 此值计算为“物料的估计价格 × 所选单位的数量”。</span><span class="sxs-lookup"><span data-stu-id="7b72f-145">**Estimated net amount** – The value is calculated as the estimated price of the item × the quantity for the selected unit.</span></span>

    <span data-ttu-id="7b72f-146">![“物料信息”对话框](media/customer-portal-item-information.png "“物料信息”对话框")</span><span class="sxs-lookup"><span data-stu-id="7b72f-146">![Item Information dialog box](media/customer-portal-item-information.png "Item Information dialog box")</span></span>

1. <span data-ttu-id="7b72f-147">选择 **提交** 将物料添加到订单。</span><span class="sxs-lookup"><span data-stu-id="7b72f-147">Select **Submit** to add the item to the order.</span></span>
1. <span data-ttu-id="7b72f-148">重复步骤 4 到 6，直到您添加了要订购的所有物料。</span><span class="sxs-lookup"><span data-stu-id="7b72f-148">Repeat steps 4 through 6 until you've added all the items that you want to order.</span></span>
1. <span data-ttu-id="7b72f-149">添加完物料后，在 **物料** 页上选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="7b72f-149">When you've finished adding items, select **Next** on the **Items** page.</span></span>
1. <span data-ttu-id="7b72f-150">**订单信息** 页提供订单摘要。</span><span class="sxs-lookup"><span data-stu-id="7b72f-150">The **Order Information** page provides a summary of the order.</span></span> <span data-ttu-id="7b72f-151">查看订单内容和交货详细信息。</span><span class="sxs-lookup"><span data-stu-id="7b72f-151">Review the order contents and delivery details.</span></span> <span data-ttu-id="7b72f-152">如果每一项看起来都正确，选择 **提交** 提交订单。</span><span class="sxs-lookup"><span data-stu-id="7b72f-152">If everything looks correct, select **Submit** to submit the order.</span></span>

    <span data-ttu-id="7b72f-153">![“订单信息”页面](media/customer-portal-order-submit.png "“订单信息”页面")</span><span class="sxs-lookup"><span data-stu-id="7b72f-153">![Order Information page](media/customer-portal-order-submit.png "Order Information page")</span></span>

### <a name="standard-data-setup"></a><span data-ttu-id="7b72f-154">标准数据设置</span><span class="sxs-lookup"><span data-stu-id="7b72f-154">Standard data setup</span></span>

<span data-ttu-id="7b72f-155">为了帮助确保流畅的用户体验，客户门户会自动填充几个必填字段的值。</span><span class="sxs-lookup"><span data-stu-id="7b72f-155">To help ensure a smooth user experience, the Customer portal automatically fills in values for several required fields.</span></span> <span data-ttu-id="7b72f-156">这些值基于提交订单的客户的联系记录中的信息。</span><span class="sxs-lookup"><span data-stu-id="7b72f-156">These values are based on information in the contact record of the customer who is submitting the order.</span></span>

<span data-ttu-id="7b72f-157">对于属于将使用客户门户提交订单的客户的每个[联系人记录](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts)，必须为以下必填字段指定值。</span><span class="sxs-lookup"><span data-stu-id="7b72f-157">For each [contact record](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) that belongs to a customer who will use the Customer portal to submit orders, values must be specified for the following required fields.</span></span> <span data-ttu-id="7b72f-158">否则会发生错误。</span><span class="sxs-lookup"><span data-stu-id="7b72f-158">Otherwise, errors will occur.</span></span>

- <span data-ttu-id="7b72f-159">**公司** – 订单所属的法人</span><span class="sxs-lookup"><span data-stu-id="7b72f-159">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7b72f-160">**潜在客户** – 与订单关联的客户帐户</span><span class="sxs-lookup"><span data-stu-id="7b72f-160">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7b72f-161">**价目表** – 客户的自定义价目表</span><span class="sxs-lookup"><span data-stu-id="7b72f-161">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7b72f-162">**货币** – 价格使用的货币</span><span class="sxs-lookup"><span data-stu-id="7b72f-162">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7b72f-163">**运达国家/地区** – 物料将送达的国家或地区</span><span class="sxs-lookup"><span data-stu-id="7b72f-163">**Ship to country/region** – The country or region that the items will be delivered to</span></span>

<span data-ttu-id="7b72f-164">将自动为销售订单实体设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="7b72f-164">The following fields are automatically set for the sales order entity:</span></span>

- <span data-ttu-id="7b72f-165">**语言** – 订单的语言（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-165">**Language** – The language of the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-166">**运达国家/地区** – 物料将被运送到的国家或地区（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-166">**Ship to country/region** – The country or region that the items will be delivered to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-167">**联系人** – 可以与其联系来获取有关订单的信息的用户（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-167">**Contact person** – The user who can be contacted for information about the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-168">**公司** – 订单所属的法人（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-168">**Company** – The legal entity that the order belongs to (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-169">**潜在客户** – 与订单关联的客户帐户（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-169">**Potential customer** – The customer account that is associated with the order (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-170">**发票客户** – 订单的计费帐户（默认值为联系人记录中的潜在客户。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-170">**Invoice customer** – The billing account of the order (The default value is the potential customer from the contact record.)</span></span>
- <span data-ttu-id="7b72f-171">**销售订单名称** – 销售订单的名称（默认值为 **销售订单**。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-171">**Sales order name** – The name of the sales order (The default value is **sales order**.)</span></span>
- <span data-ttu-id="7b72f-172">**货币** – 价格使用的货币（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-172">**Currency** – The currency of the price (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-173">**价目表** – 客户的自定义价目表（默认情况下，此值取自联系人记录。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-173">**Price list** – The custom price list for the customer (By default, the value is taken from the contact record.)</span></span>
- <span data-ttu-id="7b72f-174">**交货地址描述** – 销售订单的交货地址（默认值为 **交货地址描述**。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-174">**Delivery address description** – The delivery address of the sales order (The default value is **delivery address description**.)</span></span>

### <a name="modify-the-order-creation-process"></a><span data-ttu-id="7b72f-175">修改订单创建流程</span><span class="sxs-lookup"><span data-stu-id="7b72f-175">Modify the order creation process</span></span>

<span data-ttu-id="7b72f-176">如果不更改基本订单创建流程，可以自由修改客户门户的外观和 UI。</span><span class="sxs-lookup"><span data-stu-id="7b72f-176">You can freely modify the appearance and UI of the Customer portal if you don't change the basic order creation process.</span></span> <span data-ttu-id="7b72f-177">如果要更改订单创建流程，必须牢记几点。</span><span class="sxs-lookup"><span data-stu-id="7b72f-177">If you want to change the order creation process, there are a few points that you must keep in mind.</span></span>

<span data-ttu-id="7b72f-178">不要从 Common Data Service 中的销售订单实体中删除以下字段，因为它们是以双写入方式创建销售订单所必需的：</span><span class="sxs-lookup"><span data-stu-id="7b72f-178">Don't remove the following fields from the sales order entity in Common Data Service, because they are required to create a sales order in dual-write:</span></span>

- <span data-ttu-id="7b72f-179">**公司** – 订单所属的法人</span><span class="sxs-lookup"><span data-stu-id="7b72f-179">**Company** – The legal entity that the order belongs to</span></span>
- <span data-ttu-id="7b72f-180">**名称** – 销售订单的名称</span><span class="sxs-lookup"><span data-stu-id="7b72f-180">**Name** – The name of the sales order</span></span>
- <span data-ttu-id="7b72f-181">**货币** – 价格使用的货币</span><span class="sxs-lookup"><span data-stu-id="7b72f-181">**Currency** – The currency of the price</span></span>
- <span data-ttu-id="7b72f-182">**价目表** – 客户的自定义价目表</span><span class="sxs-lookup"><span data-stu-id="7b72f-182">**Price list** – The custom price list for the customer</span></span>
- <span data-ttu-id="7b72f-183">**运达国家/地区** – 物料将送达的国家或地区</span><span class="sxs-lookup"><span data-stu-id="7b72f-183">**Ship to country/region** – The country or region that the items will be delivered to</span></span>
- <span data-ttu-id="7b72f-184">**潜在客户** – 与订单关联的客户帐户</span><span class="sxs-lookup"><span data-stu-id="7b72f-184">**Potential customer** – The customer account that is associated with the order</span></span>
- <span data-ttu-id="7b72f-185">**语言** – 订单的语言（通常，此语言是潜在客户的语言。）</span><span class="sxs-lookup"><span data-stu-id="7b72f-185">**Language** – The language of the order (Typically, this language is the language of the potential customer.)</span></span>
- <span data-ttu-id="7b72f-186">**交货地址描述** – 销售订单的交货地址</span><span class="sxs-lookup"><span data-stu-id="7b72f-186">**Delivery address description** – The delivery address of the sales order</span></span>

<span data-ttu-id="7b72f-187">对于物料，必须有以下字段：</span><span class="sxs-lookup"><span data-stu-id="7b72f-187">For items, the following fields are required:</span></span>

- <span data-ttu-id="7b72f-188">**产品** – 要订购的产品</span><span class="sxs-lookup"><span data-stu-id="7b72f-188">**Product** – The product to order</span></span>
- <span data-ttu-id="7b72f-189">**数量** – 所选产品的数量</span><span class="sxs-lookup"><span data-stu-id="7b72f-189">**Quantity** – The quantity of the selected product</span></span>
- <span data-ttu-id="7b72f-190">**单位** – 度量单位（例如，**个**、**公斤** 或 **箱**）</span><span class="sxs-lookup"><span data-stu-id="7b72f-190">**Unit** – The unit of measure (for example, **ea.**, **kgs**, or **box**)</span></span>
- <span data-ttu-id="7b72f-191">**运达国家/地区** – 交货国家或地区</span><span class="sxs-lookup"><span data-stu-id="7b72f-191">**Ship to country/region** – The country or region of delivery</span></span>
- <span data-ttu-id="7b72f-192">**交货地址描述** – 订单的交货地址</span><span class="sxs-lookup"><span data-stu-id="7b72f-192">**Delivery address description** – The delivery address of the order</span></span>

<span data-ttu-id="7b72f-193">您必须确保客户门户以某种方式提交所有这些字段的值。</span><span class="sxs-lookup"><span data-stu-id="7b72f-193">You must make sure that your Customer portal somehow submits values for all these fields.</span></span>

<span data-ttu-id="7b72f-194">如果要向页面添加字段或删除字段，请参阅[创建或编辑快速创建窗体以简化数据输入体验](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms)。</span><span class="sxs-lookup"><span data-stu-id="7b72f-194">If you want to add fields to the page, or remove fields, see [Create or edit quick create forms for a streamlined data entry experience](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/customize/create-edit-quick-create-forms).</span></span>

<span data-ttu-id="7b72f-195">如果要更改保存页面时字段的预设方式和值的设置方式，请参阅 Power Apps 门户文档中的以下信息：</span><span class="sxs-lookup"><span data-stu-id="7b72f-195">If you want to change how fields are preset and how values are set when the page is saved, see the following information in the Power Apps portals documentation:</span></span>

- [<span data-ttu-id="7b72f-196">预填充字段</span><span class="sxs-lookup"><span data-stu-id="7b72f-196">Prepopulate field</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#prepopulate-field)
- [<span data-ttu-id="7b72f-197">保存时设置值</span><span class="sxs-lookup"><span data-stu-id="7b72f-197">Set Value On Save</span></span>](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-web-form-metadata#set-value-on-save)

## <a name="customize-the-home-page"></a><span data-ttu-id="7b72f-198">自定义主页</span><span class="sxs-lookup"><span data-stu-id="7b72f-198">Customize the home page</span></span>

<span data-ttu-id="7b72f-199">客户门户中的所有控件都是内置的 Power Apps 门户控件。</span><span class="sxs-lookup"><span data-stu-id="7b72f-199">All the controls in the Customer portal are built-in Power Apps portals controls.</span></span> <span data-ttu-id="7b72f-200">您可以按照 Power Apps 门户文档中[设计页面](https://docs.microsoft.com/powerapps/maker/portals/compose-page)中的以下步骤自定义这些控件。</span><span class="sxs-lookup"><span data-stu-id="7b72f-200">You can customize them by following the steps in [Compose a page](https://docs.microsoft.com/powerapps/maker/portals/compose-page) in the Power Apps portals documentation.</span></span>

<span data-ttu-id="7b72f-201">客户门户模板中包含的唯一自定义控件用于在主页上创建磁贴。</span><span class="sxs-lookup"><span data-stu-id="7b72f-201">The only custom control that is included in the Customer portal template is used to create the tiles on the home page.</span></span>

<span data-ttu-id="7b72f-202">![主页上的磁贴](media/customer-portal-home-page-tiles.png "主页上的磁贴")</span><span class="sxs-lookup"><span data-stu-id="7b72f-202">![Tiles on the home page](media/customer-portal-home-page-tiles.png "Tiles on the home page")</span></span>

<span data-ttu-id="7b72f-203">要修改磁贴，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7b72f-203">To modify the tiles, follow these steps.</span></span>

1. <span data-ttu-id="7b72f-204">打开[“门户管理”应用](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal)。</span><span class="sxs-lookup"><span data-stu-id="7b72f-204">Open the [Portal Management app](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-portal).</span></span>
1. <span data-ttu-id="7b72f-205">在左侧的导航窗格中，选择 **页面模板**。</span><span class="sxs-lookup"><span data-stu-id="7b72f-205">In the navigation pane on the left, select **Page Templates**.</span></span>

    <span data-ttu-id="7b72f-206">![“门户管理”导航窗格](media/customer-portal-nav.png "“门户管理”导航窗格")</span><span class="sxs-lookup"><span data-stu-id="7b72f-206">![Portal Management navigation pane](media/customer-portal-nav.png "Portal Management navigation pane")</span></span>

1. <span data-ttu-id="7b72f-207">选择名为 **主页** 的页面模板。</span><span class="sxs-lookup"><span data-stu-id="7b72f-207">Select the page template that is named **Home**.</span></span>
1. <span data-ttu-id="7b72f-208">在 **Web 模板** 字段中，选择 **主页** 链接打开该页面的源代码。</span><span class="sxs-lookup"><span data-stu-id="7b72f-208">In the **Web Template** field, select the **Home** link to open the source code for that page.</span></span>

    <span data-ttu-id="7b72f-209">![“Web 模板”字段](media/customer-portal-web-template.png "“Web 模板”字段")</span><span class="sxs-lookup"><span data-stu-id="7b72f-209">![Web Template field](media/customer-portal-web-template.png "Web Template field")</span></span>

1. <span data-ttu-id="7b72f-210">现在，您应该可以看到主页的所有源代码，并可以根据需要对其进行修改。</span><span class="sxs-lookup"><span data-stu-id="7b72f-210">You should now see all the source code for the home page and can modify it as you require.</span></span>

## <a name="resources"></a><span data-ttu-id="7b72f-211">资源</span><span class="sxs-lookup"><span data-stu-id="7b72f-211">Resources</span></span>

<span data-ttu-id="7b72f-212">要了解有关如何设置和自定义客户门户的详细信息，请参阅以下资源：</span><span class="sxs-lookup"><span data-stu-id="7b72f-212">To learn more about how you can set up and customize the Customer portal, see the following resources:</span></span>

- [<span data-ttu-id="7b72f-213">Power Apps 门户文档</span><span class="sxs-lookup"><span data-stu-id="7b72f-213">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="7b72f-214">双写入文档</span><span class="sxs-lookup"><span data-stu-id="7b72f-214">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)
- [<span data-ttu-id="7b72f-215">关于门户生命周期</span><span class="sxs-lookup"><span data-stu-id="7b72f-215">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="7b72f-216">升级门户</span><span class="sxs-lookup"><span data-stu-id="7b72f-216">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="7b72f-217">迁移门户配置</span><span class="sxs-lookup"><span data-stu-id="7b72f-217">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="7b72f-218">解决方案生命周期管理：Dynamics 365 for Customer Engagement 应用</span><span class="sxs-lookup"><span data-stu-id="7b72f-218">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
