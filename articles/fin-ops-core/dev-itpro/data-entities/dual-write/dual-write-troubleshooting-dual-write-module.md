---
title: 解决 Finance and Operations 应用中的双写入问题
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 3ffeb2de0acc1761bccf62a1a124852c504e2a3a
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131237"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a><span data-ttu-id="66325-103">解决 Finance and Operations 应用中的双写入问题</span><span class="sxs-lookup"><span data-stu-id="66325-103">Troubleshoot dual-write issues in Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66325-104">本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。</span><span class="sxs-lookup"><span data-stu-id="66325-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="66325-105">具体来说，提供可以帮助您解决 Finance and Operations 应用中的 **双写入** 模块问题的信息。</span><span class="sxs-lookup"><span data-stu-id="66325-105">Specifically, it provides information that can help you fix issues with the **Dual-write** module in Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66325-106">本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。</span><span class="sxs-lookup"><span data-stu-id="66325-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="66325-107">介绍每个问题的每一节说明了是否需要特定角色或凭据。</span><span class="sxs-lookup"><span data-stu-id="66325-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a><span data-ttu-id="66325-108">您无法在 Finance and Operations 应用中加载双写入模块</span><span class="sxs-lookup"><span data-stu-id="66325-108">You can't load the dual-write module in a Finance and Operations app</span></span>

<span data-ttu-id="66325-109">如果您无法通过选择 **数据管理** 工作区中的 **双写入** 磁贴来打开 **双写入** 页面，则说明数据集成服务可能中断。</span><span class="sxs-lookup"><span data-stu-id="66325-109">If you can't open the **Dual-write** page by selecting the **Dual Write** tile in the **Data management** workspace, the data integration service is probably down.</span></span> <span data-ttu-id="66325-110">请创建支持票证请求重新启动数据集成服务。</span><span class="sxs-lookup"><span data-stu-id="66325-110">Create a support ticket to request a restart of the data integration service.</span></span>

## <a name="error-when-you-try-to-create-a-new-table-map"></a><span data-ttu-id="66325-111">尝试创建新表映射时出错</span><span class="sxs-lookup"><span data-stu-id="66325-111">Error when you try to create a new table map</span></span>

<span data-ttu-id="66325-112">**解决此问题所需的凭据：** 设置双写入的同一用户。</span><span class="sxs-lookup"><span data-stu-id="66325-112">**Required credentials to fix the issue:** The same user that setup dual-write.</span></span>

<span data-ttu-id="66325-113">当您尝试为双写入配置新表时，您可能会收到以下错误消息。</span><span class="sxs-lookup"><span data-stu-id="66325-113">You might receive the following error message when you try to configure a new table for dual-write.</span></span> <span data-ttu-id="66325-114">可以创建映射的唯一用户是设置双写入连接的用户。</span><span class="sxs-lookup"><span data-stu-id="66325-114">The only user that can create a map is the user who setup the dual-write connection.</span></span>

<span data-ttu-id="66325-115">*响应状态代码未指示成功：401（未授权）*</span><span class="sxs-lookup"><span data-stu-id="66325-115">*Response status code does not indicate success: 401 (Unauthorized)*</span></span>


## <a name="error-when-you-open-the-dual-write-user-interface"></a><span data-ttu-id="66325-116">打开双写入用户界面时出错</span><span class="sxs-lookup"><span data-stu-id="66325-116">Error when you open the dual-write user interface</span></span>

<span data-ttu-id="66325-117">当您尝试从 **数据管理** 工作区访问双写入时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="66325-117">You might receive the following error message when you try to access dual-write from the **Data management** workspace:</span></span>

<span data-ttu-id="66325-118">*login.microsoftonline.com 拒绝连接。*</span><span class="sxs-lookup"><span data-stu-id="66325-118">*login.microsoftonline.com refused to connect.*</span></span>

<span data-ttu-id="66325-119">要解决此问题，请使用 Microsoft Edge 中的隐私模式窗口、Chromium 中的匿名窗口或 Google Chrome 中的匿名窗口登录。</span><span class="sxs-lookup"><span data-stu-id="66325-119">To fix the issue, sign in by using an InPrivate window in Microsoft Edge, an incognito window in Chromium, or an incognito window in Google Chrome.</span></span> <span data-ttu-id="66325-120">您还必须取消阻止或清除第三方 Cookie。</span><span class="sxs-lookup"><span data-stu-id="66325-120">You must also unblock or clear third-party cookies.</span></span>

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a><span data-ttu-id="66325-121">为双写入链接环境或添加新表映射时出错</span><span class="sxs-lookup"><span data-stu-id="66325-121">Error when you link the environment for dual-write or add a new table mapping</span></span>

<span data-ttu-id="66325-122">**解决此问题所需的角色：** 同时是 Finance and Operations 应用和 Dataverse 的系统管理员。</span><span class="sxs-lookup"><span data-stu-id="66325-122">**Required role to fix the issue:** System administrator in both Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="66325-123">链接或创建映射时，您可能会遇到以下错误：</span><span class="sxs-lookup"><span data-stu-id="66325-123">You might encounter the following error when linking or creating maps:</span></span>

<span data-ttu-id="66325-124">*响应状态代码未指示成功：403 (tokenexchange)。<br>会话 ID：\<your session id\><br> 根活动 ID：\<your root activity id\>*</span><span class="sxs-lookup"><span data-stu-id="66325-124">*Response status code does not indicate success: 403 (tokenexchange).<br> Session ID: \<your session id\><br> Root activity ID: \<your root activity id\>*</span></span>

