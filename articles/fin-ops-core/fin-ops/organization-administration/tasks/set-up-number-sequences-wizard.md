---
title: 使用向导设置编号规则
description: 此主题说明如何同时使用向导设置所有必需的数序。
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b79924e2c8d94b5e5e160a123e9b0cde0971fd96
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560475"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="c05a8-103">使用向导设置编号规则</span><span class="sxs-lookup"><span data-stu-id="c05a8-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c05a8-104">“数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。</span><span class="sxs-lookup"><span data-stu-id="c05a8-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="c05a8-105">需要标识符的主数据或交易记录称为“参考”。</span><span class="sxs-lookup"><span data-stu-id="c05a8-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="c05a8-106">在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。</span><span class="sxs-lookup"><span data-stu-id="c05a8-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="c05a8-107">此主题说明如何同时使用向导设置所有必需的数序。</span><span class="sxs-lookup"><span data-stu-id="c05a8-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="c05a8-108">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="c05a8-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c05a8-109">转到 **导航 > 模块 > 组织管理 > 标号规则 > 编号规则**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="c05a8-110">选择 **生成**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-110">Select **Generate**.</span></span>
3. <span data-ttu-id="c05a8-111">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-111">Select **Next**.</span></span>

   - <span data-ttu-id="c05a8-112">在此页上您可以修改标识代码、最低值和最高值。</span><span class="sxs-lookup"><span data-stu-id="c05a8-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="c05a8-113">此外，您可以指示该编号规则是否必须是连续的。</span><span class="sxs-lookup"><span data-stu-id="c05a8-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="c05a8-114">如果您必须为该编号规则分配编号，请不要选择 **连续** 选项。</span><span class="sxs-lookup"><span data-stu-id="c05a8-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="c05a8-115">为了将范围段落添加到编号规则的格式，请在列表中选择该格式，然后选择 **将范围包括在格式中**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="c05a8-116">为了将范围段落从编号规则的格式中删除，请在列表中选择该格式，然后选择 **从格式中删除范围**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="c05a8-117">为了将编号规则从自动生成中排除，请在列表中选择该编号规则，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="c05a8-118">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-118">Select **Next**.</span></span>
5. <span data-ttu-id="c05a8-119">选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="c05a8-119">Select **Finish**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]