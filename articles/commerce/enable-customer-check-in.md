---
title: 在销售点 (POS) 启用客户登记通知
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b42dc7766f8a69a7409c28d21b49cc96eca18dd4
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271417"
---
# <a name="enable-customer-check-in-notifications-in-point-of-sale-pos"></a><span data-ttu-id="469ec-103">在销售点 (POS) 启用客户登记通知</span><span class="sxs-lookup"><span data-stu-id="469ec-103">Enable customer check-in notifications in point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="469ec-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 销售点 (POS) 启用客户登记通知。</span><span class="sxs-lookup"><span data-stu-id="469ec-104">This topic describes how to enable customer check-in notifications in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="469ec-105">在“订单可提货”电子邮件中，组织可以提供一个链接或按钮，让客户通知商店他们已经到达商店位置，在等待包裹出来。</span><span class="sxs-lookup"><span data-stu-id="469ec-105">In their "order ready for pickup" emails, organizations can provide a link or button that lets customers notify the store that they are on the premises and waiting for their package to be brought out to them.</span></span> <span data-ttu-id="469ec-106">然后，客户将收到登记确认，商店将在其 POS 应用程序中收到作为任务的通知。</span><span class="sxs-lookup"><span data-stu-id="469ec-106">Customers then receive a check-in confirmation, and the store receives a notification as a task in its POS application.</span></span> <span data-ttu-id="469ec-107">此任务作为提醒销售助理将订单交到客户车辆处的提示。</span><span class="sxs-lookup"><span data-stu-id="469ec-107">This task serves as a prompt for a sales associate to deliver the order to the customer's vehicle.</span></span> <span data-ttu-id="469ec-108">因此，客户不必进入商店。</span><span class="sxs-lookup"><span data-stu-id="469ec-108">Therefore, the customer doesn't have to enter the store.</span></span>

<span data-ttu-id="469ec-109">客户登记工作流也可以配置为从客户那里收集其他信息，如他们的停车位编号、车辆的品牌、型号和颜色以及交货说明。</span><span class="sxs-lookup"><span data-stu-id="469ec-109">The customer check-in workflow can also be configured to collect additional information from customers, such as their parking spot number, the make, model, and color of their vehicle, and delivery instructions.</span></span> <span data-ttu-id="469ec-110">零售商店服务员可以使用这些信息来推进订单履行。</span><span class="sxs-lookup"><span data-stu-id="469ec-110">The retail store attendant can use this information to facilitate order fulfillment.</span></span>

## <a name="enable-customer-check-in"></a><span data-ttu-id="469ec-111">启用客户登记</span><span class="sxs-lookup"><span data-stu-id="469ec-111">Enable customer check-in</span></span>

<span data-ttu-id="469ec-112">启用客户登记功能后，Commerce 会生成一个订单确认 ID（也称为渠道引用 ID）。</span><span class="sxs-lookup"><span data-stu-id="469ec-112">When the customer check-in feature is turned on, Commerce generates an order confirmation ID (also known as the channel reference ID).</span></span> <span data-ttu-id="469ec-113">另外还会为通过销售点 (POS) 或呼叫中心渠道创建的订单生成订单确认 ID。</span><span class="sxs-lookup"><span data-stu-id="469ec-113">It also generates order confirmation IDs for orders that are created through point of sale (POS) or call center channels.</span></span> 

<span data-ttu-id="469ec-114">要在 Commerce headquarters 中启用客户登记功能，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="469ec-114">To turn on the customer check-in feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="469ec-115">转到 **工作区 \> 功能管理**。</span><span class="sxs-lookup"><span data-stu-id="469ec-115">Go to **Workspaces \> Feature management**.</span></span>
2. <span data-ttu-id="469ec-116">搜索 **跨渠道生成一致的渠道引用 ID 格式** 功能。</span><span class="sxs-lookup"><span data-stu-id="469ec-116">Search for the **Generate a consistent channel reference ID format across channels** feature.</span></span> 
3. <span data-ttu-id="469ec-117">选择该功能，然后在属性窗格中选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="469ec-117">Select the feature, and then select **Enable now** in the properties pane.</span></span> 

## <a name="create-a-check-in-confirmation-page"></a><span data-ttu-id="469ec-118">创建登记确认页面</span><span class="sxs-lookup"><span data-stu-id="469ec-118">Create a check-in confirmation page</span></span>

