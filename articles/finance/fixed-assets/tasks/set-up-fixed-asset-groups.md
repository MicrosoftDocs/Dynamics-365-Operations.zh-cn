---
title: 设置固定资产组
description: 此主题介绍如何创建新的固定资产组。
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bcb78158afbf7bb0e9b83b35e37b1532a7c6283
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440606"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="11318-103">设置固定资产组</span><span class="sxs-lookup"><span data-stu-id="11318-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11318-104">此主题介绍如何创建新的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="11318-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="11318-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="11318-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="11318-106">在导航窗格中，转到 **模块 > 固定资产 > 设置 > 固定资产组**。</span><span class="sxs-lookup"><span data-stu-id="11318-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="11318-107">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="11318-107">Select **New**.</span></span>
3. <span data-ttu-id="11318-108">在 **固定资产组** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="11318-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="11318-109">在 **名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="11318-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="11318-110">**固定资产** 组为固定资产自动生成编号及编号规则代码将覆盖固定资产参数上的设置。</span><span class="sxs-lookup"><span data-stu-id="11318-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="11318-111">如果固定资产组中的资产具有与其他组不同的编号，您可以在此进行更改。</span><span class="sxs-lookup"><span data-stu-id="11318-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="11318-112">选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="11318-112">Select **Books**.</span></span>
6. <span data-ttu-id="11318-113">在 **帐簿** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="11318-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="11318-114">如果将 **计算折旧** 字段设置为 **是**，资产帐簿将包含于折旧方案中。</span><span class="sxs-lookup"><span data-stu-id="11318-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="11318-115">如果 **计算折旧** 设置为 **否**，资产将不自动折旧。</span><span class="sxs-lookup"><span data-stu-id="11318-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="11318-116">设置资产的使用年限，用年表示。</span><span class="sxs-lookup"><span data-stu-id="11318-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="11318-117">请注意，在设置使用年限后，计算 **折旧期间** 字段值。</span><span class="sxs-lookup"><span data-stu-id="11318-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="11318-118">在 **折旧惯例** 字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="11318-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="11318-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="11318-119">Close the page.</span></span>

