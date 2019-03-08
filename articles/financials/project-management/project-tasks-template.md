---
title: '将项目任务从 Project Service Automation 直接同步到 Finance and Operations '
description: 此主题介绍用于直接同步 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 的项目任务的模板和基础任务。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "355165"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="9fef9-103">将项目任务从 Project Service Automation 直接同步到 Finance and Operations </span><span class="sxs-lookup"><span data-stu-id="9fef9-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9fef9-104">此主题介绍用于直接同步 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 的项目任务的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="9fef9-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="9fef9-105">Microsoft Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="9fef9-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="9fef9-106">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="9fef9-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="9fef9-107">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="9fef9-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="9fef9-108">Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="9fef9-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="9fef9-109">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="9fef9-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="9fef9-110">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="9fef9-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="9fef9-111">可通过数据集成功能提供的集成模板将有关项目任务的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="9fef9-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="9fef9-112">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="9fef9-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="9fef9-113">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="9fef9-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="9fef9-114">模板和任务</span><span class="sxs-lookup"><span data-stu-id="9fef9-114">Template and task</span></span>

<span data-ttu-id="9fef9-115">若要访问此模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="9fef9-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="9fef9-116">以下模板和基础任务用于将项目任务从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="9fef9-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="9fef9-117">**数据集成中的模板名称：** 项目任务（PSA 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="9fef9-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="9fef9-118">**项目中的任务名称：** 项目任务</span><span class="sxs-lookup"><span data-stu-id="9fef9-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="9fef9-119">必须先同步项目合同和项目，才能同步项目任务。</span><span class="sxs-lookup"><span data-stu-id="9fef9-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="9fef9-120">实体集</span><span class="sxs-lookup"><span data-stu-id="9fef9-120">Entity set</span></span>

| <span data-ttu-id="9fef9-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="9fef9-121">Project Service Automation</span></span> | <span data-ttu-id="9fef9-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9fef9-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="9fef9-123">项目任务</span><span class="sxs-lookup"><span data-stu-id="9fef9-123">Project Tasks</span></span>              | <span data-ttu-id="9fef9-124">项目任务集成实体</span><span class="sxs-lookup"><span data-stu-id="9fef9-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="9fef9-125">实体流</span><span class="sxs-lookup"><span data-stu-id="9fef9-125">Entity flow</span></span>

<span data-ttu-id="9fef9-126">项目任务在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目活动。</span><span class="sxs-lookup"><span data-stu-id="9fef9-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9fef9-127">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="9fef9-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="9fef9-128">必须先同步项目合同和项目，才能同步项目任务。</span><span class="sxs-lookup"><span data-stu-id="9fef9-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="9fef9-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="9fef9-129">Power Query</span></span>

<span data-ttu-id="9fef9-130">如果满足以下条件，则必须使用 Microsoft Power Query for Excel：</span><span class="sxs-lookup"><span data-stu-id="9fef9-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="9fef9-131">项目任务内有资源特定的记录。</span><span class="sxs-lookup"><span data-stu-id="9fef9-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="9fef9-132">如果必须使用 Power Query，请遵守以下准则：</span><span class="sxs-lookup"><span data-stu-id="9fef9-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="9fef9-133">“项目任务（PSA 到 Fin and Ops）”模板有一个默认筛选器，用于通过在 **IsLineTask** 中将该筛选器设置为 **False**，从项目任务内排除资源特定的记录。</span><span class="sxs-lookup"><span data-stu-id="9fef9-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="9fef9-134">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="9fef9-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="9fef9-135">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="9fef9-135">Template mapping in Data integration</span></span>

<span data-ttu-id="9fef9-136">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="9fef9-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="9fef9-137">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="9fef9-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="9fef9-138">[![模板映射](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="9fef9-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
