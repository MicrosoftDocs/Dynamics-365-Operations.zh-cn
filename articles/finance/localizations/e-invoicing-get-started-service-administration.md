---
title: 开始使用电子开票服务管理
description: 本主题说明如何开始使用电子开票。
author: gionoder
ms.date: 05/24/2021
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
ms.openlocfilehash: 7c4d69edd4a8f7c7acc2ac1bc22c1ba6eaba25ae
ms.sourcegitcommit: 90a289962598394ad98209026013689322854b7b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6092398"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a><span data-ttu-id="9f644-103">开始使用电子开票服务管理</span><span class="sxs-lookup"><span data-stu-id="9f644-103">Get started with Electronic invoicing service administration</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9f644-104">先决条件</span><span class="sxs-lookup"><span data-stu-id="9f644-104">Prerequisites</span></span>

<span data-ttu-id="9f644-105">在完成本主题中的过程之前，必须具备以下先决条件：</span><span class="sxs-lookup"><span data-stu-id="9f644-105">Before you complete the procedures in this topic, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="9f644-106">您必须有权访问您的 Microsoft Dynamics Lifecycle Services (LCS) 帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-106">You must have access to your Microsoft Dynamics Lifecycle Services (LCS) account.</span></span>
- <span data-ttu-id="9f644-107">您必须有包含版本 10.0.17 或更高版本的 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="9f644-107">You must have an LCS project that includes version 10.0.17 or later of Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9f644-108">此外，必须将这些应用部署在以下 Azure 地理区域之一：</span><span class="sxs-lookup"><span data-stu-id="9f644-108">Additionally, these apps must be deployed in one of the following Azure geographies:</span></span>

    - <span data-ttu-id="9f644-109">美国</span><span class="sxs-lookup"><span data-stu-id="9f644-109">United States</span></span>
    - <span data-ttu-id="9f644-110">欧洲</span><span class="sxs-lookup"><span data-stu-id="9f644-110">Europe</span></span>
    - <span data-ttu-id="9f644-111">英国</span><span class="sxs-lookup"><span data-stu-id="9f644-111">United Kingdom</span></span>
    - <span data-ttu-id="9f644-112">亚洲</span><span class="sxs-lookup"><span data-stu-id="9f644-112">Asia</span></span>

- <span data-ttu-id="9f644-113">您必须有权访问您的 Dynamics 365 Regulatory Configuration Services (RCS) 帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-113">You must have access to your Dynamics 365 Regulatory Configuration Services (RCS) account.</span></span>
- <span data-ttu-id="9f644-114">您必须在“功能管理”中为 RCS 帐户激活全球化功能。</span><span class="sxs-lookup"><span data-stu-id="9f644-114">You must activate the Globalization feature for your RCS account in Feature management.</span></span> <span data-ttu-id="9f644-115">有关详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。</span><span class="sxs-lookup"><span data-stu-id="9f644-115">For more information, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md).</span></span>
- <span data-ttu-id="9f644-116">您必须在 Azure 中创建密钥保管库和存储帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-116">You must create a key vault and a storage account in Azure.</span></span> <span data-ttu-id="9f644-117">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="9f644-117">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a><span data-ttu-id="9f644-118">在 Lifecycle Services 中安装微服务的加载项</span><span class="sxs-lookup"><span data-stu-id="9f644-118">Install the add-in for microservices in Lifecycle Services</span></span>

