---
title: 零售报表的付款配置
description: 此程序会演示 Commerce 商店付款方式的配置（这会影响到如何创建和过帐对帐单）。
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3c8c7678d88b3c01138aa098b8830336885e6445fb41931b19bcda2b95b86b5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712349"
---
# <a name="payment-configurations-for-retail-statements"></a>零售报表的付款配置

[!include [banner](../includes/banner.md)]

此程序会演示 Commerce 商店付款方式的配置（这会影响到如何创建和过帐对帐单）。

此记录使用 USRT 演示公司。

1. 转至“Retail 和 Commerce”>“渠道”>“商店”>“所有商店”。
2. 在列表中，找到并选择所需记录。
3. 在列表中，单击所选行中的链接。
4. 单击“操作窗格”上的“设置”。
5. 单击“付款方式”。
6. 展开或折叠“过帐”部分。
7. 单击“编辑”。
    * 选择此付款方式收到的金额是否应过帐到会计科目或银行科目。  
    * 选择此付款方式收到的金额应过帐到的科目。  
    * 选择一个科目，以过帐收到的总交易金额与用于此付款方式盘点的金额之间的可能差额。  
    * 在此字段中，您可以输入一个金额，以控制何时将差异金额过帐到其他差额科目。 您可以使用这个跟踪较大差额。  
    * 选择一个科目，以便在超过“最大差额”字段中定义的值时，过帐收到的总交易金额与盘点金额之间的可能差额。  
    * 选择“是”，以将银行投箱金额过帐到单独的科目。  
    * 在此字段中，您可以选择是否应将收到的银行投箱金额过帐到会计科目或银行科目。  
    * 选择将银行投箱金额过帐到其中的科目。  
    * 选择在将银行投箱金额过帐到银行科目时使用的银行交易类型。  
    * 选择“是”，以将金库投箱金额过帐到单独的科目。  
    * 选择是否应将金库投箱金额过帐到会计科目或银行科目。  
    * 选择将金库投箱金额过帐到其中的科目。  
8. 单击“保存”。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]