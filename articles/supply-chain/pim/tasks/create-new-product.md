---
title: 创建新产品
description: 此主题描述如何创建新共享产品。
author: ShylaThompson
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d33a13920e1881cdc69ad7c100180d3b3b441d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820026"
---
# <a name="create-a-new-product"></a><span data-ttu-id="d9b48-103">创建新产品</span><span class="sxs-lookup"><span data-stu-id="d9b48-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9b48-104">此主题描述如何创建新共享产品。</span><span class="sxs-lookup"><span data-stu-id="d9b48-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="d9b48-105">它通常由产品设计器执行。</span><span class="sxs-lookup"><span data-stu-id="d9b48-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="d9b48-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="d9b48-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="d9b48-107">创建产品</span><span class="sxs-lookup"><span data-stu-id="d9b48-107">Create a product</span></span>
1. <span data-ttu-id="d9b48-108">在导航窗格中，转到 **导航窗格 > 模块 > 产品信息管理 > 产品 > 产品**。</span><span class="sxs-lookup"><span data-stu-id="d9b48-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="d9b48-109">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d9b48-109">Select **New**.</span></span>
3. <span data-ttu-id="d9b48-110">在 **产品编号** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d9b48-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="d9b48-111">如果编号规则没有为产品编号设置，必须手动输入它。</span><span class="sxs-lookup"><span data-stu-id="d9b48-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="d9b48-112">在 **产品名称** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d9b48-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="d9b48-113">产品名称默认为搜索名称。</span><span class="sxs-lookup"><span data-stu-id="d9b48-113">The product name defaults to the search name.</span></span> <span data-ttu-id="d9b48-114">可以根据需要更改。</span><span class="sxs-lookup"><span data-stu-id="d9b48-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="d9b48-115">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d9b48-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="d9b48-116">设置维度组</span><span class="sxs-lookup"><span data-stu-id="d9b48-116">Set up dimension groups</span></span>
1. <span data-ttu-id="d9b48-117">单击 **维度组** 以打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="d9b48-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="d9b48-118">在 **存储维度组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d9b48-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="d9b48-119">存储维度组确定哪些存储维度您必须在产品的每个交易记录中输入，以及如何在库存中跟踪。</span><span class="sxs-lookup"><span data-stu-id="d9b48-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="d9b48-120">在 **跟踪维度组** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d9b48-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="d9b48-121">跟踪维度组确定哪些跟踪维度您必须为产品的每个交易记录输入，以及如何在库存中处置。</span><span class="sxs-lookup"><span data-stu-id="d9b48-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="d9b48-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d9b48-122">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]