---
title: 资产服务级别
description: 本主题介绍资产管理中的资产服务级别。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35e7a55b1ba230be6bb72b20fcd805ea061b648e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216566"
---
# <a name="asset-service-levels"></a><span data-ttu-id="485f6-103">资产服务级别</span><span class="sxs-lookup"><span data-stu-id="485f6-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="485f6-104">本主题介绍资产管理中的资产服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="485f6-105">资产服务级别与资产关联，并转化为维护请求和工作订单。</span><span class="sxs-lookup"><span data-stu-id="485f6-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="485f6-106">用于在工作订单排产期间计算工作订单的优先级。</span><span class="sxs-lookup"><span data-stu-id="485f6-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="485f6-107">如果需要更改资产服务级别，则可更改。</span><span class="sxs-lookup"><span data-stu-id="485f6-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="485f6-108">有关与计算工作订单排产的等级评分关联的设置的详细信息，请参阅[资产管理参数](../setup-for-objects/enterprise-asset-management-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="485f6-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="485f6-109">必须为资产服务级别设置至少一个默认记录。</span><span class="sxs-lookup"><span data-stu-id="485f6-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="485f6-110">如果工作订单排产期间未找到其他匹配项，则使用默认记录。</span><span class="sxs-lookup"><span data-stu-id="485f6-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="485f6-111">**示例 1：** 未找到其他匹配项时使用的默认服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="485f6-112">在此记录中，仅选择一个服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="485f6-113">**示例 2：** 用于为沃尔沃卡车引擎安排作业的高服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="485f6-114">在此记录中，选择相关资产类型（如**卡车引擎**）、制造商（**沃尔沃**）和服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="485f6-115">设置资产服务级别</span><span class="sxs-lookup"><span data-stu-id="485f6-115">Set up asset service levels</span></span>

1. <span data-ttu-id="485f6-116">选择**资产管理** \> **设置** \> **资产服务级别**。</span><span class="sxs-lookup"><span data-stu-id="485f6-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="485f6-117">选择**新建**创建记录。</span><span class="sxs-lookup"><span data-stu-id="485f6-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="485f6-118">根据资产服务级别所需默认级别，在**功能位置**、**资产类型**、**制造商**、**模型**、**资产**、**工作订单类型**和**服务级别**字段中进行相关选择。</span><span class="sxs-lookup"><span data-stu-id="485f6-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="485f6-119">将资产服务级别用于维护请求和工作订单时，资产管理检查所有资产服务级别记录以查找可能的匹配项。</span><span class="sxs-lookup"><span data-stu-id="485f6-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="485f6-120">始终先检查最具体的组合。</span><span class="sxs-lookup"><span data-stu-id="485f6-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="485f6-121">换句话说，资产管理首先会检查**工作订单类型**字段的匹配项。</span><span class="sxs-lookup"><span data-stu-id="485f6-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="485f6-122">如果未找到匹配项，将检查**资产**字段的匹配项，以此类推。</span><span class="sxs-lookup"><span data-stu-id="485f6-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="485f6-123">如**资产服务级别**页面布局中显示，此行为表示为了找到最具体的组合，资产管理从右到左检查每个记录以查找匹配项。</span><span class="sxs-lookup"><span data-stu-id="485f6-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="485f6-124">如果未找到匹配项，将使用这些字段中无可供选择的内容的默认记录。</span><span class="sxs-lookup"><span data-stu-id="485f6-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="485f6-125">在**服务级别**字段中，选择一个数字，用于指示服务级别（优先级）。</span><span class="sxs-lookup"><span data-stu-id="485f6-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="485f6-126">如果在**资产服务级别**页中更改已用于工作订单的资产服务级别记录，则不会相应更改维护请求和工作订单的服务级别。</span><span class="sxs-lookup"><span data-stu-id="485f6-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>
