---
title: 开始使用电子开票附加产品服务管理
description: 本主题说明如何开始使用电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: 05b00380cec7511adad2467d3f252799a4aaee5c
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592518"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a><span data-ttu-id="a8fac-103">开始使用电子开票附加产品服务管理</span><span class="sxs-lookup"><span data-stu-id="a8fac-103">Get started with Electronic invoicing add-on service administration</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="a8fac-104">先决条件</span><span class="sxs-lookup"><span data-stu-id="a8fac-104">Prerequisites</span></span>

<span data-ttu-id="a8fac-105">在完成本主题中的过程之前，必须具备以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="a8fac-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="a8fac-106">您必须有权访问您的 Microsoft Dynamics Lifecycle Services (LCS) 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="a8fac-107">您必须有包含版本 10.0.17 或更高版本的 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="a8fac-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a8fac-108">此外，必须将这些应用部署在以下 Azure 地理区域之一：</span><span class="sxs-lookup"><span data-stu-id="a8fac-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="a8fac-109">美国东部</span><span class="sxs-lookup"><span data-stu-id="a8fac-109">East US</span></span>
    - <span data-ttu-id="a8fac-110">美国西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-110">West US</span></span>
    - <span data-ttu-id="a8fac-111">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="a8fac-111">North EU</span></span>
    - <span data-ttu-id="a8fac-112">欧洲西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-112">West EU</span></span>

- <span data-ttu-id="a8fac-113">您必须有权访问您的 Dynamics 365 Regulatory Configuration Services (RCS) 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="a8fac-114">您必须在“功能管理”中为 RCS 帐户激活全球化功能。</span><span class="sxs-lookup"><span data-stu-id="a8fac-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="a8fac-115">有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="a8fac-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="a8fac-116">您必须在 Azure 中创建密钥保管库和存储帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="a8fac-117">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="a8fac-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a><span data-ttu-id="a8fac-118">在 Lifecycle Services 中安装微服务附加产品</span><span class="sxs-lookup"><span data-stu-id="a8fac-118">Install the add-on for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="a8fac-119">登录您的 LCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-119">Sign in to your LCS account.</span></span>
2. <span data-ttu-id="a8fac-120">选择 **预览功能管理** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a8fac-120">Select the **Preview feature management** tile.</span></span>
3. <span data-ttu-id="a8fac-121">在 **公开预览功能** 部分，选择 **电子开票服务**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-121">In the **Public Preview Features** section, select **e-Invoicing service**.</span></span>
4. <span data-ttu-id="a8fac-122">确保 **预览功能已启用** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-122">Make sure that the **Preview feature enabled** option is set to **Yes**.</span></span>
5. <span data-ttu-id="a8fac-123">在 LCS 仪表板上，选择 LCS 部署项目。</span><span class="sxs-lookup"><span data-stu-id="a8fac-123">On your LCS dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="a8fac-124">LCS 项目必须正在运行。</span><span class="sxs-lookup"><span data-stu-id="a8fac-124">The LCS project must be running.</span></span>
7. <span data-ttu-id="a8fac-125">在 **环境加载项** 选项卡上，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-125">On the **Environment add-ins** tab, select **Install a new add-in**.</span></span>
8. <span data-ttu-id="a8fac-126">选择 **电子发票服务** 并在 **AAD 应用程序 ID** 字段中输入 **091c98b0-a1c9-4b02-b62c-7753395ccabe**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-126">Select **e-invoicing Services** and in the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="a8fac-127">这是一个固定值。</span><span class="sxs-lookup"><span data-stu-id="a8fac-127">This is a fixed value.</span></span>
10. <span data-ttu-id="a8fac-128">在 **AAD 租户 ID** 字段中，输入您的 Azure 订阅帐户的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="a8fac-128">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
11. <span data-ttu-id="a8fac-129">查看条款和条件，然后选中相应的复选框。</span><span class="sxs-lookup"><span data-stu-id="a8fac-129">Review the terms and conditions, and then select the check box.</span></span>
12. <span data-ttu-id="a8fac-130">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-130">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="a8fac-131">为与电子开票附加产品的 RCS 集成设置参数。</span><span class="sxs-lookup"><span data-stu-id="a8fac-131">Set up the parameters for RCS integration with the Electronic invoicing add-on</span></span>

