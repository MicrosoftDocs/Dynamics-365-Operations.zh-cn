---
title: 即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置
description: 即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049454"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="59f3b-103">即使未进行任何更改，系统仍会提示您保存物料覆盖范围设置</span><span class="sxs-lookup"><span data-stu-id="59f3b-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="59f3b-104">知识库编号：4615588</span><span class="sxs-lookup"><span data-stu-id="59f3b-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="59f3b-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="59f3b-105">Symptoms</span></span>

<span data-ttu-id="59f3b-106">在某些情况下，您在通过 *物料覆盖范围 V2* 实体导入物料后，打开 **物料覆盖范围** 页时可能会收到以下消息：</span><span class="sxs-lookup"><span data-stu-id="59f3b-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="59f3b-107">是否要在关闭之前保存更改?</span><span class="sxs-lookup"><span data-stu-id="59f3b-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="59f3b-108">即使您没有进行任何更改，您仍然会收到此消息。</span><span class="sxs-lookup"><span data-stu-id="59f3b-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="59f3b-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="59f3b-109">Resolution</span></span>

<span data-ttu-id="59f3b-110">**物料覆盖范围** 页包含复杂的默认逻辑，可能会导致在最近对数据库进行直接更改（如通过实体导入）后显示消息。</span><span class="sxs-lookup"><span data-stu-id="59f3b-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="59f3b-111">例如，`AREGENERALSETTINGSOVERRIDDEN` 实体字段设置为 *否*，但您导入的文件为 `PRODUCTCOVERAGEGROUPID` 和/或 `VENDORACCOUNTNUMBER` 等字段提供了新值或修改后的值。</span><span class="sxs-lookup"><span data-stu-id="59f3b-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="59f3b-112">在这种情况下，由于 `AREGENERALSETTINGSOVERRIDDEN` 字段设置为 *否*，导入后第一次打开 **物料覆盖范围** 页时，这些值会自动从字段中清除。</span><span class="sxs-lookup"><span data-stu-id="59f3b-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="59f3b-113">如果将更改保存为消息框提示，它们将存储在数据库中。</span><span class="sxs-lookup"><span data-stu-id="59f3b-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="59f3b-114">否则，您下次打开页面时将收到相同的消息。</span><span class="sxs-lookup"><span data-stu-id="59f3b-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="59f3b-115">要防止出现这种行为，同时还要通过实体导入包含诸如 `PRODUCTCOVERAGEGROUPID` 等字段的值，请在导入时将 `AREGENERALSETTINGSOVERRIDDEN` 设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="59f3b-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
