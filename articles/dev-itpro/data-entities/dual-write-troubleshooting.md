---
title: 数据集成疑难解答指南
description: 本主题提供 Microsoft Dynamics 365 for Finance and Operations 与 Common Data Service 之间的数据集成的疑难解答信息。
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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873097"
---
# <a name="troubleshooting-guide-for-data-integration"></a><span data-ttu-id="ea7c2-103">数据集成疑难解答指南</span><span class="sxs-lookup"><span data-stu-id="ea7c2-103">Troubleshooting guide for data integration</span></span>

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a><span data-ttu-id="ea7c2-104">在 Common Data Service 中启用插件跟踪日志和检查双写入插件错误详细信息</span><span class="sxs-lookup"><span data-stu-id="ea7c2-104">Enable plug-in trace logs in Common Data Service and inspect the dual-write plug-in error details</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="ea7c2-105">如果在双写入同步期间遇到问题或错误，请执行以下步骤在跟踪日志中检查这些错误。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-105">If you experience an issue or error during dual-write synchronization, follow these steps to inspect the errors in the trace log.</span></span>

1. <span data-ttu-id="ea7c2-106">必须先启用插件跟踪日志，才能检查这些错误。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-106">Before you can inspect the errors, you must enable plug-in trace logs.</span></span> <span data-ttu-id="ea7c2-107">有关说明，请参阅[教程：编写和注册插件](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs)中的“查看跟踪日志”部分。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-107">For instructions, see the "View trace logs" section of [Tutorial: Write and register a plug-in](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).</span></span>

    <span data-ttu-id="ea7c2-108">现在可以检查错误。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-108">You can now inspect the errors.</span></span>

2. <span data-ttu-id="ea7c2-109">登录 Microsoft Dynamics 365 for Sales。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-109">Sign in to Microsoft Dynamics 365 for Sales.</span></span>
3. <span data-ttu-id="ea7c2-110">选择**设置**按钮（齿轮符号），然后选择**高级设置**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-110">Select the **Settings** button (the gear symbol), and then select **Advanced Settings**.</span></span>
4. <span data-ttu-id="ea7c2-111">在**设置**菜单中，选择**自定义 \> 插件跟踪日志**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-111">On the **Settings** menu, select **Customization \> Plug-In Trace Log**.</span></span>
5. <span data-ttu-id="ea7c2-112">为类型名称选择 **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** 以显示错误详细信息。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-112">Select **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** as the type name to show the error details.</span></span>

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a><span data-ttu-id="ea7c2-113">在 Finance and Operations 中检查双写入同步错误</span><span class="sxs-lookup"><span data-stu-id="ea7c2-113">Inspect dual-write synchronization errors in Finance and Operations</span></span>

<span data-ttu-id="ea7c2-114">执行以下步骤以在测试期间检查错误。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-114">Follow these steps to inspect errors during testing.</span></span>

1. <span data-ttu-id="ea7c2-115">登录 Microsoft Dynamics Lifecycle Services (LCS)。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-115">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="ea7c2-116">打开要为其执行双写入测试的 LCS 项目。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-116">Open the LCS project to do dual-write testing for.</span></span>
3. <span data-ttu-id="ea7c2-117">选择**云托管的环境**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-117">Select **Cloud-hosted environments**.</span></span>
4. <span data-ttu-id="ea7c2-118">使用 LCS 中显示的本地帐户建立与 Dynamics 365 for Finance and Operations 虚拟机 (VM) 之间的远程桌面连接。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-118">Make a Remote desktop connection to the Dynamics 365 for Finance and Operations virtual machine (VM) by using local account that is shown in LCS.</span></span>
5. <span data-ttu-id="ea7c2-119">打开事件查看器。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-119">Open Event Viewer.</span></span> 
6. <span data-ttu-id="ea7c2-120">转到**应用程序和服务日志 \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-120">Go to **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span> <span data-ttu-id="ea7c2-121">将显示错误和详细信息。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-121">The errors and details are shown.</span></span>

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a><span data-ttu-id="ea7c2-122">取消一个 Common Data Service 环境与 Finance and Operations 之间的链接并链接另一个环境</span><span class="sxs-lookup"><span data-stu-id="ea7c2-122">Unlink one Common Data Service environment from Finance and Operations and link another environment</span></span>

<span data-ttu-id="ea7c2-123">执行以下步骤以更新链接。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-123">Follow these steps to update links.</span></span>

1. <span data-ttu-id="ea7c2-124">转到 Finance and Operations 环境。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-124">Go to the Finance and Operations environment.</span></span>
2. <span data-ttu-id="ea7c2-125">打开数据管理</span><span class="sxs-lookup"><span data-stu-id="ea7c2-125">Open Data Management.</span></span>
3. <span data-ttu-id="ea7c2-126">选择**链接到面向应用程序的 CDS**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-126">Select **Link to CDS for apps**.</span></span>
4. <span data-ttu-id="ea7c2-127">选择正在运行的所有映射，然后选择**停止**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-127">Select all the mappings that are running, and then select **Stop**.</span></span>
5. <span data-ttu-id="ea7c2-128">选择所有映射，然后选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-128">Select all the mappings, and then select **Delete**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea7c2-129">如果选择 **CustomerV3-Account** 模板，则**删除**选项不可用。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-129">The **Delete** option isn't available if the **CustomerV3-Account** template is selected.</span></span> <span data-ttu-id="ea7c2-130">根据需要取消选择此模板。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-130">Clear the selection of this template as required.</span></span> <span data-ttu-id="ea7c2-131">**CustomerV3-Account** 是较早设置的模板，支持目标客户到现金解决方案。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-131">**CustomerV3-Account** is an older provisioned template and works with the Prospect to Cash solution.</span></span> <span data-ttu-id="ea7c2-132">因为是全局发布的，所以在所有模板下都显示。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-132">Because it's globally released, it appears under all templates.</span></span>

6. <span data-ttu-id="ea7c2-133">选择**取消链接环境**。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-133">Select **Unlink environment**.</span></span>
7. <span data-ttu-id="ea7c2-134">选择**是**以确认操作。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-134">Select **Yes** to confirm the operation.</span></span>
8. <span data-ttu-id="ea7c2-135">若要链接新的环境，请执行[安装指南](https://aka.ms/dualwrite-docs)中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ea7c2-135">To link the new environment, follow the steps in the [installation guide](https://aka.ms/dualwrite-docs).</span></span>
