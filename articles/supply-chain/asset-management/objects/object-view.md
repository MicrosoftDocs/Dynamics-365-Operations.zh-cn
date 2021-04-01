---
title: 资产视图
description: 本主题介绍资产管理中的资产视图。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a770831c564d44de534642cc462b27b0818e9a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253102"
---
# <a name="asset-view"></a><span data-ttu-id="6cf1d-103">资产视图</span><span class="sxs-lookup"><span data-stu-id="6cf1d-103">Asset view</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="6cf1d-104">本主题介绍资产管理中的资产视图。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-104">This topic describes the asset view in Asset Management.</span></span> <span data-ttu-id="6cf1d-105">**资产视图** 页以树视图显示有效资产和功能位置。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-105">The **Asset view** page shows active assets and functional locations in a tree view.</span></span> <span data-ttu-id="6cf1d-106">因此，您可以轻松获取资产与功能位置之间的关系的概览。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-106">Therefore, you can easily get an overview of asset relations to functional locations.</span></span> <span data-ttu-id="6cf1d-107">此外，还可以查看有关功能位置、资产和相关物料清单 (BOM) 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-107">Additionally, you can view detailed information about functional locations, assets, and related bills of materials (BOMs).</span></span> <span data-ttu-id="6cf1d-108">还可以快速获取与资产有关的有效维护请求和工作订单的概览。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-108">You can also get a quick overview of active maintenance requests and work orders that are related to an asset.</span></span>

1. <span data-ttu-id="6cf1d-109">选择 **资产管理** \> **常用** \> **资产** \> **资产视图**。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-109">Select **Asset management** \> **Common** \> **Assets** \> **Asset view**.</span></span>
2. <span data-ttu-id="6cf1d-110">若要更改页面上显示的视图，请在 **视图** 字段中选择一个新值。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-110">To change the view that is shown on the page, select a new value in the **View** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6cf1d-111">打开 **资产视图** 页时显示的默认视图取决于 **资产管理参数** 页（**资产管理** \> **设置** \> **资产管理参数**）**资产** 选项卡上 **视图** 字段中选择的值。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-111">The default view that is shown when you open the **Asset view** page depends on the value that is selected in the **View** field on the **Assets** tab of the **Asset management parameters** page (**Asset management** \> **Setup** \> **Asset management parameters**).</span></span>

<span data-ttu-id="6cf1d-112">页面右侧的快速选项卡显示所选视图的详细信息。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-112">On the right side of the page, FastTabs shows details of the selected view.</span></span>

<span data-ttu-id="6cf1d-113">树视图上方显示的痕迹显示树视图中当前选择的内容。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-113">The breadcrumb trail that appears above the tree view shows the current selection in the tree view.</span></span> <span data-ttu-id="6cf1d-114">此痕迹使用以下格式：</span><span class="sxs-lookup"><span data-stu-id="6cf1d-114">This breadcrumb trail uses the following format:</span></span>

<span data-ttu-id="6cf1d-115">功能位置 ID/功能位置 ID（如果有多个功能位置）\> 资产 ID/资产 ID（如果有多个资产）- 物料编号。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-115">Functional location ID / Functional location ID (if there is more than one functional location) \> Asset ID / Asset ID (if there is more than one asset) - Item number.</span></span>

<span data-ttu-id="6cf1d-116">如果已经在树视图中选择了一个资产，则可选择 **有效请求** 或 **有效工作订单** 查看与资产有关的维护请求或工作订单。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-116">If you've selected an asset in the tree view, you can select **Active requests** or **Active work orders** to view the maintenance requests or work orders that are related to the asset.</span></span> <span data-ttu-id="6cf1d-117">也可以选择 **打开** \> **功能位置**、**资产** 或 **资产 BOM** 以打开相关视图。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-117">You can also select **Open** \> **Functional location**, **Asset**, or **Asset BOM** to open the related view.</span></span>

<span data-ttu-id="6cf1d-118">可在其中选择资产的任何资产查找中也提供可在 **视图** 字段中选择的 **资产功能位置** 选项。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-118">The **Asset functional locations** option that you can select in the **View** field is also available in any asset lookup where you can select an asset.</span></span> <span data-ttu-id="6cf1d-119">例如，**资产视图** 选项卡上将显示树视图，可在其中[创建资产](../objects/create-an-object.md)，创建维护请求或创建工作订单。</span><span class="sxs-lookup"><span data-stu-id="6cf1d-119">The tree view is shown on an **Asset view** tab, for example, where you [create an asset](../objects/create-an-object.md), create a maintenance request, or create a work order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]