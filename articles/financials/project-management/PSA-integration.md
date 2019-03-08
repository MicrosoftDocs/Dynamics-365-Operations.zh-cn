---
title: Project Service Automation
description: 此主题提供有关 Project Service Automation 到 Finance and Operations 集成解决方案的信息。 此集成解决方案使用数据集成功能，通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "335684"
---
# <a name="project-service-automation"></a><span data-ttu-id="61c7b-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61c7b-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="61c7b-105">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能，通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。</span><span class="sxs-lookup"><span data-stu-id="61c7b-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="61c7b-106">可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="61c7b-107">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="61c7b-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="61c7b-108">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="61c7b-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="61c7b-109">如果在使用 Finance and Operations 7.3.0，则必须安装 KB 4074835。</span><span class="sxs-lookup"><span data-stu-id="61c7b-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="61c7b-110">然后就可以集成固定价格项目。</span><span class="sxs-lookup"><span data-stu-id="61c7b-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="61c7b-111">如果在使用 Finance and Operations 7.3.0，并从 Project Service Automation 导入免费交易记录，则必须安装 KB 4345320，以便将这些费用添加到该项目发票中。</span><span class="sxs-lookup"><span data-stu-id="61c7b-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="61c7b-112">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations 版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="61c7b-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="61c7b-113">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本，则可以同步实际值。</span><span class="sxs-lookup"><span data-stu-id="61c7b-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="61c7b-114">必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance and Operations 集成。</span><span class="sxs-lookup"><span data-stu-id="61c7b-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="61c7b-115">有关详细信息，请参阅 [Project Service Automation 集成参数](PSA-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="61c7b-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="61c7b-116">以下情况下，可通过集成解决方案直接同步：</span><span class="sxs-lookup"><span data-stu-id="61c7b-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="61c7b-117">在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-118">在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-119">在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-120">在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-121">在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-122">在 Finance and Operations 中维护费用交易记录类别，并将其直接从 Finance and Operations 同步到 Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="61c7b-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="61c7b-123">在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-124">在 Project Service Automation 中创建项目支出估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="61c7b-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="61c7b-125">在 Project Service Automation 中创建项目时间、费用和费用实际值，并在 Project Service Automation 集成日记帐中创建项目交易记录，以便在 Finance and Operations 中过帐。</span><span class="sxs-lookup"><span data-stu-id="61c7b-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="61c7b-126">数据同步</span><span class="sxs-lookup"><span data-stu-id="61c7b-126">Data synchronization</span></span>

<span data-ttu-id="61c7b-127">下图显示 Project Service Automation 与 Finance and Operations 之间的集成中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="61c7b-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="61c7b-128">并非所有模板当前都可用。</span><span class="sxs-lookup"><span data-stu-id="61c7b-128">Not all templates are currently available.</span></span> <span data-ttu-id="61c7b-129">模板将在准备好后发布。</span><span class="sxs-lookup"><span data-stu-id="61c7b-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="61c7b-130">[![Project Service Automation 与 Finance and Operations 集成](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="61c7b-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="61c7b-131">Finance and Operations 的系统要求</span><span class="sxs-lookup"><span data-stu-id="61c7b-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="61c7b-132">若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装带平台更新 12 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3。</span><span class="sxs-lookup"><span data-stu-id="61c7b-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="61c7b-133">Project Service Automation 的系统要求</span><span class="sxs-lookup"><span data-stu-id="61c7b-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="61c7b-134">若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装以下组件：</span><span class="sxs-lookup"><span data-stu-id="61c7b-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="61c7b-135">Microsoft Dynamics 365 for Project Service Automation 版本 9.0.0.0 或更高版本</span><span class="sxs-lookup"><span data-stu-id="61c7b-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="61c7b-136">Microsoft Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案</span><span class="sxs-lookup"><span data-stu-id="61c7b-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="61c7b-137">适用于 Microsoft Dynamics 365 for Project Service Automation 版本 1.0.0.0 或更高版本的 Project Service Automation 到 Finance and Operations 解决方案</span><span class="sxs-lookup"><span data-stu-id="61c7b-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="61c7b-138">在 Project Service Automation 中安装 Project Service Automation 到 Finance and Operations 集成解决方案</span><span class="sxs-lookup"><span data-stu-id="61c7b-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="61c7b-139">从 [Microsoft 下载中心](https://www.microsoft.com/en-us/download/details.aspx?id=57016)下载 Project Service Automation 到 Finance and Operations 集成解决方案，然后按照该解决方案随附的说明操作。</span><span class="sxs-lookup"><span data-stu-id="61c7b-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
