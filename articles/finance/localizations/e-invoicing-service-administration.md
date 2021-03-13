---
title: 电子开票附加产品管理组件
description: 本主题提供有关与电子开票附加产品的管理相关的组件的信息。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104350"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="b419a-103">电子开票附加产品管理组件</span><span class="sxs-lookup"><span data-stu-id="b419a-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="b419a-104">本主题提供有关与电子开票附加产品的管理相关的组件的信息。</span><span class="sxs-lookup"><span data-stu-id="b419a-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="b419a-105">另外还提供有关如何配置电子开票附加产品服务的信息。</span><span class="sxs-lookup"><span data-stu-id="b419a-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="b419a-106">Azure</span><span class="sxs-lookup"><span data-stu-id="b419a-106">Azure</span></span>

<span data-ttu-id="b419a-107">使用 Microsoft Azure 为密钥保管库和存储帐户创建机密。</span><span class="sxs-lookup"><span data-stu-id="b419a-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="b419a-108">然后在电子开票附加产品的配置中使用这些机密。</span><span class="sxs-lookup"><span data-stu-id="b419a-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="b419a-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b419a-109">Lifecycle Services</span></span>

<span data-ttu-id="b419a-110">使用 Microsoft Dynamics Lifecycle Services (LCS) 为您的 LCS 部署项目启用微服务附加产品。</span><span class="sxs-lookup"><span data-stu-id="b419a-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="b419a-111">在 LCS 中，选择 **预览功能管理** 磁贴，然后打开 **电子开票服务** 功能。</span><span class="sxs-lookup"><span data-stu-id="b419a-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="b419a-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="b419a-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="b419a-113">Dynamics 365 Regulatory Configuration Services (RCS) 是用于配置电子开票附加产品的界面。</span><span class="sxs-lookup"><span data-stu-id="b419a-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="b419a-114">将在 RCS 中创建、维护和托管环境和电子开票功能等资源。</span><span class="sxs-lookup"><span data-stu-id="b419a-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="b419a-115">当资源准备好后，它们将被发布到电子开票附加产品服务。</span><span class="sxs-lookup"><span data-stu-id="b419a-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="b419a-116">有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="b419a-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="b419a-117">与电子开票附加产品集成</span><span class="sxs-lookup"><span data-stu-id="b419a-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="b419a-118">必须先配置 RCS 以允许与电子开票附加产品通信，然后才能够使用 RCS 配置电子发票。</span><span class="sxs-lookup"><span data-stu-id="b419a-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="b419a-119">您在 **电子报告参数** 页的 **电子开票附加产品** 选项卡上完成此配置。</span><span class="sxs-lookup"><span data-stu-id="b419a-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="b419a-120">服务终结点</span><span class="sxs-lookup"><span data-stu-id="b419a-120">Service endpoint</span></span>

<span data-ttu-id="b419a-121">电子开票附加产品终结点的 URL 可能根据 Azure 数据中心的地理位置发生变化。</span><span class="sxs-lookup"><span data-stu-id="b419a-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="b419a-122">下表列出了每个区域的可用性：</span><span class="sxs-lookup"><span data-stu-id="b419a-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="b419a-123">Azure 数据中心地理位置</span><span class="sxs-lookup"><span data-stu-id="b419a-123">Azure datacenter geography</span></span> | <span data-ttu-id="b419a-124">服务终结点 URL</span><span class="sxs-lookup"><span data-stu-id="b419a-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="b419a-125">美国东部</span><span class="sxs-lookup"><span data-stu-id="b419a-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="b419a-126">美国西部</span><span class="sxs-lookup"><span data-stu-id="b419a-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="b419a-127">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="b419a-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="b419a-128">欧洲西部</span><span class="sxs-lookup"><span data-stu-id="b419a-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="b419a-129">申请 ID</span><span class="sxs-lookup"><span data-stu-id="b419a-129">Application ID</span></span>

