---
title: 对已发布的基础产品分配产品生命周期状态
description: 此过程显示如何将产品生命周期状态分配给已发布的基础产品及其变型。
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992212"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>对已发布的基础产品分配产品生命周期状态

[!include [banner](../../includes/banner.md)]

此过程显示如何将产品生命周期状态分配给已发布的基础产品及其变型。 先决条件：您需要先播放任务指南“创建新的产品生命周期状态”以确保至少创建了一个产品生命周期状态，然后才可以播放此任务指南。


## <a name="find-a-released-product-master"></a>查找已发布的基础产品
1. 转到“产品信息管理”>“产品”>“已发布产品”。
2. 在列表中，找到并选择所需记录。

> [!NOTE]
> 基础产品包含产品子类型基础产品。  

## <a name="update-the-lifecycle-state"></a>更新生命周期状态
1. 单击“编辑”。
2. 在“产品生命周期状态”字段中，输入或选择一个值。
3. 单击“保存”。
4. 单击“是”。

> [!NOTE]
> 如果选择“是”，与已发布基础产品具有相同原始状态的所有相关的已发布产品变型也会更新到新的产品生命周期状态。 如果选择“否”，所有变型都会保留其实际状态。 具有与已发布基础产品不同的产品生命周期状态的变型不会更新。  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>验证变型的生命周期状态
1. 单击“已发布的产品变型”。

> [!NOTE]
> 请注意，所有变型均已从发布的基础产品继承所选生命周期状态。  

2. 在列表中，标记所选的行。
3. 在“产品生命周期状态”字段中，输入或选择一个值。

