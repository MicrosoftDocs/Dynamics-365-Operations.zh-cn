---
title: 在 LCS 中安装 IoT 智能加载项
description: 此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 04333b3659f090b15cc0d0ee216f14dabc588883
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386489"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a><span data-ttu-id="69347-103">在 LCS 中安装 IoT 智能加载项</span><span class="sxs-lookup"><span data-stu-id="69347-103">Install the IoT Intelligence add-in in LCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="69347-104">此主题介绍如何在 Microsoft Dynamics Lifecycle Services (LCS) 中安装 IoT 智能加载项。</span><span class="sxs-lookup"><span data-stu-id="69347-104">This topic explains how to install the IoT Intelligence add-in in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="69347-105">必须先[创建 Azure 资源](iot-azure-setup.md)，然后才能安装此加载项。</span><span class="sxs-lookup"><span data-stu-id="69347-105">Before you can install the add-in, you must [create the Azure resources](iot-azure-setup.md).</span></span>

## <a name="set-up-the-lcs-environment"></a><span data-ttu-id="69347-106">设置 LCS 环境</span><span class="sxs-lookup"><span data-stu-id="69347-106">Set up the LCS environment</span></span>

1. <span data-ttu-id="69347-107">打开 LCS，然后转到您的 Microsoft Dynamics 365 Supply Chain Management环境。</span><span class="sxs-lookup"><span data-stu-id="69347-107">Open LCS, and go to your Microsoft Dynamics 365 Supply Chain Management environment.</span></span>
2. <span data-ttu-id="69347-108">滚动到**环境加载项**部分。</span><span class="sxs-lookup"><span data-stu-id="69347-108">Scroll to the **Environment add-ins** section.</span></span>
3. <span data-ttu-id="69347-109">选择**安装新加载项**显示已为环境启用的加载项的列表。</span><span class="sxs-lookup"><span data-stu-id="69347-109">Select **Install a new add-in** to show the list of add-ins that have been enabled for the environment.</span></span>
4. <span data-ttu-id="69347-110">在**选择要安装的加载项**对话框中，选择 **IoT 智能**。</span><span class="sxs-lookup"><span data-stu-id="69347-110">In the **Select an add-in to install** dialog box, select **IoT Intelligence**.</span></span>
5. <span data-ttu-id="69347-111">在**设置加载项**对话框中，提供 IoT 中心和 Redis 缓存的详细信息。</span><span class="sxs-lookup"><span data-stu-id="69347-111">In the **Setup add-in** dialog box, provide the details of your IoT hub and Redis cache.</span></span> <span data-ttu-id="69347-112">可以在您在[创建 Azure 资源](iot-azure-setup.md)中创建的密钥保管库中找到所需值。</span><span class="sxs-lookup"><span data-stu-id="69347-112">You can find the required values in the key vault that you created in [Create Azure resources](iot-azure-setup.md).</span></span>

    + <span data-ttu-id="69347-113">**租户 ID** – 在 Azure 门户中，转到密钥保管库，然后在左侧导航窗格中，选择**概览**，然后复制**目录 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="69347-113">**Tenant ID** – In the Azure portal, go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **Directory ID** value.</span></span> <span data-ttu-id="69347-114">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="69347-114">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="69347-115">**IoT 事件中心兼容的终结点密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择**概览**，然后复制 **DNS 名称**值。</span><span class="sxs-lookup"><span data-stu-id="69347-115">**IoT Event Hub-compatible endpoint Key Vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="69347-116">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="69347-116">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="69347-117">**IoT 事件中心兼容的终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择**密码**，然后复制其中存储 IoT 中心的事件中心连接字符串的密码的名称。</span><span class="sxs-lookup"><span data-stu-id="69347-117">**IoT Event Hub-compatible endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the event hub connection string for the IoT hub is stored.</span></span> <span data-ttu-id="69347-118">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="69347-118">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="69347-119">**Redis 缓存密钥保管库 URI** – 转到密钥保管库，在左侧导航窗格中，选择**概览**，然后复制 **DNS 名称**值。</span><span class="sxs-lookup"><span data-stu-id="69347-119">**Redis cache key vault URI** – Go to the key vault, and then, in the left navigation pane, select **Overview**, and copy the **DNS name** value.</span></span> <span data-ttu-id="69347-120">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="69347-120">Paste that value in the **Setup add-in** dialog box.</span></span>
    + <span data-ttu-id="69347-121">**Redis 缓存终结点密码名称** – 转到密钥保管库，在左侧导航窗格中，选择**密码**，然后复制其中存储 Redis 缓存的连接字符串的密码的名称。</span><span class="sxs-lookup"><span data-stu-id="69347-121">**Redis cache endpoint secret name** – Go to the key vault, and then, in the left navigation pane, select **Secrets**, and copy the name of the secret where the connection string for the Redis cache is stored.</span></span> <span data-ttu-id="69347-122">将该值粘贴到**设置加载项**对话框中。</span><span class="sxs-lookup"><span data-stu-id="69347-122">Paste that value in the **Setup add-in** dialog box.</span></span>

6. <span data-ttu-id="69347-123">选中复选框接受条款和条件。</span><span class="sxs-lookup"><span data-stu-id="69347-123">Select the check box to accept the terms and conditions.</span></span>
7. <span data-ttu-id="69347-124">选择**安装**。</span><span class="sxs-lookup"><span data-stu-id="69347-124">Select **Install**.</span></span>
8. <span data-ttu-id="69347-125">将显示一个消息框，内容为“已成功触发加载项安装。”</span><span class="sxs-lookup"><span data-stu-id="69347-125">A message box appears that states, "Add-in has been successfully triggered for installation."</span></span> <span data-ttu-id="69347-126">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="69347-126">Select **OK**.</span></span>

<span data-ttu-id="69347-127">现已完成 LCS 设置。</span><span class="sxs-lookup"><span data-stu-id="69347-127">LCS setup is now completed.</span></span> <span data-ttu-id="69347-128">下一步是[设置方案](iot-scenario-setup.md)。</span><span class="sxs-lookup"><span data-stu-id="69347-128">The next step is to [set up the scenarios](iot-scenario-setup.md).</span></span>

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a><span data-ttu-id="69347-129">卸载加载项</span><span class="sxs-lookup"><span data-stu-id="69347-129">Uninstall the add-in</span></span>

1. <span data-ttu-id="69347-130">在 Supply Chain Management 中[禁用方案](iot-scenario-setup.md#how-to-disable-a-scenario)。</span><span class="sxs-lookup"><span data-stu-id="69347-130">In Supply Chain Management, [disable the scenarios](iot-scenario-setup.md#how-to-disable-a-scenario).</span></span>
2. <span data-ttu-id="69347-131">在 LCS 中，转到您的 Supply Chain Management 环境详细信息。</span><span class="sxs-lookup"><span data-stu-id="69347-131">In LCS, go to your Supply Chain Management environment details.</span></span>
3. <span data-ttu-id="69347-132">滚动到**环境加载项**部分。</span><span class="sxs-lookup"><span data-stu-id="69347-132">Scroll to the **Environment add-ins** section.</span></span>
4. <span data-ttu-id="69347-133">为 IoT 智能加载项选择**卸载**。</span><span class="sxs-lookup"><span data-stu-id="69347-133">Select **Uninstall** for the IoT Intelligence add-in.</span></span>
