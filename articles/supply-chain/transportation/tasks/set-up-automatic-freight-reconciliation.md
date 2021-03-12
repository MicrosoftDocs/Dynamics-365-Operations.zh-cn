---
title: 设置自动装运对帐
description: 此过程显示如何为自动货运对帐设置数据。
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSFreightBillTypeAssignment, TMSCarrierCodeLookup, DefaultDashboard, TMSAuditMaster
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bfd96fcae78fd0fe383781112c17c7a3b5ea1d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974002"
---
# <a name="set-up-automatic-freight-reconciliation"></a>设置自动装运对帐

[!include [banner](../../includes/banner.md)]

此过程显示如何为自动货运对帐设置数据。 此操作通常由仓库经理完成。 您可以在演示数据公司 USMF 中使用此过程。


## <a name="set-up-the-freight-bill-type"></a>设置货运帐单类型
1. 转到“运输管理”>“设置”>“货运对帐”>“货运帐单类型”。
    * 货运帐单类型定义应如何匹配货运帐单和承运人发票。  
2. 单击“新建”。
3. 在“货运帐单类型”字段中，键入一个值。
4. 在“引擎程序集”字段中，键入“Microsoft.Dynamics.Ax.Tms.dll”。
    * 这是标准运输管理匹配引擎代码库。  
5. 在“引擎类”字段中，键入“Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer”。
    * 这是标准运输管理匹配引擎类。  
6. 单击“新建”。
7. 在"描述"字段中，选择在货运帐单和承运人发票上应匹配的值。  
8. 在“需要匹配”字段中选择“是”。
    * 如果将此字段设置为“是”，则表示“描述”字段中选择的值在货运帐单和承运人发票上均匹配。 如果设置为“否”，此字段在其中一个上可以为空。  
9. 单击“保存”。

## <a name="set-up-the-freight-bill-type-assignment"></a>设置货运帐单类型分配
1. 关闭该页面。
2. 转到“运输管理”>“设置”>“货运对帐”>“货运帐单类型分配”。
    * 运费帐单类型分配用于指定为特定承运人使用哪种货运帐单类型。   
3. 单击“新建”。
4. 在“模式”字段中，输入或选择一个值。
5. 在“装运承运人”字段中，输入或选择一个值。
6. 在“货运帐单类型”字段中，选择您之前创建的货运帐单类型。
7. 关闭该页面。

## <a name="set-up-the-audit-master"></a>设置审计主数据
1. 转到“运输管理”>“设置”>“货运对帐”>“审计主数据”。
    * 审计主数据定义自动货运对帐的容差限制。 它指定货运帐单和承运人发票上可以相差多少货币金额的情况下仍然允许对帐。 还定义如何处理差异。  
2. 单击“新建”。
3. 在“审计主数据 ID”字段中，键入一个值。
4. 在“装运承运人”字段中，选择您之前选择的同一位装运承运人。
5. 在“货运帐单类型”字段中，选择您之前创建的货运帐单类型。
6. 展开“容差”部分。
7. 在“最小容差级别”字段中，输入一个数字。
8. 在“最大容差级别”字段中，输入一个数字。
9. 展开“结果”部分。
10. 在“超额支付原因代码”字段中，输入或选择一个值。
    * 如果货运帐单和承运人发票上的货币金额不同，则只要差值在容差级别内，超额支付和未足额支付原因代码将指定应登记的差异金额。  
11. 在“未足额支付原因代码”字段中，输入或选择一个值。
12. 关闭该页面。

