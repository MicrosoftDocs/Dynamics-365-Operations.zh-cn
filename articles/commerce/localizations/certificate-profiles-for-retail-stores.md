---
title: 用于零售商店的用户定义的证书配置文件
description: 本主题概述了如何在零售商店中使用证书。
author: josaw
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 66a2cc5c87f5567f0e65842638017e5127d68a13
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798853"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="f9794-103">用于零售商店的用户定义的证书配置文件</span><span class="sxs-lookup"><span data-stu-id="f9794-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]


## <a name="overview"></a><span data-ttu-id="f9794-104">概览</span><span class="sxs-lookup"><span data-stu-id="f9794-104">Overview</span></span>

<span data-ttu-id="f9794-105">本主题概述了在 Microsoft Dynamics 365 Commerce 中可用的证书配置文件。</span><span class="sxs-lookup"><span data-stu-id="f9794-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="f9794-106">此功能通过添加对本地证书的支持扩展了[管理零售渠道机密](../dev-itpro/manage-secrets.md)功能。</span><span class="sxs-lookup"><span data-stu-id="f9794-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="f9794-107">销售点 (POS) 在脱机模式下运行，它无法访问存储在密钥保管库中的证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="f9794-108">应该改为使用本地证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-108">The local certificate should be used instead.</span></span> <span data-ttu-id="f9794-109">支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="f9794-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="f9794-110">在密钥保管库后备方案中使用本地证书</span><span class="sxs-lookup"><span data-stu-id="f9794-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="f9794-111">使用本地证书，但不在密钥保管库中（例如，在本地安装中）</span><span class="sxs-lookup"><span data-stu-id="f9794-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="f9794-112">逐步更新证书，其中一些商店和终端使用证书的新版本，而其他商店和终端继续使用以前的版本</span><span class="sxs-lookup"><span data-stu-id="f9794-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="f9794-113">证书配置文件功能使您可以指定默认证书，并设置搜索同一证书配置文件中的证书的顺序。</span><span class="sxs-lookup"><span data-stu-id="f9794-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="f9794-114">此功能还为本地证书和密钥保管库证书提供了类似的设置方法。</span><span class="sxs-lookup"><span data-stu-id="f9794-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="f9794-115">您可以为证书添加公司特定的设置，但是可以在 Commerce 渠道中使用每个证书的唯一跨公司标识符。</span><span class="sxs-lookup"><span data-stu-id="f9794-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="f9794-116">方案</span><span class="sxs-lookup"><span data-stu-id="f9794-116">Scenarios</span></span>

<span data-ttu-id="f9794-117">在 Commerce 渠道中，证书配置文件功能支持以下方案：</span><span class="sxs-lookup"><span data-stu-id="f9794-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="f9794-118">在密钥保管库后备方案中使用本地证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="f9794-119">以下是这些后备方案的一些示例：</span><span class="sxs-lookup"><span data-stu-id="f9794-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="f9794-120">无法访问密钥保管库存储。</span><span class="sxs-lookup"><span data-stu-id="f9794-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="f9794-121">在密钥保管库存储中找不到证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="f9794-122">POS 在脱机模式下运行。</span><span class="sxs-lookup"><span data-stu-id="f9794-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="f9794-123">使用本地证书，但不将它们存储在本地保管库中（例如，在本地安装中）。</span><span class="sxs-lookup"><span data-stu-id="f9794-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="f9794-124">逐步更新证书，其中证书的新版本仅在已经有新版本的商店或终端中使用。</span><span class="sxs-lookup"><span data-stu-id="f9794-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="f9794-125">在多家公司中使用相同的证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="f9794-126">设置证书配置文件</span><span class="sxs-lookup"><span data-stu-id="f9794-126">Set up certificate profiles</span></span>

