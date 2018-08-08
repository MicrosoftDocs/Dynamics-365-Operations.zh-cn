--- 
title: "设置固定资产组"
description: "此过程显示如何创建新的固定资产组。"
author: saraschi2
manager: AnnBe
ms.date: 02/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d6a4468a05e3e9560c52b9b88071ec5893610c24
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="0b442-103">设置固定资产组</span><span class="sxs-lookup"><span data-stu-id="0b442-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0b442-104">此过程显示如何创建新的固定资产组。</span><span class="sxs-lookup"><span data-stu-id="0b442-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="0b442-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="0b442-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="0b442-106">转到“固定资产”>“设置”>“固定资产组”。</span><span class="sxs-lookup"><span data-stu-id="0b442-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="0b442-107">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0b442-107">Click New.</span></span>
3. <span data-ttu-id="0b442-108">在“固定资产组”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0b442-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="0b442-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="0b442-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0b442-110">固定资产组为固定资产自动生成编号及编号规则代码将覆盖固定资产参数上的设置。</span><span class="sxs-lookup"><span data-stu-id="0b442-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="0b442-111">如果固定资产组中的资产具有与其他组不同的编号，您可以在此进行更改。</span><span class="sxs-lookup"><span data-stu-id="0b442-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="0b442-112">单击“帐簿”。</span><span class="sxs-lookup"><span data-stu-id="0b442-112">Click Books.</span></span>
6. <span data-ttu-id="0b442-113">在“帐簿”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0b442-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="0b442-114">如果将“计算折旧”字段设置为“是”，资产帐簿将包含于折旧方案中。</span><span class="sxs-lookup"><span data-stu-id="0b442-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="0b442-115">如果“计算折旧”设置为“否”，资产将不自动折旧。</span><span class="sxs-lookup"><span data-stu-id="0b442-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="0b442-116">设置资产的使用年限，用年表示。</span><span class="sxs-lookup"><span data-stu-id="0b442-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="0b442-117">请注意，在设置使用年限后，计算“折旧期间”字段值。</span><span class="sxs-lookup"><span data-stu-id="0b442-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="0b442-118">在“折旧惯例”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="0b442-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="0b442-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0b442-119">Close the page.</span></span>


