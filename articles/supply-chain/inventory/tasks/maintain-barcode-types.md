---
title: 维护条码类型
description: 该过程显示如何设置新条码定义，这可作为领料单报表的一部分。
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 979726a1d094146b546bbc6d31963367de2c59f5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423257"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="6249f-103">维护条码类型</span><span class="sxs-lookup"><span data-stu-id="6249f-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6249f-104">该过程显示如何设置新条码定义，这可作为领料单报表的一部分。</span><span class="sxs-lookup"><span data-stu-id="6249f-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="6249f-105">您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。</span><span class="sxs-lookup"><span data-stu-id="6249f-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="6249f-106">如果您正在使用 USMF，则可以使用显示的示例值。</span><span class="sxs-lookup"><span data-stu-id="6249f-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="6249f-107">这些任务通常由仓库管理员完成。</span><span class="sxs-lookup"><span data-stu-id="6249f-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="6249f-108">转到“条码”。</span><span class="sxs-lookup"><span data-stu-id="6249f-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="6249f-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="6249f-109">Click New.</span></span>
3. <span data-ttu-id="6249f-110">在“条码设置”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6249f-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="6249f-111">在“描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="6249f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6249f-112">在“条码类型”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="6249f-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="6249f-113">如果您使用 USMF，您可以选择“代码 39”。</span><span class="sxs-lookup"><span data-stu-id="6249f-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="6249f-114">在“大小”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6249f-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="6249f-115">在“最大长度”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="6249f-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="6249f-116">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6249f-116">Click Save.</span></span>
9. <span data-ttu-id="6249f-117">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6249f-117">Close the page.</span></span>
10. <span data-ttu-id="6249f-118">转到“库存和仓库管理参数”。</span><span class="sxs-lookup"><span data-stu-id="6249f-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="6249f-119">在“条码设置”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="6249f-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="6249f-120">选择您先前创建的条码设置，但请注意，条码格式必须匹配流程中使用的记录类型的唯一标识符的格式。</span><span class="sxs-lookup"><span data-stu-id="6249f-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="6249f-121">例如，对于领料路径，条码格式必须匹配领料路径引用的格式，这通常为一个序号。</span><span class="sxs-lookup"><span data-stu-id="6249f-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="6249f-122">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="6249f-122">Click Save.</span></span>
13. <span data-ttu-id="6249f-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="6249f-123">Close the page.</span></span>

