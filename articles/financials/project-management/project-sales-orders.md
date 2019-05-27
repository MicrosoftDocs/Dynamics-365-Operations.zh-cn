---
title: 项目销售订单
description: 本主题介绍如何为时间和材料项目创建基于项目的销售订单。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
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
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529894"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="87fb8-103">时间和材料项目的项目销售订单</span><span class="sxs-lookup"><span data-stu-id="87fb8-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="87fb8-104">此主题描述如何为项目创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="87fb8-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="87fb8-105">只能为类型为**时间和材料**的项目创建销售订单。</span><span class="sxs-lookup"><span data-stu-id="87fb8-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="87fb8-106">如果时间和材料项目的项目合同中有多个融资来源，则必须启用**项目管理与核算参数**页面上的**允许项目的销售订单具有多个融资来源**参数。</span><span class="sxs-lookup"><span data-stu-id="87fb8-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="87fb8-107">从应用程序版本 10.0.2 及更高版本开始，支持具有多个融资来源的项目销售订单。</span><span class="sxs-lookup"><span data-stu-id="87fb8-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="87fb8-108">2020 年 4 月发布波次中将删除用于启用对具有多个融资来源的项目销售订单的支持的参数，之后将始终启用此功能。</span><span class="sxs-lookup"><span data-stu-id="87fb8-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="87fb8-109">可通过两种方法创建基于项目的销售订单：</span><span class="sxs-lookup"><span data-stu-id="87fb8-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="87fb8-110">转到项目本身。</span><span class="sxs-lookup"><span data-stu-id="87fb8-110">Go to the project itself.</span></span> <span data-ttu-id="87fb8-111">在操作窗格上，选择**管理 > 物料任务 > 销售订单**。</span><span class="sxs-lookup"><span data-stu-id="87fb8-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="87fb8-112">项目信息默认为项目的销售订单。</span><span class="sxs-lookup"><span data-stu-id="87fb8-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="87fb8-113">如果项目合同有多个融资来源，您将需要选择融资来源才能为销售订单设置客户。</span><span class="sxs-lookup"><span data-stu-id="87fb8-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="87fb8-114">如果项目只有一个融资来源，将自动设置客户。</span><span class="sxs-lookup"><span data-stu-id="87fb8-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="87fb8-115">转到**所有销售订单**列表页并创建一个新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="87fb8-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="87fb8-116">您将需要为销售订单选择项目。</span><span class="sxs-lookup"><span data-stu-id="87fb8-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="87fb8-117">选择项目之后，将从融资来源设置客户，而如果项目合同有多个融资来源，则您将需要选择此融资来源。</span><span class="sxs-lookup"><span data-stu-id="87fb8-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

