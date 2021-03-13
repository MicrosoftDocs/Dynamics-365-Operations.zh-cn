---
title: 创建 Azure 存储帐户和密钥保管库
description: 本主题说明如何创建 Azure 存储帐户和密钥保管库。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104221"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="c6186-103">创建 Azure 存储帐户和密钥保管库</span><span class="sxs-lookup"><span data-stu-id="c6186-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="c6186-104">先决条件</span><span class="sxs-lookup"><span data-stu-id="c6186-104">Prerequisites</span></span>

<span data-ttu-id="c6186-105">您必须确保先完成以下任务，然后才能完成本主题中的步骤：</span><span class="sxs-lookup"><span data-stu-id="c6186-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="c6186-106">在 Azure 中创建密钥保管库资源。</span><span class="sxs-lookup"><span data-stu-id="c6186-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="c6186-107">有关详细信息，请参阅[关于 Azure 密钥保管库](https://docs.microsoft.com/azure/key-vault/general/overview)。</span><span class="sxs-lookup"><span data-stu-id="c6186-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="c6186-108">创建 Azure 存储帐户（Blob 存储）。</span><span class="sxs-lookup"><span data-stu-id="c6186-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="c6186-109">有关详细信息，请参阅[维护 Azure 存储帐户](https://docs.microsoft.com/azure/storage/blobs/)。</span><span class="sxs-lookup"><span data-stu-id="c6186-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="c6186-110">概览</span><span class="sxs-lookup"><span data-stu-id="c6186-110">Overview</span></span>

<span data-ttu-id="c6186-111">在本主题中，您将完成两个主要步骤：</span><span class="sxs-lookup"><span data-stu-id="c6186-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="c6186-112">设置 Azure 存储帐户以获取存储帐户 URI。</span><span class="sxs-lookup"><span data-stu-id="c6186-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="c6186-113">设置密钥保管库以存储存储帐户 URI。</span><span class="sxs-lookup"><span data-stu-id="c6186-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="c6186-114">设置 Azure 存储帐户以获取存储帐户 URI</span><span class="sxs-lookup"><span data-stu-id="c6186-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="c6186-115">打开您计划与电子开票附加产品一起使用的存储帐户。</span><span class="sxs-lookup"><span data-stu-id="c6186-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="c6186-116">转到 **Blob 服务** \> **容器**，创建一个新容器。</span><span class="sxs-lookup"><span data-stu-id="c6186-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="c6186-117">为容器输入名称，然后将 **公共访问级别** 字段设置为 **专用(无匿名访问)**。</span><span class="sxs-lookup"><span data-stu-id="c6186-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="c6186-118">打开容器，转到 **设置 \> 访问策略**。</span><span class="sxs-lookup"><span data-stu-id="c6186-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="c6186-119">选择 **添加策略** 添加存储的访问策略。</span><span class="sxs-lookup"><span data-stu-id="c6186-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="c6186-120">根据需要设置 **标识符** 和 **权限** 字段。</span><span class="sxs-lookup"><span data-stu-id="c6186-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="c6186-121">在 **权限** 字段中，您应该选择所有权限。</span><span class="sxs-lookup"><span data-stu-id="c6186-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![授予 Blob 存储权限](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="c6186-123">输入开始日期和到期日期。</span><span class="sxs-lookup"><span data-stu-id="c6186-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="c6186-124">到期日期应该在将来。</span><span class="sxs-lookup"><span data-stu-id="c6186-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="c6186-125">选择 **确定** 保存策略，然后保存对容器进行的更改。</span><span class="sxs-lookup"><span data-stu-id="c6186-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="c6186-126">返回到存储帐户，打开 **存储资源管理器(预览)**。</span><span class="sxs-lookup"><span data-stu-id="c6186-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="c6186-127">用鼠标右键单击容器，然后选择 **获取共享访问签名**。</span><span class="sxs-lookup"><span data-stu-id="c6186-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="c6186-128">在 **共享访问签名** 对话框中，将值复制并存储到 **URI** 字段中。</span><span class="sxs-lookup"><span data-stu-id="c6186-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="c6186-129">此值将在下一个过程中使用，将称为 *共享访问签名 URI*。</span><span class="sxs-lookup"><span data-stu-id="c6186-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![选择并复制 URI 值](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="c6186-131">设置密钥保管库以存储存储帐户 URI</span><span class="sxs-lookup"><span data-stu-id="c6186-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="c6186-132">打开您打算与电子开票附加产品一起使用的密钥保管库。</span><span class="sxs-lookup"><span data-stu-id="c6186-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="c6186-133">转到 **设置** \> **密码**，然后选择 **生成/导入** 创造新密码。</span><span class="sxs-lookup"><span data-stu-id="c6186-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="c6186-134">在 **创建密码** 页上，在 **上载选项** 字段中，选择 **手动**。</span><span class="sxs-lookup"><span data-stu-id="c6186-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="c6186-135">输入密码的名称。</span><span class="sxs-lookup"><span data-stu-id="c6186-135">Enter the name of the secret.</span></span> <span data-ttu-id="c6186-136">此名称将在 Regulatory Configuration Service (RCS) 中的服务设置期间使用，将称为 *密钥保管库密码名称*。</span><span class="sxs-lookup"><span data-stu-id="c6186-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="c6186-137">在 **值** 字段中，选择 **共享访问签名 URI**，然后选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="c6186-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="c6186-138">设置访问策略，以授予电子开票附加产品访问您创建的密码的正确安全访问级别。</span><span class="sxs-lookup"><span data-stu-id="c6186-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="c6186-139">转到 **设置 \> 访问策略**，选择 **添加访问策略**。</span><span class="sxs-lookup"><span data-stu-id="c6186-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="c6186-140">为 **获取** 和 **列出** 操作设置密码权限。</span><span class="sxs-lookup"><span data-stu-id="c6186-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![授予服务访问权限](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="c6186-142">为 **获取** 和 **列出** 操作设置证书权限。</span><span class="sxs-lookup"><span data-stu-id="c6186-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![授予证书权限](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="c6186-144">在 **主体** 对话框中，通过添加 **电子开票附加产品** 选择主体。</span><span class="sxs-lookup"><span data-stu-id="c6186-144">In the **Principal** dialog box, select the principal by adding **Electronic invoicing add-on**.</span></span>
10. <span data-ttu-id="c6186-145">选择 **添加**，然后选择 **保存密钥保管库更改**。</span><span class="sxs-lookup"><span data-stu-id="c6186-145">Select **Add**, and then select **Save Key Vault changes**.</span></span>
11. <span data-ttu-id="c6186-146">在 **概览** 页上，复制密钥保管库的 **DNS 名称** 值。</span><span class="sxs-lookup"><span data-stu-id="c6186-146">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="c6186-147">此值将在 RCS 中的服务设置期间使用，将称为 *密钥保管库 URI*。</span><span class="sxs-lookup"><span data-stu-id="c6186-147">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>