1. <span data-ttu-id="a8fac-132">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-132">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="a8fac-133">在 **电子申报** 工作区的 **相关链接** 部分中，选择 **电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-133">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="a8fac-134">在 **电子开票服务** 选项卡上，在 **服务终结点 URI** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="a8fac-134">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="a8fac-135">数据中心 Azure 地理位置</span><span class="sxs-lookup"><span data-stu-id="a8fac-135">Datacenter Azure geography</span></span> | <span data-ttu-id="a8fac-136">服务终结点 URI</span><span class="sxs-lookup"><span data-stu-id="a8fac-136">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a8fac-137">美国东部</span><span class="sxs-lookup"><span data-stu-id="a8fac-137">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-138">美国西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-138">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-139">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="a8fac-139">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-140">欧洲西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-140">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. <span data-ttu-id="a8fac-141">确认 **应用程序 ID** 字段设置为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-141">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="a8fac-142">此值是一个固定值。</span><span class="sxs-lookup"><span data-stu-id="a8fac-142">This value is a fixed value.</span></span>
5. <span data-ttu-id="a8fac-143">在 **LCS 环境 ID** 字段中，输入您的 LCS 订阅帐户的 ID。</span><span class="sxs-lookup"><span data-stu-id="a8fac-143">In the **LCS Environment Id** field, enter the ID of your LCS subscription account.</span></span>
6. <span data-ttu-id="a8fac-144">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-144">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-secret"></a><span data-ttu-id="a8fac-145">创建密钥保管库密码</span><span class="sxs-lookup"><span data-stu-id="a8fac-145">Create Key Vault secret</span></span>

1. <span data-ttu-id="a8fac-146">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-146">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="a8fac-147">在 **全球化功能** 工作区的 **环境** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a8fac-147">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>
3. <span data-ttu-id="a8fac-148">在 **环境设置** 页上的操作窗格上，选择 **服务环境**，然后选择 **密钥保管库参数**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-148">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="a8fac-149">选择 **新建** 创建密钥保管库密码。</span><span class="sxs-lookup"><span data-stu-id="a8fac-149">Select **New** to create a key vault secret.</span></span>
5. <span data-ttu-id="a8fac-150">在 **名称** 字段中，输入密钥保管库密码的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-150">In the **Name** field, enter the name of the key vault secret.</span></span> <span data-ttu-id="a8fac-151">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="a8fac-151">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="a8fac-152">在 **密钥保管库 URI** 字段，粘贴来自 Azure 密钥保管库的密码。</span><span class="sxs-lookup"><span data-stu-id="a8fac-152">In the **Key Vault URI** field, paste the secret from Azure Key Vault.</span></span>
7. <span data-ttu-id="a8fac-153">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-153">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="a8fac-154">创建存储帐户密码</span><span class="sxs-lookup"><span data-stu-id="a8fac-154">Create Storage account secret</span></span>

1. <span data-ttu-id="a8fac-155">转到 **系统管理** > **设置** > **密钥保管库参数**，然后选择一个密钥保管库密钥。</span><span class="sxs-lookup"><span data-stu-id="a8fac-155">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="a8fac-156">在 **证书** 部分，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-156">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="a8fac-157">在 **名称** 字段中，输入存储帐户机密的名称，然后在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="a8fac-157">In the **Name** field, enter the name of the storage account secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a8fac-158">在 **类型** 字段中，选择 **证书**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-158">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="a8fac-159">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-159">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="a8fac-160">创建数字证书机密</span><span class="sxs-lookup"><span data-stu-id="a8fac-160">Create a digital certificate secret</span></span>