<span data-ttu-id="f9794-127">以下过程说明了如何设置证书配置文件。</span><span class="sxs-lookup"><span data-stu-id="f9794-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="f9794-128">在 Commerce 渠道中使用证书配置文件之前，请按照以下步骤配置设置。</span><span class="sxs-lookup"><span data-stu-id="f9794-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="f9794-129">在 **功能管理** 工作区中，打开 **零售商店的用户定义的证书配置文件** 功能。</span><span class="sxs-lookup"><span data-stu-id="f9794-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="f9794-130">转到 **系统管理 \> 设置 \> 证书配置文件**。</span><span class="sxs-lookup"><span data-stu-id="f9794-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="f9794-131">创建一条记录，设置它的 **证书配置文件**、**名称** 和 **描述** 字段。</span><span class="sxs-lookup"><span data-stu-id="f9794-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9794-132">证书配置文件是跨所有公司和 Commerce 组件的证书的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f9794-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="f9794-133">在 **法人** 选项卡上，添加一行，然后选择应该使用当前证书配置文件的法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="f9794-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="f9794-134">如果证书配置文件应该用于多个法人，请重复此步骤，为每个其他法人添加一行。</span><span class="sxs-lookup"><span data-stu-id="f9794-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="f9794-135">选择 **设置** 以打开 **证书配置文件设置** 页面，您可以在其中为证书配置文件输入公司特定的设置。</span><span class="sxs-lookup"><span data-stu-id="f9794-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="f9794-136">证书配置文件设置</span><span class="sxs-lookup"><span data-stu-id="f9794-136">Certificate profile settings</span></span>

<span data-ttu-id="f9794-137">当您为证书配置文件行选择 **设置** 时，**证书配置文件设置** 页面将显示。</span><span class="sxs-lookup"><span data-stu-id="f9794-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="f9794-138">通过此页面，您可以指定在 Commerce 渠道中调用当前证书配置文件时可以使用哪些证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="f9794-139">您还可以指定搜索证书的顺序。</span><span class="sxs-lookup"><span data-stu-id="f9794-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="f9794-140">**优先级** 字段将自动设置。</span><span class="sxs-lookup"><span data-stu-id="f9794-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="f9794-141">值 **1** 表示最高优先级。</span><span class="sxs-lookup"><span data-stu-id="f9794-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="f9794-142">当在 **证书配置文件设置** 页面上添加新行时，将其优先级设置为比上一行高一个优先级的数字。</span><span class="sxs-lookup"><span data-stu-id="f9794-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="f9794-143">若要更改特定行的优先级，请选择该行，然后选择 **上移** 来提高优先级，或选择 **下移** 来降低优先级。</span><span class="sxs-lookup"><span data-stu-id="f9794-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="f9794-144">当您将新行添加到 **证书配置文件设置** 页面时，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f9794-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="f9794-145">**位置类型** – 选择证书的存储位置。</span><span class="sxs-lookup"><span data-stu-id="f9794-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="f9794-146">该字段有两个可能的值：**本地证书** 和 **密钥保管库**。</span><span class="sxs-lookup"><span data-stu-id="f9794-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="f9794-147">**密钥保管库证书** – 如果您将 **位置类型** 设置为 **密钥保管库**，此字段为必填字段。</span><span class="sxs-lookup"><span data-stu-id="f9794-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="f9794-148">使用它来指定密钥保管库证书机密。</span><span class="sxs-lookup"><span data-stu-id="f9794-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9794-149">在证书配置文件中使用密钥保管库证书之前，请确保将证书上传到密钥保管库存储，并按照[设置 Azure 密钥保管库客户端](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client)中的说明操作。</span><span class="sxs-lookup"><span data-stu-id="f9794-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span></span>

