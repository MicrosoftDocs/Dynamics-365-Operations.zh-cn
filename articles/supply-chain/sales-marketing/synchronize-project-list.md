---
title: 将项目列表从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的项目的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: b5aeb4c3925994d7488e8e113e88b9d06ee6b350
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "312500"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="cbd0c-103">将项目列表从 Finance and Operations 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="cbd0c-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cbd0c-104">此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的项目的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cbd0c-105">[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cbd0c-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cbd0c-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="cbd0c-106">Templates and tasks</span></span>
<span data-ttu-id="cbd0c-107">以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的项目的同步。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="cbd0c-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-108">**Template in Data integration**</span></span>
- <span data-ttu-id="cbd0c-109">项目（Finance and Operations 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="cbd0c-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="cbd0c-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="cbd0c-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="cbd0c-111">项目</span><span class="sxs-lookup"><span data-stu-id="cbd0c-111">Projects</span></span>

<span data-ttu-id="cbd0c-112">在发生项目列表同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="cbd0c-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="cbd0c-113">帐户（Sales 到 Finance and Operations）</span><span class="sxs-lookup"><span data-stu-id="cbd0c-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="cbd0c-114">实体集</span><span class="sxs-lookup"><span data-stu-id="cbd0c-114">Entity set</span></span>
| <span data-ttu-id="cbd0c-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="cbd0c-115">Field Service</span></span>           | <span data-ttu-id="cbd0c-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbd0c-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="cbd0c-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="cbd0c-117">msdynce_externalprojects</span></span> | <span data-ttu-id="cbd0c-118">项目</span><span class="sxs-lookup"><span data-stu-id="cbd0c-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="cbd0c-119">实体流</span><span class="sxs-lookup"><span data-stu-id="cbd0c-119">Entity flow</span></span>
<span data-ttu-id="cbd0c-120">项目在 Finance and Operations 中创建。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="cbd0c-121">将**项目类型**设置为**时间和材料**并将**项目阶段**设置为**进行中**的项目将同步到 Field Service 中的**外部项目**实体，包括项目编号、项目名称、项目阶段和客户帐户信息。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="cbd0c-122">**外部项目**列表用于将 Field service 工作订单与 Finance and Operations 项目匹配。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cbd0c-123">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="cbd0c-123">Field Service CRM solution</span></span>
<span data-ttu-id="cbd0c-124">**外部项目**实体从 Finance and Operations 获取所有项目。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="cbd0c-125">**外部项目**字段已添加到**工作订单**实体。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="cbd0c-126">此字段是查找字段，因此，通过标记项目的工作订单，销售订单将被连接到 Finance and Operations 内的一个项目。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="cbd0c-127">**系统状态**将**打开 - 正在进行(690,970,000)** 更改为更高状态后，**外部项目**字段将被锁定，您将无法再添加、删除或更改值。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="cbd0c-128">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="cbd0c-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="cbd0c-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cbd0c-129">Finance and Operations</span></span>
<span data-ttu-id="cbd0c-130">为数据实体项目启用更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="cbd0c-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cbd0c-131">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="cbd0c-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="cbd0c-132">项目（Finance and Operations 到 Field Service）：项目</span><span class="sxs-lookup"><span data-stu-id="cbd0c-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="cbd0c-133">[![数据集成中的模板映射](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="cbd0c-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
