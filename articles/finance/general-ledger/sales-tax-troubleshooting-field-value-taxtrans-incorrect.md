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
# <a name="incorrect-field-value-in-taxtrans"></a>TaxTrans 中的不正确字段值

[!include [banner](../includes/banner.md)]

如果 **TaxTrans** 中的字段值不正确，请使用本主题中的信息来尝试解决此问题。

## <a name="overview-of-values"></a>值概览
以下列表显示了 **TaxTrans**、**TaxUncommitted** 和 **TmpTaxWorkTrans** 是怎样的相似数据集，其工作方式不同。

  - **TaxTrans** 是数据库中一直保留的最终的已过帐税收交易结果。
  - **TaxUncommitted** 是数据库中持续保留的中间的计算得出的税收结果（如果适用），以后将在过帐中使用。
  - **TmpTaxWorkTrans** 是内存表中临时的计算得出的税收结果（表类型 = InMemory）。

如果您发现 **TaxTrans** 列不正确的根本原因，那么您同时也找到了 **TaxUncommitted** 或 **TmpTaxWorkTrans** 列不正确的根本原因。 这是因为这三个列是相互复制的。

通常，在计算税款时，将生成 **TmpTaxWorkTrans**，然后生成 **TaxUncommitted**（如果适用）。 在税款过帐期间，生成 **TaxTrans**。


## <a name="add-breakpoints"></a>添加中断点
要添加中断点，请完成以下步骤： 

1. 在扩展名中的 *insert()* 和 *update()* 中添加扩展名和中断点，如下所示。

     - **TaxTrans**

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

     - **TaxUncommitted**

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

     - **TmpTaxWorkTrans**

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

2. 或者，您可以在未包括 **TaxUncommitted** 时直接添加中断点。

     - *TaxTrans.insert()*、*TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*、*TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>重现和调试

设置中断点后，在调试过程中可以看到每个数据持久性变化。 要查找 **TaxTrans**、**TaxUncommitted** 或 **TmpTaxWorkTrans** 列不正确的根本原因，请查看并注意以下各项：

- 列正确的最后一个中断点。
- 列不正确的第一个中断点。
- 在这两个点之间发生了什么。

## <a name="determine-whether-customization-exists"></a>确定是否存在自定义
如果您已经完成了前面几节中的步骤，但还不能解决问题，请确定是否存在自定义。 如果不存在自定义，请联系 Microsoft 支持部门寻求帮助。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

