---
title: "产品类别管理和创建"
description: "此主题描述对零售产品类别的管理体验进行的改进。 这些改进使促销活动经理在零售产品层次结构与已发布的产品详细信息之间具有相关性。"
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 6b9afb40b68b672514c083d99efbc9bd098dd561
ms.openlocfilehash: b158ff5b277c125e0aa158c071007ed8a0f25482
ms.contentlocale: zh-cn
ms.lasthandoff: 10/03/2017

---

# <a name="product-category-management-and-creation"></a>产品类别管理和创建

[!include[banner](./includes/banner.md)]

对零售产品类别的管理体验进行的改进使促销活动经理在零售产品层次结构与已发布的产品详细信息之间具有相关性。 若要查看这些改进，在**类别和产品管理**工作区，选择**零售产品层次结构**以打开**零售产品类别的新结构**页。 

在以前的版本中，产品属性基于其适用范围划分为基本产品属性和零售产品属性。 零售产品属性为*全局*。 换言之，对于给定的产品属性，在所有法人之间共享相同的值。 基本产品属性是*法人 - 特定*。 换言之，基于各个业务需求，不同法人之间的给定产品属性可能不同。

通过这些改进，对于零售产品类别的产品属性，我们继续基于其在一个组中的适用性分隔字段，以反映已发布产品详细信息窗体结构。

您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。 只需根据需要选择**查看/编辑所有法人**或**查看/编辑特定法人**。

促销活动经理还可以在个别类别级别定义一组附加产品属性的默认值。 在产品创建时，这些属性值由产品基于其与类别之间的关联继承。

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a>从零售产品类别窗体中选择要更新产品的属性。

您可以使用逻辑分组属性来选择应推送到关联产品的更新的产品属性。

促销活动经理可以对每个产品修改这些继承的产品属性，以满足单独的业务要求。

