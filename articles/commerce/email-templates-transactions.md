---
title: 为交易事件创建电子邮件模板
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建、上传和配置电子邮件模板。
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 756e2a64ef4c33c347106968eb6bc79a413c3ff7
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555237"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="704d5-103">创建交易事件的电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="704d5-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="704d5-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中为交易事件创建、上传和配置电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="704d5-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="704d5-105">概览</span><span class="sxs-lookup"><span data-stu-id="704d5-105">Overview</span></span>

<span data-ttu-id="704d5-106">Dynamics 365 Commerce 提供用于发送电子邮件的现成解决方案以向客户警示交易事件（例如，下达订单时，订单准备好领料时，或已经为订单发货了时）。</span><span class="sxs-lookup"><span data-stu-id="704d5-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="704d5-107">此主题介绍创建，上传和配置用于发送交易电子邮件的电子邮件模板的步骤。</span><span class="sxs-lookup"><span data-stu-id="704d5-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="704d5-108">创建电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="704d5-108">Create an email template</span></span>

<span data-ttu-id="704d5-109">必须先创建模板，才能将特定交易事件映射到电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="704d5-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="704d5-110">若要创建电子邮件模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="704d5-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="704d5-111">在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 组织电子邮件模板** 或 **组织管理 \> 设置 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="704d5-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="704d5-112">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="704d5-112">Select **New**.</span></span>
1. <span data-ttu-id="704d5-113">在 **常规** 下，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="704d5-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="704d5-114">**电子邮件 ID** – 电子邮件 ID 是模板的唯一标识，这是选择要映射到事件的模板时显示的值。</span><span class="sxs-lookup"><span data-stu-id="704d5-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="704d5-115">**电子邮件说明** – 可以使用这个可选字段提供模板的说明。</span><span class="sxs-lookup"><span data-stu-id="704d5-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="704d5-116">您输入的值仅在 Commerce Headquarters 中显示。</span><span class="sxs-lookup"><span data-stu-id="704d5-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="704d5-117">**发件人姓名** – 您输入的姓名在大多数电子邮件客户端的“发件人”字段中显示。</span><span class="sxs-lookup"><span data-stu-id="704d5-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="704d5-118">**发件人电子邮件** – 输入应该用于使用此模板发送的电子邮件的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="704d5-119">**默认语言代码** – 如果调用此模板的渠道未提供语言，此字段指定默认发送的电子邮件的本地化版本。</span><span class="sxs-lookup"><span data-stu-id="704d5-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="704d5-120">在 **电子邮件内容** 下，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="704d5-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="704d5-121">在 **语言** 字段中，输入电子邮件模板的语言。</span><span class="sxs-lookup"><span data-stu-id="704d5-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="704d5-122">以后可以添加更多语言和本地化的模板。</span><span class="sxs-lookup"><span data-stu-id="704d5-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="704d5-123">在 **主题** 字段中，输入应该在电子邮件的主题字段中显示的电子邮件主题。</span><span class="sxs-lookup"><span data-stu-id="704d5-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="704d5-124">选择 **编辑** 上传您的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="704d5-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="704d5-125">使用 HTML 创建电子邮件正文</span><span class="sxs-lookup"><span data-stu-id="704d5-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="704d5-126">将使用 HTML 撰写电子邮件正文。</span><span class="sxs-lookup"><span data-stu-id="704d5-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="704d5-127">可使用 HTML 和内嵌级联样式表 (CSS) 允许的任何布局、样式和品牌。</span><span class="sxs-lookup"><span data-stu-id="704d5-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="704d5-128">也可以使用在公开提供的 Web 终结点中托管的图像。</span><span class="sxs-lookup"><span data-stu-id="704d5-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="704d5-129">若要添加图像，请在 HTML **&lt;img&gt;** 标记的 **src** 属性中输入图像的 URL。</span><span class="sxs-lookup"><span data-stu-id="704d5-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="704d5-130">每个电子邮件客户端实施的布局和样式限制可能需要调整用于消息正文的 HTML 和 CSS。</span><span class="sxs-lookup"><span data-stu-id="704d5-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="704d5-131">建议您自己熟悉有关最受欢迎电子邮件客户端支持的 HTML 的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="704d5-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="704d5-132">在电子邮件正文中添加占位符</span><span class="sxs-lookup"><span data-stu-id="704d5-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="704d5-133">您的电子邮件中可以包含生成电子邮件时将替换为客户特定的和交易特定的值的占位符。</span><span class="sxs-lookup"><span data-stu-id="704d5-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="704d5-134">占位符两侧始终是百分比符号 (%)，并且将直接插入到 HTML 文档中。</span><span class="sxs-lookup"><span data-stu-id="704d5-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="704d5-135">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="704d5-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="704d5-136">订单占位符（销售订单级）</span><span class="sxs-lookup"><span data-stu-id="704d5-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="704d5-137">以下占位符检索和显示销售订单级（相对销售行级）定义的数据。</span><span class="sxs-lookup"><span data-stu-id="704d5-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="704d5-138">占位符名称</span><span class="sxs-lookup"><span data-stu-id="704d5-138">Placeholder name</span></span>     | <span data-ttu-id="704d5-139">占位符值</span><span class="sxs-lookup"><span data-stu-id="704d5-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="704d5-140">customername</span><span class="sxs-lookup"><span data-stu-id="704d5-140">customername</span></span>         | <span data-ttu-id="704d5-141">下订单的客户的姓名。</span><span class="sxs-lookup"><span data-stu-id="704d5-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="704d5-142">salesid</span><span class="sxs-lookup"><span data-stu-id="704d5-142">salesid</span></span>              | <span data-ttu-id="704d5-143">订单的销售 ID。</span><span class="sxs-lookup"><span data-stu-id="704d5-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="704d5-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="704d5-144">deliveryaddress</span></span>      | <span data-ttu-id="704d5-145">所装运订单的交货地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="704d5-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="704d5-146">customeraddress</span></span>      | <span data-ttu-id="704d5-147">客户的地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="704d5-148">customeremailaddress</span><span class="sxs-lookup"><span data-stu-id="704d5-148">customeremailaddress</span></span> | <span data-ttu-id="704d5-149">客户在结帐时输入的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="704d5-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="704d5-150">deliverydate</span></span>         | <span data-ttu-id="704d5-151">交货日期。</span><span class="sxs-lookup"><span data-stu-id="704d5-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="704d5-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="704d5-152">shipdate</span></span>             | <span data-ttu-id="704d5-153">装运日期。</span><span class="sxs-lookup"><span data-stu-id="704d5-153">The ship date.</span></span>                                               |
| <span data-ttu-id="704d5-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="704d5-154">modeofdelivery</span></span>       | <span data-ttu-id="704d5-155">订单的交货方式。</span><span class="sxs-lookup"><span data-stu-id="704d5-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="704d5-156">费用</span><span class="sxs-lookup"><span data-stu-id="704d5-156">charges</span></span>              | <span data-ttu-id="704d5-157">订单的总费用。</span><span class="sxs-lookup"><span data-stu-id="704d5-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="704d5-158">税</span><span class="sxs-lookup"><span data-stu-id="704d5-158">tax</span></span>                  | <span data-ttu-id="704d5-159">订单的总税金。</span><span class="sxs-lookup"><span data-stu-id="704d5-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="704d5-160">合计</span><span class="sxs-lookup"><span data-stu-id="704d5-160">total</span></span>                | <span data-ttu-id="704d5-161">订单的总金额。</span><span class="sxs-lookup"><span data-stu-id="704d5-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="704d5-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="704d5-162">ordernetamount</span></span>       | <span data-ttu-id="704d5-163">订单的总金额减去总税金。</span><span class="sxs-lookup"><span data-stu-id="704d5-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="704d5-164">discount / 折扣</span><span class="sxs-lookup"><span data-stu-id="704d5-164">discount</span></span>             | <span data-ttu-id="704d5-165">订单的总折扣。</span><span class="sxs-lookup"><span data-stu-id="704d5-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="704d5-166">storename</span><span class="sxs-lookup"><span data-stu-id="704d5-166">storename</span></span>            | <span data-ttu-id="704d5-167">下订单所在商店的名称。</span><span class="sxs-lookup"><span data-stu-id="704d5-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="704d5-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="704d5-168">storeaddress</span></span>         | <span data-ttu-id="704d5-169">下订单的商店的地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="704d5-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="704d5-170">storeopenfrom</span></span>        | <span data-ttu-id="704d5-171">下订单的商店的上班时间。</span><span class="sxs-lookup"><span data-stu-id="704d5-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="704d5-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="704d5-172">storeopento</span></span>          | <span data-ttu-id="704d5-173">下订单的商店的下班时间。</span><span class="sxs-lookup"><span data-stu-id="704d5-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="704d5-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="704d5-174">pickupstorename</span></span>      | <span data-ttu-id="704d5-175">订单提货所在商店的名称。</span><span class="sxs-lookup"><span data-stu-id="704d5-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="704d5-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="704d5-176">pickupstoreaddress</span></span>   | <span data-ttu-id="704d5-177">订单提货所在商店的地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="704d5-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="704d5-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="704d5-179">订单提货所在商店的上班时间。</span><span class="sxs-lookup"><span data-stu-id="704d5-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="704d5-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="704d5-180">pickupopenstoreto</span></span>    | <span data-ttu-id="704d5-181">订单提货所在商店的下班时间。</span><span class="sxs-lookup"><span data-stu-id="704d5-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="704d5-182">订单行占位符（销售行级）</span><span class="sxs-lookup"><span data-stu-id="704d5-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="704d5-183">以下占位符检索和显示销售订单中单个产品（行）的数据。</span><span class="sxs-lookup"><span data-stu-id="704d5-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="704d5-184">占位符名称</span><span class="sxs-lookup"><span data-stu-id="704d5-184">Placeholder name</span></span>               | <span data-ttu-id="704d5-185">占位符值</span><span class="sxs-lookup"><span data-stu-id="704d5-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="704d5-186">productid</span><span class="sxs-lookup"><span data-stu-id="704d5-186">productid</span></span>                      | <span data-ttu-id="704d5-187">行的产品 ID。</span><span class="sxs-lookup"><span data-stu-id="704d5-187">The product ID for the line.</span></span> |
| <span data-ttu-id="704d5-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="704d5-188">lineproductname</span></span>                | <span data-ttu-id="704d5-189">产品的名称。</span><span class="sxs-lookup"><span data-stu-id="704d5-189">The name of the product.</span></span> |
| <span data-ttu-id="704d5-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="704d5-190">lineproductdescription</span></span>         | <span data-ttu-id="704d5-191">产品的描述。</span><span class="sxs-lookup"><span data-stu-id="704d5-191">The description of the product.</span></span> |
| <span data-ttu-id="704d5-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="704d5-192">linequantity</span></span>                   | <span data-ttu-id="704d5-193">为行订购的单位数量加度量单位（例如，**ea** 或 **对**）。</span><span class="sxs-lookup"><span data-stu-id="704d5-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="704d5-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="704d5-194">lineunit</span></span>                       | <span data-ttu-id="704d5-195">行的度量单位。</span><span class="sxs-lookup"><span data-stu-id="704d5-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="704d5-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="704d5-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="704d5-197">为行订购的单位数量，但不含度量单位。</span><span class="sxs-lookup"><span data-stu-id="704d5-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="704d5-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="704d5-198">linequantitypicked</span></span>             | <span data-ttu-id="704d5-199">使用 **PickOrder** 事件时，为提货单位数量。</span><span class="sxs-lookup"><span data-stu-id="704d5-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="704d5-200">否则为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="704d5-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="704d5-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="704d5-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="704d5-202">使用 **PickOrder** 事件时，为提货单位数量，但不含度量单位。</span><span class="sxs-lookup"><span data-stu-id="704d5-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="704d5-203">否则为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="704d5-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="704d5-204">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="704d5-204">linequantitypacked</span></span>             | <span data-ttu-id="704d5-205">使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量。</span><span class="sxs-lookup"><span data-stu-id="704d5-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="704d5-206">否则为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="704d5-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="704d5-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="704d5-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="704d5-208">使用 **PackOrder** 和 **订单可提货** 事件时，为包装单位数量，但不含度量单位。</span><span class="sxs-lookup"><span data-stu-id="704d5-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="704d5-209">否则为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="704d5-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="704d5-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="704d5-210">linequantityshipped</span></span>            | <span data-ttu-id="704d5-211">始终为 **0**，除了使用特定事件时，如下一行中所述。</span><span class="sxs-lookup"><span data-stu-id="704d5-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="704d5-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="704d5-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="704d5-213">使用 **ShipOrder** 事件时，为提货单位数量，但不含度量单位。</span><span class="sxs-lookup"><span data-stu-id="704d5-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="704d5-214">否则为 **0**（零）。</span><span class="sxs-lookup"><span data-stu-id="704d5-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="704d5-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="704d5-215">lineprice</span></span>                      | <span data-ttu-id="704d5-216">一个单位的价格。</span><span class="sxs-lookup"><span data-stu-id="704d5-216">The price of a single unit.</span></span> |
| <span data-ttu-id="704d5-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="704d5-217">linenetamount</span></span>                  | <span data-ttu-id="704d5-218">实施单位数量和折扣后的行价格。</span><span class="sxs-lookup"><span data-stu-id="704d5-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="704d5-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="704d5-219">linediscount</span></span>                   | <span data-ttu-id="704d5-220">单个单位的折扣。</span><span class="sxs-lookup"><span data-stu-id="704d5-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="704d5-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="704d5-221">lineshipdate</span></span>                   | <span data-ttu-id="704d5-222">行的装运日期。</span><span class="sxs-lookup"><span data-stu-id="704d5-222">The ship date for the line.</span></span> |
| <span data-ttu-id="704d5-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="704d5-223">linedeliverydate</span></span>               | <span data-ttu-id="704d5-224">行的交货日期。</span><span class="sxs-lookup"><span data-stu-id="704d5-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="704d5-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="704d5-225">linedeliverymode</span></span>               | <span data-ttu-id="704d5-226">行的交货方式。</span><span class="sxs-lookup"><span data-stu-id="704d5-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="704d5-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="704d5-227">linedeliveryaddress</span></span>            | <span data-ttu-id="704d5-228">行的交货地址。</span><span class="sxs-lookup"><span data-stu-id="704d5-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="704d5-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="704d5-229">giftcardnumber</span></span>                 | <span data-ttu-id="704d5-230">礼品卡类型产品的礼品卡编号。</span><span class="sxs-lookup"><span data-stu-id="704d5-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="704d5-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="704d5-231">giftcardbalance</span></span>                | <span data-ttu-id="704d5-232">礼品卡类型产品的礼品卡余额。</span><span class="sxs-lookup"><span data-stu-id="704d5-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="704d5-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="704d5-233">giftcardmessage</span></span>                | <span data-ttu-id="704d5-234">礼品卡类型产品的礼品卡消息。</span><span class="sxs-lookup"><span data-stu-id="704d5-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="704d5-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="704d5-235">giftcardpin</span></span>                    | <span data-ttu-id="704d5-236">礼品卡类型产品的礼品卡个人标识号 (PIN)。</span><span class="sxs-lookup"><span data-stu-id="704d5-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="704d5-237">（此占位符特定于外部礼品卡。）</span><span class="sxs-lookup"><span data-stu-id="704d5-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="704d5-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="704d5-238">giftcardexpiration</span></span>             | <span data-ttu-id="704d5-239">礼品卡类型产品的礼品卡到期日期。</span><span class="sxs-lookup"><span data-stu-id="704d5-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="704d5-240">（此占位符特定于外部礼品卡。）</span><span class="sxs-lookup"><span data-stu-id="704d5-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="704d5-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="704d5-241">giftcardrecipientname</span></span>          | <span data-ttu-id="704d5-242">礼品卡类型产品的礼品卡接收人姓名。</span><span class="sxs-lookup"><span data-stu-id="704d5-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="704d5-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="704d5-243">giftcardbuyername</span></span>              | <span data-ttu-id="704d5-244">礼品卡类型产品的礼品卡购买者姓名。</span><span class="sxs-lookup"><span data-stu-id="704d5-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="704d5-245">电子邮件正文中的订单行占位符的格式</span><span class="sxs-lookup"><span data-stu-id="704d5-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="704d5-246">为电子邮件正文中的单个订单行创建 HTML 时，在行的重复 HTML 块和占位符两侧加上放到 HTML 注释标记内的以下占位符。</span><span class="sxs-lookup"><span data-stu-id="704d5-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="704d5-247">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="704d5-247">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="704d5-248">为通过电子邮件发送的收据创建模板</span><span class="sxs-lookup"><span data-stu-id="704d5-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="704d5-249">可以通过电子邮件将收据发给在销售点 (POS) 进行购买的客户。</span><span class="sxs-lookup"><span data-stu-id="704d5-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="704d5-250">通过电子邮件发送的收据模板的创建步骤与其他交易事件的模板的创建步骤相同。</span><span class="sxs-lookup"><span data-stu-id="704d5-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="704d5-251">但是需要进行以下更改：</span><span class="sxs-lookup"><span data-stu-id="704d5-251">However, the following changes are required:</span></span>