<span data-ttu-id="b419a-130">应用程序 ID 是电子开票附加产品应用程序的 ID。</span><span class="sxs-lookup"><span data-stu-id="b419a-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="b419a-131">在此例中，此值是固定的：**0cdb527f-a8d1-4bf8-9436-b352c68682b2**。</span><span class="sxs-lookup"><span data-stu-id="b419a-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="b419a-132">LCS 环境 ID</span><span class="sxs-lookup"><span data-stu-id="b419a-132">LCS environment ID</span></span>

<span data-ttu-id="b419a-133">LCS 环境 ID 是您组织的 LCS 订阅的 ID。</span><span class="sxs-lookup"><span data-stu-id="b419a-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="b419a-134">服务环境</span><span class="sxs-lookup"><span data-stu-id="b419a-134">Service environments</span></span>

<span data-ttu-id="b419a-135">服务环境是逻辑分区，创建这些逻辑分区用以支持电子开票附加产品中电子开票功能的执行。</span><span class="sxs-lookup"><span data-stu-id="b419a-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="b419a-136">必须在服务环境级别配置安全机密和数字证书以及治理（即访问权限）。</span><span class="sxs-lookup"><span data-stu-id="b419a-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="b419a-137">客户可以根据需要创建任意数量的服务环境。</span><span class="sxs-lookup"><span data-stu-id="b419a-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="b419a-138">客户创建的所有服务环境都是相互独立的。</span><span class="sxs-lookup"><span data-stu-id="b419a-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="b419a-139">必须在 RCS 中创建和维护服务环境。</span><span class="sxs-lookup"><span data-stu-id="b419a-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="b419a-140">当服务环境准备好后，它们必须被发布到电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="b419a-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="b419a-141">服务环境的状态</span><span class="sxs-lookup"><span data-stu-id="b419a-141">Service environment status</span></span>

<span data-ttu-id="b419a-142">服务环境可以通过状态进行管理。</span><span class="sxs-lookup"><span data-stu-id="b419a-142">Service environments can be managed through status.</span></span> <span data-ttu-id="b419a-143">可能的选项有：</span><span class="sxs-lookup"><span data-stu-id="b419a-143">The possible options are:</span></span>

- <span data-ttu-id="b419a-144">**未发布** – 环境已经创建，但尚未发布。</span><span class="sxs-lookup"><span data-stu-id="b419a-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="b419a-145">**已发布** – 环境已发布到电子开票附加产品。</span><span class="sxs-lookup"><span data-stu-id="b419a-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="b419a-146">**已更改** – 已发布环境的属性已更改，但更改尚未发布。</span><span class="sxs-lookup"><span data-stu-id="b419a-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="b419a-147">客户机密</span><span class="sxs-lookup"><span data-stu-id="b419a-147">Customer secrets</span></span>

<span data-ttu-id="b419a-148">电子开票附加产品服务负责将所有业务数据存储在您的公司拥有的 Azure 资源中。</span><span class="sxs-lookup"><span data-stu-id="b419a-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="b419a-149">为确保服务正常运行，并且仅电子开票附加产品能够访问此附加产品所需的和生成的所有业务数据，您必须创建两个主要的 Azure 资源：</span><span class="sxs-lookup"><span data-stu-id="b419a-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="b419a-150">将存储电子发票的 Azure 存储帐户（Blob 存储）</span><span class="sxs-lookup"><span data-stu-id="b419a-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="b419a-151">将存储证书和存储帐户的统一资源标识符 (URI) 的 Azure 密钥保管库</span><span class="sxs-lookup"><span data-stu-id="b419a-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="b419a-152">必须专门分配专用的密钥保管库和客户存储帐户，以与电子开票附加产品一起使用。</span><span class="sxs-lookup"><span data-stu-id="b419a-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="b419a-153">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="b419a-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="b419a-154">用户</span><span class="sxs-lookup"><span data-stu-id="b419a-154">Users</span></span>