1. <span data-ttu-id="a8fac-161">转到 **系统管理** > **设置** > **密钥保管库参数**，然后选择一个密钥保管库密钥。</span><span class="sxs-lookup"><span data-stu-id="a8fac-161">Go to **System administration** > **Setup** > **Key Vault parameters**, and select a Key vault secret.</span></span>
2. <span data-ttu-id="a8fac-162">在 **证书** 部分，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-162">In the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="a8fac-163">在 **名称** 字段中，输入数字证书机密的名称，然后在 **描述** 字段中，输入“描述”。</span><span class="sxs-lookup"><span data-stu-id="a8fac-163">In the **Name** field, enter the name of the digital certificate secret and in the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a8fac-164">在 **类型** 字段中，选择 **证书**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-164">In the **Type** field, select **Certificate**.</span></span>
5. <span data-ttu-id="a8fac-165">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-165">Select **Save**, and then close the page.</span></span>

## <a name="create-an-electronic-invoicing-add-on-environment"></a><span data-ttu-id="a8fac-166">创建电子开票附加产品环境</span><span class="sxs-lookup"><span data-stu-id="a8fac-166">Create an Electronic invoicing add-on environment</span></span>

1. <span data-ttu-id="a8fac-167">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-167">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="a8fac-168">在 **全球化功能** 工作区的 **环境** 部分，选择 **电子开票附加产品** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a8fac-168">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing add-on** tile.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="a8fac-169">创建服务环境</span><span class="sxs-lookup"><span data-stu-id="a8fac-169">Create a service environment</span></span>

1. <span data-ttu-id="a8fac-170">在 **环境设置** 页上的操作窗格上，选择 **服务环境**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-170">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
2. <span data-ttu-id="a8fac-171">选择 **新建** 创建新服务环境。</span><span class="sxs-lookup"><span data-stu-id="a8fac-171">Select **New** to create a new service environment.</span></span>
3. <span data-ttu-id="a8fac-172">在 **名称** 字段中，输入电子开票环境的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-172">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="a8fac-173">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="a8fac-173">In the **Description** field, enter a description.</span></span>
4. <span data-ttu-id="a8fac-174">在 **存储 SAS 令牌密码** 字段中，选择必须用于验证对存储帐户的访问权限的存储帐户机密的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-174">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
5. <span data-ttu-id="a8fac-175">在 **用户** 部分，选择 **添加** 添加允许通过环境提交电子发票并连接到存储帐户的用户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-175">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
6. <span data-ttu-id="a8fac-176">在 **用户 ID** 字段中，输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="a8fac-176">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="a8fac-177">在 **电子邮件** 字段中，输入用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="a8fac-177">In the **Email** field, enter the user's email address.</span></span>
7. <span data-ttu-id="a8fac-178">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-178">Select **Save**.</span></span>
8. <span data-ttu-id="a8fac-179">如果您的国家/地区特定发票需要证书链应用数字签名，请在操作窗格上，选择 **密钥保管库参数**，然后选择 **证书链**，并按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="a8fac-179">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>

    1. <span data-ttu-id="a8fac-180">选择 **新建** 创建证书链。</span><span class="sxs-lookup"><span data-stu-id="a8fac-180">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="a8fac-181">在 **名称** 字段中，输入证书链的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-181">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="a8fac-182">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="a8fac-182">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="a8fac-183">在 **证书** 部分，选择 **添加** 将证书添加到链中。</span><span class="sxs-lookup"><span data-stu-id="a8fac-183">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="a8fac-184">使用 **向上** 或 **向下** 按钮更改证书在链中的位置。</span><span class="sxs-lookup"><span data-stu-id="a8fac-184">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="a8fac-185">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-185">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="a8fac-186">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-186">Close the page.</span></span>
9. <span data-ttu-id="a8fac-187">在 **服务环境** 页上的操作窗格上，选择 **发布** 将环境发布到云中。</span><span class="sxs-lookup"><span data-stu-id="a8fac-187">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="a8fac-188">**状态** 字段的值将更改为 **已发布**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-188">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="a8fac-189">创建连接的应用程序</span><span class="sxs-lookup"><span data-stu-id="a8fac-189">Create a connected application</span></span>

