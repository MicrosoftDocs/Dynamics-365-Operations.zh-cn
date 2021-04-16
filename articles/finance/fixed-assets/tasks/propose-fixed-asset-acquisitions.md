---
title: 建议固定资产购置
description: 本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817149"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="9eb3c-103">建议固定资产购置</span><span class="sxs-lookup"><span data-stu-id="9eb3c-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9eb3c-104">本主题介绍如何使用固定资产日记帐中的购置方案购置固定资产。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="9eb3c-105">它为 USMF 法人实体使用会计角色和演示数据。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="9eb3c-106">要通过固定资产建议日记帐获取固定资产，必须首先创建固定资产记录，然后在资产帐簿中定义购置价格。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="9eb3c-107">创建资产购置方案</span><span class="sxs-lookup"><span data-stu-id="9eb3c-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="9eb3c-108">完成以下步骤以创建资产购置方案。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="9eb3c-109">在导航窗格中，转到 **模块 > 固定资产 > 日记帐条目 > 固定资产日记帐**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="9eb3c-110">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-110">Select **New**.</span></span>
3. <span data-ttu-id="9eb3c-111">在 **名称** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="9eb3c-112">在操作窗格中，选择 **行**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="9eb3c-113">选择 **方案**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="9eb3c-114">选择 **购置方案**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="9eb3c-115">选择 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-115">Select **Filter**.</span></span> <span data-ttu-id="9eb3c-116">选择 **重置** 以清除先前的值。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="9eb3c-117">选择 **固定资产编号** 行。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="9eb3c-118">在 **标准** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="9eb3c-119">为您想要以此方案购置的固定资产设置其他条件。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="9eb3c-120">选择 **确定** 两次退出窗格。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="9eb3c-121">验证已创建交易行。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="9eb3c-122">只有在帐簿中设置了购置日期和购置价格的固定资产才会包含在购置方案中。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="9eb3c-123">在页面上，选择 **帐簿** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="9eb3c-124">选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="9eb3c-125">在购置方案中包括默认的财务维度</span><span class="sxs-lookup"><span data-stu-id="9eb3c-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="9eb3c-126">通过转到 **固定资产 > 日记帐条目 > 固定资产日记帐**，可以使用 Excel 加载项创建购置交易。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="9eb3c-127">创建新日记帐，移动到页面上的 **行** 部分，选择 Excel 图标，然后选择固定资产日记帐行。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="9eb3c-128">系统将创建并打开表示日记帐行的 Excel 模板。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="9eb3c-129">您可以为要添加到模板中的日记帐行添加数据，然后将该信息发布回系统中。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="9eb3c-130">如果已为所选的资产薄和在 Excel 模板中输入的相应固定资产设置默认维度，当日记帐从 Excel 发布到系统时，将从资产薄主数据中调用默认财务维度。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="9eb3c-131">若要在从 Excel 加载项发布固定资产日记帐时自动在资产簿上包括财务维度，必须预先设置默认维度。</span><span class="sxs-lookup"><span data-stu-id="9eb3c-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
