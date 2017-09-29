--- 
title: "通过使用向导设置编号规则"
description: "“数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。"
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96c1bc711350b447611977c3f2070fbc08fbae0f
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="0aed4-103">通过使用向导设置编号规则</span><span class="sxs-lookup"><span data-stu-id="0aed4-103">Set up number sequences by using a wizard</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0aed4-104">“数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="0aed4-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="0aed4-105">需要标识符的主数据或交易记录称为“参考”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="0aed4-106">在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。</span><span class="sxs-lookup"><span data-stu-id="0aed4-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="0aed4-107">该过程会说明如何同时使用向导设置所有必需的数序。</span><span class="sxs-lookup"><span data-stu-id="0aed4-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="0aed4-108">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0aed4-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0aed4-109">转到“组织管理”>“标号规则”>“编号规则”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="0aed4-110">单击“生成”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-110">Click Generate.</span></span>
3. <span data-ttu-id="0aed4-111">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-111">Click Next.</span></span>
    * <span data-ttu-id="0aed4-112">在此页上您可以修改标识代码、最低值和最高值。</span><span class="sxs-lookup"><span data-stu-id="0aed4-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="0aed4-113">此外，您可以指示该编号规则是否必须是连续的。</span><span class="sxs-lookup"><span data-stu-id="0aed4-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="0aed4-114">如果您必须为该编号规则分配编号，请不要选择“连续”选项。</span><span class="sxs-lookup"><span data-stu-id="0aed4-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="0aed4-115">为了将范围段落添加到编号规则的格式，请在列表中选择该格式，然后单击“将范围包括在格式中”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="0aed4-116">为了将范围段落从编号规则的格式中删除，请在列表中选择该格式，然后单击“从格式中删除范围”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="0aed4-117">为了将编号规则从自动生成中排除，请在列表中选择该编号规则，然后单击“删除”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="0aed4-118">单击“下一步”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-118">Click Next.</span></span>
5. <span data-ttu-id="0aed4-119">单击“完成”。</span><span class="sxs-lookup"><span data-stu-id="0aed4-119">Click Finish.</span></span>


