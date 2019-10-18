---
title: 高级银行对帐 MT940 导入 - 综合数据实体升级
description: 需要将序列号添加到银行对账单导入实体以支持 MT940 格式。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88eb5b3c408d36620ab550b29d2e5a3278d25d8a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188456"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="63842-103">高级银行对帐 MT940 导入 - 综合数据实体升级</span><span class="sxs-lookup"><span data-stu-id="63842-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63842-104">需要将序列号添加到银行对账单导入实体以支持 MT940 格式。</span><span class="sxs-lookup"><span data-stu-id="63842-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="63842-105">使用以下步骤添加银行对账单导入实体以支持 MT940 格式。</span><span class="sxs-lookup"><span data-stu-id="63842-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="63842-106">编译并同步以下操作：</span><span class="sxs-lookup"><span data-stu-id="63842-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="63842-107">组合实体\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="63842-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="63842-108">实体\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="63842-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="63842-109">实体\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="63842-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="63842-110">实体\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="63842-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="63842-111">实体\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="63842-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="63842-112">表\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="63842-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="63842-113">数据管理\\数据项目。</span><span class="sxs-lookup"><span data-stu-id="63842-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="63842-114">负荷 MT940 导入项目</span><span class="sxs-lookup"><span data-stu-id="63842-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="63842-115">变更 XSLT。</span><span class="sxs-lookup"><span data-stu-id="63842-115">Change XSLT.</span></span>
            -   <span data-ttu-id="63842-116">单击**查看映射**。</span><span class="sxs-lookup"><span data-stu-id="63842-116">Click **View map**.</span></span>
            -   <span data-ttu-id="63842-117">单击银行对账单单据上的**查看映射**。</span><span class="sxs-lookup"><span data-stu-id="63842-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="63842-118">单击**转换**</span><span class="sxs-lookup"><span data-stu-id="63842-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="63842-119">删除 BankReconiliation-to-Composite.xslt 文件。</span><span class="sxs-lookup"><span data-stu-id="63842-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="63842-120">添加 BankReconiliation-to-Composite.xsl 的新版本。</span><span class="sxs-lookup"><span data-stu-id="63842-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="63842-121">在**源数据**版式上公开**序列号**。</span><span class="sxs-lookup"><span data-stu-id="63842-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="63842-122">源数据格式 = XML 元素。</span><span class="sxs-lookup"><span data-stu-id="63842-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="63842-123">实体名称 = 银行对账单。</span><span class="sxs-lookup"><span data-stu-id="63842-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="63842-124">上载数据文件 = SampleBankCompositeEntity.xml 的新版本。</span><span class="sxs-lookup"><span data-stu-id="63842-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="63842-125">单击**是**以覆盖现有文件。</span><span class="sxs-lookup"><span data-stu-id="63842-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="63842-126">单击**是**生成新的映射。</span><span class="sxs-lookup"><span data-stu-id="63842-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="63842-127">验证S**equenceNumber**是否已映射。</span><span class="sxs-lookup"><span data-stu-id="63842-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="63842-128">单击对账单实体上的**查看映射**。</span><span class="sxs-lookup"><span data-stu-id="63842-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="63842-129">验证**SequenceNumber**是否已从源映射到暂存。</span><span class="sxs-lookup"><span data-stu-id="63842-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="63842-130">导入新的对账单。</span><span class="sxs-lookup"><span data-stu-id="63842-130">Import the new statement.</span></span>




