--- 
title: "设置帐簿"
description: "此过程显示如何创建新固定资产帐簿并将其与固定资产组关联。"
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a29cae6cdcd03903359a3a468243c6ad03c7adc6
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-books"></a>设置帐簿

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何创建新固定资产帐簿并将其与固定资产组关联。 它为 USMF 法人实体使用会计角色和演示数据。


## <a name="create-a-book"></a>创建帐簿
1. 转到“固定资产”>“设置”>“帐簿”。
2. 单击“新建”。
3. 在“帐簿”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
    * 如果选择“计算折旧”，关联资产帐簿将包含于折旧方案中。 如果未选择它，资产帐簿将不自动折旧。  
5. 在“计算折旧”字段中选择“是”。
6. 在“折旧模板”字段中，输入或选择一个值。
    * 备选折旧模板也称作折旧转换方法。 当备选模板计算等于或大于默认折旧模板的折旧金额时，折旧方案将切换到此模板。  
    * 异常折旧模板用于异常情况下资产的额外折旧。 例如，您可以使用此来记录自然灾害导致的折旧。  
    * 如果选择“使用基础调整创建折旧调整”，在资产价值更新时将自动创建折旧调整。 如果未选择它，更新资产价值将只影响后面的折旧计算。  
7. 在“使用基本调整创建折旧调整”字段中选择“是”。
    * 默认情况下，固定资产帐簿交易记录将过帐到总帐。 可以通过将“过帐到总帐”字段设置为“否”，为帐簿禁用过帐到总帐。 不过帐到总帐的帐簿通常用于报税用途。 这样您的灵活性更高，可以删除资产帐簿的历史交易信息，因为这些信息尚未提交给总帐。  
    * 如果帐簿过帐到总帐，则“过帐层”为“当前层”，否则为“无”。 如果您需要将此帐簿的交易过帐到不同层，则更新过帐层。  
8. 在“日历”字段中，输入或选择一个值。
    * 派生帐簿将把交易同时过帐到不同帐簿。 可以使用主要帐簿创建交易，并在过帐期间将一模一样的交易副本过帐到衍生帐簿。 不对衍生帐簿交易进行重新计算，所以不应将其用于折旧交易。  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>将帐簿与固定资产组关联
1. 单击“固定资产组”。
2. 在“固定资产组”字段中，输入或选择一个值。
3. 在“使用年限”字段中，输入一个数字。
    * 请注意，在设置使用年限后，计算“折旧期间”。  
    * 您可以为税务目的将折扣惯例设置为必需。  