1. <span data-ttu-id="9f644-119">登录您的 LCS 帐户，在 LCS 项目仪表板上选择一个 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="9f644-119">Sign in to your LCS account, and on the LCS project dashboard, select an LCS project.</span></span>
2. <span data-ttu-id="9f644-120">在该项目中，在环境仪表板上，选择您的 LCS 部署项目。</span><span class="sxs-lookup"><span data-stu-id="9f644-120">In the project, on the environment dashboard, select your LCS deployment project.</span></span> <span data-ttu-id="9f644-121">您选择的项目必须在运行。</span><span class="sxs-lookup"><span data-stu-id="9f644-121">The project you select must must be running.</span></span>
3. <span data-ttu-id="9f644-122">在 **Power Platform 集成** 选项卡上，在 **环境加载项** 字段组中，选择 **安装新加载项**。</span><span class="sxs-lookup"><span data-stu-id="9f644-122">On the **Power Platform Integration** tab, in the **Environment add-ins** field group, select **Install a new add-in**.</span></span>
4. <span data-ttu-id="9f644-123">选择 **电子开票**。</span><span class="sxs-lookup"><span data-stu-id="9f644-123">Select **Electronic Invoicing**.</span></span>
5. <span data-ttu-id="9f644-124">在 **AAD 应用程序 ID** 字段中，输入 **091c98b0-a1c9-4b02-b62c-7753395ccabe**。</span><span class="sxs-lookup"><span data-stu-id="9f644-124">In the **AAD application ID** field, enter **091c98b0-a1c9-4b02-b62c-7753395ccabe**.</span></span> <span data-ttu-id="9f644-125">这是一个固定值。</span><span class="sxs-lookup"><span data-stu-id="9f644-125">This is a fixed value.</span></span>
6. <span data-ttu-id="9f644-126">在 **AAD 租户 ID** 字段中，输入您的 Azure 订阅帐户的租户 ID。</span><span class="sxs-lookup"><span data-stu-id="9f644-126">In the **AAD tenant ID** field, enter the tenant ID of your Azure subscription account.</span></span>
7. <span data-ttu-id="9f644-127">查看条款和条件，然后选中相应的复选框。</span><span class="sxs-lookup"><span data-stu-id="9f644-127">Review the terms and conditions, and then select the check box.</span></span>
8. <span data-ttu-id="9f644-128">选择 **安装**。</span><span class="sxs-lookup"><span data-stu-id="9f644-128">Select **Install**.</span></span>


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a><span data-ttu-id="9f644-129">为与电子开票的 RCS 集成设置参数</span><span class="sxs-lookup"><span data-stu-id="9f644-129">Set up the parameters for RCS integration with Electronic invoicing</span></span>

1. <span data-ttu-id="9f644-130">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-130">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9f644-131">在 **电子申报** 工作区的 **相关链接** 部分中，选择 **电子申报参数**。</span><span class="sxs-lookup"><span data-stu-id="9f644-131">In the **Electronic reporting** workspace, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="9f644-132">在 **电子开票服务** 选项卡上，在 **服务终结点 URI** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="9f644-132">On the **e-Invoicing service** tab, in the **Service endpoint URI** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9f644-133">数据中心 Azure 地理位置</span><span class="sxs-lookup"><span data-stu-id="9f644-133">Datacenter Azure geography</span></span> | <span data-ttu-id="9f644-134">服务终结点 URI</span><span class="sxs-lookup"><span data-stu-id="9f644-134">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9f644-135">美国</span><span class="sxs-lookup"><span data-stu-id="9f644-135">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-136">欧洲</span><span class="sxs-lookup"><span data-stu-id="9f644-136">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-137">英国</span><span class="sxs-lookup"><span data-stu-id="9f644-137">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-138">亚洲</span><span class="sxs-lookup"><span data-stu-id="9f644-138">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. <span data-ttu-id="9f644-139">确认 **应用程序 ID** 字段设置为 **0cdb527f-a8d1-4bf8-9436-b352c68682b2**。</span><span class="sxs-lookup"><span data-stu-id="9f644-139">Verify that the **Application Id** field is set to **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span> <span data-ttu-id="9f644-140">此值是一个固定值。</span><span class="sxs-lookup"><span data-stu-id="9f644-140">This value is a fixed value.</span></span>
5. <span data-ttu-id="9f644-141">在 **LCS 环境 ID** 字段中，输入您的 LCS 环境的 ID。</span><span class="sxs-lookup"><span data-stu-id="9f644-141">In the **LCS Environment Id** field, enter the ID of your LCS environment.</span></span>
6. <span data-ttu-id="9f644-142">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-142">Select **Save**, and then close the page.</span></span>

## <a name="create-key-vault-references"></a><span data-ttu-id="9f644-143">创建密钥保管库参考</span><span class="sxs-lookup"><span data-stu-id="9f644-143">Create Key Vault references</span></span>