1. <span data-ttu-id="a8fac-190">在 **环境设置** 页上的操作窗格上，选择 **相连应用程序**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-190">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="a8fac-191">选择 **新建** 创建连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="a8fac-191">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="a8fac-192">在 **名称** 字段中，输入要连接的应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-192">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="a8fac-193">在 **应用程序** 字段中，输入要连接的 Finance 和 Supply Chain Management 环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="a8fac-193">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="a8fac-194">在 **租户** 字段中，输入 Finance 和 Supply Chain Management 环境的租户。</span><span class="sxs-lookup"><span data-stu-id="a8fac-194">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="a8fac-195">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-195">Select **Save**.</span></span>
6. <span data-ttu-id="a8fac-196">在操作窗格上，选择 **检查连接** 测试与环境的连接。</span><span class="sxs-lookup"><span data-stu-id="a8fac-196">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="a8fac-197">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-197">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="a8fac-198">将连接的应用程序链接到环境</span><span class="sxs-lookup"><span data-stu-id="a8fac-198">Link connected applications to environments</span></span>

1. <span data-ttu-id="a8fac-199">在 **环境设置** 页上，选择 **新建** 将连接的应用程序分配给环境。</span><span class="sxs-lookup"><span data-stu-id="a8fac-199">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="a8fac-200">在 **相连应用程序** 字段中，选择一个连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="a8fac-200">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="a8fac-201">在 **服务环境** 字段中，选择一个服务环境。</span><span class="sxs-lookup"><span data-stu-id="a8fac-201">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="a8fac-202">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-202">Select **Save**, and then close the page.</span></span>

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="a8fac-203">在 Finance 和 Supply Chain Management 中设置电子开票附加产品集成</span><span class="sxs-lookup"><span data-stu-id="a8fac-203">Set up the Electronic invoicing add-on integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="a8fac-204">打开电子开票附加产品集成功能</span><span class="sxs-lookup"><span data-stu-id="a8fac-204">Turn on the Electronic invoicing add-on integration feature</span></span>

1. <span data-ttu-id="a8fac-205">登录您的 Finance 或 Supply Chain Management 实例。</span><span class="sxs-lookup"><span data-stu-id="a8fac-205">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="a8fac-206">在 **功能管理** 工作区中，搜索 **电子开票附加产品集成** 功能。</span><span class="sxs-lookup"><span data-stu-id="a8fac-206">In the **Feature management** workspace, search for the **Electronic invoicing add-on integration** feature.</span></span> <span data-ttu-id="a8fac-207">如果此功能未出现在页面上，请选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-207">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="a8fac-208">选择此功能，然后然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-208">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="a8fac-209">设置服务终结点 URL</span><span class="sxs-lookup"><span data-stu-id="a8fac-209">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="a8fac-210">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="a8fac-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="a8fac-211">在 **提交服务** 选项卡上，在 **服务终结点 URL** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="a8fac-211">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="a8fac-212">数据中心 Azure 地理位置</span><span class="sxs-lookup"><span data-stu-id="a8fac-212">Datacenter Azure geography</span></span> | <span data-ttu-id="a8fac-213">服务终结点 URL</span><span class="sxs-lookup"><span data-stu-id="a8fac-213">Service endpoint URL</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="a8fac-214">美国东部</span><span class="sxs-lookup"><span data-stu-id="a8fac-214">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-215">美国西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-215">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-216">欧洲北部</span><span class="sxs-lookup"><span data-stu-id="a8fac-216">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | <span data-ttu-id="a8fac-217">欧洲西部</span><span class="sxs-lookup"><span data-stu-id="a8fac-217">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. <span data-ttu-id="a8fac-218">在 **环境** 字段中，输入电子开票附加产品环境的名称。</span><span class="sxs-lookup"><span data-stu-id="a8fac-218">In the **Environment** field, enter the name of the Electronic invoicing add-on environment.</span></span>
4. <span data-ttu-id="a8fac-219">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a8fac-219">Select **Save**, and then close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
