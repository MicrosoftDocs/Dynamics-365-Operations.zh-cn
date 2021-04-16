---
title: 税务计算服务（预览）
description: 本主题说明税务计算服务的总体范围和功能。
author: wangchen
ms.date: 03/02/2021
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
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818216"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="ec030-103">税务计算服务（预览）</span><span class="sxs-lookup"><span data-stu-id="ec030-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="ec030-104">税务计算服务是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。</span><span class="sxs-lookup"><span data-stu-id="ec030-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="ec030-105">税务引擎完全可配置。</span><span class="sxs-lookup"><span data-stu-id="ec030-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="ec030-106">可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。</span><span class="sxs-lookup"><span data-stu-id="ec030-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="ec030-107">税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="ec030-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="ec030-108">税务计算服务与 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。</span><span class="sxs-lookup"><span data-stu-id="ec030-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ec030-109">最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="ec030-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="ec030-110">税务计算服务是基于 Microsoft 的税务引擎，可提供指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="ec030-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="ec030-111">它可以帮助您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="ec030-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="ec030-112">通过 Regulatory Configuration Service (RCS) 配置税务计算服务。</span><span class="sxs-lookup"><span data-stu-id="ec030-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="ec030-113">RCS 是增强版本的电子报告 (ER) 设计器，可作为独立服务提供。</span><span class="sxs-lookup"><span data-stu-id="ec030-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="ec030-114">配置税务矩阵以自动确定税码和税率。</span><span class="sxs-lookup"><span data-stu-id="ec030-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="ec030-115">配置税务矩阵以自动确定税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="ec030-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="ec030-116">配置税务计算设计器以定义公式和条件。</span><span class="sxs-lookup"><span data-stu-id="ec030-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="ec030-117">跨法人共享税务确定和计算解决方案。</span><span class="sxs-lookup"><span data-stu-id="ec030-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="ec030-118">若要使用税务计算服务，请在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目安装税务计算服务加载项。</span><span class="sxs-lookup"><span data-stu-id="ec030-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="ec030-119">然后，在 RCS 中完成设置，并在 Finance 和 Supply Chain Management 中启用税务计算服务。</span><span class="sxs-lookup"><span data-stu-id="ec030-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="ec030-120">有关详细信息，请参阅[开始使用税务服务](https://go.microsoft.com/fwlink/?linkid=2138482)。</span><span class="sxs-lookup"><span data-stu-id="ec030-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="ec030-121">可用性</span><span class="sxs-lookup"><span data-stu-id="ec030-121">Availability</span></span>

<span data-ttu-id="ec030-122">税务计算服务通过公开预览版计划仅在沙盒环境中对所选客户可用。</span><span class="sxs-lookup"><span data-stu-id="ec030-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="ec030-123">最终，它将在生产环境中对所有客户公开可用。</span><span class="sxs-lookup"><span data-stu-id="ec030-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="ec030-124">新功能将继续在税务计算服务中提供。</span><span class="sxs-lookup"><span data-stu-id="ec030-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="ec030-125">因此，请务必经常查看最新文档，以了解受支持功能的覆盖率和范围。</span><span class="sxs-lookup"><span data-stu-id="ec030-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="ec030-126">税务计算服务在以下 Azure 地理区域中部署。</span><span class="sxs-lookup"><span data-stu-id="ec030-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="ec030-127">它还将根据客户需求部署到更多 Azure 地理区域：</span><span class="sxs-lookup"><span data-stu-id="ec030-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="ec030-128">美国</span><span class="sxs-lookup"><span data-stu-id="ec030-128">United States</span></span>
- <span data-ttu-id="ec030-129">欧洲</span><span class="sxs-lookup"><span data-stu-id="ec030-129">Europe</span></span>
- <span data-ttu-id="ec030-130">法国</span><span class="sxs-lookup"><span data-stu-id="ec030-130">France</span></span>
- <span data-ttu-id="ec030-131">英国</span><span class="sxs-lookup"><span data-stu-id="ec030-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="ec030-132">税务计算服务不支持 Dynamics 365 的本地部署。</span><span class="sxs-lookup"><span data-stu-id="ec030-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="ec030-133">它还不支持早期版本，例如 Dynamics AX 2012。</span><span class="sxs-lookup"><span data-stu-id="ec030-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="ec030-134">功能亮点</span><span class="sxs-lookup"><span data-stu-id="ec030-134">Feature highlights</span></span>

- <span data-ttu-id="ec030-135">可配置的税务矩阵，用于自动确定和计算税务</span><span class="sxs-lookup"><span data-stu-id="ec030-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="ec030-136">对多个增值税 (VAT) 登记编号的支持</span><span class="sxs-lookup"><span data-stu-id="ec030-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="ec030-137">对税务确定和计算的转移单支持</span><span class="sxs-lookup"><span data-stu-id="ec030-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="ec030-138">对确定多个增值税登记编号的转移单支持</span><span class="sxs-lookup"><span data-stu-id="ec030-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="ec030-139">支持的交易</span><span class="sxs-lookup"><span data-stu-id="ec030-139">Supported transactions</span></span>

