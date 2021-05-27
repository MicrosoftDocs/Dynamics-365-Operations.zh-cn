---
title: TaxTrans 中的不正确字段值
description: 本主题提供有关解决 TaxTrans 中的不正确字段值的信息。
author: bijian
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 488ff54f1dd99208db940024a2fe8b2d25861f44
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020155"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="10442-103">TaxTrans 中的不正确字段值</span><span class="sxs-lookup"><span data-stu-id="10442-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10442-104">如果 **TaxTrans** 中的字段值不正确，请使用本主题中的信息来尝试解决此问题。</span><span class="sxs-lookup"><span data-stu-id="10442-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="10442-105">值概览</span><span class="sxs-lookup"><span data-stu-id="10442-105">Overview of values</span></span>
<span data-ttu-id="10442-106">以下列表显示了 **TaxTrans**、**TaxUncommitted** 和 **TmpTaxWorkTrans** 是怎样的相似数据集，其工作方式不同。</span><span class="sxs-lookup"><span data-stu-id="10442-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="10442-107">**TaxTrans** 是数据库中一直保留的最终的已过帐税收交易结果。</span><span class="sxs-lookup"><span data-stu-id="10442-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="10442-108">**TaxUncommitted** 是数据库中持续保留的中间的计算得出的税收结果（如果适用），以后将在过帐中使用。</span><span class="sxs-lookup"><span data-stu-id="10442-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="10442-109">**TmpTaxWorkTrans** 是内存表中临时的计算得出的税收结果（表类型 = InMemory）。</span><span class="sxs-lookup"><span data-stu-id="10442-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="10442-110">如果您发现 **TaxTrans** 列不正确的根本原因，那么您同时也找到了 **TaxUncommitted** 或 **TmpTaxWorkTrans** 列不正确的根本原因。</span><span class="sxs-lookup"><span data-stu-id="10442-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="10442-111">这是因为这三个列是相互复制的。</span><span class="sxs-lookup"><span data-stu-id="10442-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="10442-112">通常，在计算税款时，将生成 **TmpTaxWorkTrans**，然后生成 **TaxUncommitted**（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="10442-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="10442-113">在税款过帐期间，生成 **TaxTrans**。</span><span class="sxs-lookup"><span data-stu-id="10442-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="10442-114">添加中断点</span><span class="sxs-lookup"><span data-stu-id="10442-114">Add breakpoints</span></span>
<span data-ttu-id="10442-115">要添加中断点，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="10442-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="10442-116">在扩展名中的 *insert()* 和 *update()* 中添加扩展名和中断点，如下所示。</span><span class="sxs-lookup"><span data-stu-id="10442-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="10442-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="10442-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="10442-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="10442-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="10442-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="10442-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="10442-120">或者，您可以在未包括 **TaxUncommitted** 时直接添加中断点。</span><span class="sxs-lookup"><span data-stu-id="10442-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="10442-121">*TaxTrans.insert()*、*TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="10442-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="10442-122">*TmpTaxWorkTrans.insert()*、*TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="10442-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="10442-123">重现和调试</span><span class="sxs-lookup"><span data-stu-id="10442-123">Reproduce and debug</span></span>

<span data-ttu-id="10442-124">设置中断点后，在调试过程中可以看到每个数据持久性变化。</span><span class="sxs-lookup"><span data-stu-id="10442-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="10442-125">要查找 **TaxTrans**、**TaxUncommitted** 或 **TmpTaxWorkTrans** 列不正确的根本原因，请查看并注意以下各项：</span><span class="sxs-lookup"><span data-stu-id="10442-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="10442-126">列正确的最后一个中断点。</span><span class="sxs-lookup"><span data-stu-id="10442-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="10442-127">列不正确的第一个中断点。</span><span class="sxs-lookup"><span data-stu-id="10442-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="10442-128">在这两个点之间发生了什么。</span><span class="sxs-lookup"><span data-stu-id="10442-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="10442-129">确定是否存在自定义</span><span class="sxs-lookup"><span data-stu-id="10442-129">Determine whether customization exists</span></span>
<span data-ttu-id="10442-130">如果您已经完成了前面几节中的步骤，但还不能解决问题，请确定是否存在自定义。</span><span class="sxs-lookup"><span data-stu-id="10442-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="10442-131">如果不存在自定义，请联系 Microsoft 支持部门寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="10442-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

