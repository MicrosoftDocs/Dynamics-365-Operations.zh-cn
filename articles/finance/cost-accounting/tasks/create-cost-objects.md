---
title: 创建成本对象
description: 此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810046"
---
# <a name="create-cost-objects"></a><span data-ttu-id="cff19-103">创建成本对象</span><span class="sxs-lookup"><span data-stu-id="cff19-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cff19-104">此过程显示如何通过数据连接器将成本中心财务维度导入成本核算来创建成本对象。</span><span class="sxs-lookup"><span data-stu-id="cff19-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="cff19-105">用于创建该过程的是演示公司 USMF。</span><span class="sxs-lookup"><span data-stu-id="cff19-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="cff19-106">新建成本对象</span><span class="sxs-lookup"><span data-stu-id="cff19-106">Create new cost objects</span></span>
1. <span data-ttu-id="cff19-107">转到“成本核算”>“维度”>“成本对象维度”。</span><span class="sxs-lookup"><span data-stu-id="cff19-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="cff19-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="cff19-108">Click New.</span></span>
3. <span data-ttu-id="cff19-109">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cff19-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cff19-110">在“维度成员的数据连接器”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="cff19-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="cff19-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="cff19-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="cff19-112">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="cff19-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="cff19-113">配置数据连接器</span><span class="sxs-lookup"><span data-stu-id="cff19-113">Configure the data connector</span></span>
1. <span data-ttu-id="cff19-114">单击“配置维度成员提供方”。</span><span class="sxs-lookup"><span data-stu-id="cff19-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="cff19-115">选择 CostCenter 将 CostCenter 维度导入成本核算中。</span><span class="sxs-lookup"><span data-stu-id="cff19-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="cff19-116">在“维度名称”字段中，选择“成本中心”。</span><span class="sxs-lookup"><span data-stu-id="cff19-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="cff19-117">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cff19-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="cff19-118">导入成本中心</span><span class="sxs-lookup"><span data-stu-id="cff19-118">Import cost centers</span></span>
1. <span data-ttu-id="cff19-119">单击“导入维度成员”。</span><span class="sxs-lookup"><span data-stu-id="cff19-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="cff19-120">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cff19-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="cff19-121">查看导入的成本中心</span><span class="sxs-lookup"><span data-stu-id="cff19-121">View the imported cost centers</span></span>
1. <span data-ttu-id="cff19-122">单击“查看维度成员”。</span><span class="sxs-lookup"><span data-stu-id="cff19-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]