1. <span data-ttu-id="9f644-144">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-144">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9f644-145">在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f644-145">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="9f644-146">在 **环境设置** 页上的操作窗格上，选择 **服务环境**，然后选择 **密钥保管库参数**。</span><span class="sxs-lookup"><span data-stu-id="9f644-146">On the **Environment setups** page, on the action Pane, select **Service environment**, and then select **Key Vault parameters**.</span></span>
4. <span data-ttu-id="9f644-147">选择 **新建** 以创建密钥保管库参考。</span><span class="sxs-lookup"><span data-stu-id="9f644-147">Select **New** to create a key vault reference.</span></span>
5. <span data-ttu-id="9f644-148">在 **名称** 字段中，输入密钥保管库参考的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-148">In the **Name** field, enter the name of the key vault reference.</span></span> <span data-ttu-id="9f644-149">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9f644-149">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="9f644-150">在 **密钥保管库 URI** 字段中，粘贴来自 Azure 密钥保管库的密钥保管库密码。</span><span class="sxs-lookup"><span data-stu-id="9f644-150">In the **Key Vault URI** field, paste the key vault secret from Azure Key Vault.</span></span> <span data-ttu-id="9f644-151">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="9f644-151">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
7. <span data-ttu-id="9f644-152">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f644-152">Select **Save**.</span></span>

## <a name="create-storage-account-secret"></a><span data-ttu-id="9f644-153">创建存储帐户密码</span><span class="sxs-lookup"><span data-stu-id="9f644-153">Create Storage account secret</span></span>

1. <span data-ttu-id="9f644-154">在 **环境设置** 页面上的操作窗格上，选择 **服务环境** > **密钥保管库参数**。</span><span class="sxs-lookup"><span data-stu-id="9f644-154">On the **Environment setups** page, on the Action Pane, select **Service environment** > **Key Vault parameters**.</span></span>
2. <span data-ttu-id="9f644-155">选择 **密钥保管库参考**，然后在 **证书** 部分中，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9f644-155">Select a **Key Vault reference** and in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="9f644-156">在 **名称** 字段中，输入存储帐户密码的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-156">In the **Name** field, enter the name of the storage account secret.</span></span> <span data-ttu-id="9f644-157">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="9f644-157">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="9f644-158">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9f644-158">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="9f644-159">在 **类型** 字段中，选择 **密码**。</span><span class="sxs-lookup"><span data-stu-id="9f644-159">In the **Type** field, select **Secret**.</span></span>
6. <span data-ttu-id="9f644-160">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-160">Select **Save**, and then close the page.</span></span>

## <a name="create-a-digital-certificate-secret"></a><span data-ttu-id="9f644-161">创建数字证书机密</span><span class="sxs-lookup"><span data-stu-id="9f644-161">Create a digital certificate secret</span></span>

1. <span data-ttu-id="9f644-162">在 **环境设置** 页面上的操作窗格上，选择 **服务环境**，然后选择 **密钥保管库参数**。</span><span class="sxs-lookup"><span data-stu-id="9f644-162">On the **Environment setups** page, on the action Pane, select **Service environment** and then select **Key Vault parameters**.</span></span>
2. <span data-ttu-id="9f644-163">选择 **密钥保管库参考**，然后在 **证书** 部分中，选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="9f644-163">Select a **Key Vault reference** and then in the **Certificates** section, select **Add**.</span></span>
3. <span data-ttu-id="9f644-164">在 **名称** 字段中，输入数字证书机密的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-164">In the **Name** field, enter the name of the digital certificate secret.</span></span> <span data-ttu-id="9f644-165">有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。</span><span class="sxs-lookup"><span data-stu-id="9f644-165">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>
4. <span data-ttu-id="9f644-166">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9f644-166">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="9f644-167">在 **类型** 字段中，选择 **证书**。</span><span class="sxs-lookup"><span data-stu-id="9f644-167">In the **Type** field, select **Certificate**.</span></span>
6. <span data-ttu-id="9f644-168">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-168">Select **Save**, and then close the page.</span></span>

