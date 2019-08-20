---
title: 数据集成疑难解答指南
description: 本主题提供有关 Microsoft Dynamics 365 for Finance and Operations 与 Common Data Service 之间的数据集成的疑难解答信息。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797267"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="90342-103">数据集成疑难解答指南</span><span class="sxs-lookup"><span data-stu-id="90342-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a><span data-ttu-id="90342-104">启用  Common Data Service 中的插件跟踪和检查双写入插件错误详细信息</span><span class="sxs-lookup"><span data-stu-id="90342-104">Enable Plugin Trace in Common Data Service and check the dual-write Plugin error details</span></span>

<span data-ttu-id="90342-105">如果遇到了双写入同步问题或错误，可以在跟踪日志中检查错误：</span><span class="sxs-lookup"><span data-stu-id="90342-105">If you are facing an issue or error with dual-write synchronization, you can inspect the errors in the trace log:</span></span>

1. <span data-ttu-id="90342-106">必须先按照[登记簿插件](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)中有关启用插件跟踪说明启用插件跟踪，才能检查错误。</span><span class="sxs-lookup"><span data-stu-id="90342-106">Before you can inspect the errors, you must enable Plugin trace using the instructions in [Register plug-in](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs) to enable Plugin trace.</span></span> <span data-ttu-id="90342-107">现在可以检查错误。</span><span class="sxs-lookup"><span data-stu-id="90342-107">Now you can inspect the errors.</span></span>
2. <span data-ttu-id="90342-108">登录到 Dynamics 365 for Sales。</span><span class="sxs-lookup"><span data-stu-id="90342-108">Login to Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="90342-109">单击“设置”图标（齿轮），然后选择**高级设置**。</span><span class="sxs-lookup"><span data-stu-id="90342-109">Click on the Settings icon (a gear), and select **Advanced Settings**.</span></span>
4. <span data-ttu-id="90342-110">在**设置**菜单中，选择**自定义 > 插件跟踪日志**。</span><span class="sxs-lookup"><span data-stu-id="90342-110">In the **Settings** menu, choose **Customization > Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="90342-111">单击类型名称 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** 以显示错误详细信息。</span><span class="sxs-lookup"><span data-stu-id="90342-111">Click the type name **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** to display the error details.</span></span>

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="90342-112">在 Finance and Operations 中检查双写入同步错误</span><span class="sxs-lookup"><span data-stu-id="90342-112">Check dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="90342-113">可通过执行以下步骤检查测试期间发生的错误：</span><span class="sxs-lookup"><span data-stu-id="90342-113">You can check the errors during testing by following these steps:</span></span>

+ <span data-ttu-id="90342-114">登录 LifeCycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="90342-114">Login to LifeCycle Services (LCS).</span></span>
+ <span data-ttu-id="90342-115">打开选择要对其执行双写入测试的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="90342-115">Open the LCS project that you chose to perform dual-write testing.</span></span>
+ <span data-ttu-id="90342-116">转到云托管的环境。</span><span class="sxs-lookup"><span data-stu-id="90342-116">Go to Cloud Hosted Environments.</span></span>
+ <span data-ttu-id="90342-117">将在 LCS 中显示使用本地帐户的 Finance and Operations VM 的远程桌面。</span><span class="sxs-lookup"><span data-stu-id="90342-117">Remote desktop to Finance and Operations VM using local account that is displayed in LCS.</span></span>
+ <span data-ttu-id="90342-118">打开事件查看器。</span><span class="sxs-lookup"><span data-stu-id="90342-118">Open the event viewer.</span></span> 
+ <span data-ttu-id="90342-119">导航到**应用程序和服务日志 > Microsoft > Dynamics > AX-DualWriteSync > Operational**。</span><span class="sxs-lookup"><span data-stu-id="90342-119">Navigate to **Applications and Services logs > Microsoft > Dynamics > AX-DualWriteSync > Operational**.</span></span> <span data-ttu-id="90342-120">将显示错误和详细信息。</span><span class="sxs-lookup"><span data-stu-id="90342-120">The errors and details are displayed.</span></span>

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a><span data-ttu-id="90342-121">如何从 Finance and Operations 取消链接和链接其他 Common Data Service 环境</span><span class="sxs-lookup"><span data-stu-id="90342-121">How to unlink and link another Common Data Service environment from Finance and Operations</span></span>

<span data-ttu-id="90342-122">可通过执行以下步骤更新链接：</span><span class="sxs-lookup"><span data-stu-id="90342-122">You can update links by following these steps:</span></span>

+ <span data-ttu-id="90342-123">导航到 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="90342-123">Navigate to the Finance and Operations environment.</span></span>
+ <span data-ttu-id="90342-124">打开数据管理</span><span class="sxs-lookup"><span data-stu-id="90342-124">Open Data Management.</span></span>
+ <span data-ttu-id="90342-125">单击**链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="90342-125">Click on **Link to CDS for apps**.</span></span>
+ <span data-ttu-id="90342-126">选择所有正在运行的映射，然后单击**停止**。</span><span class="sxs-lookup"><span data-stu-id="90342-126">Select all the running mappings and click **Stop**.</span></span> 
+ <span data-ttu-id="90342-127">选择所有映射，然后单击**删除**。</span><span class="sxs-lookup"><span data-stu-id="90342-127">Select all the mappings and click **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="90342-128">如果选择 **CustomerV3-Account** 模板，则不显示**删除**选项。</span><span class="sxs-lookup"><span data-stu-id="90342-128">The **Delete** option will not appear if **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="90342-129">如果需要，则不选择。</span><span class="sxs-lookup"><span data-stu-id="90342-129">Unselect it if needed.</span></span> <span data-ttu-id="90342-130">**CustomerV3-Account** 是较早设置的模板，支持目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="90342-130">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="90342-131">因为是全局发布的，所以在所有模板下都显示。</span><span class="sxs-lookup"><span data-stu-id="90342-131">Because it is globally released, it shows up under all templates.</span></span>

+ <span data-ttu-id="90342-132">单击**取消链接环境**。</span><span class="sxs-lookup"><span data-stu-id="90342-132">Click **Unlink environment**.</span></span>
+ <span data-ttu-id="90342-133">单击**是**确认。</span><span class="sxs-lookup"><span data-stu-id="90342-133">Click **Yes** for confirmation.</span></span>
+ <span data-ttu-id="90342-134">若要链接新的环境，请执行[安装指南](https://aka.ms/dualwrite-docs)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="90342-134">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>

