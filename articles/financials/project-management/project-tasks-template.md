---
title: "从 Project Service Automation 同步项目任务"
description: "本主题介绍用于将项目任务直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="4b9a0-103">将项目任务从 Project Service Automation 直接同步到 Finance and Operations 中的项目活动</span><span class="sxs-lookup"><span data-stu-id="4b9a0-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="4b9a0-104">本主题介绍用于将项目任务直接从 Microsoft Dynamics 365 for Project Service Automation 同步到 Dynamics 365 for Finance and Operations 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="4b9a0-105">Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="4b9a0-106">Project Service Automation 到 Finance and Operations 的数据传输</span><span class="sxs-lookup"><span data-stu-id="4b9a0-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="4b9a0-107">Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能在 Project Service Automation 和 Finance and Operations 的实例之间同步数据。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="4b9a0-108">可通过数据集成功能提供的集成模板将有关项目任务的数据从 Project Service Automation 传输到 Finance and Operations。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4b9a0-109">下图显示 Project Service Automation 与 Finance and Operations 之间中如何同步数据。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="4b9a0-110">[![Project Service Automation 与 Finance and Operations 集成的数据传输](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="4b9a0-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="4b9a0-111">模板和任务</span><span class="sxs-lookup"><span data-stu-id="4b9a0-111">Template and task</span></span>

<span data-ttu-id="4b9a0-112">若要访问此模板，请在 Microsoft PowerApps 管理员中心中选择**项目**，然后在右上角中选择**新建项目**以选择公共模板。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="4b9a0-113">以下模板和基础任务用于将项目任务从 Project Service Automation 同步到 Finance and Operations：</span><span class="sxs-lookup"><span data-stu-id="4b9a0-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="4b9a0-114">-**项目中的模板名称：** 项目任务（PSA 到 Fin and Ops）-**项目中的任务名称：** 项目任务</span><span class="sxs-lookup"><span data-stu-id="4b9a0-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="4b9a0-115">必须先同步项目合同和项目，才能同步项目任务。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="4b9a0-116">实体集</span><span class="sxs-lookup"><span data-stu-id="4b9a0-116">Entity set</span></span>

|<span data-ttu-id="4b9a0-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="4b9a0-117">Project Service Automation</span></span>               | <span data-ttu-id="4b9a0-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4b9a0-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="4b9a0-119">项目任务</span><span class="sxs-lookup"><span data-stu-id="4b9a0-119">Project Tasks</span></span>                           | <span data-ttu-id="4b9a0-120">项目任务的集成实体。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="4b9a0-121">实体流</span><span class="sxs-lookup"><span data-stu-id="4b9a0-121">Entity flow</span></span>

<span data-ttu-id="4b9a0-122">项目任务在 Project Service Automation 中管理，并同步到 Finance and Operations 中充当项目活动。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="4b9a0-123">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="4b9a0-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="4b9a0-124">必须先同步项目合同和项目，才能同步项目任务。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="4b9a0-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="4b9a0-125">Power Query</span></span>

<span data-ttu-id="4b9a0-126">如果满足以下条件，则必须使用 Microsoft Power Query：</span><span class="sxs-lookup"><span data-stu-id="4b9a0-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="4b9a0-127">项目任务内有资源特定的记录。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="4b9a0-128">如果必须使用 Power Query，请遵守以下准则：</span><span class="sxs-lookup"><span data-stu-id="4b9a0-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="4b9a0-129">“项目任务（PSA 到 Fin and Ops）”模板有一个默认筛选器，通过在 **IsLineTask** 中将该筛选器设置为 **False**，可以从项目任务内排除资源特定的记录。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="4b9a0-130">如果创建自己的模板，则必须添加这个筛选器。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="4b9a0-131">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="4b9a0-131">Template mapping in Data integration</span></span>

<span data-ttu-id="4b9a0-132">下图显示了数据集成中的模板任务映射的一个示例。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="4b9a0-133">此映射显示将从 Project Service Automation 同步到 Finance and Operations 的字段信息。</span><span class="sxs-lookup"><span data-stu-id="4b9a0-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="4b9a0-134">[![模板映射](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="4b9a0-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


