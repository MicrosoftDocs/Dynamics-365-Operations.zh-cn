--- 
title: "设置 ISO20022 直接借记的付款方式"
description: "此过程显示如何通过电子申报生成文件来为 ISO20022 直接借记或其他任何付款类型设置客户付款方式。"
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 57c184d5b8f6b42f738142e4f448aafe6225dcb0
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a><span data-ttu-id="d9bca-103">设置 ISO20022 直接借记的付款方式</span><span class="sxs-lookup"><span data-stu-id="d9bca-103">Set up method of payment for ISO20022 direct debit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9bca-104">此过程显示如何通过电子申报生成文件来为 ISO20022 直接借记或其他任何付款类型设置客户付款方式。</span><span class="sxs-lookup"><span data-stu-id="d9bca-104">This procedure shows how to set up the customer method of payment for ISO20022 direct debit or any other payment type using electronic reporting.</span></span> 



<span data-ttu-id="d9bca-105">必须先设置导出格式配置和付款帐户，才能完成此任务。</span><span class="sxs-lookup"><span data-stu-id="d9bca-105">Before you complete this task, you must set up export format configurations and payment accounts.</span></span>



<span data-ttu-id="d9bca-106">本流程用演示公司DEMF数据生成的。</span><span class="sxs-lookup"><span data-stu-id="d9bca-106">This procedure was created using the demo data company DEMF.</span></span>



<span data-ttu-id="d9bca-107">这是五个用于演示使用电子申报配置的客户付款流程的过程中的第三个。</span><span class="sxs-lookup"><span data-stu-id="d9bca-107">This is the third of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="d9bca-108">转到“应收帐款”>“付款设置”>“付款方式”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-108">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="d9bca-109">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="d9bca-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d9bca-110">例如，在含有“ELECTRONIC”值的“付款方式”字段中筛选。</span><span class="sxs-lookup"><span data-stu-id="d9bca-110">For example, filter on the Method of payment field with a value of 'ELECTRONIC'.</span></span>
3. <span data-ttu-id="d9bca-111">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-111">Click Edit.</span></span>
4. <span data-ttu-id="d9bca-112">在“付款帐户”字段中，指定“DEMF OPER”值。</span><span class="sxs-lookup"><span data-stu-id="d9bca-112">In the Payment account field, specify the values 'DEMF OPER'.</span></span>
5. <span data-ttu-id="d9bca-113">展开“文件格式”部分。</span><span class="sxs-lookup"><span data-stu-id="d9bca-113">Expand the File formats section.</span></span>
6. <span data-ttu-id="d9bca-114">在“普通电子申报”字段中，选择“是”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-114">Select Yes in the Generic electronic reporting field.</span></span>
7. <span data-ttu-id="d9bca-115">在“导出格式配置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d9bca-115">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="d9bca-116">在列表中，选择“ISO20022 直接借记（德国）”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-116">In the list, select ISO20022 Direct debit (DE).</span></span>  <span data-ttu-id="d9bca-117">如果该列表为空，则客户付款导出格式配置尚未导入，也不有效。</span><span class="sxs-lookup"><span data-stu-id="d9bca-117">If the list is empty, the customer payment export format configuration has not been imported and active.</span></span>  
8. <span data-ttu-id="d9bca-118">在“需要授权”字段选择“是”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-118">Select Yes in the Require mandate field.</span></span>
    * <span data-ttu-id="d9bca-119">为客户付款格式选择“需要授权单参数”，这些格式要求付款消息中包含授权单信息，如 SEPA 直接借记。</span><span class="sxs-lookup"><span data-stu-id="d9bca-119">Select the Require mandate parameter for customer payment formats, which require including mandate information in the payment message, like SEPA direct debit.</span></span>  
9. <span data-ttu-id="d9bca-120">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d9bca-120">Click Save.</span></span>

