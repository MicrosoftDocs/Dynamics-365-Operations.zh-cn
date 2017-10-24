--- 
title: "设置 I-9 文档类型"
description: "此过程显示如何查看和设置 I-9 表格验证所使用的文件类型。"
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="cc1b4-103">设置 I-9 文档类型</span><span class="sxs-lookup"><span data-stu-id="cc1b4-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="cc1b4-104">此过程显示如何查看和设置 I-9 表格验证所使用的文件类型。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="cc1b4-105">在设置 I-9 文件类型前，您还必须设置签发机构和标识类型。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="cc1b4-106">使用 USMF 公司演示数据创建此过程，该演示数据包括完成此过程所需的签发机构和标识类型的示例。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="cc1b4-107">转到“人力资源”>“工作人员”>“I-9”>“I-9 文件类型”。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="cc1b4-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-108">Click New.</span></span>
3. <span data-ttu-id="cc1b4-109">在“I-9 文件类型”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="cc1b4-110">示例：学校 ID。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-110">Example: School ID.</span></span>  
4. <span data-ttu-id="cc1b4-111">选择标识类型。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-111">Select the identification type.</span></span>  <span data-ttu-id="cc1b4-112">示例：学校 ID</span><span class="sxs-lookup"><span data-stu-id="cc1b4-112">Example:  School ID</span></span>
    * <span data-ttu-id="cc1b4-113">标识类型的示例包括社会保险号 (SSN)、签证号、护照 ID 或驾照。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="cc1b4-114">选择文件类型使用的 I-9 文件列表。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="cc1b4-115">作为 I-9 流程的一部分，员工必须出示证明其身份和雇用授权的文件。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="cc1b4-116">美国公民及移民服务局网站含有可接受文件以及文件所属列表的信息。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="cc1b4-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="cc1b4-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="cc1b4-118">在“表格”字段中，输入该文件类型的官方表格编号。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="cc1b4-119">示例：学校 ID。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-119">Example: School ID.</span></span>
    * <span data-ttu-id="cc1b4-120">官方表格编号可在美国公民及移民服务局网站查看。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="cc1b4-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="cc1b4-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="cc1b4-122">选择或取消选择“有效”复选框。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="cc1b4-123">在“到期日期”字段中，设置日期为“2019-10-27”。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="cc1b4-124">到期日期为可选项。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="cc1b4-125">选择签发该文件类型的机构。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="cc1b4-126">示例：省/直辖市/自治区/区域</span><span class="sxs-lookup"><span data-stu-id="cc1b4-126">Example: Province/territory</span></span>
10. <span data-ttu-id="cc1b4-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cc1b4-127">Click Save.</span></span>


