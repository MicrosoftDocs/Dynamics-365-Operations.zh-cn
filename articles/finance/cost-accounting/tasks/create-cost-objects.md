---
title: 创建成本对象
description: 此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91c25c52a2c6dc7f096a494577b361ff30406e9c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236786"
---
# <a name="create-cost-objects"></a><span data-ttu-id="d7671-103">创建成本对象</span><span class="sxs-lookup"><span data-stu-id="d7671-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d7671-104">此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。</span><span class="sxs-lookup"><span data-stu-id="d7671-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="d7671-105">用于创建该过程的是演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="d7671-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="d7671-106">新建成本对象</span><span class="sxs-lookup"><span data-stu-id="d7671-106">Create new cost objects</span></span>
1. <span data-ttu-id="d7671-107">转到“成本核算”>“维度”>“成本对象维度”。</span><span class="sxs-lookup"><span data-stu-id="d7671-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="d7671-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d7671-108">Click New.</span></span>
3. <span data-ttu-id="d7671-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d7671-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d7671-110">在“维度成员的数据连接器”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7671-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="d7671-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d7671-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d7671-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="d7671-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="d7671-113">配置数据连接器</span><span class="sxs-lookup"><span data-stu-id="d7671-113">Configure the data connector</span></span>
1. <span data-ttu-id="d7671-114">单击“配置维度成员提供方”。</span><span class="sxs-lookup"><span data-stu-id="d7671-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="d7671-115">选择 CostCenter 将 CostCenter 维度导入成本核算中。</span><span class="sxs-lookup"><span data-stu-id="d7671-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="d7671-116">在“维度名称”字段中，选择“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="d7671-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="d7671-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7671-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="d7671-118">导入成本中心</span><span class="sxs-lookup"><span data-stu-id="d7671-118">Import cost centers</span></span>
1. <span data-ttu-id="d7671-119">单击“导入维度成员”。</span><span class="sxs-lookup"><span data-stu-id="d7671-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="d7671-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7671-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="d7671-121">查看导入的成本中心</span><span class="sxs-lookup"><span data-stu-id="d7671-121">View the imported cost centers</span></span>
1. <span data-ttu-id="d7671-122">单击“查看维度成员”。</span><span class="sxs-lookup"><span data-stu-id="d7671-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]