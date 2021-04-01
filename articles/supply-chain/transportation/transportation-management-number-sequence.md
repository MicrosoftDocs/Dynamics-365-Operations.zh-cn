---
title: 运输管理编号规则
description: 此主题介绍如何设置运输管理的编号规则。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233359"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="ce273-103">运输管理编号规则</span><span class="sxs-lookup"><span data-stu-id="ce273-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce273-104">使用运输管理模块中的 **编号规则** 页来设置不同专业编号。</span><span class="sxs-lookup"><span data-stu-id="ce273-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="ce273-105">承运人使用专业编号来组织和跟踪每个装运的进度。</span><span class="sxs-lookup"><span data-stu-id="ce273-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="ce273-106">创建专业编号的编号规则</span><span class="sxs-lookup"><span data-stu-id="ce273-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="ce273-107">要为专业编号创建编号规则，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ce273-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="ce273-108">转到 **运输管理 \> 设置 \> 承运人 \> 编号规则**。</span><span class="sxs-lookup"><span data-stu-id="ce273-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="ce273-109">选择 **新建** 创建新编号规则。</span><span class="sxs-lookup"><span data-stu-id="ce273-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="ce273-110">为编号规则输入唯一 ID 和描述名称。</span><span class="sxs-lookup"><span data-stu-id="ce273-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="ce273-111">在 **编号规则类型** 字段中，*专业编号* 是唯一选项。</span><span class="sxs-lookup"><span data-stu-id="ce273-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="ce273-112">在 **校验位** 字段中，*校验位* 是唯一选项，设置为通用引擎。</span><span class="sxs-lookup"><span data-stu-id="ce273-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="ce273-113">在 **序列** 快速选项卡上，提供有关序列的信息。</span><span class="sxs-lookup"><span data-stu-id="ce273-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="ce273-114">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ce273-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="ce273-115">将编号规则链接到装运承运人</span><span class="sxs-lookup"><span data-stu-id="ce273-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="ce273-116">要将编号规则链接到承运人，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="ce273-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="ce273-117">转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。</span><span class="sxs-lookup"><span data-stu-id="ce273-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="ce273-118">选择装运承运人。</span><span class="sxs-lookup"><span data-stu-id="ce273-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="ce273-119">选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="ce273-119">Select **Edit**.</span></span>
1. <span data-ttu-id="ce273-120">在 **概览** 快速选项卡上，在 **专业编号规则** 字段中选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="ce273-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="ce273-121">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ce273-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]