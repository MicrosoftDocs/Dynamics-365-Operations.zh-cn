---
title: 设置 IoT 智能的 Azure 资源
description: 此主题介绍如何创建和配置 IoT 智能所需 Microsoft Azure 资源。
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f728f3b5736bc7368ffb39bf2be398fb91fb373e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224946"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a><span data-ttu-id="6c666-103">设置 IoT 智能的 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="6c666-103">Set up Azure resources for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c666-104">此主题介绍如何创建和配置 IoT 智能所需 Microsoft Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-104">This topic explains how to create and configure the Microsoft Azure resources that you require for IoT Intelligence.</span></span>

## <a name="create-azure-resources"></a><span data-ttu-id="6c666-105">创建 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="6c666-105">Create Azure resources</span></span>

<span data-ttu-id="6c666-106">执行以下步骤创建 Microsoft Dynamics 365 Supply Chain Management 可访问的 IoT 中心、Redis 缓存和密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="6c666-106">Follow these steps to create an IoT hub, a Redis cache, and a key vault that can be accessed by Microsoft Dynamics 365 Supply Chain Management.</span></span>

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a><span data-ttu-id="6c666-107">验证租户中是否有 Microsoft Dynamics ERP Microservices 第一方应用 ID</span><span class="sxs-lookup"><span data-stu-id="6c666-107">Verify that the Microsoft Dynamics ERP Microservices first-party app ID is in your tenant</span></span>

<span data-ttu-id="6c666-108">若要验证租户中是否有 Microsoft Dynamics ERP Microservices 第一方应用的应用 ID，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-108">To verify that the app ID for the Microsoft Dynamics ERP Microservices first-party app is in your tenant, follow these steps.</span></span>

1. <span data-ttu-id="6c666-109">登录 Azure 门户，地址为 <https://portal.azure.com>。</span><span class="sxs-lookup"><span data-stu-id="6c666-109">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
2. <span data-ttu-id="6c666-110">转到 **Azure Active Directory**。</span><span class="sxs-lookup"><span data-stu-id="6c666-110">Go to **Azure Active Directory**.</span></span>
3. <span data-ttu-id="6c666-111">转到 **企业应用程序**。</span><span class="sxs-lookup"><span data-stu-id="6c666-111">Go to **Enterprise applications**.</span></span>
4. <span data-ttu-id="6c666-112">在 **应用程序类型** 字段中，选择 **Microsoft 应用程序**。</span><span class="sxs-lookup"><span data-stu-id="6c666-112">In the **Application type** field, select **Microsoft applications**.</span></span>
5. <span data-ttu-id="6c666-113">在搜索字段中，输入 **Microsoft Dynamics ERP Microservices**。</span><span class="sxs-lookup"><span data-stu-id="6c666-113">In the search field, enter **Microsoft Dynamics ERP Microservices**.</span></span>
6. <span data-ttu-id="6c666-114">验证列表中是否有 **Microsoft Dynamics ERP Microservices**。</span><span class="sxs-lookup"><span data-stu-id="6c666-114">Verify that **Microsoft Dynamics ERP Microservices** is in the list.</span></span> <span data-ttu-id="6c666-115">其他应用程序的名称类似。</span><span class="sxs-lookup"><span data-stu-id="6c666-115">Other applications have similar names.</span></span> <span data-ttu-id="6c666-116">因此，请务必查找正确的应用程序。</span><span class="sxs-lookup"><span data-stu-id="6c666-116">Therefore, make sure that you find the correct application.</span></span> <span data-ttu-id="6c666-117">应用 ID 为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。</span><span class="sxs-lookup"><span data-stu-id="6c666-117">The app ID is **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="6c666-118">如果列表中无此应用程序，则必须将其添加到您的租户中：</span><span class="sxs-lookup"><span data-stu-id="6c666-118">If the application isn't in the list, you must add it to your tenant:</span></span>

    1. <span data-ttu-id="6c666-119">在 Azure 门户中工具栏上，选择按钮打开 Azure Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="6c666-119">In the Azure portal, on the toolbar, select the button to open Azure Cloud Shell.</span></span>
    2. <span data-ttu-id="6c666-120">运行命令 **Install-Module AzureAD**。</span><span class="sxs-lookup"><span data-stu-id="6c666-120">Run the command **Install-Module AzureAD**.</span></span> <span data-ttu-id="6c666-121">输入 **Y** 安装此模块。</span><span class="sxs-lookup"><span data-stu-id="6c666-121">Enter **Y** to install the module.</span></span>
    3. <span data-ttu-id="6c666-122">运行命令 **Get-InstalledModule -Name "AzureAD"** 验证是否安装了此模块。</span><span class="sxs-lookup"><span data-stu-id="6c666-122">Run the command **Get-InstalledModule -Name "AzureAD"** to verify that the module is installed.</span></span>
    4. <span data-ttu-id="6c666-123">运行 **Connect-AzureAD -Confirm** 运行身份验证。</span><span class="sxs-lookup"><span data-stu-id="6c666-123">Run the command **Connect-AzureAD -Confirm** to run the authentication.</span></span>
    5. <span data-ttu-id="6c666-124">运行命令 **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**。</span><span class="sxs-lookup"><span data-stu-id="6c666-124">Run the command **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

    <span data-ttu-id="6c666-125">现在可重复步骤 1 到 6 验证租户中是否有此应用 ID。</span><span class="sxs-lookup"><span data-stu-id="6c666-125">You can now repeat steps 1 through 6 to verify that the app ID is in your tenant.</span></span>

