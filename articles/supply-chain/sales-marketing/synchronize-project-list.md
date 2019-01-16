---
title: "将项目列表从 Finance and Operations 同步到 Field Service"
description: "本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的项目同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: zh-cn
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="7a623-103">将项目列表从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="7a623-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7a623-104">本主题讨论用于将来自 Microsoft Dynamics 365 for Finance and Operations 的项目同步到 Microsoft Dynamics 365 for Field Service 的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="7a623-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7a623-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="7a623-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7a623-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="7a623-106">Templates and tasks</span></span>
<span data-ttu-id="7a623-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的项目的同步。</span><span class="sxs-lookup"><span data-stu-id="7a623-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="7a623-108">**数据集成中的模板名称：**</span><span class="sxs-lookup"><span data-stu-id="7a623-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="7a623-109">项目（Finance and Operations 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="7a623-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="7a623-110">**数据集成项目中的任务名称：**</span><span class="sxs-lookup"><span data-stu-id="7a623-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="7a623-111">项目</span><span class="sxs-lookup"><span data-stu-id="7a623-111">Projects</span></span>

<span data-ttu-id="7a623-112">在发生项目列表同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="7a623-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="7a623-113">帐户（Sales 到 Finance and Operations）</span><span class="sxs-lookup"><span data-stu-id="7a623-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="7a623-114">实体集</span><span class="sxs-lookup"><span data-stu-id="7a623-114">Entity set</span></span>
<span data-ttu-id="7a623-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a623-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="7a623-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="7a623-116">Field Service</span></span>           | <span data-ttu-id="7a623-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a623-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="7a623-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="7a623-118">msdynce_externalprojects</span></span> | <span data-ttu-id="7a623-119">项目</span><span class="sxs-lookup"><span data-stu-id="7a623-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="7a623-120">实体流</span><span class="sxs-lookup"><span data-stu-id="7a623-120">Entity flow</span></span>
<span data-ttu-id="7a623-121">项目在 Finance and Operations 中创建。</span><span class="sxs-lookup"><span data-stu-id="7a623-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="7a623-122">具有**项目类型**时间和材料以及进行中的**项目阶段**的产品将同步到 Field Service 中的**外部项目**实体，包括项目编号、项目名称、项目阶段和客户帐户信息。</span><span class="sxs-lookup"><span data-stu-id="7a623-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="7a623-123">**外部项目**的列表用于将 Field service 工作订单与 Finance and Operations 项目匹配。</span><span class="sxs-lookup"><span data-stu-id="7a623-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="7a623-124">Field Service CRM 解决方案 外部项目是从 Operations 获取所有项目的新实体。</span><span class="sxs-lookup"><span data-stu-id="7a623-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="7a623-125">外部项目字段已添加到“工作订单”实体。</span><span class="sxs-lookup"><span data-stu-id="7a623-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="7a623-126">此字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Operations 内的一个项目。</span><span class="sxs-lookup"><span data-stu-id="7a623-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="7a623-127">“系统状态”将“打开 - 正在进行(690,970,000)”更改为更高状态后，“外部项目”字段将被锁定，您将无法添加、删除或更改值。</span><span class="sxs-lookup"><span data-stu-id="7a623-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="7a623-128">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="7a623-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="7a623-129">在 Finance and Operations 中</span><span class="sxs-lookup"><span data-stu-id="7a623-129">In Finance and Operations</span></span>
<span data-ttu-id="7a623-130">为数据实体项目启用更改跟踪</span><span class="sxs-lookup"><span data-stu-id="7a623-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7a623-131">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="7a623-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="7a623-132">项目（Finance and Operations 到 Field Service）：项目</span><span class="sxs-lookup"><span data-stu-id="7a623-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="7a623-133">[![数据集成中的模板映射](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="7a623-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

