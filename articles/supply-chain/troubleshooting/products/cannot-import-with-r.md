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
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764684"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>您不能使用已发布产品 V2 实体导入物料

知识库编号：4611825

## <a name="symptoms"></a>故障特征

当您尝试使用 *已发布产品 V2* 实体导入物料时，将收到类似于以下示例的错误消息：

> 无法在“物料 - 跟踪维度组”(EcoResTrackingDimensionGroupItem) 中创建记录。 物料编号：2040663，批。 该记录已存在。

## <a name="resolution"></a>解决方法

要导入新的已发布产品，您必须使用 *已发布产品创建 V2* 实体而不是 *已发布产品 V2* 实体。
