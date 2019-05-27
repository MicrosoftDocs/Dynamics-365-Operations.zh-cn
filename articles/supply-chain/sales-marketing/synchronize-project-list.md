---
title: 将项目列表从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的项目的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1525869"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="64165-103">将项目列表从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="64165-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="64165-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的项目的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="64165-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="64165-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="64165-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="64165-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="64165-106">Templates and tasks</span></span>
<span data-ttu-id="64165-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的项目的同步。</span><span class="sxs-lookup"><span data-stu-id="64165-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="64165-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="64165-108">**Template in Data integration**</span></span>
- <span data-ttu-id="64165-109">项目（Fin and Ops 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="64165-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="64165-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="64165-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="64165-111">项目</span><span class="sxs-lookup"><span data-stu-id="64165-111">Projects</span></span>

<span data-ttu-id="64165-112">在发生项目列表同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="64165-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="64165-113">科目（Sales 到 Fin and Ops）</span><span class="sxs-lookup"><span data-stu-id="64165-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="64165-114">实体集</span><span class="sxs-lookup"><span data-stu-id="64165-114">Entity set</span></span>
| <span data-ttu-id="64165-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="64165-115">Field Service</span></span>           | <span data-ttu-id="64165-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="64165-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="64165-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="64165-117">msdynce_externalprojects</span></span> | <span data-ttu-id="64165-118">项目</span><span class="sxs-lookup"><span data-stu-id="64165-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="64165-119">实体流</span><span class="sxs-lookup"><span data-stu-id="64165-119">Entity flow</span></span>
<span data-ttu-id="64165-120">项目在 Finance and Operations 中创建。</span><span class="sxs-lookup"><span data-stu-id="64165-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="64165-121">将**项目类型**设置为**时间和材料**并将**项目阶段**设置为**进行中**的项目将同步到 Field Service 中的**外部项目**实体，包括项目编号、项目名称、项目阶段和客户帐户信息。</span><span class="sxs-lookup"><span data-stu-id="64165-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="64165-122">**外部项目**列表用于将 Field service 工作订单与 Finance and Operations 项目匹配。</span><span class="sxs-lookup"><span data-stu-id="64165-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="64165-123">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="64165-123">Field Service CRM solution</span></span>
<span data-ttu-id="64165-124">**外部项目**实体从 Finance and Operations 获取所有项目。</span><span class="sxs-lookup"><span data-stu-id="64165-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="64165-125">**外部项目**字段已添加到**工作订单**实体。</span><span class="sxs-lookup"><span data-stu-id="64165-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="64165-126">此字段是查找字段，因此，通过标记项目的工作订单，销售订单将被连接到 Finance and Operations 内的一个项目。</span><span class="sxs-lookup"><span data-stu-id="64165-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="64165-127">**系统状态**将**打开 - 正在进行(690,970,000)** 更改为更高状态后，**外部项目**字段将被锁定，您将无法再添加、删除或更改值。</span><span class="sxs-lookup"><span data-stu-id="64165-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="64165-128">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="64165-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="64165-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="64165-129">Finance and Operations</span></span>
<span data-ttu-id="64165-130">为数据实体项目启用更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="64165-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="64165-131">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="64165-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="64165-132">项目（Fin and Ops 到 Field Service）：项目</span><span class="sxs-lookup"><span data-stu-id="64165-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="64165-133">[![数据集成中的模板映射](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="64165-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
