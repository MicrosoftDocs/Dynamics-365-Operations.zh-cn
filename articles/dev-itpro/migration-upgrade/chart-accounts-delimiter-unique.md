---
title: "会计科目表分隔符必须是唯一的。"
description: "在 Dynamics 365 for Finance and Operations 中，科目表和维度值的分隔符不能相同。 必须在升级后更改分隔符值。"
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e12c47e4acd6aa8a92a909d490da9e590b5fcd20
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a><span data-ttu-id="d6dd1-104">会计科目表分隔符必须是唯一的。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-104">Chart of accounts delimiter must be unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6dd1-105">在 Microsoft Dynamics AX 2012 中，可为科目表和维度值使用相同分隔符。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="d6dd1-106">在 Dynamics 365 for Finance and Operations 中，科目表和维度值的分隔符不能相同。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-106">In Dynamics 365 for Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="d6dd1-107">如果有相同分隔符，可在升级后更改。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="d6dd1-108">以下产品中有此功能：</span><span class="sxs-lookup"><span data-stu-id="d6dd1-108">This feature is available in:</span></span>
- <span data-ttu-id="d6dd1-109">Dynamics 365 for Finance and Operations 版本 8.0</span><span class="sxs-lookup"><span data-stu-id="d6dd1-109">Dynamics 365 for Finance and Operations version 8.0</span></span>
- <span data-ttu-id="d6dd1-110">Dynamics 365 for Finance and Operations 版本 7.1 KB 4094701：维度值中包含科目表分隔符时，不能输入财务维度</span><span class="sxs-lookup"><span data-stu-id="d6dd1-110">Dynamics 365 for Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="d6dd1-111">Dynamics 365 for Finance and Operations 版本 7.2 KB 4092967：子项目格式中包含维度分隔符时，不能选择子项目作为维度</span><span class="sxs-lookup"><span data-stu-id="d6dd1-111">Dynamics 365 for Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="d6dd1-112">更新分隔符</span><span class="sxs-lookup"><span data-stu-id="d6dd1-112">Update delimiter</span></span>
<span data-ttu-id="d6dd1-113">如果科目表存在冲突，则可更改科目表分隔符和项目/子项目 ID。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-113">If there is a conflict with the Chart of Accounts, the Chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="d6dd1-114">不能更改其他维度分隔符。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="d6dd1-115">升级到 Finance and Operations 之后，可在**总帐参数** > **会计科目表和维度** > **更改分隔符**中更改会计科目表分隔符。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-115">You can change the chart of accounts delimiter after upgrade to Finance and Operations in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="d6dd1-116">如果只有项目/子项目 ID 格式冲突，则可在**项目管理与核算参数** > **常规** > **修改子项目格式**中更改该值。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="d6dd1-117">如何确定环境是否需要更新后的分隔符</span><span class="sxs-lookup"><span data-stu-id="d6dd1-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="d6dd1-118">如果升级后的环境中的分隔符冲突，在细分条目控件或维度条目控件中输入值时，可能遇到不稳定。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="d6dd1-119">这意味着输入科目和维度组合时，始终需要使用查找或弹出菜单。</span><span class="sxs-lookup"><span data-stu-id="d6dd1-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>

