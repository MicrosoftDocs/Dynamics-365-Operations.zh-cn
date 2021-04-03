---
title: 创建产品生命周期状态以从主计划中排除产品
description: 此过程显示如何创建从主计划和物料清单级别计算中排除产品的新产品生命周期状态。
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
ms.openlocfilehash: fc24aad05499adf9bfb2db3613c7f134c3a70770
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264690"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>创建产品生命周期状态以从主计划中排除产品

[!include [banner](../../includes/banner.md)]

此过程显示如何创建从主计划和物料清单级别计算中排除产品的新产品生命周期状态。


## <a name="create-an-obsolete-state"></a>创建过时状态
1. 转到“产品信息管理”>“设置”>“产品生命周期状态”。
2. 单击“新建”。
3. 在“状态”字段中，键入一个值。
4. 在“对于计划有效”字段中选择“否”。
5. 在“描述”字段中，键入一个值。

## <a name="associate-the-obsolete-state-to-a-released-product"></a>将过时状态与已发布产品关联
1. 关闭该页面。
2. 转到“产品信息管理”>“产品”>“已发布产品”。
3. 使用“快速筛选器”以查找记录。 例如，使用值“M00”在“搜索名称”字段中进行筛选。
4. 单击“编辑”。
5. 在列表中，标记所选的行。
6. 在“产品生命周期状态”字段中，输入或选择一个值。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]