---
title: 在交易和收据电子邮件中添加 QR 码或条形码
description: 本主题说明了如何在 Microsoft Dynamics 365 Commerce 中将表示订单 ID 的 QR 码和条形码插入交易和收据电子邮件。
author: bicyclingfool
manager: annbe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3cc4fcb1237f8409a89b3d4818c132c60c57b5a0
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555414"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="f852d-103">在交易和收据电子邮件中添加 QR 码或条形码</span><span class="sxs-lookup"><span data-stu-id="f852d-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f852d-104">本主题说明了如何在 Microsoft Dynamics 365 Commerce 中将表示订单 ID 的 QR 码和条形码插入交易和收据电子邮件。</span><span class="sxs-lookup"><span data-stu-id="f852d-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f852d-105">您可以轻松地在交易电子邮件中包含 QR 码和条形码，以在零售环境中帮助加快订单查找过程。</span><span class="sxs-lookup"><span data-stu-id="f852d-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="f852d-106">要将 QR 码和条形码插入电子邮件，请使用 HTML **\<img\>** 标签，从生成和呈现服务请求 QR 码或条形码图像。</span><span class="sxs-lookup"><span data-stu-id="f852d-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="f852d-107">Microsoft 不提供此服务。</span><span class="sxs-lookup"><span data-stu-id="f852d-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="f852d-108">但是，有许多免费或廉价的服务，可以提供根据在查询字符串中传递的值动态生成的 QR 码或条形码。</span><span class="sxs-lookup"><span data-stu-id="f852d-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="f852d-109">在交易电子邮件中添加 QR 码或条形码</span><span class="sxs-lookup"><span data-stu-id="f852d-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="f852d-110">要将 QR 码或条形码插入到在电子商务购买过程中发送的交易电子邮件中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f852d-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="f852d-111">打开交易电子邮件模板的源 HTML，然后添加指向您的 QR 码或条形码服务的 HTML **\<img\>** 标记。</span><span class="sxs-lookup"><span data-stu-id="f852d-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="f852d-112">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="f852d-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="f852d-113">以下是对上述示例的说明：</span><span class="sxs-lookup"><span data-stu-id="f852d-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="f852d-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** 代表您的 QR 码或条形码服务的域。</span><span class="sxs-lookup"><span data-stu-id="f852d-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="f852d-115">**数据** 表示 QR 码或条形码服务接收应呈现为 QR 码或条形码的内容所使用的参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="f852d-116">必须给该参数分配 **%salesid%** 值。</span><span class="sxs-lookup"><span data-stu-id="f852d-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="f852d-117">在此示例中，请注意，该值还用作图像的替代文本。</span><span class="sxs-lookup"><span data-stu-id="f852d-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="f852d-118">**param1** 和 **param2** 表示其他可选参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="f852d-119">转到 **Retail 和 Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**，然后将更新的 HTML 上传到适当的交易电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="f852d-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="f852d-120">在 QR 码和条形码服务提供商之间，参数可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="f852d-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="f852d-121">因此，请确保与您的服务提供商联系以确认您必须为其分配值的参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="f852d-122">在收据电子邮件中添加 QR 码或条形码</span><span class="sxs-lookup"><span data-stu-id="f852d-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="f852d-123">要将 QR 码或条形码插入到可以在销售点 (POS) 购买后发送的收据电子邮件中，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f852d-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="f852d-124">打开收据电子邮件模板的源 HTML，然后添加指向您的 QR 码或条形码服务的 HTML **\<img\>** 标记。</span><span class="sxs-lookup"><span data-stu-id="f852d-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="f852d-125">下面是一个示例。</span><span class="sxs-lookup"><span data-stu-id="f852d-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="f852d-126">以下是对上述示例的说明：</span><span class="sxs-lookup"><span data-stu-id="f852d-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="f852d-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** 代表您的 QR 码或条形码服务的域。</span><span class="sxs-lookup"><span data-stu-id="f852d-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="f852d-128">**数据** 表示 QR 码或条形码服务接收应呈现为 QR 码或条形码的内容所使用的参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="f852d-129">必须给该参数分配 **%receiptid%** 值。</span><span class="sxs-lookup"><span data-stu-id="f852d-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="f852d-130">在此示例中，请注意，该值还用作图像的替代文本。</span><span class="sxs-lookup"><span data-stu-id="f852d-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="f852d-131">**param1** 和 **param2** 表示其他可选参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="f852d-132">转到 **Retail 和 Commerce \> 总部设置 \> 参数 \> 组织电子邮件模板**，然后将更新的 HTML 上传到具有电子邮件 ID **emailrecpt** 的电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="f852d-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="f852d-133">在 QR 码和条形码服务提供商之间，参数可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="f852d-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="f852d-134">因此，请确保与您的服务提供商联系以确认您必须为其分配值的参数。</span><span class="sxs-lookup"><span data-stu-id="f852d-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f852d-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="f852d-135">Additional resources</span></span>

[<span data-ttu-id="f852d-136">从 Modern POS (MPOS) 发送电子邮件收据</span><span class="sxs-lookup"><span data-stu-id="f852d-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="f852d-137">创建交易事件的电子邮件模板</span><span class="sxs-lookup"><span data-stu-id="f852d-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
