---
title: 小型包裹装运
description: 本主题提供有关小型包裹装运 (SPS) 功能的信息。 此功能让 Microsoft Dynamics 365 Supply Chain Management 可以将有关已装箱集装箱的详细信息提交给承运人，然后从该承运人处接收发货标签、装运费用和跟踪号。
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 37f07139853c30da25c067a3d736b4b9bf4eb361
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501166"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="6bba8-104">小型包裹装运</span><span class="sxs-lookup"><span data-stu-id="6bba8-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6bba8-105">小型包裹装运 (SPS) 功能提供通过承运人 API 进行通信的框架，以此让 Microsoft Dynamics 365 Supply Chain Management 可以直接与装运承运人交互。</span><span class="sxs-lookup"><span data-stu-id="6bba8-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="6bba8-106">当您通过商业装运承运人装运各个销售订单，而不是使用集装箱装运或零担 (LTL) 装运时，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="6bba8-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="6bba8-107">SPS 功能通过专用的 *费率引擎* 与您的装运承运人交互。</span><span class="sxs-lookup"><span data-stu-id="6bba8-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="6bba8-108">您的组织必须与您的承运人或承运人中心服务合作开发此费率引擎。</span><span class="sxs-lookup"><span data-stu-id="6bba8-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="6bba8-109">费率引擎让 Supply Chain Management 可以将有关已装箱集装箱的详细信息提交给您的承运人，然后从该承运人处接收发货标签、装运费用和跟踪号。</span><span class="sxs-lookup"><span data-stu-id="6bba8-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="6bba8-110">返回的装运费用作为杂项费用添加到关联的销售订单中。</span><span class="sxs-lookup"><span data-stu-id="6bba8-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="6bba8-111">然后，可以使用 Zebra 编程语言 (ZPL) 打印机自动打印返回的发货标签，在装运时使用。</span><span class="sxs-lookup"><span data-stu-id="6bba8-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="6bba8-112">承运人在您的仓库领取包裹时会扫描此发货标签。</span><span class="sxs-lookup"><span data-stu-id="6bba8-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="6bba8-113">准备系统以支持 SPS</span><span class="sxs-lookup"><span data-stu-id="6bba8-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="6bba8-114">您必须先在“功能管理”中打开 SPS 功能，添加费率引擎，并设置 **运输管理** 和 **仓库管理** 模块以支持它，然后才能够开始使用 SPS 功能。</span><span class="sxs-lookup"><span data-stu-id="6bba8-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="6bba8-115">开启 SPS 功能</span><span class="sxs-lookup"><span data-stu-id="6bba8-115">Turn on the SPS feature</span></span>

