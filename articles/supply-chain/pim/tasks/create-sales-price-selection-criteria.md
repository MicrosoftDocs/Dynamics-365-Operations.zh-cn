---
title: 创建销售价选择条件
description: 此过程显示如何为基于属性的销售价模型创建销售价选择条件。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60a7c7230d4eb57d840121f6ee490bf829e0dc8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999648"
---
# <a name="create-sales-price-selection-criteria"></a>创建销售价选择条件

[!include [banner](../../includes/banner.md)]

此过程显示如何为基于属性的销售价模型创建销售价选择条件。 此过程要求至少有一个销售价模型可用。 此示例使用 USMF 演示数据公司中的扬声器解决方案销售价模型的价格模型。 通常，产品经理使用此过程。


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>为现有销售价模型添加新条件
1. 单击“产品变型模型定义”。
2. 单击“产品配置模型”。
3. 在此列表中，选择扬声器解决方案产品模型的行，但是不单击模型名称的链接。
4. 在“操作窗格”上单击“模型”。
5. 单击“价格模型条件”。
6. 单击“新建”。
7. 在“名称”字段中，键入“客户组 10”。
    * 价格模型条件的名称用于帮助识别基础选择条件。  
8. 在“价格模型”字段中，输入或选择一个值。
9. 在“订单类型”字段中选择“销售订单”。
    * 订单类型确定将可用于选择查询的数据库字段。  
10. 在“生效日期”字段中输入日期。
11. 在“到期日期”字段中输入日期。
12. 单击“保存”。

## <a name="create-the-query-for-the-selection-criteria"></a>为选择条件创建查询
1. 单击“编辑”。
2. 在“表”字段中，选择“客户”。 
3. 在“字段”字段中，选择“客户组”。
    * 在此示例中，我们为选择条件使用特定客户组。  
4. 在“条件”字段中，选择“客户组 10”。 
5. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]