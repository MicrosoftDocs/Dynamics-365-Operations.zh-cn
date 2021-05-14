---
title: 电子开票管理组件
description: 本主题提供有关与电子开票的管理相关的组件的信息。
author: gionoder
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 3ac4a03d75898680b5655421f3024dc6f666464c
ms.sourcegitcommit: 54d3ec0c006bfa9d2b849590205be08551c4e0f0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/30/2021
ms.locfileid: "5963183"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="31f26-103">电子开票管理组件</span><span class="sxs-lookup"><span data-stu-id="31f26-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="31f26-104">本主题提供有关与电子开票的管理相关的组件的信息。</span><span class="sxs-lookup"><span data-stu-id="31f26-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="31f26-105">另外还提供有关如何配置电子开票服务的信息。</span><span class="sxs-lookup"><span data-stu-id="31f26-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="31f26-106">Azure</span><span class="sxs-lookup"><span data-stu-id="31f26-106">Azure</span></span>

<span data-ttu-id="31f26-107">使用 Microsoft Azure 为密钥保管库和存储帐户创建机密。</span><span class="sxs-lookup"><span data-stu-id="31f26-107">Use Microsoft Azure to create the secrets for the Key Vault and storage account.</span></span> <span data-ttu-id="31f26-108">然后，在电子开票的配置中使用这些机密。</span><span class="sxs-lookup"><span data-stu-id="31f26-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="31f26-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="31f26-109">Lifecycle Services</span></span>