- <span data-ttu-id="704d5-252">使用 **%message%**  占位符将收据的文本插入到电子邮件中。</span><span class="sxs-lookup"><span data-stu-id="704d5-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="704d5-253">若要确保正确显示收据正文，请在 **%message%** 占位符两侧添加 HTML **&lt;pre&gt;** 和 **&lt;/pre&gt;** 标记。</span><span class="sxs-lookup"><span data-stu-id="704d5-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="704d5-254">**%receiptid%** 占位符可用于显示代表收据 ID 的 QR 码或条形码。</span><span class="sxs-lookup"><span data-stu-id="704d5-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="704d5-255">（QR 码和条形码是由第三方服务动态生成和提供的。）有关如何在电子邮件收据中显示 QR 码或条形码的更多信息，请参见[在交易和收据电子邮件中添加 QR 码或条形码](add-qr-code-barcode-email.md)。</span><span class="sxs-lookup"><span data-stu-id="704d5-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="704d5-256">上传电子邮件 HTML</span><span class="sxs-lookup"><span data-stu-id="704d5-256">Upload the email HTML</span></span>

<span data-ttu-id="704d5-257">创建和测试邮件正文的 HTML 之后，必须将其上传到 Commerce Headquarters。</span><span class="sxs-lookup"><span data-stu-id="704d5-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="704d5-258">现在不能导出电子邮件 HTML。</span><span class="sxs-lookup"><span data-stu-id="704d5-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="704d5-259">因此，必须在 Commerce Headquarters 外部维护 HTML 的主副本。</span><span class="sxs-lookup"><span data-stu-id="704d5-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="704d5-260">若要上传新的或编辑后的电子邮件模板 HTML，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="704d5-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="704d5-261">在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 组织电子邮件模板**。</span><span class="sxs-lookup"><span data-stu-id="704d5-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="704d5-262">选择要为其添加或替换 HTML 的语言的行。</span><span class="sxs-lookup"><span data-stu-id="704d5-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="704d5-263">也可以选择 **新建** 为新语言创建行。</span><span class="sxs-lookup"><span data-stu-id="704d5-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="704d5-264">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="704d5-264">Select **Edit**.</span></span>
1. <span data-ttu-id="704d5-265">在显示的对话框中，选择 **浏览**。</span><span class="sxs-lookup"><span data-stu-id="704d5-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="704d5-266">浏览到要上传的 HTML 文档，选中，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="704d5-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="704d5-267">选择 **上载**。</span><span class="sxs-lookup"><span data-stu-id="704d5-267">Select **Upload**.</span></span>
1. <span data-ttu-id="704d5-268">预览窗口中显示您的电子邮件 HTML 之后，请选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="704d5-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="704d5-269">确保为行选中 **有正文** 复选框。</span><span class="sxs-lookup"><span data-stu-id="704d5-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="704d5-270">如果已经配置了 Commerce Headquarters 以发送电子邮件，将把您的新的或更新后的电子邮件发送给执行的交易将调用映射到模板的事件的所有客户。</span><span class="sxs-lookup"><span data-stu-id="704d5-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="704d5-271">有关如何在 Dynamics 365 Commerce 中配置电子邮件的详细信息，请参阅[配置和发送电子邮件](../fin-ops-core/fin-ops/organization-administration/configure-email.md)。</span><span class="sxs-lookup"><span data-stu-id="704d5-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="704d5-272">其他资源</span><span class="sxs-lookup"><span data-stu-id="704d5-272">Additional resources</span></span> 

[<span data-ttu-id="704d5-273">设置电子邮件通知配置文件</span><span class="sxs-lookup"><span data-stu-id="704d5-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="704d5-274">配置和发送电子邮件</span><span class="sxs-lookup"><span data-stu-id="704d5-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="704d5-275">设置电子邮件收据</span><span class="sxs-lookup"><span data-stu-id="704d5-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="704d5-276">从 Modern POS 发送电子邮件收据</span><span class="sxs-lookup"><span data-stu-id="704d5-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
