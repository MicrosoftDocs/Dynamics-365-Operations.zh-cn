---
title: 设置中心附属费用和附属主数据
description: 此过程显示如何为中心创建附属主数据，并使用主数据来创建中心附加费。
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2e9125c7a38d1dc5e6866a056fb71f25e40928
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233671"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="a8047-103">设置中心附属费用和附属主数据</span><span class="sxs-lookup"><span data-stu-id="a8047-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8047-104">此过程显示如何为中心创建附属主数据，并使用主数据来创建中心附加费。</span><span class="sxs-lookup"><span data-stu-id="a8047-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="a8047-105">此过程使用 USMF 数据集。</span><span class="sxs-lookup"><span data-stu-id="a8047-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="a8047-106">此设置通常由运输协调员完成。</span><span class="sxs-lookup"><span data-stu-id="a8047-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="a8047-107">设置汇集点主</span><span class="sxs-lookup"><span data-stu-id="a8047-107">Set up a hub master</span></span>
1. <span data-ttu-id="a8047-108">转到“运输管理”>“设置”>“评级”>“附属主数据”。</span><span class="sxs-lookup"><span data-stu-id="a8047-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="a8047-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a8047-109">Click New.</span></span>
3. <span data-ttu-id="a8047-110">在“附属主数据”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8047-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="a8047-111">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8047-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a8047-112">在“附属类型”字段中，选择“中心”。</span><span class="sxs-lookup"><span data-stu-id="a8047-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="a8047-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a8047-113">Click Save.</span></span>
7. <span data-ttu-id="a8047-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8047-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="a8047-115">设置中心附加费</span><span class="sxs-lookup"><span data-stu-id="a8047-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="a8047-116">转到“运输管理”>“设置”>“评级”>“中心附加费”。</span><span class="sxs-lookup"><span data-stu-id="a8047-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="a8047-117">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="a8047-117">Click New.</span></span>
3. <span data-ttu-id="a8047-118">在“中心附属 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="a8047-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="a8047-119">在“中心”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a8047-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a8047-120">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="a8047-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a8047-121">在“中心位置”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="a8047-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="a8047-122">您可以创建装货或卸货费用。</span><span class="sxs-lookup"><span data-stu-id="a8047-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="a8047-123">根据您的选择，费用将适用于您的路线中相应的运输细分市场。</span><span class="sxs-lookup"><span data-stu-id="a8047-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="a8047-124">在“附属主数据”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="a8047-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a8047-125">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="a8047-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a8047-126">选择您刚创建的主数据。</span><span class="sxs-lookup"><span data-stu-id="a8047-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="a8047-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="a8047-127">Click Save.</span></span>
10. <span data-ttu-id="a8047-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="a8047-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]