- <span data-ttu-id="f9794-150">**存储名称** – 该字段是可选字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。</span><span class="sxs-lookup"><span data-stu-id="f9794-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="f9794-151">使用它来指定应该用于搜索本地证书的默认存储名称。</span><span class="sxs-lookup"><span data-stu-id="f9794-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="f9794-152">**存储位置** – 该字段是可选字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。</span><span class="sxs-lookup"><span data-stu-id="f9794-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="f9794-153">使用它来指定应该用于搜索本地证书的默认存储位置。</span><span class="sxs-lookup"><span data-stu-id="f9794-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f9794-154">添加默认存储名称和存储位置，以简化在 Commerce Runtime 中搜索本地证书的过程。</span><span class="sxs-lookup"><span data-stu-id="f9794-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="f9794-155">X509StoreProvider 具有存储证书的文件夹列表。</span><span class="sxs-lookup"><span data-stu-id="f9794-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="f9794-156">如果未指定默认存储名称和默认存储位置，则 X509StoreProvider 会尝试在其列表上的其他文件夹中查找证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="f9794-157">**指纹** – 该字段是必填字段，仅在您将 **位置类型** 字段设置为 **本地证书** 时才可用。</span><span class="sxs-lookup"><span data-stu-id="f9794-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="f9794-158">使用它来指定证书指纹。</span><span class="sxs-lookup"><span data-stu-id="f9794-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="f9794-159">**注释** – 该字段是可选字段，允许用户输入说明。</span><span class="sxs-lookup"><span data-stu-id="f9794-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="f9794-160">工作流：在 Commerce Runtime 中搜索证书</span><span class="sxs-lookup"><span data-stu-id="f9794-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="f9794-161">这是用于在 Commerce Runtime 中调用证书配置文件时搜索证书的基本工作流。</span><span class="sxs-lookup"><span data-stu-id="f9794-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="f9794-162">系统识别证书配置文件是否具有当前法人的公司特定设置。</span><span class="sxs-lookup"><span data-stu-id="f9794-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="f9794-163">系统尝试通过对 **优先级** 字段设置为 **1** 的行使用 **证书配置文件设置** 页面上的值来查找证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="f9794-164">如果 **位置类型** 字段设置为 **密钥保管库**，**密钥保险库证书机密** 字段的值将用于搜索 **密钥保管库参数** 页面上的证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="f9794-165">然后，在密钥保管库存储中搜索证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="f9794-166">如果 **位置类型** 字段设置为 **本地证书**，如果指定了这些参数，则 X509StoreProvider 首先使用默认存储名称和存储位置搜索证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="f9794-167">然后，它搜索其文件夹列表上的所有其他文件夹。</span><span class="sxs-lookup"><span data-stu-id="f9794-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="f9794-168">如果找不到证书，则针对 **优先级** 字段设置为 **2** 的行重复该过程，以此类推。</span><span class="sxs-lookup"><span data-stu-id="f9794-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="f9794-169">如果证书配置文件没有当前法人的设置，或者证书搜索对 **证书配置文件设置** 页面上的所有行都不起作用，则找不到证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="f9794-170">缓存证书搜索的结果</span><span class="sxs-lookup"><span data-stu-id="f9794-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="f9794-171">缓存证书搜索的结果。</span><span class="sxs-lookup"><span data-stu-id="f9794-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="f9794-172">缓存的默认到期时间为一小时。</span><span class="sxs-lookup"><span data-stu-id="f9794-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="f9794-173">但是，该时间可以自定义，并且最大值可以设置为 24 小时。</span><span class="sxs-lookup"><span data-stu-id="f9794-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="f9794-174">逐步更新</span><span class="sxs-lookup"><span data-stu-id="f9794-174">Gradual update</span></span>

<span data-ttu-id="f9794-175">如果引入了新版本的证书，但不能同时在所有商店中更新它，则证书配置文件功能可以逐渐更新证书。</span><span class="sxs-lookup"><span data-stu-id="f9794-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="f9794-176">查找证书配置文件和应更新的行，然后选择 **设置**。</span><span class="sxs-lookup"><span data-stu-id="f9794-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="f9794-177">添加一行，然后指定与证书的最新版本相关的设置。</span><span class="sxs-lookup"><span data-stu-id="f9794-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="f9794-178">增加新行的 **优先级** 值。</span><span class="sxs-lookup"><span data-stu-id="f9794-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="f9794-179">使用 **上移** 按钮以移动该行，使其位于同一证书的上一版本的行上方。</span><span class="sxs-lookup"><span data-stu-id="f9794-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="f9794-180">在 Commerce Runtime 中，将首先调用证书的新版本。</span><span class="sxs-lookup"><span data-stu-id="f9794-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="f9794-181">如果尚未在特定商店或特定终端中更新证书，则将调用以前的版本。</span><span class="sxs-lookup"><span data-stu-id="f9794-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]