---
title: 创建默认的产品生命周期状态
description: 此过程显示如何创建默认产品生命周期状态以及如何将默认状态与已发布产品关联。
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e7e637157ee06a3d07a1a9c5da71295eb75b424
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564170"
---
# <a name="create-a-default-product-lifecycle-state"></a>创建默认的产品生命周期状态

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何创建默认产品生命周期状态以及如何将默认状态与已发布产品关联。


## <a name="create-a-default-lifecycle-state"></a>创建默认的生命周期状态
1. 转到“产品信息管理”>“设置”>“产品生命周期状态”。
2. 单击“新建”。
3. 在“状态”字段中，键入一个值。
4. 在发布到“法人”字段时在“默认”中选择“是”。
5. 在“描述”字段中，键入一个值。
6. 在“对于计划有效”字段中选择“否”。

> [!NOTE]
> 如果新发布的产品不应包含在主计划中，请选择“否”。 如果应包含在主计划中，则将控制留为默认值“是”。  

## <a name="create-a-new-released-product"></a>创建新的已发布产品
1. 关闭该页面。
2. 转到“产品信息管理”>“产品”>“已发布产品”。
3. 单击“新建”。
4. 在“产品编号”字段中，键入一个值。
5. 在“产品名称”字段中，键入一个值。
6. 在“搜索名称”字段中，键入一个值。
7. 在“物料模型组”字段中，输入或选择一个值。
8. 在“物料组”字段中，输入或选择一个值。
9. 在“存储维度组”字段中，输入或选择一个值。
10. 在“跟踪维度组”字段中，输入或选择一个值。
11. 单击“确定”。

> [!NOTE]
> 默认产品生命周期状态是一种全局定义。  

## <a name="change-the-product-to-an-active-state"></a>将产品更改为有效状态
1. 在“产品生命周期状态”字段中，输入或选择一个值。

> [!NOTE]
> 假设您设置了活动状态，您现在可以选择此活动状态来允许产品用于主计划和物料清单级别计算。 显然，这只在为一致计划指定了所需的所有产品详细信息时才有意义。  

