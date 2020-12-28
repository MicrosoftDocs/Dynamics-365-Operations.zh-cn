---
title: 更新银行日记帐组合实体
description: 需按照以下步骤将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中。
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ec196600a54a2aed4565cf422dc386d6646ff524
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440618"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="3cc00-103">更新银行日记帐组合实体</span><span class="sxs-lookup"><span data-stu-id="3cc00-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cc00-104">需按照以下步骤将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中。</span><span class="sxs-lookup"><span data-stu-id="3cc00-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="3cc00-105">按照以下步骤将更多 BankTransactionType 字段添加到组合 BankJournalEntity 中。</span><span class="sxs-lookup"><span data-stu-id="3cc00-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="3cc00-106">编译和同步以下银行日记帐组合实体、实体和暂存表：</span><span class="sxs-lookup"><span data-stu-id="3cc00-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="3cc00-107">组合实体\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="3cc00-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="3cc00-108">实体\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="3cc00-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="3cc00-109">实体\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="3cc00-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="3cc00-110">表\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="3cc00-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="3cc00-111">表\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="3cc00-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="3cc00-112">数据管理\\数据项目</span><span class="sxs-lookup"><span data-stu-id="3cc00-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="3cc00-113">在 **源数据** 版式上公开 **银行交易记录** 类型。</span><span class="sxs-lookup"><span data-stu-id="3cc00-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="3cc00-114">源数据格式 = XML-元素</span><span class="sxs-lookup"><span data-stu-id="3cc00-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="3cc00-115">实体名称 = 银行日记帐</span><span class="sxs-lookup"><span data-stu-id="3cc00-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="3cc00-116">上载数据文件 = SampleBankJournalCompositeEntity.xml 的新版本</span><span class="sxs-lookup"><span data-stu-id="3cc00-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="3cc00-117">单击 **是** 以覆盖现有文件。</span><span class="sxs-lookup"><span data-stu-id="3cc00-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="3cc00-118">单击 **是** 从头开始生成新的映射。</span><span class="sxs-lookup"><span data-stu-id="3cc00-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="3cc00-119">验证银行交易记录类型是否已映射。</span><span class="sxs-lookup"><span data-stu-id="3cc00-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="3cc00-120">单击“行”实体上的 **查看映射**。</span><span class="sxs-lookup"><span data-stu-id="3cc00-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="3cc00-121">验证“银行交易记录”类型是否已从源映射到暂存。</span><span class="sxs-lookup"><span data-stu-id="3cc00-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="3cc00-122">导入新的对账单。</span><span class="sxs-lookup"><span data-stu-id="3cc00-122">Import the new statement.</span></span>




