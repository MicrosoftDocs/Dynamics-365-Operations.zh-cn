---
title: 解决初始设置过程中的问题
description: 本主题提供故障排除信息，可以帮助您解决在 Finance and Operations 应用和 Common Data Service 之间的双写入集成的初始设置期间可能发生的问题。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172660"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="78f05-103">解决初始设置过程中的问题</span><span class="sxs-lookup"><span data-stu-id="78f05-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="78f05-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="78f05-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="78f05-105">具体来说，提供可以帮助您解决在双写入集成的初始设置期间可能发生的问题的信息。</span><span class="sxs-lookup"><span data-stu-id="78f05-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="78f05-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="78f05-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="78f05-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="78f05-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="78f05-108">您无法将 Finance and Operations 应用链接到 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="78f05-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="78f05-109">**设置双写入所需的凭据：** Azure AD 租户管理员</span><span class="sxs-lookup"><span data-stu-id="78f05-109">**Required credentials to set up dual-write:** Azure AD tenant admin</span></span>

<span data-ttu-id="78f05-110">**设置到 Common Data Service 的链接**页面上的错误通常是由不完整的设置或权限问题引起的。</span><span class="sxs-lookup"><span data-stu-id="78f05-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="78f05-111">请在**设置到 Common Data Service 的链接**页面上通过了整个运行状况检查，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="78f05-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="78f05-112">除非整个运行状况检查通过，否则您无法链接双写入。</span><span class="sxs-lookup"><span data-stu-id="78f05-112">You can't link dual-write unless the whole health check passes.</span></span>

![成功的运行状况检查](media/health_check.png)

<span data-ttu-id="78f05-114">您必须具有 Azure AD 租户管理员凭据才能链接 Finance and Operations 和 Common Data Service 环境。</span><span class="sxs-lookup"><span data-stu-id="78f05-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="78f05-115">链接环境后，用户可以使用其帐户凭据登录并更新现有实体映射。</span><span class="sxs-lookup"><span data-stu-id="78f05-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="78f05-116">当您打开“链接到 Common Data Service”页面时出错</span><span class="sxs-lookup"><span data-stu-id="78f05-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="78f05-117">**解决此问题所需的凭据：** Azure AD 租户管理员</span><span class="sxs-lookup"><span data-stu-id="78f05-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="78f05-118">当您在 Finance and Operations 应用中打开**链接到 Common Data Service** 页面时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="78f05-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="78f05-119">*响应状态代码未指示成功：404（未找到）。*</span><span class="sxs-lookup"><span data-stu-id="78f05-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="78f05-120">当同意步骤尚未完成时，将发生此错误。</span><span class="sxs-lookup"><span data-stu-id="78f05-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="78f05-121">若要验证同意步骤是否已完成，请使用 Azure AD 租户管理员帐户登录 portal.Azure.com，然后查看具有 ID **33976c19-1db5-4c02-810e-c243db79efde** 的第三方应用是否出现在 Azure AD **企业应用程序**列表中。</span><span class="sxs-lookup"><span data-stu-id="78f05-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="78f05-122">如果未出现，您必须向应用提供同意表示。</span><span class="sxs-lookup"><span data-stu-id="78f05-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="78f05-123">要向应用提供同意表示，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="78f05-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="78f05-124">使用您的管理员凭据打开以下 URL。</span><span class="sxs-lookup"><span data-stu-id="78f05-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="78f05-125">应会提示您同意。</span><span class="sxs-lookup"><span data-stu-id="78f05-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="78f05-126">选择**接受**指示您同意在您的租户中安装具有 ID **33976c19-1db5-4c02-810e-c243db79efde** 的应用。</span><span class="sxs-lookup"><span data-stu-id="78f05-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="78f05-127">需要此应用才能链接 Common Data Service 和 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="78f05-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="78f05-128">如果您在执行此步骤时遇到问题，请以匿名模式（在 Google Chrome 中）或隐私模式（在 Microsoft Edge 中）打开浏览器。</span><span class="sxs-lookup"><span data-stu-id="78f05-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="78f05-129">验证链接期间是否正确设置了公司数据和双写入团队</span><span class="sxs-lookup"><span data-stu-id="78f05-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="78f05-130">为确保双写入正常工作，将在 Common Data Service 环境中创建您在配置过程中选择的公司。</span><span class="sxs-lookup"><span data-stu-id="78f05-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="78f05-131">默认情况下，这些公司是只读的，**IsDualWriteEnable** 属性设置为 **True**。</span><span class="sxs-lookup"><span data-stu-id="78f05-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="78f05-132">此外，还将创建默认的负责业务单位负责人和团队，并包括公司名称。</span><span class="sxs-lookup"><span data-stu-id="78f05-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="78f05-133">在启用映射之前，请验证是否已指定默认团队负责人。</span><span class="sxs-lookup"><span data-stu-id="78f05-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="78f05-134">要查找**公司(CDM\_公司)** 实体，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="78f05-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="78f05-135">在 Dynamics 365 中的模型驱动应用中，选择右上角的筛选器。</span><span class="sxs-lookup"><span data-stu-id="78f05-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="78f05-136">在下拉列表中，选择**公司**。</span><span class="sxs-lookup"><span data-stu-id="78f05-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="78f05-137">选择**运行**查看结果。</span><span class="sxs-lookup"><span data-stu-id="78f05-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="78f05-138">选择配置双写入时链接的公司。</span><span class="sxs-lookup"><span data-stu-id="78f05-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="78f05-139">验证**默认负责团队**字段是否具有值。</span><span class="sxs-lookup"><span data-stu-id="78f05-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="78f05-140">在下图中，**默认负责团队**字段设置为 **USMF 双写入**。</span><span class="sxs-lookup"><span data-stu-id="78f05-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![验证默认负责团队](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="78f05-142">查找可以为双写入链接的法人或公司的数量限制</span><span class="sxs-lookup"><span data-stu-id="78f05-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="78f05-143">当您尝试启用映射时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="78f05-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="78f05-144">*双写入失败 - 插件注册失败：\[（无法获取项目的分区映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea。错误超出了映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea 允许的最大分区）\]，发生一个或多个错误。*</span><span class="sxs-lookup"><span data-stu-id="78f05-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="78f05-145">链接环境时的当前限制约为 40 个法人。</span><span class="sxs-lookup"><span data-stu-id="78f05-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="78f05-146">如果您尝试启用映射，并且在环境之间链接了超过 40 个法人，将发生此错误。</span><span class="sxs-lookup"><span data-stu-id="78f05-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
