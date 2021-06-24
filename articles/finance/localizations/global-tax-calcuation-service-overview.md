---
title: 税款计算(预览版)
description: 本主题说明税务计算功能的总体范围和功能。
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184093"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="39ab1-103">税款计算(预览版)</span><span class="sxs-lookup"><span data-stu-id="39ab1-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="39ab1-104">税务计算是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。</span><span class="sxs-lookup"><span data-stu-id="39ab1-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="39ab1-105">税务引擎完全可配置。</span><span class="sxs-lookup"><span data-stu-id="39ab1-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="39ab1-106">可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。</span><span class="sxs-lookup"><span data-stu-id="39ab1-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="39ab1-107">税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="39ab1-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="39ab1-108">税务计算与 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。</span><span class="sxs-lookup"><span data-stu-id="39ab1-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="39ab1-109">最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。</span><span class="sxs-lookup"><span data-stu-id="39ab1-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39ab1-110">当您启用税务计算服务时，可能在数据中心（维护您的服务数据的数据中心除外）中执行对相关数据的某些操作。</span><span class="sxs-lookup"><span data-stu-id="39ab1-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="39ab1-111">在启用税务计算服务之前，查看[条款和条件](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)。</span><span class="sxs-lookup"><span data-stu-id="39ab1-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="39ab1-112">我们非常尊重您的隐私。</span><span class="sxs-lookup"><span data-stu-id="39ab1-112">Your privacy is important to us.</span></span> <span data-ttu-id="39ab1-113">要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。</span><span class="sxs-lookup"><span data-stu-id="39ab1-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="39ab1-114">税务计算是基于微服务的税务引擎，可提供指数可扩展性。</span><span class="sxs-lookup"><span data-stu-id="39ab1-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="39ab1-115">它可以帮助您执行以下任务：</span><span class="sxs-lookup"><span data-stu-id="39ab1-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="39ab1-116">通过 Regulatory Configuration Service (RCS) 配置税务计算。</span><span class="sxs-lookup"><span data-stu-id="39ab1-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="39ab1-117">RCS 是增强版本的电子报告 (ER) 设计器，可作为独立服务提供。</span><span class="sxs-lookup"><span data-stu-id="39ab1-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="39ab1-118">配置税务矩阵以自动确定税码和税率。</span><span class="sxs-lookup"><span data-stu-id="39ab1-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="39ab1-119">配置税务矩阵以自动确定税务登记编号。</span><span class="sxs-lookup"><span data-stu-id="39ab1-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="39ab1-120">配置税务计算设计器以定义公式和条件。</span><span class="sxs-lookup"><span data-stu-id="39ab1-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="39ab1-121">跨法人共享税务确定和计算解决方案。</span><span class="sxs-lookup"><span data-stu-id="39ab1-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="39ab1-122">若要使用税务计算服务，请在 Microsoft Dynamics Lifecycle Services (LCS) 中从您的项目安装税务计算服务加载项。</span><span class="sxs-lookup"><span data-stu-id="39ab1-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="39ab1-123">然后，在 RCS 中完成设置，并在 Finance 和 Supply Chain Management 中启用税务计算服务。</span><span class="sxs-lookup"><span data-stu-id="39ab1-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="39ab1-124">有关详细信息，请参阅[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)。</span><span class="sxs-lookup"><span data-stu-id="39ab1-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="39ab1-125">可用性</span><span class="sxs-lookup"><span data-stu-id="39ab1-125">Availability</span></span>

<span data-ttu-id="39ab1-126">税务计算通过公开预览版计划仅在沙盒环境中对所选客户可用。</span><span class="sxs-lookup"><span data-stu-id="39ab1-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="39ab1-127">最终，它将在生产环境中对所有客户公开可用。</span><span class="sxs-lookup"><span data-stu-id="39ab1-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="39ab1-128">将继续提供新功能，因此务必经常查看最新文档，以了解受支持功能的覆盖率和范围。</span><span class="sxs-lookup"><span data-stu-id="39ab1-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="39ab1-129">税务计算在以下 Azure 地理区域中部署。</span><span class="sxs-lookup"><span data-stu-id="39ab1-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="39ab1-130">它还将根据客户需求部署到更多 Azure 地理区域：</span><span class="sxs-lookup"><span data-stu-id="39ab1-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="39ab1-131">美国</span><span class="sxs-lookup"><span data-stu-id="39ab1-131">United States</span></span>
- <span data-ttu-id="39ab1-132">欧洲</span><span class="sxs-lookup"><span data-stu-id="39ab1-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="39ab1-133">税务计算不支持 Dynamics 365 的本地部署。</span><span class="sxs-lookup"><span data-stu-id="39ab1-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="39ab1-134">它还不支持早期版本，例如 Dynamics AX 2012。</span><span class="sxs-lookup"><span data-stu-id="39ab1-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="39ab1-135">功能亮点</span><span class="sxs-lookup"><span data-stu-id="39ab1-135">Feature highlights</span></span>

