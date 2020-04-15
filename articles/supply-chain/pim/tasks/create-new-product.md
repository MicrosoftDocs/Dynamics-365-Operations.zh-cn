---
title: 创建新产品
description: 此主题描述如何创建新共享产品。
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 611fc0cff7fe2d580e971149630e92afd16be228
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147840"
---
# <a name="create-a-new-product"></a>创建新产品

[!include [banner](../../includes/banner.md)]

此主题描述如何创建新共享产品。 它通常由产品设计器执行。 创建此任务的演示数据公司是 USMF。


## <a name="create-a-product"></a>创建产品
1. 在导航窗格中，转到**导航窗格 > 模块 > 产品信息管理 > 产品 > 产品**。
2. 选择**新建**。
3. 在**产品编号**字段中，键入一个值。 如果编号规则没有为产品编号设置，必须手动输入它。  
4. 在**产品名称**字段中，键入一个值。 产品名称默认为搜索名称。 可以根据需要更改。  
5. 选择**确定**。

## <a name="set-up-dimension-groups"></a>设置维度组
1. 单击**维度组**以打开下拉对话框。
2. 在**存储维度组**字段中，输入或选择一个值。 存储维度组确定哪些存储维度您必须在产品的每个交易记录中输入，以及如何在库存中跟踪。  
3. 在**跟踪维度组**字段中，输入或选择一个值。 跟踪维度组确定哪些跟踪维度您必须为产品的每个交易记录输入，以及如何在库存中处置。  
4. 选择**确定**。

