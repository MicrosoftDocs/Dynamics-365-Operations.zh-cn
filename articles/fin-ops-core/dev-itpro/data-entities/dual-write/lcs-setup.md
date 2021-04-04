---
title: Lifecycle Services 的双写入设置
description: 本主题说明如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置双写入连接。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567712"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="66328-103">Lifecycle Services 的双写入设置</span><span class="sxs-lookup"><span data-stu-id="66328-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="66328-104">此主题介绍如何从 Microsoft Dynamics Lifecycle Services (LCS) 设置新 Finance and Operations 环境与新 Dataverse 环境之间的双写入连接。</span><span class="sxs-lookup"><span data-stu-id="66328-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66328-105">先决条件</span><span class="sxs-lookup"><span data-stu-id="66328-105">Prerequisites</span></span>

<span data-ttu-id="66328-106">您必须是管理员才能设置双写入连接。</span><span class="sxs-lookup"><span data-stu-id="66328-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="66328-107">您必须有权访问该租户。</span><span class="sxs-lookup"><span data-stu-id="66328-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="66328-108">您必须同时是 Finance and Operations 环境和 Dataverse 环境中的管理员。</span><span class="sxs-lookup"><span data-stu-id="66328-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="66328-109">设置双写入连接</span><span class="sxs-lookup"><span data-stu-id="66328-109">Set up a dual-write connection</span></span>

<span data-ttu-id="66328-110">按照以下步骤设置双写入连接。</span><span class="sxs-lookup"><span data-stu-id="66328-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="66328-111">在 LCS 中，转到您的项目。</span><span class="sxs-lookup"><span data-stu-id="66328-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="66328-112">选择 **配置** 部署新环境。</span><span class="sxs-lookup"><span data-stu-id="66328-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="66328-113">选择版本。</span><span class="sxs-lookup"><span data-stu-id="66328-113">Select the version.</span></span> 
4. <span data-ttu-id="66328-114">选择拓扑。</span><span class="sxs-lookup"><span data-stu-id="66328-114">Select the topology.</span></span> <span data-ttu-id="66328-115">如果只有一种拓扑可用，将自动选择该拓扑。</span><span class="sxs-lookup"><span data-stu-id="66328-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="66328-116">完成 **部署设置** 向导中的第一批步骤。</span><span class="sxs-lookup"><span data-stu-id="66328-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="66328-117">在 **Dataverse** 选项卡中，执行以下步骤之一：</span><span class="sxs-lookup"><span data-stu-id="66328-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="66328-118">如果已经为您的租户预配了一个 Dataverse 环境，可以选择该环境。</span><span class="sxs-lookup"><span data-stu-id="66328-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="66328-119">将 **配置 Dataverse** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="66328-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="66328-120">在 **可用环境** 列中，选择要与您的 Finance and Operations 数据集成的环境。</span><span class="sxs-lookup"><span data-stu-id="66328-120">In the **Available environments** column, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="66328-121">此列表中包含您拥有其管理员权限的所有环境。</span><span class="sxs-lookup"><span data-stu-id="66328-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="66328-122">选中 **同意** 复选框表示您同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="66328-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse 选项卡，如果已经为您的租户预配了一个 Dataverse 环境](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="66328-124">如果您的租户还没有 Dataverse 环境，将预配一个新环境。</span><span class="sxs-lookup"><span data-stu-id="66328-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="66328-125">将 **配置 Dataverse** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="66328-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="66328-126">输入 Dataverse 环境的名称。</span><span class="sxs-lookup"><span data-stu-id="66328-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="66328-127">选择要在其中部署环境的区域。</span><span class="sxs-lookup"><span data-stu-id="66328-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="66328-128">选择环境的默认语言和货币。</span><span class="sxs-lookup"><span data-stu-id="66328-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="66328-129">以后不能更改语言和货币。</span><span class="sxs-lookup"><span data-stu-id="66328-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="66328-130">选中 **同意** 复选框表示您同意条款和条件。</span><span class="sxs-lookup"><span data-stu-id="66328-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![Dataverse 选项卡，当租户还没有 Dataverse 环境时](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="66328-132">完成 **部署设置** 向导中的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="66328-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="66328-133">环境的状态为 **已部署** 之后，打开环境详细信息页。</span><span class="sxs-lookup"><span data-stu-id="66328-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="66328-134">**Power Platform 集成** 部分显示链接的 Finance and Operations 环境和 Dataverse 环境的名称。</span><span class="sxs-lookup"><span data-stu-id="66328-134">The **Power Platform Integration** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Power Platform 集成部分](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="66328-136">Finance and Operations 环境管理员必须登录 LCS 并选择 **链接到面向应用程序的 CDS** 以完成链接。</span><span class="sxs-lookup"><span data-stu-id="66328-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="66328-137">环境详细信息页中显示管理员的联系信息。</span><span class="sxs-lookup"><span data-stu-id="66328-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="66328-138">完成链接之后，将把状态更新为 **已成功完成环境链接**。</span><span class="sxs-lookup"><span data-stu-id="66328-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="66328-139">若要在 Finance and Operations 环境中打开 **数据集成** 工作区和控制可用模板，请选择 **链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="66328-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Power Platform 集成部分的“链接到面向应用程序的 CDS”按钮](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="66328-141">不能使用 LCS 取消链接环境。</span><span class="sxs-lookup"><span data-stu-id="66328-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="66328-142">若要取消链接环境，请在 Finance and Operations 环境中打开 **数据集成** 工作区，然后选择 **取消链接**。</span><span class="sxs-lookup"><span data-stu-id="66328-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]