- <span data-ttu-id="39ab1-136">可配置的税务矩阵，用于自动确定和计算税务</span><span class="sxs-lookup"><span data-stu-id="39ab1-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="39ab1-137">支持多个税务登记编号</span><span class="sxs-lookup"><span data-stu-id="39ab1-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="39ab1-138">对税务确定和计算的转移单支持</span><span class="sxs-lookup"><span data-stu-id="39ab1-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="39ab1-139">对确定多个税务登记编号的转移单支持</span><span class="sxs-lookup"><span data-stu-id="39ab1-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="39ab1-140">支持的交易</span><span class="sxs-lookup"><span data-stu-id="39ab1-140">Supported transactions</span></span>

<span data-ttu-id="39ab1-141">可以通过法人和交易启用税务计算。</span><span class="sxs-lookup"><span data-stu-id="39ab1-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="39ab1-142">支持以下交易：</span><span class="sxs-lookup"><span data-stu-id="39ab1-142">The following transactions are supported:</span></span>

- <span data-ttu-id="39ab1-143">销售流程</span><span class="sxs-lookup"><span data-stu-id="39ab1-143">Sales process</span></span>

    - <span data-ttu-id="39ab1-144">销售报价</span><span class="sxs-lookup"><span data-stu-id="39ab1-144">Sales quotation</span></span>
    - <span data-ttu-id="39ab1-145">销售订单</span><span class="sxs-lookup"><span data-stu-id="39ab1-145">Sales order</span></span>
    - <span data-ttu-id="39ab1-146">确认单</span><span class="sxs-lookup"><span data-stu-id="39ab1-146">Confirmation</span></span>
    - <span data-ttu-id="39ab1-147">领料单</span><span class="sxs-lookup"><span data-stu-id="39ab1-147">Picking list</span></span>
    - <span data-ttu-id="39ab1-148">装箱单</span><span class="sxs-lookup"><span data-stu-id="39ab1-148">Packing slip</span></span>
    - <span data-ttu-id="39ab1-149">销售账单</span><span class="sxs-lookup"><span data-stu-id="39ab1-149">Sales invoice</span></span>
    - <span data-ttu-id="39ab1-150">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="39ab1-150">Credit note</span></span>
    - <span data-ttu-id="39ab1-151">退货单</span><span class="sxs-lookup"><span data-stu-id="39ab1-151">Return order</span></span>
    - <span data-ttu-id="39ab1-152">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="39ab1-153">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="39ab1-154">采购流程</span><span class="sxs-lookup"><span data-stu-id="39ab1-154">Purchase process</span></span>

    - <span data-ttu-id="39ab1-155">采购订单</span><span class="sxs-lookup"><span data-stu-id="39ab1-155">Purchase order</span></span>
    - <span data-ttu-id="39ab1-156">确认单</span><span class="sxs-lookup"><span data-stu-id="39ab1-156">Confirmation</span></span>
    - <span data-ttu-id="39ab1-157">收货清单</span><span class="sxs-lookup"><span data-stu-id="39ab1-157">Receipts list</span></span>
    - <span data-ttu-id="39ab1-158">产品收据</span><span class="sxs-lookup"><span data-stu-id="39ab1-158">Product receipt</span></span>
    - <span data-ttu-id="39ab1-159">采购账单</span><span class="sxs-lookup"><span data-stu-id="39ab1-159">Purchase invoice</span></span>
    - <span data-ttu-id="39ab1-160">标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="39ab1-161">行杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="39ab1-162">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="39ab1-162">Credit note</span></span>
    - <span data-ttu-id="39ab1-163">退货单</span><span class="sxs-lookup"><span data-stu-id="39ab1-163">Return order</span></span>
    - <span data-ttu-id="39ab1-164">采购申请</span><span class="sxs-lookup"><span data-stu-id="39ab1-164">Purchase requisition</span></span>
    - <span data-ttu-id="39ab1-165">采购申请行杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="39ab1-166">询价</span><span class="sxs-lookup"><span data-stu-id="39ab1-166">Request for quotation</span></span>
    - <span data-ttu-id="39ab1-167">询价标题杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="39ab1-168">询价行杂项费用</span><span class="sxs-lookup"><span data-stu-id="39ab1-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="39ab1-169">库存流程</span><span class="sxs-lookup"><span data-stu-id="39ab1-169">Inventory process</span></span>

    - <span data-ttu-id="39ab1-170">转移单 – 装运</span><span class="sxs-lookup"><span data-stu-id="39ab1-170">Transfer order – ship</span></span>
    - <span data-ttu-id="39ab1-171">转移单 – 接收</span><span class="sxs-lookup"><span data-stu-id="39ab1-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="39ab1-172">相关资源</span><span class="sxs-lookup"><span data-stu-id="39ab1-172">Related resources</span></span>

[<span data-ttu-id="39ab1-173">开始使用税务服务</span><span class="sxs-lookup"><span data-stu-id="39ab1-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="39ab1-174">多个增值税登记编号</span><span class="sxs-lookup"><span data-stu-id="39ab1-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="39ab1-175">转移单的税务功能支持</span><span class="sxs-lookup"><span data-stu-id="39ab1-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="39ab1-176">如何在税务服务中生成扩展</span><span class="sxs-lookup"><span data-stu-id="39ab1-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
