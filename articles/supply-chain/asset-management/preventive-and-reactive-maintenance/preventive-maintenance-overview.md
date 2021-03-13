---
title: 预防性维护概述
description: 本主题介绍资产管理中的预防性维护。
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 36a70a3e60566fd8048ad404e0c391d898053a0a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016720"
---
# <a name="preventive-maintenance-overview"></a><span data-ttu-id="a500d-103">预防性维护概述</span><span class="sxs-lookup"><span data-stu-id="a500d-103">Preventive maintenance overview</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a500d-104">本主题介绍资产管理中的预防性维护。</span><span class="sxs-lookup"><span data-stu-id="a500d-104">This topic explains preventive maintenance in Asset Management.</span></span> <span data-ttu-id="a500d-105">预防性维护是一门涉及计划的维护作业（如常规服务、校准和检验）的学科。</span><span class="sxs-lookup"><span data-stu-id="a500d-105">Preventive maintenance is a discipline involving planned maintenance jobs, for example, regular service, calibration, and inspections.</span></span> <span data-ttu-id="a500d-106">在 **资产管理** 中，可创建维护安排，并为其设置资产和功能位置。</span><span class="sxs-lookup"><span data-stu-id="a500d-106">In **Asset Management**, you can create maintenance plans and set them up on assets and functional locations.</span></span> <span data-ttu-id="a500d-107">也可以为功能位置设置维护阶段。</span><span class="sxs-lookup"><span data-stu-id="a500d-107">You can also set up maintenance rounds on functional locations.</span></span> <span data-ttu-id="a500d-108">无论资产安装在何处，其维护安排均有效。</span><span class="sxs-lookup"><span data-stu-id="a500d-108">Maintenance plans on assets are active regardless of where the asset is installed.</span></span> <span data-ttu-id="a500d-109">功能位置的维护安排和维护阶段对该位置当前安装的资产有效。</span><span class="sxs-lookup"><span data-stu-id="a500d-109">Maintenance plans and maintenance rounds on functional location are active for the assets currently installed at the location.</span></span> <span data-ttu-id="a500d-110">可以不为资产设置维护安排，或部位功能位置设置维护阶段，而是创建其中包含需要按照相同工作例程对其执行相关类型的维护作业的多个资产。</span><span class="sxs-lookup"><span data-stu-id="a500d-110">Instead of setting up maintenance plans on assets, or setting up maintenance rounds on functional locations, you can create maintenance rounds that include multiple assets on which you need to perform related types of maintenance jobs in the same work routine.</span></span> <span data-ttu-id="a500d-111">从资产创建维护阶段，而不是为功能位置创建，这意味着可以为一个维护阶段选择多个不是安装在同一个功能位置的资产。</span><span class="sxs-lookup"><span data-stu-id="a500d-111">Maintenance rounds created from assets - instead of created on functional locations - means that you can select a number of assets for one maintenance round, which are not installed on the same functional location.</span></span>

<span data-ttu-id="a500d-112">维护安排用于对单个资产执行的预防性和反应性维护。</span><span class="sxs-lookup"><span data-stu-id="a500d-112">Maintenance plans are used for preventive and reactive maintenance on individual assets.</span></span> <span data-ttu-id="a500d-113">维护阶段用于对一组或一套资产执行的预防性维护。</span><span class="sxs-lookup"><span data-stu-id="a500d-113">Maintenance rounds are used for preventive maintenance on a group or a set of assets.</span></span> <span data-ttu-id="a500d-114">维护安排和维护阶段用于生成工作订单方案。</span><span class="sxs-lookup"><span data-stu-id="a500d-114">Maintenance plans and maintenance rounds are used for generating work order proposals.</span></span> <span data-ttu-id="a500d-115">工作订单方案保存为维护安排行，可捆绑在一起并转化为工作订单。</span><span class="sxs-lookup"><span data-stu-id="a500d-115">The work order proposals are saved as maintenance schedule lines, which can be bundled and converted into work orders.</span></span>

<span data-ttu-id="a500d-116">下图提供从创建维护安排和维护阶段到基于这些维护安排和维护阶段为资产创建工作订单的工作流的概览。</span><span class="sxs-lookup"><span data-stu-id="a500d-116">The following illustration provides an overview of the work flow from creating maintenance plans and maintenance rounds to creating work orders for assets, based on those maintenance plans and maintenance rounds.</span></span>

![图 1](media/01-preventive-maintenance.png)