<span data-ttu-id="6bba8-116">SPS 此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="6bba8-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="6bba8-117">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查此功能的状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="6bba8-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="6bba8-118">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="6bba8-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6bba8-119">**模块**：*运输管理*</span><span class="sxs-lookup"><span data-stu-id="6bba8-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="6bba8-120">**功能名称**：*小型包裹装运*</span><span class="sxs-lookup"><span data-stu-id="6bba8-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="6bba8-121">部署和设置费率引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="6bba8-122">Supply Chain Management 不包括任何费率引擎。</span><span class="sxs-lookup"><span data-stu-id="6bba8-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="6bba8-123">您必须获取或创建所需的任何费率引擎，然后将它们添加到系统中。</span><span class="sxs-lookup"><span data-stu-id="6bba8-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="6bba8-124">不过，Microsoft 提供了可用于测试的演示费率引擎。</span><span class="sxs-lookup"><span data-stu-id="6bba8-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="6bba8-125">下载和部署演示费率引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="6bba8-126">请按照以下步骤获取演示费率引擎。</span><span class="sxs-lookup"><span data-stu-id="6bba8-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="6bba8-127">在 GitHub 上，下载[演示费率引擎的动态链接库 (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS)。</span><span class="sxs-lookup"><span data-stu-id="6bba8-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="6bba8-128">在您的 Supply Chain Management 服务器上，将 DLL 保存在 **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** 文件夹中。</span><span class="sxs-lookup"><span data-stu-id="6bba8-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="6bba8-129">创建和部署功能费率引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="6bba8-130">有关如何创建和部署功能费率引擎以可以在生产或测试环境中使用的信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="6bba8-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="6bba8-131">创建新的运输管理引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="6bba8-132">设置运输管理引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="6bba8-133">有关如何创建 SPS 费率引擎的详细信息，请参阅以下博客文章：[小型包裹装运：如何利用 Microsoft Dynamics 365 中的小型包裹装运功能](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5)。</span><span class="sxs-lookup"><span data-stu-id="6bba8-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="6bba8-134">在 Supply Chain Management 中设置费率引擎</span><span class="sxs-lookup"><span data-stu-id="6bba8-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="6bba8-135">为 SPS 创建和部署费率引擎后，请按照以下步骤进行设置。</span><span class="sxs-lookup"><span data-stu-id="6bba8-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="6bba8-136">转到 **运输管理 \> 设置 \> 引擎 \> 费率引擎**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="6bba8-137">在操作窗格上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="6bba8-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="6bba8-138">在新行中，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="6bba8-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="6bba8-139">**费率引擎** – 为费率引擎输入唯一名称。</span><span class="sxs-lookup"><span data-stu-id="6bba8-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="6bba8-140">如果您使用的是演示费率引擎，请输入 *演示费率引擎*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="6bba8-141">**名称** – 输入费率引擎的简短描述。</span><span class="sxs-lookup"><span data-stu-id="6bba8-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="6bba8-142">如果您使用的是演示费率引擎，请输入 *演示费率引擎*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="6bba8-143">**评级元数据 ID** – 选择应该用于计算费率的依据。</span><span class="sxs-lookup"><span data-stu-id="6bba8-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="6bba8-144">例如，您的费率可能根据距离来计算。</span><span class="sxs-lookup"><span data-stu-id="6bba8-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="6bba8-145">如果您使用的是演示费率引擎，可以将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="6bba8-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="6bba8-146">**引擎程序集** – 输入您部署的 DLL 包的文件名。</span><span class="sxs-lookup"><span data-stu-id="6bba8-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="6bba8-147">如果您使用的是演示费率引擎，请输入 *TMSSmallParcelShippingEngine.dll*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="6bba8-148">**引擎类** – 输入为您的费率引擎确定的类名称。</span><span class="sxs-lookup"><span data-stu-id="6bba8-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="6bba8-149">如果您使用的是演示费率引擎，请输入 *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="6bba8-150">示例场景</span><span class="sxs-lookup"><span data-stu-id="6bba8-150">Example scenario</span></span>

<span data-ttu-id="6bba8-151">此示例场景演示了在准备好系统后如何设置和使用 SPS，如本主题前面所述。</span><span class="sxs-lookup"><span data-stu-id="6bba8-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="6bba8-152">此场景使用前面提到的演示费率引擎。</span><span class="sxs-lookup"><span data-stu-id="6bba8-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="6bba8-153">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="6bba8-153">Make demo data available</span></span>

<span data-ttu-id="6bba8-154">若要使用此处指定的演示记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="6bba8-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="6bba8-155">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="6bba8-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="6bba8-156">设置场景</span><span class="sxs-lookup"><span data-stu-id="6bba8-156">Set up the scenario</span></span>

<span data-ttu-id="6bba8-157">对于此示例场景，您必须有演示承运人、承运人组、装箱策略和装箱模板。</span><span class="sxs-lookup"><span data-stu-id="6bba8-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="6bba8-158">以下小节说明如何准备场景所需的记录。</span><span class="sxs-lookup"><span data-stu-id="6bba8-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="6bba8-159">在生产场景中，设置流程通常类似于此处描述的流程。</span><span class="sxs-lookup"><span data-stu-id="6bba8-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="6bba8-160">但是，您将设置不同的值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="6bba8-161">设置承运人</span><span class="sxs-lookup"><span data-stu-id="6bba8-161">Set up carriers</span></span>

<span data-ttu-id="6bba8-162">请按照以下步骤设置承运人。</span><span class="sxs-lookup"><span data-stu-id="6bba8-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="6bba8-163">转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="6bba8-164">在操作窗格中，选择 **新建** 添加承运人。</span><span class="sxs-lookup"><span data-stu-id="6bba8-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="6bba8-165">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="6bba8-166">**装运承运人**：*演示承运人*</span><span class="sxs-lookup"><span data-stu-id="6bba8-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="6bba8-167">**名称**：*演示承运人*</span><span class="sxs-lookup"><span data-stu-id="6bba8-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="6bba8-168">**模式**：*陆运*</span><span class="sxs-lookup"><span data-stu-id="6bba8-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="6bba8-169">在 **概览** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6bba8-170">**启用装运承运人**：*是*</span><span class="sxs-lookup"><span data-stu-id="6bba8-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="6bba8-171">**启用承运人评级**：*是*</span><span class="sxs-lookup"><span data-stu-id="6bba8-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="6bba8-172">在 **服务** 快速选项卡上，选择 **新建** 向网格添加服务。</span><span class="sxs-lookup"><span data-stu-id="6bba8-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="6bba8-173">为新服务设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="6bba8-174">**承运人服务**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="6bba8-175">**名称**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="6bba8-176">**运输方式**：*陆运*</span><span class="sxs-lookup"><span data-stu-id="6bba8-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="6bba8-177">根据需要为所有其他字段输入任意值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="6bba8-178">（当您保存新的装运承运人记录时，将创建新的交货模式，**交货方式** 字段将自动设置。）</span><span class="sxs-lookup"><span data-stu-id="6bba8-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="6bba8-179">在 **评级模板** 快速选项卡上，选择 **新建** 将评级模板添加到网格。</span><span class="sxs-lookup"><span data-stu-id="6bba8-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="6bba8-180">为新模板设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="6bba8-181">**评级模板**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="6bba8-182">**名称**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="6bba8-183">**费率引擎**：*演示费率引擎*</span><span class="sxs-lookup"><span data-stu-id="6bba8-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="6bba8-184">根据需要为所有其他字段输入任意值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="6bba8-185">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="6bba8-186">有关如何设置承运人的详细信息，请参阅[设置装运承运人](../transportation/tasks/set-up-shipping-carriers.md)。</span><span class="sxs-lookup"><span data-stu-id="6bba8-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="6bba8-187">设置承运人服务帐户</span><span class="sxs-lookup"><span data-stu-id="6bba8-187">Set up carrier service accounts</span></span>

<span data-ttu-id="6bba8-188">请按照以下步骤设置承运人服务帐户。</span><span class="sxs-lookup"><span data-stu-id="6bba8-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="6bba8-189">转到 **运输管理 \> 设置 \> 评级 \> 承运人服务帐户**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="6bba8-190">在操作窗格上，选择 **新建** 添加承运人服务帐户。</span><span class="sxs-lookup"><span data-stu-id="6bba8-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="6bba8-191">为新帐户设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="6bba8-192">**装运承运人**：*演示承运人*</span><span class="sxs-lookup"><span data-stu-id="6bba8-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="6bba8-193">**承运人服务**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="6bba8-194">**承运人客户帐号：** 用于对与装运承运人的连接进行验证和身份验证的承运人客户帐号。</span><span class="sxs-lookup"><span data-stu-id="6bba8-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="6bba8-195">您的承运人会提供此值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-195">Your carrier will provide this value.</span></span> <span data-ttu-id="6bba8-196">如果您使用的是演示服务，可以输入任意值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="6bba8-197">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6bba8-197">**Site:** *6*</span></span>
    - <span data-ttu-id="6bba8-198">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="6bba8-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="6bba8-199">通常，**承运人客户帐号** 值是对连接进行身份验证所需的唯一值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="6bba8-200">但是，如果承运人需要其他身份验证参数，您的组织应自定义此页面来适当添加其他字段。</span><span class="sxs-lookup"><span data-stu-id="6bba8-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="6bba8-201">设置集装箱装箱策略</span><span class="sxs-lookup"><span data-stu-id="6bba8-201">Set up a container packing policy</span></span>

<span data-ttu-id="6bba8-202">请按照以下步骤设置集装箱装箱策略。</span><span class="sxs-lookup"><span data-stu-id="6bba8-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="6bba8-203">如果尚未设置 ZPL 打印机定义，请使用文档路线选择代理应用程序进行设置。</span><span class="sxs-lookup"><span data-stu-id="6bba8-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="6bba8-204">有关详细信息，请参阅[文档打印概述](../../fin-ops-core/dev-itpro/analytics/print-documents.md)及相关主题。</span><span class="sxs-lookup"><span data-stu-id="6bba8-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="6bba8-205">转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱装箱策略**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="6bba8-206">在操作窗格上，选择 **新建** 添加集装箱装箱策略。</span><span class="sxs-lookup"><span data-stu-id="6bba8-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="6bba8-207">在新策略的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="6bba8-208">**集装箱装箱策略**：*演示装箱策略*</span><span class="sxs-lookup"><span data-stu-id="6bba8-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="6bba8-209">**描述：** 策略的描述</span><span class="sxs-lookup"><span data-stu-id="6bba8-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="6bba8-210">在 **概览** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6bba8-211">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="6bba8-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="6bba8-212">**最终装运的默认位置**：*货架门*</span><span class="sxs-lookup"><span data-stu-id="6bba8-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="6bba8-213">**重量单位**：*千克*</span><span class="sxs-lookup"><span data-stu-id="6bba8-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="6bba8-214">**集装箱封闭策略**：*自动发放*</span><span class="sxs-lookup"><span data-stu-id="6bba8-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="6bba8-215">**集装箱发放策略**：*发往最终装运位置*</span><span class="sxs-lookup"><span data-stu-id="6bba8-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="6bba8-216">在 **集装箱清单** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6bba8-217">**容器关闭时自动显示清单**：*是*</span><span class="sxs-lookup"><span data-stu-id="6bba8-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="6bba8-218">**集装箱的清单要求**：*运输管理*</span><span class="sxs-lookup"><span data-stu-id="6bba8-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="6bba8-219">**打印集装箱内容**：*否*</span><span class="sxs-lookup"><span data-stu-id="6bba8-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="6bba8-220">在 **承运人标签打印** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6bba8-221">**打印集装箱发货标签**：*始终*</span><span class="sxs-lookup"><span data-stu-id="6bba8-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="6bba8-222">**打印机名称：** 应打印发货标签的 ZPL 打印机的名称</span><span class="sxs-lookup"><span data-stu-id="6bba8-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="6bba8-223">设置装箱模板</span><span class="sxs-lookup"><span data-stu-id="6bba8-223">Set up a packing profile</span></span>

<span data-ttu-id="6bba8-224">请按照以下步骤设置装箱模板。</span><span class="sxs-lookup"><span data-stu-id="6bba8-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="6bba8-225">转到 **仓库管理 \> 设置 \> 装箱 \> 装箱模板**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="6bba8-226">在操作窗格上，选择 **新建** 向网格添加装箱模板。</span><span class="sxs-lookup"><span data-stu-id="6bba8-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="6bba8-227">为新模板设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="6bba8-228">**装箱模板 ID**：*演示装箱模板*</span><span class="sxs-lookup"><span data-stu-id="6bba8-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="6bba8-229">**描述：** 模板的描述</span><span class="sxs-lookup"><span data-stu-id="6bba8-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="6bba8-230">**集装箱装箱策略**：*演示装箱策略*</span><span class="sxs-lookup"><span data-stu-id="6bba8-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="6bba8-231">**集装箱 ID 模式**：*自动*</span><span class="sxs-lookup"><span data-stu-id="6bba8-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="6bba8-232">**集装箱类型**：*小箱*</span><span class="sxs-lookup"><span data-stu-id="6bba8-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="6bba8-233">将客户设置为使用 SPS 承运人</span><span class="sxs-lookup"><span data-stu-id="6bba8-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="6bba8-234">请按照以下步骤设置客户，让客户可以使用您创建的承运人。</span><span class="sxs-lookup"><span data-stu-id="6bba8-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="6bba8-235">转到 **应收帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="6bba8-236">在网格中，找到并选择客户 *US-027*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="6bba8-237">在操作窗格的 **常规** 选项卡上，在 **设置** 组中，选择 **承运人客户帐户**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="6bba8-238">在 **承运人客户帐户** 页上的操作窗格上，选择 **新建** 向网格添加帐户。</span><span class="sxs-lookup"><span data-stu-id="6bba8-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="6bba8-239">为新帐户设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="6bba8-240">**装运承运人**：*演示承运人*</span><span class="sxs-lookup"><span data-stu-id="6bba8-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="6bba8-241">**承运人客户帐号**：*12345*（此值对于此场景不重要，但将在下一节中引用。）</span><span class="sxs-lookup"><span data-stu-id="6bba8-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="6bba8-242">完成示例场景</span><span class="sxs-lookup"><span data-stu-id="6bba8-242">Go through the example scenario</span></span>

<span data-ttu-id="6bba8-243">如上一节所述设置了所有示例数据之后，您就可以开始完成示例场景了。</span><span class="sxs-lookup"><span data-stu-id="6bba8-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="6bba8-244">创建销售订单与处理工作</span><span class="sxs-lookup"><span data-stu-id="6bba8-244">Create a sales order and process the work</span></span>

<span data-ttu-id="6bba8-245">请按照以下步骤创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="6bba8-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="6bba8-246">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="6bba8-247">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="6bba8-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="6bba8-248">在 **创建销售订单** 对话框中，将 **客户帐户** 字段设置为 *US-027*。</span><span class="sxs-lookup"><span data-stu-id="6bba8-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="6bba8-249">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="6bba8-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="6bba8-250">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="6bba8-250">The new sales order is opened.</span></span> <span data-ttu-id="6bba8-251">在 **销售订单头** 快速选项卡上，将 **承运人客户帐号** 字段设置为您先前为此客户选择的值 (*12345*)。</span><span class="sxs-lookup"><span data-stu-id="6bba8-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="6bba8-252">在 **销售订单行** 部分，添加一行，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="6bba8-253">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="6bba8-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="6bba8-254">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="6bba8-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="6bba8-255">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6bba8-255">**Site:** *6*</span></span>
    - <span data-ttu-id="6bba8-256">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="6bba8-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="6bba8-257">切换到 **标题** 视图。</span><span class="sxs-lookup"><span data-stu-id="6bba8-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="6bba8-258">在 **交货** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="6bba8-259">**装运承运人**：*演示承运人*</span><span class="sxs-lookup"><span data-stu-id="6bba8-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="6bba8-260">**承运人服务**：*演示承运人服务*</span><span class="sxs-lookup"><span data-stu-id="6bba8-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="6bba8-261">切换回 **行** 视图。</span><span class="sxs-lookup"><span data-stu-id="6bba8-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="6bba8-262">如果系统提示您更新销售行的交货方式，请选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="6bba8-263">在 **销售订单行** 部分，选择您之前设置的订单行，然后选择 **库存 \> 预留**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="6bba8-264">在 **预留** 页中，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="6bba8-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="6bba8-265">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="6bba8-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="6bba8-266">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="6bba8-267">将创建将物料从领料位置移到装箱工作站的工作。</span><span class="sxs-lookup"><span data-stu-id="6bba8-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="6bba8-268">在 **销售订单行** 部分，选择 **仓库 \> 装运详细信息**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="6bba8-269">在 **装运详细信息** 页上，记下装运 ID。</span><span class="sxs-lookup"><span data-stu-id="6bba8-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="6bba8-270">在装箱工作站为装运装箱时，您将需要它。</span><span class="sxs-lookup"><span data-stu-id="6bba8-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="6bba8-271">关闭 **装运详细信息** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="6bba8-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="6bba8-272">记下销售订单编号，然后转到 **仓库管理 \> 工作 \> 所有工作**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="6bba8-273">使用销售订单编号查找并选择为订单创建的工作。</span><span class="sxs-lookup"><span data-stu-id="6bba8-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="6bba8-274">在操作窗格上的 **工作** 选项卡中，选择 **完成工作**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="6bba8-275">在 **工作完成** 页上，在 **用户 ID** 字段中，选择一个用户 ID。</span><span class="sxs-lookup"><span data-stu-id="6bba8-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="6bba8-276">然后，在操作窗格中，选择 **验证工作**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="6bba8-277">如果工作通过验证，在操作窗格上选择 **完成工作**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="6bba8-278">工作将被标记为已完成，以模拟将物料移到装箱工作站。</span><span class="sxs-lookup"><span data-stu-id="6bba8-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="6bba8-279">装运装箱</span><span class="sxs-lookup"><span data-stu-id="6bba8-279">Pack the shipment</span></span>

<span data-ttu-id="6bba8-280">请按照以下步骤为装运装箱。</span><span class="sxs-lookup"><span data-stu-id="6bba8-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="6bba8-281">转到 **仓库管理 \> 设置 \> 工作人员**，确保您的用户帐户与用于仓库管理的工作人员帐户相关联。</span><span class="sxs-lookup"><span data-stu-id="6bba8-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="6bba8-282">转到 **仓库管理 \> 领料和集装化 \> 装箱**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="6bba8-283">在 **选择装箱工作站** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="6bba8-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="6bba8-284">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="6bba8-284">**Site:** *6*</span></span>
    - <span data-ttu-id="6bba8-285">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="6bba8-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="6bba8-286">**位置**：*装箱*</span><span class="sxs-lookup"><span data-stu-id="6bba8-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="6bba8-287">**装箱模板 ID**：*演示装箱模板*</span><span class="sxs-lookup"><span data-stu-id="6bba8-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="6bba8-288">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-288">Select **OK**.</span></span>
1. <span data-ttu-id="6bba8-289">**装箱** 页将显示。</span><span class="sxs-lookup"><span data-stu-id="6bba8-289">The **Pack** page appears.</span></span> <span data-ttu-id="6bba8-290">在生产场景中，工作人员将扫描牌照或装运 ID。</span><span class="sxs-lookup"><span data-stu-id="6bba8-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="6bba8-291">但是，对于此场景，请打开 **所有装运** 页，查找您刚才创建的装运的装运编号。</span><span class="sxs-lookup"><span data-stu-id="6bba8-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="6bba8-292">然后，在 **装箱** 页上的 **牌照或装运** 字段中输入此值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="6bba8-293">或者，输入您之前记下的装运 ID。</span><span class="sxs-lookup"><span data-stu-id="6bba8-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="6bba8-294">在“操作窗格”上，选择 **新建集装箱**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="6bba8-295">出现的对话框将显示有关新集装箱的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6bba8-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="6bba8-296">保留默认值，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="6bba8-297">在 **装箱** 页上的 **物料装箱** 快速选项卡上，在 **标识符** 字段中，选择 *A0002* 将该物料装箱。</span><span class="sxs-lookup"><span data-stu-id="6bba8-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="6bba8-298">物料将添加到集装箱中。</span><span class="sxs-lookup"><span data-stu-id="6bba8-298">The item is added to the container.</span></span>
1. <span data-ttu-id="6bba8-299">在操作窗格上，选择 **装运集装箱**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="6bba8-300">出现的 **装运集装箱** 页上将有您刚才创建的集装箱的行。</span><span class="sxs-lookup"><span data-stu-id="6bba8-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="6bba8-301">但是，该行中的 **集装箱清单 ID** 字段当前为空白，因为您还未从承运人那里收到发货标签和跟踪号。</span><span class="sxs-lookup"><span data-stu-id="6bba8-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="6bba8-302">在“操作窗格”上，选择 **封闭集装箱**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="6bba8-303">在 **封闭集装箱** 对话框中，将 **毛重** 字段设置为 *1 千克*，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="6bba8-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="6bba8-304">发货标签现在应该已经在您先前选择的 ZPL 打印机上打印。</span><span class="sxs-lookup"><span data-stu-id="6bba8-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="6bba8-305">标签应类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="6bba8-305">It should resemble the following example.</span></span>

    <span data-ttu-id="6bba8-306">![示例发货标签](media/sps-label-example.png "示例发货标签")</span><span class="sxs-lookup"><span data-stu-id="6bba8-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="6bba8-307">注意 **集装箱清单 ID** 和 **总运费** 值已添加从承运人处收到的值。</span><span class="sxs-lookup"><span data-stu-id="6bba8-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]