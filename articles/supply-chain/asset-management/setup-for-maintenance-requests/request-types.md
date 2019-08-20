---
title: 维护请求类型
description: 本主题说明如何在资产管理中设置维护请求类型。
author: josaw1
manager: AnnBe
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 19d529df6c8aab036de59502b4f14101e1a07707
ms.sourcegitcommit: 2c73749779274e0b0abbcb4041bbc1df0fb6d6e4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/26/2019
ms.locfileid: "1790469"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="b8a4f-103">维护请求类型</span><span class="sxs-lookup"><span data-stu-id="b8a4f-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b8a4f-104">维护请求类型用于为维护请求分类。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="b8a4f-105">例如，您可能有与预防性维护和修复性维护有关的维护请求。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="b8a4f-106">也可能有用于管理资产维修（仓库维修）的特殊维护请求类型。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="b8a4f-107">维护请求类型定义与维护请求生命周期状态组（维护生命周期模型）之间的隶属关系。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="b8a4f-108">维护请求生命周期模型定义可为维护请求设置的生命周期状态。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="b8a4f-109">（维护请求生命周期状态的示例包括**已创建**、**活动**和**已结束**。）</span><span class="sxs-lookup"><span data-stu-id="b8a4f-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="b8a4f-110">选择**资产管理** \> **设置** \> **维护请求** \> **维护请求类型**。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="b8a4f-111">选择**新建**创建维护请求类型。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="b8a4f-112">在**维护请求类型**字段中，输入维护请求类型的 ID。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="b8a4f-113">在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="b8a4f-114">在**常规**快速选项卡上的**维护请求生命周期模型**字段中，选择一个维护请求生命周期模型。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="b8a4f-115">在**工作订单类型**字段中，选择一个工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="b8a4f-116">维护请求转化为工作订单之后，该工作订单将自动获取与维护请求类型关联的工作订单类型。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="b8a4f-117">下图显示**维护请求类型**页的示例。</span><span class="sxs-lookup"><span data-stu-id="b8a4f-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![图 1](media/07-setup-for-requests.png)