## <a name="create-a-service-environment"></a><span data-ttu-id="9f644-169">创建服务环境</span><span class="sxs-lookup"><span data-stu-id="9f644-169">Create a service environment</span></span>

1. <span data-ttu-id="9f644-170">登录您的 RCS 帐户。</span><span class="sxs-lookup"><span data-stu-id="9f644-170">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="9f644-171">在 **全球化功能** 工作区的 **环境** 部分中，选择 **电子开票** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="9f644-171">In the **Globalization feature** workspace, in the **Environment** section, select the **Electronic invoicing** tile.</span></span>
3. <span data-ttu-id="9f644-172">在 **环境设置** 页上的操作窗格上，选择 **服务环境**。</span><span class="sxs-lookup"><span data-stu-id="9f644-172">On the **Environment setups** page, on the Action Pane, select **Service environment**.</span></span>
4. <span data-ttu-id="9f644-173">选择 **新建** 创建新服务环境。</span><span class="sxs-lookup"><span data-stu-id="9f644-173">Select **New** to create a new service environment.</span></span>
5. <span data-ttu-id="9f644-174">在 **名称** 字段中，输入电子开票环境的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-174">In the **Name** field, enter the name of the e-Invoicing environment.</span></span> <span data-ttu-id="9f644-175">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9f644-175">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="9f644-176">在 **存储 SAS 令牌密码** 字段中，选择必须用于验证对存储帐户的访问权限的存储帐户机密的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-176">In the **Storage SAS token secret** field, select the name of the storage account secret that must be used to authenticate access to the storage account.</span></span>
7. <span data-ttu-id="9f644-177">在 **用户** 部分，选择 **添加** 添加允许通过环境提交电子发票并连接到存储帐户的用户。</span><span class="sxs-lookup"><span data-stu-id="9f644-177">In the **Users** section, select **Add** to add a user who is allowed to submit electronic invoices through the environment and also connect to the storage account.</span></span>
8. <span data-ttu-id="9f644-178">在 **用户 ID** 字段中，输入用户的别名。</span><span class="sxs-lookup"><span data-stu-id="9f644-178">In the **User ID** field, enter the alias of the user.</span></span> <span data-ttu-id="9f644-179">在 **电子邮件** 字段中，输入用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="9f644-179">In the **Email** field, enter the user's email address.</span></span>
9. <span data-ttu-id="9f644-180">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f644-180">Select **Save**.</span></span>
10. <span data-ttu-id="9f644-181">如果您的国家/地区特定发票需要证书链应用数字签名，请在操作窗格上，选择 **密钥保管库参数**，然后选择 **证书链**，并按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="9f644-181">If your country/region-specific invoices require a chain of certificates to apply digital signatures, on the Action pane, select **Key Vault parameters**, then select **Chain of certificates**, and follow these steps:</span></span>
    1. <span data-ttu-id="9f644-182">选择 **新建** 创建证书链。</span><span class="sxs-lookup"><span data-stu-id="9f644-182">Select **New** to create a chain of certificates.</span></span>
    2. <span data-ttu-id="9f644-183">在 **名称** 字段中，输入证书链的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-183">In the **Name** field, enter the name of the chain of certificate.</span></span> <span data-ttu-id="9f644-184">在 **描述** 字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="9f644-184">In the **Description** field, enter a description.</span></span>
    3. <span data-ttu-id="9f644-185">在 **证书** 部分，选择 **添加** 将证书添加到链中。</span><span class="sxs-lookup"><span data-stu-id="9f644-185">In the **Certificates** section, select **Add** to add a certificate to the chain.</span></span>
    4. <span data-ttu-id="9f644-186">使用 **向上** 或 **向下** 按钮更改证书在链中的位置。</span><span class="sxs-lookup"><span data-stu-id="9f644-186">Use the **Up** or **Down** button to change the position of the certificate in the chain.</span></span>
    5. <span data-ttu-id="9f644-187">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-187">Select **Save**, and then close the page.</span></span>
    6. <span data-ttu-id="9f644-188">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-188">Close the page.</span></span>
