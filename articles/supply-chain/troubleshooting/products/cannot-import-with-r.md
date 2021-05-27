---
title: 您不能使用已发布产品 V2 实体导入物料
description: 您不能使用已发布产品 V2 实体导入物料。
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026295"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>您不能使用已发布产品 V2 实体导入物料

知识库编号：4611825

## <a name="symptoms"></a>故障特征

当您尝试使用 *已发布产品 V2* 实体导入物料时，将收到类似于以下示例的错误消息：

> 无法在“物料 - 跟踪维度组”(EcoResTrackingDimensionGroupItem) 中创建记录。 物料编号：2040663，批。 该记录已存在。

## <a name="resolution"></a>解决方法

要导入新的已发布产品，您必须使用 *已发布产品创建 V2* 实体而不是 *已发布产品 V2* 实体。
