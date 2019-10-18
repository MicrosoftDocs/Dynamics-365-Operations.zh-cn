---
title: 为日记帐启用延迟税金计算
description: 此主题介绍如何**为日记帐启用延迟税金计算**功能在有大量日记帐行时提高税金计算的性能。
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176562"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="de49f-103">为日记帐启用延迟税金计算</span><span class="sxs-lookup"><span data-stu-id="de49f-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="de49f-104">此主题介绍如何**为日记帐启用延迟税金计算**功能在有大量日记帐行时提高税金计算的性能。</span><span class="sxs-lookup"><span data-stu-id="de49f-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="de49f-105">日记帐的当前销售税计算行为在用户更新与税金有关的字段（如销售税组/物料销售税组）时实时触发。</span><span class="sxs-lookup"><span data-stu-id="de49f-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="de49f-106">日记帐行级别的任何更新都将重新计算所有日记帐行中的税额。</span><span class="sxs-lookup"><span data-stu-id="de49f-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="de49f-107">它可帮助用户查看实时计算的税额，但是如果日记帐行数量非常大，也可以导致性能问题。</span><span class="sxs-lookup"><span data-stu-id="de49f-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="de49f-108">此功能提供了一个选项，用于推迟税金计算以解决性能问题。</span><span class="sxs-lookup"><span data-stu-id="de49f-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="de49f-109">如果开启了此功能，则仅当用户单击“销售税”命令或过帐日记帐时，才会计算税额。</span><span class="sxs-lookup"><span data-stu-id="de49f-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="de49f-110">用户可在三个级别开启/关闭此参数：</span><span class="sxs-lookup"><span data-stu-id="de49f-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="de49f-111">按法人</span><span class="sxs-lookup"><span data-stu-id="de49f-111">By legal entity</span></span>
- <span data-ttu-id="de49f-112">按日记帐名称</span><span class="sxs-lookup"><span data-stu-id="de49f-112">By journal name</span></span>
- <span data-ttu-id="de49f-113">按日记帐标题</span><span class="sxs-lookup"><span data-stu-id="de49f-113">By journal header</span></span>

<span data-ttu-id="de49f-114">系统将把日记帐标题中的参数值视为最终值。</span><span class="sxs-lookup"><span data-stu-id="de49f-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="de49f-115">日记帐标题中的参数值默认取自日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="de49f-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="de49f-116">日记帐名称中的参数值默认取自创建日记帐名称时生成的分类帐参数。</span><span class="sxs-lookup"><span data-stu-id="de49f-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="de49f-117">如果开启此参数，将隐藏日记帐中的“实际销售税金额”和“已计算销售税金额”字段。</span><span class="sxs-lookup"><span data-stu-id="de49f-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="de49f-118">目标是不让用户迷惑，因为用户触发税金计算之前，这两个字段的值始终显示 0。</span><span class="sxs-lookup"><span data-stu-id="de49f-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="de49f-119">按法人启用延迟的税金计算</span><span class="sxs-lookup"><span data-stu-id="de49f-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="de49f-120">转到**总帐 > 分类帐设置 > 总帐参数**</span><span class="sxs-lookup"><span data-stu-id="de49f-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="de49f-121">单击**销售税**选项卡</span><span class="sxs-lookup"><span data-stu-id="de49f-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="de49f-122">在**常规**快速选项卡下，找到参数**延迟的税金计算**，然后开启/关闭该参数</span><span class="sxs-lookup"><span data-stu-id="de49f-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="de49f-123">按日记帐名称启用延迟的税金计算</span><span class="sxs-lookup"><span data-stu-id="de49f-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="de49f-124">转到**总帐 > 日记帐设置 > 日记帐名称**</span><span class="sxs-lookup"><span data-stu-id="de49f-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="de49f-125">在**常规**快速选项卡下，找到参数**延迟的税金计算**，然后开启/关闭该参数</span><span class="sxs-lookup"><span data-stu-id="de49f-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="de49f-126">按日记帐启用延迟的税金计算</span><span class="sxs-lookup"><span data-stu-id="de49f-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="de49f-127">转到**总帐 > 日记帐条目 > 普通日记帐**</span><span class="sxs-lookup"><span data-stu-id="de49f-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="de49f-128">单击**新建**</span><span class="sxs-lookup"><span data-stu-id="de49f-128">Click **New**</span></span>
3. <span data-ttu-id="de49f-129">选择一个日记帐名称</span><span class="sxs-lookup"><span data-stu-id="de49f-129">Select a journal name</span></span>
4. <span data-ttu-id="de49f-130">单击**设置**</span><span class="sxs-lookup"><span data-stu-id="de49f-130">Click **Setup**</span></span>
5. <span data-ttu-id="de49f-131">找到参数**延迟的税金计算**，然后开启/关闭该参数</span><span class="sxs-lookup"><span data-stu-id="de49f-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