<span data-ttu-id="b419a-155">每个服务环境必须在电子开票附加产品中列出可以从 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 连接的用户。</span><span class="sxs-lookup"><span data-stu-id="b419a-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="b419a-156">发布</span><span class="sxs-lookup"><span data-stu-id="b419a-156">Publication</span></span>

<span data-ttu-id="b419a-157">服务环境必须先发布到电子开票附加产品中，然后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b419a-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="b419a-158">仅已发布的环境可以由 Finance 和 Supply Chain Management 访问。</span><span class="sxs-lookup"><span data-stu-id="b419a-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="b419a-159">此外，必须在服务环境属性的任何更新在电子开票服务中生效前发布服务环境。</span><span class="sxs-lookup"><span data-stu-id="b419a-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="b419a-160">已连接的应用程序</span><span class="sxs-lookup"><span data-stu-id="b419a-160">Connected applications</span></span>

<span data-ttu-id="b419a-161">连接的应用程序是您可能希望通过 RCS 到达的 Finance 和 Supply Chain Management 的实例。</span><span class="sxs-lookup"><span data-stu-id="b419a-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="b419a-162">除了应用程序 URL 及其租户外，连接的应用程序还包含让 RCS 可以连接到环境的凭证。</span><span class="sxs-lookup"><span data-stu-id="b419a-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="b419a-163">通过连接的应用程序，您可以在 Finance 和 Supply Chain Management 中配置电子开票功能的一部分，来让整个电子开票功能正常工作。</span><span class="sxs-lookup"><span data-stu-id="b419a-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="b419a-164">Finance 和 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b419a-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="b419a-165">与电子开票附加产品集成</span><span class="sxs-lookup"><span data-stu-id="b419a-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="b419a-166">必须先将电子开票附加产品配置为允许与服务通信，然后才能够通过电子开票附加产品使用 Finance 和 Supply Chain Management 开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="b419a-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="b419a-167">电子开票附加产品集成功能</span><span class="sxs-lookup"><span data-stu-id="b419a-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="b419a-168">要启用 Finance 和 Supply Chain Management 与电子开票附加产品之间的通信，必须在 **功能管理** 工作区打开 **电子开票附加产品集成** 功能。</span><span class="sxs-lookup"><span data-stu-id="b419a-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="b419a-169">服务终结点</span><span class="sxs-lookup"><span data-stu-id="b419a-169">Service endpoint</span></span>

<span data-ttu-id="b419a-170">服务终结点是电子开票附加产品所在的 URL。</span><span class="sxs-lookup"><span data-stu-id="b419a-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="b419a-171">必须先在 Finance 和 Supply Chain Management 配置服务终结点以允许与服务通信，然后才能够开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="b419a-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="b419a-172">要配置服务终结点，转到 **组织管理 \> 设置 \> 电子单据参数**，然后在 **提交服务** 选项卡上的 **电子开票附加产品 URL** 字段中，按照 **服务终结点** 一节所述的表中的说明输入 URL。</span><span class="sxs-lookup"><span data-stu-id="b419a-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="b419a-173">环境</span><span class="sxs-lookup"><span data-stu-id="b419a-173">Environments</span></span>

<span data-ttu-id="b419a-174">在 Finance 和 Supply Chain Management 中输入的环境名称是指在 RCS 中创建并发布到电子开票附加产品的环境的名称。</span><span class="sxs-lookup"><span data-stu-id="b419a-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="b419a-175">必须在 **电子单据参数** 页的 **提交服务** 选项卡上配置环境，让每个开具电子发票的请求都包含电子开票附加产品可以确定哪个电子开票功能必须处理请求的环境。</span><span class="sxs-lookup"><span data-stu-id="b419a-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b419a-176">其他资源</span><span class="sxs-lookup"><span data-stu-id="b419a-176">Additional resources</span></span>

- [<span data-ttu-id="b419a-177">在 RCS 中配置电子发票</span><span class="sxs-lookup"><span data-stu-id="b419a-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="b419a-178">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="b419a-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
