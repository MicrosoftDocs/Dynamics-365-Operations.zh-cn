---
title: 资产制造商和模型
description: 本主题介绍如何在资产管理中设置资产制造商和相关模型。
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e20ccf16bc751898b239214771821fd2872638d1
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783103"
---
# <a name="asset-manufacturers-and-models"></a><span data-ttu-id="741db-103">资产制造商和模型</span><span class="sxs-lookup"><span data-stu-id="741db-103">Asset manufacturers and models</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="741db-104">本主题介绍如何在资产管理中设置资产制造商和相关模型。</span><span class="sxs-lookup"><span data-stu-id="741db-104">This topic explains how to set up asset manufacturers and related models in Asset Management.</span></span> <span data-ttu-id="741db-105">可以将模型与资产类型关联。</span><span class="sxs-lookup"><span data-stu-id="741db-105">Models can be related to asset types.</span></span>

## <a name="set-up-product-model-relations"></a><span data-ttu-id="741db-106">设置产品-模型关系</span><span class="sxs-lookup"><span data-stu-id="741db-106">Set up product-model relations</span></span>

1. <span data-ttu-id="741db-107">选择**资产管理** \> **设置** \> **资产** \> **制造商和模型**。</span><span class="sxs-lookup"><span data-stu-id="741db-107">Select **Asset management** \> **Setup** \> **Assets** \> **Manufacturer and model**.</span></span>
2. <span data-ttu-id="741db-108">选择**新建**以创建新产品。</span><span class="sxs-lookup"><span data-stu-id="741db-108">Select **New** to create a new product.</span></span>
3. <span data-ttu-id="741db-109">在**制造商**字段中，输入资产制造商的名称。</span><span class="sxs-lookup"><span data-stu-id="741db-109">In the **Manufacturer** field, enter a name for the asset manufacturer.</span></span>
4. <span data-ttu-id="741db-110">在**描述**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="741db-110">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="741db-111">在**模型**快速选项卡上，选择**添加**创建应该与资产制造商关联的资产模型。</span><span class="sxs-lookup"><span data-stu-id="741db-111">On the **Models** FastTab, select **Add** to create an asset model that should be related to the asset manufacturer.</span></span>
6. <span data-ttu-id="741db-112">在**模型**字段中，输入资产模型的名称。</span><span class="sxs-lookup"><span data-stu-id="741db-112">In the **Model** field, enter a name for the asset model.</span></span>
7. <span data-ttu-id="741db-113">在**描述**字段中，输入描述。</span><span class="sxs-lookup"><span data-stu-id="741db-113">In the **Description** field, enter a description.</span></span>
8. <span data-ttu-id="741db-114">在**资产类型**字段中，选择制造商模型应关联的资产类型。</span><span class="sxs-lookup"><span data-stu-id="741db-114">In the **Asset type** field, select the asset type that the manufacturer model should be related to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="741db-115">也可以在**资产类型**查找中为资产类型、制造商和模型设置关系。</span><span class="sxs-lookup"><span data-stu-id="741db-115">You can also set up relations for asset types, manufacturers, and models in the **Asset types** lookup.</span></span> <span data-ttu-id="741db-116">有关详细信息，请参阅[创建资产类型](../setup-for-objects/object-types.md)。</span><span class="sxs-lookup"><span data-stu-id="741db-116">For more information, see [Create asset type](../setup-for-objects/object-types.md).</span></span>

    <span data-ttu-id="741db-117">**详细信息**快速选项卡中的**模型**字段显示为所选资产制造商设置的资产模型数量。</span><span class="sxs-lookup"><span data-stu-id="741db-117">In the **Details** FastTab, the **Models** field shows the number of asset models that are set up on the selected asset manufacturer.</span></span> <span data-ttu-id="741db-118">**资产**字段显示使用所选制造商的资产的数量。</span><span class="sxs-lookup"><span data-stu-id="741db-118">The **Assets** field shows the number of assets that are using the selected manufacturer.</span></span>
    
    <span data-ttu-id="741db-119">**资产**字段显示使用所选制造商模型的对象的数量。</span><span class="sxs-lookup"><span data-stu-id="741db-119">The **Assets** field shows the number of objects that are using the manufacturer model.</span></span>

> [!NOTE]
> <span data-ttu-id="741db-120">资产类型可以没有资产制造商模型关系，可以与一个资产制造商模型关联，也可以与多个资产制造商模型关联。</span><span class="sxs-lookup"><span data-stu-id="741db-120">An asset type can have no asset manufacturer model relations, it can be related to one asset manufacturer model, or it can be related multiple asset manufacturer models.</span></span> <span data-ttu-id="741db-121">如果一个资产类型与至少一个制造商模型关联，则只能在其中可设置资产类型、制造商和模型组合的“资产管理”页面中选择在**制造商模型**查找中设置的组合。</span><span class="sxs-lookup"><span data-stu-id="741db-121">If an asset type is related to at least one manufacturer model, only the combinations that are set up in the **Manufacturer model** lookup can be selected on those Asset Management pages where a combination of an asset type, manufacturer, and model can be set up.</span></span> <span data-ttu-id="741db-122">这些页面包括**所有资产**、**资产服务级别**、**作业类型默认值**和**维护预算行**。</span><span class="sxs-lookup"><span data-stu-id="741db-122">These pages include **All assets**, **Asset service levels**, **Job type defaults**, and **Maintenance budget lines**.</span></span> <span data-ttu-id="741db-123">如果某些资产类型不与任何制造商模型关联，则页面中仅显示这些资产类型，以及也不与资产类型关联的制造商模型。</span><span class="sxs-lookup"><span data-stu-id="741db-123">If some asset types aren't related to any manufacturer model, only those asset types, and manufacturer models that also have no relation to asset types, are shown on the pages.</span></span>

## <a name="select-a-manufacturer-and-model-on-an-object"></a><span data-ttu-id="741db-124">为对象选择制造商和模型</span><span class="sxs-lookup"><span data-stu-id="741db-124">Select a manufacturer and model on an object</span></span>

1. <span data-ttu-id="741db-125">选择**资产管理** \> **常用** \> **资产** \> **所有资产**。</span><span class="sxs-lookup"><span data-stu-id="741db-125">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="741db-126">在**资产**列中，选择资产的链接。</span><span class="sxs-lookup"><span data-stu-id="741db-126">In the **Asset** column, select the link for the asset.</span></span> <span data-ttu-id="741db-127">将显示**详细信息**页。</span><span class="sxs-lookup"><span data-stu-id="741db-127">The **Details** page appears.</span></span>
3. <span data-ttu-id="741db-128">选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="741db-128">Select **Edit**.</span></span>
4. <span data-ttu-id="741db-129">在**常规**快速选项卡上的**制造商**和**模型**字段中选择值。</span><span class="sxs-lookup"><span data-stu-id="741db-129">On the **General** FastTab, select values in the **Manufacturer** and **Model** fields.</span></span>
