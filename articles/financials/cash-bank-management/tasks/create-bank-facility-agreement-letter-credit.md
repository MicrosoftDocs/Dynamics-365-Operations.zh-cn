---
title: 创建信用证的银行信贷协议
description: 此任务可以简单了解如何创建银行信贷协议以办理信用证。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18395f300965df7e024f0eec2b53fa4e8ad2cc3e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566194"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="ce372-103">创建信用证的银行信贷协议</span><span class="sxs-lookup"><span data-stu-id="ce372-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce372-104">此任务可以简单了解如何创建银行信贷协议以办理信用证。</span><span class="sxs-lookup"><span data-stu-id="ce372-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="ce372-105">在执行此任务之前，您需要建立银行信贷并邮寄个人档案。</span><span class="sxs-lookup"><span data-stu-id="ce372-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="ce372-106">此任务使用演示公司“USMF”。</span><span class="sxs-lookup"><span data-stu-id="ce372-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="ce372-107">创建银行信贷协议</span><span class="sxs-lookup"><span data-stu-id="ce372-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="ce372-108">转到“现金与银行管理”>“信用证”>“银行信贷协议”。</span><span class="sxs-lookup"><span data-stu-id="ce372-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="ce372-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="ce372-109">Click New.</span></span>
3. <span data-ttu-id="ce372-110">在“协议编号”字段，根据银行的协议输入对应的协议编号。</span><span class="sxs-lookup"><span data-stu-id="ce372-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="ce372-111">在“银行帐户”字段中，输入开户银行的帐号。</span><span class="sxs-lookup"><span data-stu-id="ce372-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="ce372-112">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ce372-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="ce372-113">在“开始日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="ce372-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="ce372-114">在“结束日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="ce372-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="ce372-115">展开或收起“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="ce372-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="ce372-116">单击“添加行”。</span><span class="sxs-lookup"><span data-stu-id="ce372-116">Click Add line.</span></span>
10. <span data-ttu-id="ce372-117">在“融资类型”字段中，单击下拉键打开查询。</span><span class="sxs-lookup"><span data-stu-id="ce372-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ce372-118">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="ce372-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ce372-119">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="ce372-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ce372-120">在“额度”字段中，输入与银行协商所达成的授信额度。</span><span class="sxs-lookup"><span data-stu-id="ce372-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="ce372-121">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="ce372-121">Click Save.</span></span>
15. <span data-ttu-id="ce372-122">单击“扩展”打开垂直对话框。</span><span class="sxs-lookup"><span data-stu-id="ce372-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="ce372-123">在“新协议数目”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ce372-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="ce372-124">在“结束日期”字段中，输入日期和时间。</span><span class="sxs-lookup"><span data-stu-id="ce372-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="ce372-125">单击“扩展”。</span><span class="sxs-lookup"><span data-stu-id="ce372-125">Click Extend.</span></span>
19. <span data-ttu-id="ce372-126">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="ce372-126">Close the page.</span></span>