### <a name="create-a-key-vault-resource"></a><span data-ttu-id="6c666-126">创建密钥保管库资源</span><span class="sxs-lookup"><span data-stu-id="6c666-126">Create a key vault resource</span></span>

<span data-ttu-id="6c666-127">若要创建密钥保管库资源，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-127">To create a key vault resource, follow these steps.</span></span>

1. <span data-ttu-id="6c666-128">在 Azure 门户中，创建或转到资源组。</span><span class="sxs-lookup"><span data-stu-id="6c666-128">In the Azure portal, create or go to a resource group.</span></span>
2. <span data-ttu-id="6c666-129">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6c666-129">Select **Add**.</span></span>
3. <span data-ttu-id="6c666-130">在 **新建** 页的搜索字段中，输入 **密钥保管库**。</span><span class="sxs-lookup"><span data-stu-id="6c666-130">On the **New** page, in the search field, enter **Key vault**.</span></span> <span data-ttu-id="6c666-131">然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-131">Then select **Create**.</span></span>
4. <span data-ttu-id="6c666-132">在 **创建密钥保管库** 页的 **密钥保管库名称** 字段中，输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="6c666-132">On the **Create key vault** page, in the **Key vault name** field, enter a name.</span></span>
5. <span data-ttu-id="6c666-133">查看默认值，然后选择 **查看 + 创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-133">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="6c666-134">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-134">Select **Create**.</span></span>

<span data-ttu-id="6c666-135">将在后台创建密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="6c666-135">The key vault is created in the background.</span></span>

### <a name="create-an-iot-hub-resource"></a><span data-ttu-id="6c666-136">创建 IoT 中心资源</span><span class="sxs-lookup"><span data-stu-id="6c666-136">Create an IoT hub resource</span></span>

<span data-ttu-id="6c666-137">若要创建 IoT 中心资源，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-137">To create an IoT hub resource, follow these steps.</span></span>

1. <span data-ttu-id="6c666-138">创建或转到一个资源组。</span><span class="sxs-lookup"><span data-stu-id="6c666-138">Create or go to a resource group.</span></span>
2. <span data-ttu-id="6c666-139">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6c666-139">Select **Add**.</span></span>
3. <span data-ttu-id="6c666-140">在 **新建** 页的搜索字段中，输入 **IoT 中心**。</span><span class="sxs-lookup"><span data-stu-id="6c666-140">On the **New** page, in the search field, enter **Iot Hub**.</span></span> <span data-ttu-id="6c666-141">然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-141">Then select **Create**.</span></span>
4. <span data-ttu-id="6c666-142">在 **IoT 中心名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="6c666-142">In the **IoT hub name** field, enter a name.</span></span>
5. <span data-ttu-id="6c666-143">查看默认值，然后选择 **查看 + 创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-143">Review the default values, and then select **Review + create**.</span></span>
6. <span data-ttu-id="6c666-144">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-144">Select **Create**.</span></span>

<span data-ttu-id="6c666-145">将在后台创建 IoT 中心。</span><span class="sxs-lookup"><span data-stu-id="6c666-145">The IoT hub is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="6c666-146">建议仅为每个环境创建一个 IoT 中心资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-146">We recommend that you create only one IoT hub resource per environment.</span></span>

### <a name="create-a-redis-cache-resource"></a><span data-ttu-id="6c666-147">创建 Redis 缓存资源</span><span class="sxs-lookup"><span data-stu-id="6c666-147">Create a Redis cache resource</span></span>

<span data-ttu-id="6c666-148">若要创建 Redis 缓存资源，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-148">To create a Redis cache resource, follow these steps.</span></span>

