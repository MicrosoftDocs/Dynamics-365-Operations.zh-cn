--- 
title: "创建成本对象"
description: "此过程显示如何通过数据连接器将 Dynamics 365 for Finance and Operations Enterprise Edition 成本中心财务维度导入成本核算来创建成本对象。"
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 52b5fe092048cd7efe7b0a697cd7061ee0f65103
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="9f42d-103">创建成本对象</span><span class="sxs-lookup"><span data-stu-id="9f42d-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f42d-104">此过程显示如何通过数据连接器将 Dynamics 365 for Finance and Operations Enterprise Edition 成本中心财务维度导入成本核算来创建成本对象。</span><span class="sxs-lookup"><span data-stu-id="9f42d-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="9f42d-105">用于创建该过程的是演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="9f42d-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="9f42d-106">此过程针对 Microsoft Dynamics 365 for Operations 版本 1611 中增加的成本核算功能。</span><span class="sxs-lookup"><span data-stu-id="9f42d-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="9f42d-107">新建成本对象</span><span class="sxs-lookup"><span data-stu-id="9f42d-107">Create new cost objects</span></span>
1. <span data-ttu-id="9f42d-108">转到“成本核算”>“维度”>“成本对象维度”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="9f42d-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-109">Click New.</span></span>
3. <span data-ttu-id="9f42d-110">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9f42d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9f42d-111">在“维度成员的数据连接器”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="9f42d-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="9f42d-112">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="9f42d-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="9f42d-113">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="9f42d-114">配置数据连接器</span><span class="sxs-lookup"><span data-stu-id="9f42d-114">Configure the data connector</span></span>
1. <span data-ttu-id="9f42d-115">单击“配置维度成员提供方”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="9f42d-116">选择 CostCenter 将 CostCenter 维度导入成本核算中。</span><span class="sxs-lookup"><span data-stu-id="9f42d-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="9f42d-117">在“维度名称”字段中，选择“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="9f42d-118">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="9f42d-119">导入成本中心</span><span class="sxs-lookup"><span data-stu-id="9f42d-119">Import cost centers</span></span>
1. <span data-ttu-id="9f42d-120">单击“导入维度成员”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="9f42d-121">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="9f42d-122">查看导入的成本中心</span><span class="sxs-lookup"><span data-stu-id="9f42d-122">View the imported cost centers</span></span>
1. <span data-ttu-id="9f42d-123">单击“查看维度成员”。</span><span class="sxs-lookup"><span data-stu-id="9f42d-123">Click View dimension members.</span></span>


