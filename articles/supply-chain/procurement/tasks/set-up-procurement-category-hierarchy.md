---
title: 设置采购类别层次结构
description: 该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。
author: mkirknel
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e45c80718c73ad785643c2a5fc0e712b291104d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423292"
---
# <a name="set-up-a-procurement-category-hierarchy"></a>设置采购类别层次结构

[!include [banner](../../includes/banner.md)]

该过程会显示如何在采购类别层次结构中创建新节点，以及如何配置采购类别以用于采购流程。 这些任务通常由采购经理完成。 在您开始该过程之前，采购类型层次结构必须存在。 如果您正在使用公司演示数据，则您可以在 USMF 公司中执行该过程。


## <a name="add-a-new-procurement-category"></a>添加新采购类别
1. 转到 **导航窗格 > 模块 > 采购 > 托运 > 采购目录**。
2. 在操作窗格上选择 **编辑类别层次结构**。 当前采购类别层次结构会显示在页左侧。 您即将修改该层次结构。  
3. 在操作窗格上选择 **新建类别节点**。 系统会默认选择顶端节点。 如果您正在运行该过程以作为任务指南，您可以单击“解除锁定”按钮，并选择另一个父节点，以插入您的新节点。 一旦完成此项操作，再次锁定任务指南，然后单击“新类别节点”。  
4. 在 **名称** 字段中，键入一个值。
5. 在 **描述** 字段中，键入一个值。
6. 在 **易记名称** 字段中，键入一个值。 易记名称是可选的。 它将连同类别名称一起显示在类别查找中。  
7. 选择 **保存**。

## <a name="add-products-to-your-new-procurement-category"></a>添加产品到您的新采购类别
1. 转到 **采购和购置 > 托运 > 采购类别**。 选择您刚添加的节点。 如果您正在运行该过程以作为任务指南，您可能需要解除任务指南锁定，以选择节点。  
2. 切换 **产品** 部分的展开项。
3. 选择 **添加** 以关联产品和采购类别。
4. 选择您想要添加到采购类别的产品。
5. 选择箭头以将产品添加到 **所选** 表中。
6. 选择 **确定**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]