1. <span data-ttu-id="6c666-149">创建或转到一个资源组。</span><span class="sxs-lookup"><span data-stu-id="6c666-149">Create or go to a resource group.</span></span>
2. <span data-ttu-id="6c666-150">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6c666-150">Select **Add**.</span></span>
3. <span data-ttu-id="6c666-151">在 **新建** 页的搜索字段中，输入 **Redis 的 Azure 缓存**。</span><span class="sxs-lookup"><span data-stu-id="6c666-151">On the **New** page, in the search field, enter **Azure Cache for Redis**.</span></span> <span data-ttu-id="6c666-152">然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-152">Then select **Create**.</span></span>
4. <span data-ttu-id="6c666-153">在 **DNS 名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="6c666-153">In the **DNS name** field, enter a name.</span></span>
5. <span data-ttu-id="6c666-154">查看默认值，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-154">Review the default values, and then select **Create**.</span></span>

<span data-ttu-id="6c666-155">将在后台创建 Redis 缓存。</span><span class="sxs-lookup"><span data-stu-id="6c666-155">The Redis cache is created in the background.</span></span>

> [!NOTE]
> <span data-ttu-id="6c666-156">建议仅为每个环境创建一个 Redis 缓存。</span><span class="sxs-lookup"><span data-stu-id="6c666-156">We recommend that you create only one Redis cache per environment.</span></span>

<span data-ttu-id="6c666-157">现在已经创建了所有资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-157">All the resources have now been created.</span></span>

## <a name="configure-the-azure-resources"></a><span data-ttu-id="6c666-158">配置 Azure 资源</span><span class="sxs-lookup"><span data-stu-id="6c666-158">Configure the Azure resources</span></span>

### <a name="configure-the-iot-hub"></a><span data-ttu-id="6c666-159">配置 IoT 中心</span><span class="sxs-lookup"><span data-stu-id="6c666-159">Configure the IoT hub</span></span>

<span data-ttu-id="6c666-160">若要配置 IoT 中心，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-160">To configure the IoT hub, follow these steps.</span></span>

1. <span data-ttu-id="6c666-161">在资源中，选择 IoT 中心资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-161">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="6c666-162">在左侧导航窗格中，选择 **内置终结点**。</span><span class="sxs-lookup"><span data-stu-id="6c666-162">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="6c666-163">在 **用户组** 下，粘贴以下用户组。</span><span class="sxs-lookup"><span data-stu-id="6c666-163">Under **Consumer groups**, paste the following consumer groups.</span></span> <span data-ttu-id="6c666-164">这些用户组对应于现成方案。</span><span class="sxs-lookup"><span data-stu-id="6c666-164">These consumer groups correspond to the out-of-box scenarios.</span></span>

    + <span data-ttu-id="6c666-165">microsoft.dynamics.iotintelligence-1</span><span class="sxs-lookup"><span data-stu-id="6c666-165">microsoft.dynamics.iotintelligence-1</span></span>
    + <span data-ttu-id="6c666-166">microsoft.dynamics.iotintelligence-2</span><span class="sxs-lookup"><span data-stu-id="6c666-166">microsoft.dynamics.iotintelligence-2</span></span>
    + <span data-ttu-id="6c666-167">microsoft.dynamics.iotintelligence-3</span><span class="sxs-lookup"><span data-stu-id="6c666-167">microsoft.dynamics.iotintelligence-3</span></span>

### <a name="configure-the-key-vault"></a><span data-ttu-id="6c666-168">配置密钥保管库</span><span class="sxs-lookup"><span data-stu-id="6c666-168">Configure the key vault</span></span>

<span data-ttu-id="6c666-169">若要配置密钥保管库，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-169">To configure the key vault, follow these steps.</span></span>

1. <span data-ttu-id="6c666-170">在资源中，选择密钥保管库资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-170">In your resources, select the key vault resource.</span></span>
2. <span data-ttu-id="6c666-171">在左侧导航窗格中，选择 **访问策略**。</span><span class="sxs-lookup"><span data-stu-id="6c666-171">In the left navigation pane, select **Access policies**.</span></span>
3. <span data-ttu-id="6c666-172">选择 **添加访问策略**。</span><span class="sxs-lookup"><span data-stu-id="6c666-172">Select **Add an access policy**.</span></span>
4. <span data-ttu-id="6c666-173">在 **添加访问策略** 页面的 **选择权限** 字段中，选择 **获取** 和 **列表**。</span><span class="sxs-lookup"><span data-stu-id="6c666-173">On the **Add access policy** page, in the **Secret permissions** field, select **Get** and **List**.</span></span>
5. <span data-ttu-id="6c666-174">在 **选择主体** 中单击。</span><span class="sxs-lookup"><span data-stu-id="6c666-174">Click in the **Select principal**.</span></span>
6. <span data-ttu-id="6c666-175">在 **主体** 对话框中，搜索并选择 **Microsoft Dynamics ERP Microservices**。</span><span class="sxs-lookup"><span data-stu-id="6c666-175">In the **Principal** dialog box, search for and select **Microsoft Dynamics ERP Microservices**.</span></span> <span data-ttu-id="6c666-176">然后选择 **选择**。</span><span class="sxs-lookup"><span data-stu-id="6c666-176">Then select **Select**.</span></span>
7. <span data-ttu-id="6c666-177">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="6c666-177">Select **Add**.</span></span>
8. <span data-ttu-id="6c666-178">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="6c666-178">Select **Save**.</span></span>

