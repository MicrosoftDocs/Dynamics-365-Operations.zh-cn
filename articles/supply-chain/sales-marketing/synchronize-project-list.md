---
title: 将项目列表从Supply Chain Management 同步到 Field Service
description: 此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的项目的模板和基础任务。
author: ChristianRytt
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5cb7f8b9a3107a7787c787ace71ab574457b1646
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828482"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="166fe-103">将项目列表从Supply Chain Management 同步到 Field Service</span><span class="sxs-lookup"><span data-stu-id="166fe-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="166fe-104">此主题介绍用于同步 Dynamics 365 Supply Chain Management 与 Dynamics 365 Field Service 的项目的模板和基础任务。</span><span class="sxs-lookup"><span data-stu-id="166fe-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="166fe-105">[![Supply Chain Management 与 Field Service 之间的业务流程同步](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="166fe-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="166fe-106">模板和任务</span><span class="sxs-lookup"><span data-stu-id="166fe-106">Templates and tasks</span></span>
<span data-ttu-id="166fe-107">以下模板和基础任务用于运行项目从 Supply Chain Management 到 Field Service 的同步。</span><span class="sxs-lookup"><span data-stu-id="166fe-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="166fe-108">**数据集成中的模板**</span><span class="sxs-lookup"><span data-stu-id="166fe-108">**Template in Data integration**</span></span>
- <span data-ttu-id="166fe-109">项目（Supply Chain Management 到 Field Service）</span><span class="sxs-lookup"><span data-stu-id="166fe-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="166fe-110">**数据集成项目中的任务**</span><span class="sxs-lookup"><span data-stu-id="166fe-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="166fe-111">项目</span><span class="sxs-lookup"><span data-stu-id="166fe-111">Projects</span></span>

<span data-ttu-id="166fe-112">在发生项目列表同步前，需要执行以下同步任务：</span><span class="sxs-lookup"><span data-stu-id="166fe-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="166fe-113">科目（Sales 到 Supply Chain Management）</span><span class="sxs-lookup"><span data-stu-id="166fe-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="166fe-114">实体集</span><span class="sxs-lookup"><span data-stu-id="166fe-114">Entity set</span></span>
| <span data-ttu-id="166fe-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="166fe-115">Field Service</span></span>           | <span data-ttu-id="166fe-116">供应链管理</span><span class="sxs-lookup"><span data-stu-id="166fe-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="166fe-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="166fe-117">msdynce_externalprojects</span></span> | <span data-ttu-id="166fe-118">项目</span><span class="sxs-lookup"><span data-stu-id="166fe-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="166fe-119">实体流</span><span class="sxs-lookup"><span data-stu-id="166fe-119">Entity flow</span></span>
<span data-ttu-id="166fe-120">项目在 Supply Chain Management 中创建。</span><span class="sxs-lookup"><span data-stu-id="166fe-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="166fe-121">将 **项目类型** 设置为 **时间和材料** 并将 **项目阶段** 设置为 **进行中** 的项目将同步到 Field Service 中的 **外部项目** 实体，包括项目编号、项目名称、项目阶段和客户帐户信息。</span><span class="sxs-lookup"><span data-stu-id="166fe-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="166fe-122">**外部项目** 列表用于将 Field service 工作订单与 Supply Chain Management 项目匹配。</span><span class="sxs-lookup"><span data-stu-id="166fe-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="166fe-123">Field Service CRM 解决方案</span><span class="sxs-lookup"><span data-stu-id="166fe-123">Field Service CRM solution</span></span>
<span data-ttu-id="166fe-124">**外部项目** 实体从 Supply Chain Management 获取所有项目。</span><span class="sxs-lookup"><span data-stu-id="166fe-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="166fe-125">**外部项目** 字段已添加到 **工作订单** 实体。</span><span class="sxs-lookup"><span data-stu-id="166fe-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="166fe-126">此备份字段是标记项目的工作订单的查找和购买，销售订单随后将被连接到 Supply Chain Management 内的一个项目。</span><span class="sxs-lookup"><span data-stu-id="166fe-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="166fe-127">**系统状态** 将 **打开 - 正在进行(690,970,000)** 更改为更高状态后，**外部项目** 字段将被锁定，您将无法再添加、删除或更改值。</span><span class="sxs-lookup"><span data-stu-id="166fe-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="166fe-128">先决条件和映射设置</span><span class="sxs-lookup"><span data-stu-id="166fe-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="166fe-129">供应链管理</span><span class="sxs-lookup"><span data-stu-id="166fe-129">Supply Chain Management</span></span>
<span data-ttu-id="166fe-130">为数据实体项目启用更改跟踪。</span><span class="sxs-lookup"><span data-stu-id="166fe-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="166fe-131">数据集成中的模板映射</span><span class="sxs-lookup"><span data-stu-id="166fe-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="166fe-132">项目（Supply Chain Management 到 Field Service）：项目</span><span class="sxs-lookup"><span data-stu-id="166fe-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="166fe-133">[![数据集成中的模板映射](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="166fe-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]