<span data-ttu-id="31f26-110">使用 Microsoft Dynamics Lifecycle Services (LCS) 为您的 LCS 部署项目启用微服务。</span><span class="sxs-lookup"><span data-stu-id="31f26-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="31f26-111">在 LCS 中安装微服务至少需要第 2 层虚拟机。</span><span class="sxs-lookup"><span data-stu-id="31f26-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="31f26-112">有关环境计划的详细信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。</span><span class="sxs-lookup"><span data-stu-id="31f26-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="31f26-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="31f26-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="31f26-114">Dynamics 365 Regulatory Configuration Services (RCS) 是用于配置电子开票的界面。</span><span class="sxs-lookup"><span data-stu-id="31f26-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="31f26-115">将在 RCS 中创建、维护和托管环境和电子开票功能等资源。</span><span class="sxs-lookup"><span data-stu-id="31f26-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="31f26-116">在资源准备就绪后，它们将发布到电子开票服务。</span><span class="sxs-lookup"><span data-stu-id="31f26-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="31f26-117">有关 RCS 注册的信息，请参见 [Regulatory services](https://marketing.configure.global.dynamics.com/)。</span><span class="sxs-lookup"><span data-stu-id="31f26-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="31f26-118">有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)</span><span class="sxs-lookup"><span data-stu-id="31f26-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="31f26-119">与电子开票的集成</span><span class="sxs-lookup"><span data-stu-id="31f26-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="31f26-120">必须先配置 RCS 以允许与电子开票通信，然后才能使用 RCS 配置电子发票。</span><span class="sxs-lookup"><span data-stu-id="31f26-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="31f26-121">您在 **电子报告参数** 页面的 **电子开票** 选项卡上完成此配置。</span><span class="sxs-lookup"><span data-stu-id="31f26-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="31f26-122">服务终结点</span><span class="sxs-lookup"><span data-stu-id="31f26-122">Service endpoint</span></span>

<span data-ttu-id="31f26-123">电子开票在一些 Azure 数据中心地理区域中可用。</span><span class="sxs-lookup"><span data-stu-id="31f26-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="31f26-124">下表列出了每个区域的可用性。</span><span class="sxs-lookup"><span data-stu-id="31f26-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="31f26-125">Azure 数据中心地理位置</span><span class="sxs-lookup"><span data-stu-id="31f26-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="31f26-126">美国东部</span><span class="sxs-lookup"><span data-stu-id="31f26-126">East US</span></span>                    |
| <span data-ttu-id="31f26-127">美国西部</span><span class="sxs-lookup"><span data-stu-id="31f26-127">West US</span></span>                    |
| <span data-ttu-id="31f26-128">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="31f26-128">North EU</span></span>                   |
| <span data-ttu-id="31f26-129">欧洲西部</span><span class="sxs-lookup"><span data-stu-id="31f26-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="31f26-130">服务环境</span><span class="sxs-lookup"><span data-stu-id="31f26-130">Service environments</span></span>

<span data-ttu-id="31f26-131">服务环境是逻辑分区，创建这些逻辑分区以支持电子开票中电子开票功能的执行。</span><span class="sxs-lookup"><span data-stu-id="31f26-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="31f26-132">必须在服务环境级别配置安全机密和数字证书以及治理（即访问权限）。</span><span class="sxs-lookup"><span data-stu-id="31f26-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="31f26-133">客户可以根据需要创建任意数量的服务环境。</span><span class="sxs-lookup"><span data-stu-id="31f26-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="31f26-134">客户创建的所有服务环境都是相互独立的。</span><span class="sxs-lookup"><span data-stu-id="31f26-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="31f26-135">必须在 RCS 中创建和维护服务环境。</span><span class="sxs-lookup"><span data-stu-id="31f26-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="31f26-136">在服务环境准备就绪后，它们必须发布到电子开票。</span><span class="sxs-lookup"><span data-stu-id="31f26-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="31f26-137">服务环境的状态</span><span class="sxs-lookup"><span data-stu-id="31f26-137">Service environment status</span></span>

<span data-ttu-id="31f26-138">服务环境可以通过状态进行管理。</span><span class="sxs-lookup"><span data-stu-id="31f26-138">Service environments can be managed through status.</span></span> <span data-ttu-id="31f26-139">可能的选项有：</span><span class="sxs-lookup"><span data-stu-id="31f26-139">The possible options are:</span></span>

- <span data-ttu-id="31f26-140">**未发布** – 环境已经创建，但尚未发布。</span><span class="sxs-lookup"><span data-stu-id="31f26-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="31f26-141">**已发布** – 环境已发布到电子开票。</span><span class="sxs-lookup"><span data-stu-id="31f26-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="31f26-142">**已更改** – 已发布环境的属性已更改，但更改尚未发布。</span><span class="sxs-lookup"><span data-stu-id="31f26-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="31f26-143">客户机密</span><span class="sxs-lookup"><span data-stu-id="31f26-143">Customer secrets</span></span>

<span data-ttu-id="31f26-144">电子开票服务负责将所有业务数据存储在您的公司拥有的 Azure 资源中。</span><span class="sxs-lookup"><span data-stu-id="31f26-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="31f26-145">若要确保服务正常运行，并且相应地访问电子开票所需和生成的所有业务数据，您必须创建两个主要 Azure 资源：</span><span class="sxs-lookup"><span data-stu-id="31f26-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="31f26-146">将存储电子发票的 Azure 存储帐户（Blob 存储）</span><span class="sxs-lookup"><span data-stu-id="31f26-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="31f26-147">将存储证书和存储帐户的统一资源标识符 (URI) 的 Azure 密钥保管库</span><span class="sxs-lookup"><span data-stu-id="31f26-147">An Azure Key Vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>


<span data-ttu-id="31f26-148">必须专门分配专用的密钥保管库和客户存储帐户，以与电子开票一起使用。</span><span class="sxs-lookup"><span data-stu-id="31f26-148">A dedicated Key Vault and customer storage account must be allocated specifically for use with Electronic Invoicing.</span></span> <span data-ttu-id="31f26-149">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="31f26-149">For more information, see [Create an Azure storage account and a Key Vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

<span data-ttu-id="31f26-150">若要监视密钥保管库的运行状况并接收警报，请为密钥保管库配置 Azure Monitor。</span><span class="sxs-lookup"><span data-stu-id="31f26-150">To monitor the health of your Key Vault and receive alerts, configure the Azure Monitor for key Vault.</span></span> <span data-ttu-id="31f26-151">通过启用密钥保管库日志记录，您可以监视哪些人如何以及何时访问了密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="31f26-151">By enabling Key Vault logging, you can monitor how, when, and by whom your Key Vaults are accessed.</span></span> <span data-ttu-id="31f26-152">有关详细信息，请参阅 [Azure 密钥保管库的监视和警报](/azure/key-vault/general/alert)和[如何启用密钥保管库日志记录](/azure/key-vault/general/howto-logging?tabs=azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="31f26-152">For more information, see [Monitoring and alerting for Azure Key Vault](/azure/key-vault/general/alert) and [How to enable Key Vault logging](/azure/key-vault/general/howto-logging?tabs=azure-cli).</span></span>

<span data-ttu-id="31f26-153">最佳做法是定期轮换使用机密。</span><span class="sxs-lookup"><span data-stu-id="31f26-153">As a best practice, periodically rotate the secrets.</span></span> <span data-ttu-id="31f26-154">有关详细信息，请参阅[机密文档](/azure/key-vault/secrets/)。</span><span class="sxs-lookup"><span data-stu-id="31f26-154">For more information, see [Secrets documentation](/azure/key-vault/secrets/).</span></span>

#### <a name="users"></a><span data-ttu-id="31f26-155">用户</span><span class="sxs-lookup"><span data-stu-id="31f26-155">Users</span></span>

<span data-ttu-id="31f26-156">每个服务环境必须在电子开票中列出可以从 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 连接的用户。</span><span class="sxs-lookup"><span data-stu-id="31f26-156">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="31f26-157">发布</span><span class="sxs-lookup"><span data-stu-id="31f26-157">Publication</span></span>

<span data-ttu-id="31f26-158">服务环境必须先发布到电子开票中，然后才能使用。</span><span class="sxs-lookup"><span data-stu-id="31f26-158">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="31f26-159">仅已发布的环境可以由 Finance 和 Supply Chain Management 访问。</span><span class="sxs-lookup"><span data-stu-id="31f26-159">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="31f26-160">此外，必须在服务环境属性的任何更新在电子开票服务中生效前发布服务环境。</span><span class="sxs-lookup"><span data-stu-id="31f26-160">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="31f26-161">已连接的应用程序</span><span class="sxs-lookup"><span data-stu-id="31f26-161">Connected applications</span></span>

<span data-ttu-id="31f26-162">连接的应用程序是您可能希望通过 RCS 到达的 Finance 和 Supply Chain Management 的实例。</span><span class="sxs-lookup"><span data-stu-id="31f26-162">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="31f26-163">除了应用程序 URL 及其租户外，连接的应用程序还包含让 RCS 可以连接到环境的凭证。</span><span class="sxs-lookup"><span data-stu-id="31f26-163">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="31f26-164">通过连接的应用程序，您可以在 Finance 和 Supply Chain Management 中配置电子开票功能的一部分，来让整个电子开票功能正常工作。</span><span class="sxs-lookup"><span data-stu-id="31f26-164">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="31f26-165">Finance 和 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="31f26-165">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="31f26-166">与电子开票的集成</span><span class="sxs-lookup"><span data-stu-id="31f26-166">Integration with Electronic invoicing</span></span>

<span data-ttu-id="31f26-167">必须先将电子开票配置为允许与服务通信，然后才能通过电子开票使用 Finance 和 Supply Chain Management 开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="31f26-167">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="31f26-168">电子开票集成功能</span><span class="sxs-lookup"><span data-stu-id="31f26-168">Electronic invoicing integration feature</span></span>

<span data-ttu-id="31f26-169">若要启用 Finance 和 Supply Chain Management 与电子开票之间的通信，必须在 **功能管理** 工作区中打开 **电子开票集成** 功能。</span><span class="sxs-lookup"><span data-stu-id="31f26-169">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="31f26-170">服务终结点</span><span class="sxs-lookup"><span data-stu-id="31f26-170">Service endpoint</span></span>

<span data-ttu-id="31f26-171">服务终结点是电子开票所在的 URL。</span><span class="sxs-lookup"><span data-stu-id="31f26-171">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="31f26-172">必须先在 Finance 和 Supply Chain Management 配置服务终结点以允许与服务通信，然后才能够开具电子发票。</span><span class="sxs-lookup"><span data-stu-id="31f26-172">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="31f26-173">若要配置服务终结点，请转到 **组织管理 \> 设置 \> 电子单据参数**，然后在 **提交服务** 选项卡上的 **电子开票 URL** 字段中，按照 **服务终结点** 部分所述的表中的说明输入 URL。</span><span class="sxs-lookup"><span data-stu-id="31f26-173">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="31f26-174">环境</span><span class="sxs-lookup"><span data-stu-id="31f26-174">Environments</span></span>

<span data-ttu-id="31f26-175">在 Finance 和 Supply Chain Management 中输入的环境名称是指在 RCS 中创建并发布到电子开票的环境的名称。</span><span class="sxs-lookup"><span data-stu-id="31f26-175">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="31f26-176">必须在 **电子单据参数** 页面的 **提交服务** 选项卡上配置环境，以便让每个开具电子发票的请求都包含电子开票可以确定哪个电子开票功能必须处理请求的环境。</span><span class="sxs-lookup"><span data-stu-id="31f26-176">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31f26-177">其他资源</span><span class="sxs-lookup"><span data-stu-id="31f26-177">Additional resources</span></span>

- [<span data-ttu-id="31f26-178">在 RCS 中配置电子发票</span><span class="sxs-lookup"><span data-stu-id="31f26-178">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="31f26-179">在 Finance 和 Supply Chain Management 中开具电子发票</span><span class="sxs-lookup"><span data-stu-id="31f26-179">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