<span data-ttu-id="6c666-179">此应用现在可访问密钥保管库中的密码。</span><span class="sxs-lookup"><span data-stu-id="6c666-179">The app now has access to the secrets in the key vault.</span></span>

### <a name="save-the-iot-hub-connection-string-secret"></a><span data-ttu-id="6c666-180">保存 IoT 中心连接字符串密码</span><span class="sxs-lookup"><span data-stu-id="6c666-180">Save the IoT hub connection string secret</span></span>

<span data-ttu-id="6c666-181">若要保存 IoT 中心连接字符串的密码，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-181">To save the secret for the IoT hub connection string, follow these steps.</span></span>

1. <span data-ttu-id="6c666-182">在资源中，选择 IoT 中心资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-182">In your resources, select the IoT hub resource.</span></span>
2. <span data-ttu-id="6c666-183">在左侧导航窗格中，选择 **内置终结点**。</span><span class="sxs-lookup"><span data-stu-id="6c666-183">In the left navigation pane, select **Built-in endpoints**.</span></span>
3. <span data-ttu-id="6c666-184">复制 **事件中心兼容的终结点** 字段中的值，</span><span class="sxs-lookup"><span data-stu-id="6c666-184">Copy the value in the **Event Hub-compatible endpoint** field.</span></span>
4. <span data-ttu-id="6c666-185">转到密钥保管库资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-185">Go to the key vault resource.</span></span>
5. <span data-ttu-id="6c666-186">在左侧导航窗格中，选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="6c666-186">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="6c666-187">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="6c666-187">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="6c666-188">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="6c666-188">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="6c666-189">在 **值** 字段中，粘贴您之前复制的终结点值。</span><span class="sxs-lookup"><span data-stu-id="6c666-189">In the **Value** field, paste the endpoint value that you copied earlier.</span></span>
9. <span data-ttu-id="6c666-190">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-190">Select **Create**.</span></span>

### <a name="save-the-redis-cache-connection-string-secret"></a><span data-ttu-id="6c666-191">保存 Redis 缓存连接字符串密码</span><span class="sxs-lookup"><span data-stu-id="6c666-191">Save the Redis cache connection string secret</span></span>

<span data-ttu-id="6c666-192">若要保存 Redis 缓存连接字符串的密码，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="6c666-192">To save the secret for the Redis cache connection string, follow these steps.</span></span>

1. <span data-ttu-id="6c666-193">在资源中，选择 Redis 缓存资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-193">In your resources, select the Redis cache resource.</span></span>
2. <span data-ttu-id="6c666-194">选择 **访问密钥**。</span><span class="sxs-lookup"><span data-stu-id="6c666-194">Select **Access keys**.</span></span>
3. <span data-ttu-id="6c666-195">复制 **主连接字符串** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="6c666-195">Copy the value in the **Primary connection string** field.</span></span>
4. <span data-ttu-id="6c666-196">转到密钥保管库资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-196">Go to the key vault resource.</span></span>
5. <span data-ttu-id="6c666-197">在左侧导航窗格中，选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="6c666-197">In the left navigation pane, select **Secrets**.</span></span>
6. <span data-ttu-id="6c666-198">选择 **生成/导入**。</span><span class="sxs-lookup"><span data-stu-id="6c666-198">Select **Generate/Import**.</span></span>
7. <span data-ttu-id="6c666-199">在 **名称** 字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="6c666-199">In the **Name** field, enter a name.</span></span>
8. <span data-ttu-id="6c666-200">在 **值** 字段中，粘贴您之前复制的连接字符串。</span><span class="sxs-lookup"><span data-stu-id="6c666-200">In the **Value** field, paste the connection string that you copied earlier.</span></span>
9. <span data-ttu-id="6c666-201">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="6c666-201">Select **Create**.</span></span>

> [!NOTE]
> <span data-ttu-id="6c666-202">只要更新其中一个连接字符串，必须也更新密码值。</span><span class="sxs-lookup"><span data-stu-id="6c666-202">Whenever you update one of the connection strings, you must also update the secret values.</span></span>

<span data-ttu-id="6c666-203">现在已预配完了所需 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="6c666-203">You've now finished provisioning the required Azure resources.</span></span> <span data-ttu-id="6c666-204">下一步是[在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项](iot-lcs-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="6c666-204">The next step is to [install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]