11. <span data-ttu-id="9f644-189">在 **服务环境** 页上的操作窗格上，选择 **发布** 将环境发布到云中。</span><span class="sxs-lookup"><span data-stu-id="9f644-189">On **Service environment** page, on the Action Pane, select **Publish** to publish the environment to the cloud.</span></span> <span data-ttu-id="9f644-190">**状态** 字段的值将更改为 **已发布**。</span><span class="sxs-lookup"><span data-stu-id="9f644-190">The value of the **Status** field is changed to **Published**.</span></span>

## <a name="create-a-connected-application"></a><span data-ttu-id="9f644-191">创建连接的应用程序</span><span class="sxs-lookup"><span data-stu-id="9f644-191">Create a connected application</span></span>

1. <span data-ttu-id="9f644-192">在 **环境设置** 页上的操作窗格上，选择 **相连应用程序**。</span><span class="sxs-lookup"><span data-stu-id="9f644-192">On the **Environment setups** page, on the action Pane, select **Connected applications**.</span></span>
2. <span data-ttu-id="9f644-193">选择 **新建** 创建连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9f644-193">Select **New** to create a connected application.</span></span>
3. <span data-ttu-id="9f644-194">在 **名称** 字段中，输入要连接的应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-194">In the **Name** field, enter the name of the application to connect.</span></span>
4. <span data-ttu-id="9f644-195">在 **应用程序** 字段中，输入要连接的 Finance 和 Supply Chain Management 环境的 URL。</span><span class="sxs-lookup"><span data-stu-id="9f644-195">In the **Application** field, enter the URL of the Finance and Supply Chain Management environment to connect.</span></span>
4. <span data-ttu-id="9f644-196">在 **租户** 字段中，输入 Finance 和 Supply Chain Management 环境的租户。</span><span class="sxs-lookup"><span data-stu-id="9f644-196">In the **Tenant** field, enter the tenant of the Finance and Supply Chain Management environment.</span></span>
5. <span data-ttu-id="9f644-197">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="9f644-197">Select **Save**.</span></span>
6. <span data-ttu-id="9f644-198">在操作窗格上，选择 **检查连接** 测试与环境的连接。</span><span class="sxs-lookup"><span data-stu-id="9f644-198">On the Action Pane, select **Check connection** to test the connection with the environment.</span></span> <span data-ttu-id="9f644-199">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-199">Then close the page.</span></span>

## <a name="link-connected-applications-to-environments"></a><span data-ttu-id="9f644-200">将连接的应用程序链接到环境</span><span class="sxs-lookup"><span data-stu-id="9f644-200">Link connected applications to environments</span></span>

1. <span data-ttu-id="9f644-201">在 **环境设置** 页上，选择 **新建** 将连接的应用程序分配给环境。</span><span class="sxs-lookup"><span data-stu-id="9f644-201">On the **Environment setups** page, select **New** to assign a connected application to an environment.</span></span>
2. <span data-ttu-id="9f644-202">在 **相连应用程序** 字段中，选择一个连接的应用程序。</span><span class="sxs-lookup"><span data-stu-id="9f644-202">In the **Connected application** field, select a connected application.</span></span>
3. <span data-ttu-id="9f644-203">在 **服务环境** 字段中，选择一个服务环境。</span><span class="sxs-lookup"><span data-stu-id="9f644-203">In the **Service environment** field, select a service environment.</span></span>
4. <span data-ttu-id="9f644-204">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-204">Select **Save**, and then close the page.</span></span>

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a><span data-ttu-id="9f644-205">在 Finance 和 Supply Chain Management 中设置电子开票集成</span><span class="sxs-lookup"><span data-stu-id="9f644-205">Set up Electronic invoicing integration in Finance and Supply Chain Management</span></span>

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a><span data-ttu-id="9f644-206">打开电子开票集成功能</span><span class="sxs-lookup"><span data-stu-id="9f644-206">Turn on the Electronic invoicing integration feature</span></span>

