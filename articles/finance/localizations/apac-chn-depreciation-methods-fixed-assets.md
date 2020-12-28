---
title: 中国的固定资产折旧法
description: 此主题描述为中国法人设置的折旧法。
author: ShylaThompson
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265244
ms.search.region: China (PRC)
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7f7a615663676b02b02c5dd7bd3bfae495ca09ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409747"
---
# <a name="fixed-assets-depreciation-methods-for-china"></a><span data-ttu-id="1da01-103">中国的固定资产折旧法</span><span class="sxs-lookup"><span data-stu-id="1da01-103">Fixed assets depreciation methods for China</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1da01-104">此主题描述为中国法人设置的折旧法。</span><span class="sxs-lookup"><span data-stu-id="1da01-104">This topic describes the depreciation method set up for legal entities in China.</span></span>

<span data-ttu-id="1da01-105">年数总和折旧法 (SYD) 是一种基于以下假设的加速折旧技术：资产越新，生产率越高，如果变旧，生产率随之下降。</span><span class="sxs-lookup"><span data-stu-id="1da01-105">The sum of the years' digits method of depreciation (SYD) is one of the accelerated depreciation techniques that is based on the assumption that assets are generally more productive when they are new and their productivity decreases as they become old.</span></span> <span data-ttu-id="1da01-106">SYD 法的折旧计算公式为：</span><span class="sxs-lookup"><span data-stu-id="1da01-106">The formula to calculate depreciation under SYD method is:</span></span>

> <span data-ttu-id="1da01-107">*SYD 折旧 = 折旧基数 × (剩余使用寿命/年数总和法)*</span><span class="sxs-lookup"><span data-stu-id="1da01-107">*SYD Depreciation = Depreciable base × (Remaining useful life/Sum of the  years digits)*</span></span>

<span data-ttu-id="1da01-108">若要创建折旧模板：</span><span class="sxs-lookup"><span data-stu-id="1da01-108">To create a depreciation profile:</span></span>

1. <span data-ttu-id="1da01-109">在 **固定资产参数** 页上，选择  **SYDM 和 DRBM** 折旧法。</span><span class="sxs-lookup"><span data-stu-id="1da01-109">On the **Fixed assets parameters** page, select the **SYDM and DRBM** depreciation methods.</span></span>
2. <span data-ttu-id="1da01-110">创建一个新折旧模板。</span><span class="sxs-lookup"><span data-stu-id="1da01-110">Create a new depreciation profile.</span></span> <span data-ttu-id="1da01-111">使用 **年数总和法** 或 **双倍余额递减法**。</span><span class="sxs-lookup"><span data-stu-id="1da01-111">Use the method of either **Sum year digits** or **Double reducing balance**.</span></span>
3. <span data-ttu-id="1da01-112">为该折旧法创建一个帐簿，请使用  **年数总和法** 或 **双倍余额递减法**。</span><span class="sxs-lookup"><span data-stu-id="1da01-112">Create a book for the depreciation method, use either  **Sum year digits** or **Double reducing balance**.</span></span>

<span data-ttu-id="1da01-113">有关详细信息，请参阅[设置固定资产折旧分摊](./tasks/fixed-asset-depreciation-allocation.md)。</span><span class="sxs-lookup"><span data-stu-id="1da01-113">For more information, see [Setup fixed asset depreciation allocation](./tasks/fixed-asset-depreciation-allocation.md).</span></span>


