---
title: 解决 Finance and Operations 应用有关双写入模块的问题
description: 本主题提供故障排除信息，可以帮助您解决 Finance and Operations 应用中的双写入模块问题。
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172752"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a><span data-ttu-id="c27b4-103">解决 Finance and Operations 应用有关双写入模块的问题</span><span class="sxs-lookup"><span data-stu-id="c27b4-103">Troubleshoot issues with the Dual-write module in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="c27b4-104">本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="c27b4-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="c27b4-105">具体来说，提供可以帮助您解决 Finance and Operations 应用中的**双写入**模块问题的信息。</span><span class="sxs-lookup"><span data-stu-id="c27b4-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c27b4-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="c27b4-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c27b4-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="c27b4-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="c27b4-108">您无法在 Finance and Operations 应用中加载双写入模块</span><span class="sxs-lookup"><span data-stu-id="c27b4-108">You can't load the Dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="c27b4-109">如果您无法通过选择**数据管理**工作区中的**双写入**磁贴来打开**双写入**页面，则说明数据集成服务可能中断。</span><span class="sxs-lookup"><span data-stu-id="c27b4-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="c27b4-110">请创建支持票证请求重新启动数据集成服务。</span><span class="sxs-lookup"><span data-stu-id="c27b4-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a><span data-ttu-id="c27b4-111">尝试创建新的实体映射时出错</span><span class="sxs-lookup"><span data-stu-id="c27b4-111">Error when you try to create a new entity mapping</span></span>

<span data-ttu-id="c27b4-112">**解决此问题所需的凭据：** Azure AD 租户管理员</span><span class="sxs-lookup"><span data-stu-id="c27b4-112">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="c27b4-113">当您尝试为双写入配置新实体时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="c27b4-113">You might receive the following error message when you try to configure a new entity for dual-write:</span></span>

<span data-ttu-id="c27b4-114">*响应状态代码未指示成功：401（未授权）*</span><span class="sxs-lookup"><span data-stu-id="c27b4-114">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>

<span data-ttu-id="c27b4-115">发生此错误是因为只有 Azure AD 租户管理员可以添加新的实体映射。</span><span class="sxs-lookup"><span data-stu-id="c27b4-115">This error occurs because only an Azure AD tenant admin can add a new entity mapping.</span></span>

<span data-ttu-id="c27b4-116">要解决此问题，请作为 Azure AD 管理员租户登录到 Finance and Operations 应用。</span><span class="sxs-lookup"><span data-stu-id="c27b4-116">To fix the issue, sign in to the Finance and Operations app as an Azure AD admin tenant.</span></span> <span data-ttu-id="c27b4-117">您还必须转到 web.PowerApps.com 重新验证您的连接。</span><span class="sxs-lookup"><span data-stu-id="c27b4-117">You must also go to web.PowerApps.com and revalidate your connection.</span></span>

## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="c27b4-118">打开双写入用户界面时出错</span><span class="sxs-lookup"><span data-stu-id="c27b4-118">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="c27b4-119">当您尝试从**数据管理**工作区访问双写入时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="c27b4-119">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="c27b4-120">*login.microsoftonline.com 拒绝连接。*</span><span class="sxs-lookup"><span data-stu-id="c27b4-120">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="c27b4-121">要解决此问题，请使用 Microsoft Edge 中的隐私模式窗口、Chromium 中的匿名窗口或 Google Chrome 中的匿名窗口登录。</span><span class="sxs-lookup"><span data-stu-id="c27b4-121">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="c27b4-122">您还必须取消阻止或清除第三方 Cookie。</span><span class="sxs-lookup"><span data-stu-id="c27b4-122">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a><span data-ttu-id="c27b4-123">为双写入链接环境或添加新实体映射时出错</span><span class="sxs-lookup"><span data-stu-id="c27b4-123">Error when you link the environment for dual-write or add a new entity mapping</span></span>

<span data-ttu-id="c27b4-124">**解决此问题所需的凭据：** Azure AD 租户管理员</span><span class="sxs-lookup"><span data-stu-id="c27b4-124">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="c27b4-125">链接或创建映射时，您可能会遇到以下错误：</span><span class="sxs-lookup"><span data-stu-id="c27b4-125">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="c27b4-126">*响应状态代码未指示成功：403 (tokenexchange)。<br>会话 ID：\<您的会话 ID\><br>根活动 ID：\<您的根活动 ID\>*</span><span class="sxs-lookup"><span data-stu-id="c27b4-126">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="c27b4-127">如果您没有足够的权限链接双写入或创建映射，则会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="c27b4-127">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="c27b4-128">您必须使用 Azure AD 租户管理员帐户链接环境和添加新实体映射。</span><span class="sxs-lookup"><span data-stu-id="c27b4-128">You must use an Azure AD tenant admin account to link environments and add new entity mappings.</span></span> <span data-ttu-id="c27b4-129">不过，设置后，您可以使用非管理员帐户监视状态和编辑映射。</span><span class="sxs-lookup"><span data-stu-id="c27b4-129">However, after setup, you can use a non-admin account to monitor status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-entity-mapping"></a><span data-ttu-id="c27b4-130">停止实体映射时出错</span><span class="sxs-lookup"><span data-stu-id="c27b4-130">Error when you stop the entity mapping</span></span>

<span data-ttu-id="c27b4-131">当您尝试停止实体映射时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="c27b4-131">You might receive the following error message when you try to stop the entity mappings:</span></span>

<span data-ttu-id="c27b4-132">*\[已禁止\]，\[{来自令牌交换的 "status":403,"source":"","message":"Error：不允许用户访问连接 dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]，远程服务器返回错误：(403) 已禁止。*</span><span class="sxs-lookup"><span data-stu-id="c27b4-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="c27b4-133">当链接的 Common Data Service 环境不可用时，将发生此错误。</span><span class="sxs-lookup"><span data-stu-id="c27b4-133">This error occurs when the linked Common Data Service environment isn't available.</span></span>

<span data-ttu-id="c27b4-134">要解决此问题，请为数据集成团队创建票证。</span><span class="sxs-lookup"><span data-stu-id="c27b4-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="c27b4-135">附加网络跟踪，以便数据集成团队可以在后端将映射标记为**未运行**。</span><span class="sxs-lookup"><span data-stu-id="c27b4-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>