1. <span data-ttu-id="9f644-207">登录您的 Finance 或 Supply Chain Management 实例。</span><span class="sxs-lookup"><span data-stu-id="9f644-207">Sign in to your Finance or Supply Chain Management instance.</span></span>
2. <span data-ttu-id="9f644-208">在 **功能管理** 工作区中，搜索 **电子开票集成** 功能。</span><span class="sxs-lookup"><span data-stu-id="9f644-208">In the **Feature management** workspace, search for the **Electronic invoicing integration** feature.</span></span> <span data-ttu-id="9f644-209">如果此功能未出现在页面上，请选择 **检查更新**。</span><span class="sxs-lookup"><span data-stu-id="9f644-209">If this feature doesn't appear on the page, select **Check for updates**.</span></span>
3. <span data-ttu-id="9f644-210">选择此功能，然后然后选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="9f644-210">Select the feature, and then select **Enable now**.</span></span>

### <a name="set-up-the-service-endpoint-url"></a><span data-ttu-id="9f644-211">设置服务终结点 URL</span><span class="sxs-lookup"><span data-stu-id="9f644-211">Set up the service endpoint URL</span></span>

1. <span data-ttu-id="9f644-212">转到 **组织管理 \> 设置 \> 电子单据参数**。</span><span class="sxs-lookup"><span data-stu-id="9f644-212">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="9f644-213">在 **提交服务** 选项卡上，在 **服务终结点 URL** 字段中，为您的 Azure 地理位置输入适当的服务终结点，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="9f644-213">On the **Submission service** tab, in the **Service endpoint URL** field, enter the appropriate service endpoint for your Azure geography, as shown in the following table.</span></span>

    | <span data-ttu-id="9f644-214">数据中心 Azure 地理位置</span><span class="sxs-lookup"><span data-stu-id="9f644-214">Datacenter Azure geography</span></span> | <span data-ttu-id="9f644-215">服务终结点 URI</span><span class="sxs-lookup"><span data-stu-id="9f644-215">Service endpoint URI</span></span>                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9f644-216">美国</span><span class="sxs-lookup"><span data-stu-id="9f644-216">United States</span></span>              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-217">欧洲</span><span class="sxs-lookup"><span data-stu-id="9f644-217">Europe</span></span>                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-218">英国</span><span class="sxs-lookup"><span data-stu-id="9f644-218">United Kingdom</span></span>             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | <span data-ttu-id="9f644-219">亚洲</span><span class="sxs-lookup"><span data-stu-id="9f644-219">Asia</span></span>                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. <span data-ttu-id="9f644-220">在 **环境** 字段中，输入在电子开票中发布的服务环境的名称。</span><span class="sxs-lookup"><span data-stu-id="9f644-220">In the **Environment** field, enter the name of the service environment published in Electronic invoicing.</span></span>
4. <span data-ttu-id="9f644-221">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="9f644-221">Select **Save**, and then close the page.</span></span>

### <a name="enable-flighting-keys"></a><span data-ttu-id="9f644-222">启用发布外部测试版密钥</span><span class="sxs-lookup"><span data-stu-id="9f644-222">Enable Flighting keys</span></span>

<span data-ttu-id="9f644-223">为 Microsoft Dynamics 365 Finance 或 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.17 或更早版本启用发布外部测试版密钥。</span><span class="sxs-lookup"><span data-stu-id="9f644-223">Enable Flight keys for  Microsoft Dynamics 365 Finance or  Microsoft Dynamics 365 Supply Chain Management versions 10.0.17 or earlier.</span></span> 
1. <span data-ttu-id="9f644-224">执行以下 SQL 命令：</span><span class="sxs-lookup"><span data-stu-id="9f644-224">Execute the following SQL command:</span></span>

    <span data-ttu-id="9f644-225">插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“BusinessDocumentSubmissionServiceEnabled”，1）</span><span class="sxs-lookup"><span data-stu-id="9f644-225">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)</span></span>
    
    <span data-ttu-id="9f644-226">插入 SYSFLIGHTING（FLIGHTNAME，已启用）值（“ElectronicInvoicingServiceIntegrationFeature”，1）</span><span class="sxs-lookup"><span data-stu-id="9f644-226">INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)</span></span>

2. <span data-ttu-id="9f644-227">执行所有 AOS 的 IISreset 命令。</span><span class="sxs-lookup"><span data-stu-id="9f644-227">Perform an IISreset command for all AOS's.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
