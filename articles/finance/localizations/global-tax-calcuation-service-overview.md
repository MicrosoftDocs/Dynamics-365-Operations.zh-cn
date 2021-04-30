---
title: 税款计算(预览版)
description: 本主题说明税务计算功能的总体范围和功能。
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3df952e0632807e55f176e63dc2047be5e622ec2
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892341"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="c3cf0-103">税款计算(预览版)</span><span class="sxs-lookup"><span data-stu-id="c3cf0-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="c3cf0-104">税务计算是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="c3cf0-105">税务引擎完全可配置。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="c3cf0-106">可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="c3cf0-107">税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="c3cf0-108">税务计算与 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c3cf0-109">最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="c3cf0-110">税务计算是基于微服务的税务引擎，可提供指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="c3cf0-111">它可以帮助您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="c3cf0-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="c3cf0-112">通过 Regulatory Configuration Service (RCS) 配置税务计算。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="c3cf0-113">RCS 是增强版本的电子报告 (ER) 设计器，可作为独立服务提供。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="c3cf0-114">配置税务矩阵以自动确定税码和税率。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="c3cf0-115">配置税务矩阵以自动确定税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="c3cf0-116">配置税务计算设计器以定义公式和条件。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="c3cf0-117">跨法人共享税务确定和计算解决方案。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="c3cf0-118">若要使用税务计算服务，请在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目安装税务计算服务加载项。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c3cf0-119">然后，在 RCS 中完成设置，并在 Finance 和 Supply Chain Management 中启用税务计算服务。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="c3cf0-120">有关详细信息，请参阅[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="c3cf0-121">可用性</span><span class="sxs-lookup"><span data-stu-id="c3cf0-121">Availability</span></span>

<span data-ttu-id="c3cf0-122">税务计算通过公开预览版计划仅在沙盒环境中对所选客户可用。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="c3cf0-123">最终，它将在生产环境中对所有客户公开可用。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="c3cf0-124">将继续提供新功能，因此务必经常查看最新文档，以了解受支持功能的覆盖率和范围。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="c3cf0-125">税务计算在以下 Azure 地理区域中部署。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="c3cf0-126">它还将根据客户需求部署到更多 Azure 地理区域：</span><span class="sxs-lookup"><span data-stu-id="c3cf0-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="c3cf0-127">美国</span><span class="sxs-lookup"><span data-stu-id="c3cf0-127">United States</span></span>
- <span data-ttu-id="c3cf0-128">欧洲</span><span class="sxs-lookup"><span data-stu-id="c3cf0-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="c3cf0-129">税务计算不支持 Dynamics 365 的本地部署。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="c3cf0-130">它还不支持早期版本，例如 Dynamics AX 2012。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="c3cf0-131">功能亮点</span><span class="sxs-lookup"><span data-stu-id="c3cf0-131">Feature highlights</span></span>

- <span data-ttu-id="c3cf0-132">可配置的税务矩阵，用于自动确定和计算税务</span><span class="sxs-lookup"><span data-stu-id="c3cf0-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="c3cf0-133">支持多个税务登记编号</span><span class="sxs-lookup"><span data-stu-id="c3cf0-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="c3cf0-134">对税务确定和计算的转移单支持</span><span class="sxs-lookup"><span data-stu-id="c3cf0-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="c3cf0-135">对确定多个税务登记编号的转移单支持</span><span class="sxs-lookup"><span data-stu-id="c3cf0-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="c3cf0-136">支持的交易</span><span class="sxs-lookup"><span data-stu-id="c3cf0-136">Supported transactions</span></span>

<span data-ttu-id="c3cf0-137">可以通过法人和交易启用税务计算。</span><span class="sxs-lookup"><span data-stu-id="c3cf0-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="c3cf0-138">支持以下交易：</span><span class="sxs-lookup"><span data-stu-id="c3cf0-138">The following transactions are supported:</span></span>

- <span data-ttu-id="c3cf0-139">销售流程</span><span class="sxs-lookup"><span data-stu-id="c3cf0-139">Sales process</span></span>

    - <span data-ttu-id="c3cf0-140">销售报价</span><span class="sxs-lookup"><span data-stu-id="c3cf0-140">Sales quotation</span></span>
    - <span data-ttu-id="c3cf0-141">销售订单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-141">Sales order</span></span>
    - <span data-ttu-id="c3cf0-142">确认单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-142">Confirmation</span></span>
    - <span data-ttu-id="c3cf0-143">领料单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-143">Picking list</span></span>
    - <span data-ttu-id="c3cf0-144">装箱单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-144">Packing slip</span></span>
    - <span data-ttu-id="c3cf0-145">销售账单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-145">Sales invoice</span></span>
    - <span data-ttu-id="c3cf0-146">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-146">Credit note</span></span>
    - <span data-ttu-id="c3cf0-147">退货单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-147">Return order</span></span>
    - <span data-ttu-id="c3cf0-148">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c3cf0-149">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="c3cf0-150">采购流程</span><span class="sxs-lookup"><span data-stu-id="c3cf0-150">Purchase process</span></span>

    - <span data-ttu-id="c3cf0-151">采购订单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-151">Purchase order</span></span>
    - <span data-ttu-id="c3cf0-152">确认单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-152">Confirmation</span></span>
    - <span data-ttu-id="c3cf0-153">收货清单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-153">Receipts list</span></span>
    - <span data-ttu-id="c3cf0-154">产品收据</span><span class="sxs-lookup"><span data-stu-id="c3cf0-154">Product receipt</span></span>
    - <span data-ttu-id="c3cf0-155">采购账单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-155">Purchase invoice</span></span>
    - <span data-ttu-id="c3cf0-156">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="c3cf0-157">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="c3cf0-158">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-158">Credit note</span></span>
    - <span data-ttu-id="c3cf0-159">退货单</span><span class="sxs-lookup"><span data-stu-id="c3cf0-159">Return order</span></span>
    - <span data-ttu-id="c3cf0-160">采购申请</span><span class="sxs-lookup"><span data-stu-id="c3cf0-160">Purchase requisition</span></span>
    - <span data-ttu-id="c3cf0-161">采购申请行杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="c3cf0-162">询价</span><span class="sxs-lookup"><span data-stu-id="c3cf0-162">Request for quotation</span></span>
    - <span data-ttu-id="c3cf0-163">询价标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="c3cf0-164">询价行杂项费用</span><span class="sxs-lookup"><span data-stu-id="c3cf0-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="c3cf0-165">库存流程</span><span class="sxs-lookup"><span data-stu-id="c3cf0-165">Inventory process</span></span>

    - <span data-ttu-id="c3cf0-166">转移单 – 装运</span><span class="sxs-lookup"><span data-stu-id="c3cf0-166">Transfer order – ship</span></span>
    - <span data-ttu-id="c3cf0-167">转移单 – 接收</span><span class="sxs-lookup"><span data-stu-id="c3cf0-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="c3cf0-168">相关资源</span><span class="sxs-lookup"><span data-stu-id="c3cf0-168">Related resources</span></span>

[<span data-ttu-id="c3cf0-169">开始使用税务服务</span><span class="sxs-lookup"><span data-stu-id="c3cf0-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="c3cf0-170">多个增值税登记编号</span><span class="sxs-lookup"><span data-stu-id="c3cf0-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="c3cf0-171">转移单的税务功能支持</span><span class="sxs-lookup"><span data-stu-id="c3cf0-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="c3cf0-172">如何在税务服务中生成扩展</span><span class="sxs-lookup"><span data-stu-id="c3cf0-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)