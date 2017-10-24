---
title: "高级银行对帐 MT940 导入 - 综合数据实体升级"
description: "需要将序列号添加到银行对账单导入实体以支持 MT940 格式。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0fb86cd4264d5420c479e14f7eed41e480c88b63
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="9562a-103">高级银行对帐 MT940 导入 - 综合数据实体升级</span><span class="sxs-lookup"><span data-stu-id="9562a-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9562a-104">需要将序列号添加到银行对账单导入实体以支持 MT940 格式。</span><span class="sxs-lookup"><span data-stu-id="9562a-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="9562a-105">使用以下步骤添加银行对账单导入实体以支持 MT940 格式。</span><span class="sxs-lookup"><span data-stu-id="9562a-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="9562a-106">编译并同步以下操作：</span><span class="sxs-lookup"><span data-stu-id="9562a-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="9562a-107">组合实体\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="9562a-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="9562a-108">实体\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="9562a-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="9562a-109">实体\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="9562a-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="9562a-110">实体\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="9562a-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="9562a-111">实体\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="9562a-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="9562a-112">表\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="9562a-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="9562a-113">数据管理\\数据项目。</span><span class="sxs-lookup"><span data-stu-id="9562a-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="9562a-114">负荷 MT940 导入项目</span><span class="sxs-lookup"><span data-stu-id="9562a-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="9562a-115">变更 XSLT。</span><span class="sxs-lookup"><span data-stu-id="9562a-115">Change XSLT.</span></span>
            -   <span data-ttu-id="9562a-116">单击“**查看映射**”。</span><span class="sxs-lookup"><span data-stu-id="9562a-116">Click **View map**.</span></span>
            -   <span data-ttu-id="9562a-117">单击银行对账单单据上的“**查看映射**”。</span><span class="sxs-lookup"><span data-stu-id="9562a-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="9562a-118">单击“**转换**”</span><span class="sxs-lookup"><span data-stu-id="9562a-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="9562a-119">删除 BankReconiliation-to-Composite.xslt 文件。</span><span class="sxs-lookup"><span data-stu-id="9562a-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="9562a-120">添加 BankReconiliation-to-Composite.xsl 的新版本。</span><span class="sxs-lookup"><span data-stu-id="9562a-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="9562a-121">在“**源数据**”版式上公开“**序列号**”。</span><span class="sxs-lookup"><span data-stu-id="9562a-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="9562a-122">源数据格式 = XML 元素。</span><span class="sxs-lookup"><span data-stu-id="9562a-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="9562a-123">实体名称 = 银行对账单。</span><span class="sxs-lookup"><span data-stu-id="9562a-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="9562a-124">上载数据文件 = SampleBankCompositeEntity.xml 的新版本。</span><span class="sxs-lookup"><span data-stu-id="9562a-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="9562a-125">单击“**是**”以覆盖现有文件。</span><span class="sxs-lookup"><span data-stu-id="9562a-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="9562a-126">单击“**是**”生成新的映射。</span><span class="sxs-lookup"><span data-stu-id="9562a-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="9562a-127">验证“S**equenceNumber**”是否已映射。</span><span class="sxs-lookup"><span data-stu-id="9562a-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="9562a-128">单击对账单实体上的“**查看映射**”。</span><span class="sxs-lookup"><span data-stu-id="9562a-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="9562a-129">验证“**SequenceNumber**”是否已从源映射到暂存。</span><span class="sxs-lookup"><span data-stu-id="9562a-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="9562a-130">导入新的对账单。</span><span class="sxs-lookup"><span data-stu-id="9562a-130">Import the new statement.</span></span>




