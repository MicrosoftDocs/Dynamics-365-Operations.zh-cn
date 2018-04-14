--- 
title: "设置 ISO20022 贷方转帐的付款方式"
description: "此过程显示如何通过电子申报生成文件来为 ISO20022 贷方转帐或其他任何付款类型设置供应商付款方式。"
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6c45324b1523e29aa5c6274b289fa823bf66ea12
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a><span data-ttu-id="f1b6c-103">设置 ISO20022 贷方转帐的付款方式</span><span class="sxs-lookup"><span data-stu-id="f1b6c-103">Set up method of payment for ISO20022 credit transfer</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1b6c-104">此过程显示如何通过电子申报生成文件来为 ISO20022 贷方转帐或其他任何付款类型设置供应商付款方式。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-104">This procedure shows how to set up the vendor method of payment for ISO20022 credit transfer or any other payment type using electronic reporting to generate a file.</span></span> 

<span data-ttu-id="f1b6c-105">必须先导出格式配置和设置付款帐户，才能完成此任务。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-105">Before you complete this task, you must export format configurations and set up payment accounts.</span></span>

<span data-ttu-id="f1b6c-106">此任务使用 DEMF 演示数据公司是创建。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-106">This task was created using the DEMF demo data company.</span></span>

<span data-ttu-id="f1b6c-107">这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第三个。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-107">This is the third procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="f1b6c-108">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="f1b6c-109">转至“应付账款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-109">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="f1b6c-110">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f1b6c-111">例如，含有“SEPA CT”值的“付款方式”字段。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-111">For example, filter on the Method of payment field with a value of 'SEPA CT'.</span></span>
3. <span data-ttu-id="f1b6c-112">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-112">Click Edit.</span></span>
4. <span data-ttu-id="f1b6c-113">在“期间”字段中，选择“全部”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-113">In the Period field, select 'Total'.</span></span>
5. <span data-ttu-id="f1b6c-114">在“付款类型”字段中，选择“电子付款”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-114">In the Payment type field, select 'Electronic payment'.</span></span>
6. <span data-ttu-id="f1b6c-115">展开“文件格式”部分。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-115">Expand the File formats section.</span></span>
7. <span data-ttu-id="f1b6c-116">在“普通电子申报”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-116">Select Yes in the Generic electronic reporting field.</span></span>
8. <span data-ttu-id="f1b6c-117">在“导出格式配置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-117">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="f1b6c-118">在列表中选择值 ISO20022 信用转帐 (DE)。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-118">In the list, select the value ISO20022 Credit transfer (DE).</span></span> <span data-ttu-id="f1b6c-119">如果该列表为空，则供应商付款导出格式配置不导入，也不有效。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-119">If the list is empty, the vendor payment export format configuration is not imported and active.</span></span>  
9. <span data-ttu-id="f1b6c-120">在“帐户类型”字段中，选择“银行”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-120">In the Account type field, select 'Bank'.</span></span>
10. <span data-ttu-id="f1b6c-121">在“付款帐户”字段中，指定“DEMF OPER”值。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-121">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
11. <span data-ttu-id="f1b6c-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="f1b6c-122">Click Save.</span></span>