<span data-ttu-id="66325-125">如果您没有足够的权限链接双写入或创建映射，则会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="66325-125">This error can occur if you don't have sufficient permissions to link dual-write or create maps.</span></span> <span data-ttu-id="66325-126">如果在不取消双写入链接的情况下重置了 Dataverse 环境，也会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="66325-126">This error can also occur if the Dataverse environment was reset without unlinking dual-write.</span></span> <span data-ttu-id="66325-127">任何在 Finance and Operations 应用和 Dataverse 中都具有系统管理员角色的用户都可以链接环境。</span><span class="sxs-lookup"><span data-stu-id="66325-127">Any user with system administrator role in both Finance and Operations apps and Dataverse can link the environments.</span></span> <span data-ttu-id="66325-128">只有设置双写入连接的用户才可以添加新表映射。</span><span class="sxs-lookup"><span data-stu-id="66325-128">Only the user who setup the dual-write connection can add new table maps.</span></span> <span data-ttu-id="66325-129">设置后，具有系统管理员角色的任何用户都可以监视状态并编辑映射。</span><span class="sxs-lookup"><span data-stu-id="66325-129">After setup, any user with system administrator role can monitor the status and edit the mappings.</span></span>

## <a name="error-when-you-stop-the-table-mapping"></a><span data-ttu-id="66325-130">停止表映射时出错</span><span class="sxs-lookup"><span data-stu-id="66325-130">Error when you stop the table mapping</span></span>

<span data-ttu-id="66325-131">当您尝试停止表映射时，您可能会收到以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="66325-131">You might receive the following error message when you try to stop the table mappings:</span></span>

<span data-ttu-id="66325-132">*\[已禁止\]，\[{来自令牌交换的 "status":403,"source":"","message":"Error：不允许用户访问连接 dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\]，远程服务器返回错误：(403) 已禁止。*</span><span class="sxs-lookup"><span data-stu-id="66325-132">*\[Forbidden\], \[{"status":403,"source":"","message":"Error from token exchange: User is not allowed to access connection dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*</span></span>

<span data-ttu-id="66325-133">当链接的 Dataverse 环境不可用时，将发生此错误。</span><span class="sxs-lookup"><span data-stu-id="66325-133">This error occurs when the linked Dataverse environment isn't available.</span></span>

<span data-ttu-id="66325-134">要解决此问题，请为数据集成团队创建票证。</span><span class="sxs-lookup"><span data-stu-id="66325-134">To fix the issue, create a ticket for the Data Integration team.</span></span> <span data-ttu-id="66325-135">附加网络跟踪，以便数据集成团队可以在后端将映射标记为 **未运行**。</span><span class="sxs-lookup"><span data-stu-id="66325-135">Attach the network trace so that the Data Integration team can mark the maps as **Not running** in the back end.</span></span>

## <a name="error-while-trying-to-start-a-table-mapping"></a><span data-ttu-id="66325-136">尝试开始表映射时出错</span><span class="sxs-lookup"><span data-stu-id="66325-136">Error while trying to start a table mapping</span></span>

<span data-ttu-id="66325-137">当您尝试将映射的状态设置为 **正在运行** 时，可能会收到如下错误：</span><span class="sxs-lookup"><span data-stu-id="66325-137">You might receive an error like the following when you try to set that state of a mapping to **Running**:</span></span>

<span data-ttu-id="66325-138">*无法完成初始数据同步。错误：双写入失败 - 插件注册失败：无法建立双写入查找元数据。错误对象引用未设置为对象的实例。*</span><span class="sxs-lookup"><span data-stu-id="66325-138">*Unable to complete initial data sync. Error: dual-write failure - plugin registration failed: Unable to build dual-write lookup metadata. Error object reference not set to an instance of an object.*</span></span>

<span data-ttu-id="66325-139">此错误的解决方法取决于错误原因：</span><span class="sxs-lookup"><span data-stu-id="66325-139">The fix for this error depends on the cause of the error:</span></span>

+ <span data-ttu-id="66325-140">如果映射具有相关映射，请确保启用此表映射的相关映射。</span><span class="sxs-lookup"><span data-stu-id="66325-140">If the mapping has dependent mappings, then make sure to enable the dependent mappings of this table mapping.</span></span>
+ <span data-ttu-id="66325-141">映射可能缺少源或目标列。</span><span class="sxs-lookup"><span data-stu-id="66325-141">The mapping might be missing source or destination columns.</span></span> <span data-ttu-id="66325-142">如果缺少 Finance and Operations 应用中的列，请按照[映射中缺少表列问题](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps)一节中的步骤进行操作。</span><span class="sxs-lookup"><span data-stu-id="66325-142">If a column in the Finance and Operations app is missing, then follow the steps in the section [Missing table columns issue on maps](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps).</span></span> <span data-ttu-id="66325-143">如果缺少 Dataverse 中的列，请单击映射上的 **刷新表** 按钮，让这些列自动填充回映射中。</span><span class="sxs-lookup"><span data-stu-id="66325-143">If a column in Dataverse is missing, then click **Refresh tables** button on the mapping so that the columns are automatically populated back into the mapping.</span></span>