<span data-ttu-id="ec030-140">可以通过法人和交易启用税务计算服务。</span><span class="sxs-lookup"><span data-stu-id="ec030-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="ec030-141">支持以下交易：</span><span class="sxs-lookup"><span data-stu-id="ec030-141">The following transactions are supported:</span></span>

- <span data-ttu-id="ec030-142">销售流程</span><span class="sxs-lookup"><span data-stu-id="ec030-142">Sales process</span></span>

    - <span data-ttu-id="ec030-143">销售报价</span><span class="sxs-lookup"><span data-stu-id="ec030-143">Sales quotation</span></span>
    - <span data-ttu-id="ec030-144">销售订单</span><span class="sxs-lookup"><span data-stu-id="ec030-144">Sales order</span></span>
    - <span data-ttu-id="ec030-145">确认单</span><span class="sxs-lookup"><span data-stu-id="ec030-145">Confirmation</span></span>
    - <span data-ttu-id="ec030-146">领料单</span><span class="sxs-lookup"><span data-stu-id="ec030-146">Picking list</span></span>
    - <span data-ttu-id="ec030-147">装箱单</span><span class="sxs-lookup"><span data-stu-id="ec030-147">Packing slip</span></span>
    - <span data-ttu-id="ec030-148">销售账单</span><span class="sxs-lookup"><span data-stu-id="ec030-148">Sales invoice</span></span>
    - <span data-ttu-id="ec030-149">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="ec030-149">Credit note</span></span>
    - <span data-ttu-id="ec030-150">退货单</span><span class="sxs-lookup"><span data-stu-id="ec030-150">Return order</span></span>
    - <span data-ttu-id="ec030-151">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ec030-152">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="ec030-153">采购流程</span><span class="sxs-lookup"><span data-stu-id="ec030-153">Purchase process</span></span>

    - <span data-ttu-id="ec030-154">采购订单</span><span class="sxs-lookup"><span data-stu-id="ec030-154">Purchase order</span></span>
    - <span data-ttu-id="ec030-155">确认单</span><span class="sxs-lookup"><span data-stu-id="ec030-155">Confirmation</span></span>
    - <span data-ttu-id="ec030-156">收货清单</span><span class="sxs-lookup"><span data-stu-id="ec030-156">Receipts list</span></span>
    - <span data-ttu-id="ec030-157">产品收据</span><span class="sxs-lookup"><span data-stu-id="ec030-157">Product receipt</span></span>
    - <span data-ttu-id="ec030-158">采购账单</span><span class="sxs-lookup"><span data-stu-id="ec030-158">Purchase invoice</span></span>
    - <span data-ttu-id="ec030-159">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="ec030-160">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="ec030-161">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="ec030-161">Credit note</span></span>
    - <span data-ttu-id="ec030-162">退货单</span><span class="sxs-lookup"><span data-stu-id="ec030-162">Return order</span></span>
    - <span data-ttu-id="ec030-163">采购申请</span><span class="sxs-lookup"><span data-stu-id="ec030-163">Purchase requisition</span></span>
    - <span data-ttu-id="ec030-164">采购申请行杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="ec030-165">询价</span><span class="sxs-lookup"><span data-stu-id="ec030-165">Request for quotation</span></span>
    - <span data-ttu-id="ec030-166">询价标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="ec030-167">询价行杂项费用</span><span class="sxs-lookup"><span data-stu-id="ec030-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="ec030-168">库存流程</span><span class="sxs-lookup"><span data-stu-id="ec030-168">Inventory process</span></span>

    - <span data-ttu-id="ec030-169">转移单 – 装运</span><span class="sxs-lookup"><span data-stu-id="ec030-169">Transfer order – ship</span></span>
    - <span data-ttu-id="ec030-170">转移单 – 接收</span><span class="sxs-lookup"><span data-stu-id="ec030-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="ec030-171">相关资源</span><span class="sxs-lookup"><span data-stu-id="ec030-171">Related resources</span></span>

[<span data-ttu-id="ec030-172">开始使用税务服务</span><span class="sxs-lookup"><span data-stu-id="ec030-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="ec030-173">多个增值税登记编号</span><span class="sxs-lookup"><span data-stu-id="ec030-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="ec030-174">转移单的税务功能支持</span><span class="sxs-lookup"><span data-stu-id="ec030-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="ec030-175">如何在税务服务中生成扩展</span><span class="sxs-lookup"><span data-stu-id="ec030-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
