---
title: 创建新产品
description: 此任务显示如何创建新的共享的产品。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548408"
---
# <a name="create-a-new-product"></a>创建新产品

[!include [task guide banner](../../includes/task-guide-banner.md)]

此任务显示如何创建新的共享的产品。 它通常由产品设计器执行。 创建此任务的演示数据公司是 USMF。

1. 转到“产品信息管理”>“产品”>“产品”。

## <a name="create-a-product"></a>创建产品
1. 单击“新建”。
2. 在“产品编号”字段中，键入一个值。
    * 如果编号规则没有为产品编号设置，必须手动输入它。  
3. 在“产品名称”字段中，键入一个值。
    * 产品名称默认为搜索名称。 可以根据需要更改。  
4. 单击“确定”。

## <a name="set-up-dimension-groups"></a>设置维度组
1. 单击“维度组”以打开下拉对话框。
2. 在“存储维度组”字段中，输入或选择一个值。
    * 存储维度组确定哪些存储维度您必须在产品的每个交易记录中输入，以及如何在库存中跟踪。  
3. 在“跟踪维度组”字段中，输入或选择一个值。
    * 跟踪维度组确定哪些跟踪维度您必须为产品的每个交易记录输入，以及如何在库存中处置。  
4. 单击“确定”。

