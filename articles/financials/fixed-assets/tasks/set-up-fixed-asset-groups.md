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
ms.openlocfilehash: 246502f66c0cfcd4b4ed3c4b9f2ae616e71a1c50
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867527"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="f0682-103">设置固定资产组</span><span class="sxs-lookup"><span data-stu-id="f0682-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0682-104">此主题介绍如何创建新的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="f0682-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="f0682-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="f0682-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f0682-106">在导航窗格中，转到**模块 > 固定资产 > 设置 > 固定资产组**。</span><span class="sxs-lookup"><span data-stu-id="f0682-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="f0682-107">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="f0682-107">Select **New**.</span></span>
3. <span data-ttu-id="f0682-108">在**固定资产组**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0682-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="f0682-109">在**名称**字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="f0682-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="f0682-110">**固定资产**组为固定资产自动生成编号及编号规则代码将覆盖固定资产参数上的设置。</span><span class="sxs-lookup"><span data-stu-id="f0682-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="f0682-111">如果固定资产组中的资产具有与其他组不同的编号，您可以在此进行更改。</span><span class="sxs-lookup"><span data-stu-id="f0682-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="f0682-112">选择**帐簿**。</span><span class="sxs-lookup"><span data-stu-id="f0682-112">Select **Books**.</span></span>
6. <span data-ttu-id="f0682-113">在**帐簿**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f0682-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="f0682-114">如果将**计算折旧**字段设置为**是**，资产帐簿将包含于折旧方案中。</span><span class="sxs-lookup"><span data-stu-id="f0682-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="f0682-115">如果**计算折旧**设置为**否**，资产将不自动折旧。</span><span class="sxs-lookup"><span data-stu-id="f0682-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="f0682-116">设置资产的使用年限，用年表示。</span><span class="sxs-lookup"><span data-stu-id="f0682-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="f0682-117">请注意，在设置使用年限后，计算**折旧期间**字段值。</span><span class="sxs-lookup"><span data-stu-id="f0682-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="f0682-118">在**折旧惯例**字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="f0682-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="f0682-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="f0682-119">Close the page.</span></span>

