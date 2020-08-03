---
title: 在 LCS 中安装 IoT 智能加载项
description: 此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。
author: robinarh
manager: tfehr
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d2bcbf69362e4ca3a156d1d404e15489ddb3f0d0
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597208"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="d8361-103">在 LCS 中安装 IoT 智能加载项</span><span class="sxs-lookup"><span data-stu-id="d8361-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8361-104">此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。</span><span class="sxs-lookup"><span data-stu-id="d8361-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d8361-105">请注意，加载项不能安装在演示/试用环境中。</span><span class="sxs-lookup"><span data-stu-id="d8361-105">Note that add-ins cannot be installed on a demo/trial environment.</span></span> <span data-ttu-id="d8361-106">必须先[创建 Azure 资源](iot-azure-setup.md)，然后才能安装此加载项。</span><span class="sxs-lookup"><span data-stu-id="d8361-106">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="d8361-107">设置 LCS 环境</span><span class="sxs-lookup"><span data-stu-id="d8361-107">Set up the LCS environment</span></span>

1. <span data-ttu-id="d8361-108">打开 LCS，然后转到您的 Microsoft Dynamics 365 Supply Chain Management环境。</span><span class="sxs-lookup"><span data-stu-id="d8361-108">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="d8361-109">滚动到**环境加载项**部分。</span><span class="sxs-lookup"><span data-stu-id="d8361-109">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="d8361-110">选择**安装新加载项**显示已为环境启用的加载项的列表。</span><span class="sxs-lookup"><span data-stu-id="d8361-110">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="d8361-111">在**选择要安装的加载项**对话框中，选择 **IoT 智能**。</span><span class="sxs-lookup"><span data-stu-id="d8361-111">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="d8361-112">在**设置加载项**对话框中，提供 IoT 中心和 Redis 缓存的详细信息。</span><span class="sxs-lookup"><span data-stu-id="d8361-112">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="d8361-113">可以在您在[创建 Azure 资源](iot-azure-setup.md)中创建的密钥保管库中找到所需值。</span><span class="sxs-lookup"><span data-stu-id="d8361-113">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="d8361-114">**租户 ID** – 在 Azure 门户中，转到密钥保管库，然后在左侧导航窗格中，选择**概览**，然后复制**目录 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="d8361-114">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="d8361-115">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="d8361-115">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d8361-116">**IoT 事件中心兼容的终结点密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择**概览**，然后复制 **DNS 名称**值。</span><span class="sxs-lookup"><span data-stu-id="d8361-116">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="d8361-117">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="d8361-117">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d8361-118">**IoT 事件中心兼容的终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择**密码**，然后复制其中存储 IoT 中心的事件中心连接字符串的密码的名称。</span><span class="sxs-lookup"><span data-stu-id="d8361-118">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="d8361-119">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="d8361-119">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d8361-120">**Redis 缓存密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择**概览**，然后复制 **DNS 名称**值。</span><span class="sxs-lookup"><span data-stu-id="d8361-120">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="d8361-121">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="d8361-121">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="d8361-122">**Redis 缓存终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择**密码**，然后复制其中存储 Redis 缓存的连接字符串的密码的名称。</span><span class="sxs-lookup"><span data-stu-id="d8361-122">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="d8361-123">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="d8361-123">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="d8361-124">选中复选框接受条款和条件。</span><span class="sxs-lookup"><span data-stu-id="d8361-124">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="d8361-125">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="d8361-125">Select **Install**.</span></span>
8. <span data-ttu-id="d8361-126">将显示一个消息框，内容为“已成功触发加载项安装。”</span><span class="sxs-lookup"><span data-stu-id="d8361-126">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="d8361-127">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="d8361-127">Select **OK**.</span></span>

<span data-ttu-id="d8361-128">现已完成 LCS 设置。</span><span class="sxs-lookup"><span data-stu-id="d8361-128">LCS setup is now completed.</span></span> <span data-ttu-id="d8361-129">下一步是[设置方案](iot-scenario-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="d8361-129">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="d8361-130">卸载加载项</span><span class="sxs-lookup"><span data-stu-id="d8361-130">Uninstall the add-in</span></span>

1. <span data-ttu-id="d8361-131">在 Supply Chain Management 中[禁用方案](iot-scenario-setup.md#how-to-disable-a-scenario)。</span><span class="sxs-lookup"><span data-stu-id="d8361-131">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="d8361-132">在 LCS 中，转到您的 Supply Chain Management 环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="d8361-132">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="d8361-133">滚动到**环境加载项**部分。</span><span class="sxs-lookup"><span data-stu-id="d8361-133">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="d8361-134">为 IoT 智能加载项选择**卸载**。</span><span class="sxs-lookup"><span data-stu-id="d8361-134">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
