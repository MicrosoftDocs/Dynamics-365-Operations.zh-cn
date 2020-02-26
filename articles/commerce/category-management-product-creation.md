---
title: 管理产品类别和产品
description: 此主题介绍促销活动经理如何使用产品类别管理商业产品层次结构与发布的产品详细信息之间的关系。
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6e0c6a8048b5a2ef9a48495cd5e2609a1324a6e2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021705"
---
# <a name="manage-product-categories-and-products"></a>管理产品类别和产品

[!include [banner](./includes/banner.md)]

此主题介绍如何在 Dynamics 365 Commerce 中通过改进的方法管理产品类别和产品。 这些改进使促销活动经理可以查看产品层次结构与已发布的产品详细信息之间共有的产品属性结构。

若要了解有关如何管理产品类别的更多信息，请在**类别和产品管理**工作区中选择**商业产品层次结构**磁贴。

请注意显示的**商业产品层次结构**页的增强结构。 在以前的应用版本中，产品属性基于其适用范围划分为*基本产品属性*和*零售产品属性*。 零售产品属性的适用范围为*全局*。 换言之，对于给定的产品属性，在所有法人之间共享相同的值。 比较而言，基本产品属性是*特定于法人的*。 换言之，对于给定基本产品属性，不同法人之间的值可能不同，具体取决于各法人各自的业务需求。

在改进的产品类别结构中，产品属性基于其在组中的适用性分隔，以反映已发布产品详细信息窗体结构的结构。

![基于属性适用范围分组的字段](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

您可以在跨所有法人管理法人特定属性与针对特定法人进行管理之间进行切换。

若要管理所有法人的属性，请选择**查看所有法人**（或 **编辑所有法人**）。

![查看/编辑所有法人](media/ToggleBackToEditForSpecificLegalEntity.PNG)

若要管理特定法人的属性，请选择**查看特定法人**（或**编辑特定法人**）。

![查看/编辑特定法人](media/ToggleToEditForAllLegalEntities.PNG)

此外，在增强的产品类别结构中，促销活动经理现在可以在单个类别级别再为一组产品属性定义默认值。 然后，创建产品时，产品将根据其产品属性与产品层次结构中的单个类别的关联，继承这些属性的默认值。 还可以针对每个产品修改这些继承的产品属性，以满足单独的业务要求。

## <a name="selecting-properties-to-update-products-on-the-commerce-product-hierarchy-page"></a>在商业产品层次结构页中选择要更新产品的属性。

可使用这个新改进的产品属性结构选择必须将哪些更新的产品属性推送到关联的产品。 在**商业产品层次结构**页上的操作窗格中，选择**类别**，然后选择**更新产品**以打开**更新产品**对话框。

![“更新产品”对话框](media/NewUpdateProductsEnhancedView.PNG)