<span data-ttu-id="469ec-119">在您的电子商务站点上，您必须创建一个新页面，用作登记确认体验。</span><span class="sxs-lookup"><span data-stu-id="469ec-119">On your e-commerce site, you must create a new page that will serve as the check-in confirmation experience.</span></span> <span data-ttu-id="469ec-120">通过额外配置，此页面还可以包含一个表单，从客户那里收集其他信息来推进订单履行。</span><span class="sxs-lookup"><span data-stu-id="469ec-120">Through additional configuration, the page can also include a form that collects additional information from customers to facilitate order fulfillment.</span></span> <span data-ttu-id="469ec-121">有关如何设置此页面和模块的信息，请参阅[客户登记模块](check-in-pickup-module.md)。</span><span class="sxs-lookup"><span data-stu-id="469ec-121">For information about how to set up the page and module, see [Customer check-in module](check-in-pickup-module.md).</span></span>

## <a name="configure-the-transactional-email-template"></a><span data-ttu-id="469ec-122">配置交易电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="469ec-122">Configure the transactional email template</span></span>

<span data-ttu-id="469ec-123">您必须在模板上添加 **我在这里** 链接或按钮，指向客户在订单准备好可以提货时收到的交易电子邮件。</span><span class="sxs-lookup"><span data-stu-id="469ec-123">You must add an **I am here** link or button to the template for the transactional email that customers receive when their order is ready for pickup.</span></span> <span data-ttu-id="469ec-124">客户将使用此链接或按钮通知商店，他们已经到达，可以提货。</span><span class="sxs-lookup"><span data-stu-id="469ec-124">Customers will use this link or button to notify the store that they have arrived to pick up their order.</span></span> 

<span data-ttu-id="469ec-125">将此链接或按钮添加到映射到 **包装已完成** 通知类型和您用于路边订单履行的交货方式的模板中。</span><span class="sxs-lookup"><span data-stu-id="469ec-125">Add the link or button to the template that is mapped to the **Packing completed** notification type and the mode of delivery that you're using for curbside order fulfillment.</span></span> <span data-ttu-id="469ec-126">在模板中，创建一个 HTML 链接或按钮，指向您创建的登记确认页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="469ec-126">In the template, create an HTML link or button that points to the URL of the check-in confirmation page that you created.</span></span> <span data-ttu-id="469ec-127">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="469ec-127">Here is an example.</span></span>

```
<a href="https://[YOUR_SITE_DOMAIN]/[CHECK-IN_CONFIRMATION_PAGE]?channelReferenceId=%channelreferenceid%&channelId=%channelid%&packingSlipId=%packingslipid%" target="_blank">I am here!</a>
```
<span data-ttu-id="469ec-128">有关如何配置电子邮件模板的详细信息，请参阅[按交货模式自定义交易电子邮件](customize-email-delivery-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="469ec-128">For more information about how to configure email templates, see [Customize transactional emails by mode of delivery](customize-email-delivery-mode.md).</span></span> 

## <a name="a-check-in-confirmation-task-is-created-in-pos"></a><span data-ttu-id="469ec-129">POS 中将创建登记确认任务</span><span class="sxs-lookup"><span data-stu-id="469ec-129">A check-in confirmation task is created in POS</span></span>

<span data-ttu-id="469ec-130">在客户通知商店他们在现场可以提货时，他们会收到登记确认通知，POS 中的任务列表中将为客户提货的商店创建一个任务。</span><span class="sxs-lookup"><span data-stu-id="469ec-130">After a customer notifies the store that they are present for pickup, they receive a check-in confirmation notification, and a task is created in the tasks list in POS for the store where the customer is picking up the order.</span></span> <span data-ttu-id="469ec-131">此任务包含履行订单所需的所有客户和订单信息。</span><span class="sxs-lookup"><span data-stu-id="469ec-131">The task contains all the customer and order information that is required to fulfill the order.</span></span> <span data-ttu-id="469ec-132">在任务中，说明字段显示通过其他信息表单从客户那里收集的所有信息。</span><span class="sxs-lookup"><span data-stu-id="469ec-132">In the task, the instructions field shows any information that was collected from the customer through the additional information form.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="469ec-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="469ec-133">Additional resources</span></span>

[<span data-ttu-id="469ec-134">提货登记模块</span><span class="sxs-lookup"><span data-stu-id="469ec-134">Check-in for pickup module</span></span>](check-in-pickup-module.md)
