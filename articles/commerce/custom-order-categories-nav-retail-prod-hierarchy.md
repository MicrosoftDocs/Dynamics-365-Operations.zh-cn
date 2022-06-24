---
title: 更改促销实体的排序顺序
description: 本文介绍与在 Dynamics 365 Commerce 中控制各种促销相关实体的显示顺序有关的概念。
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4e7a7bd42b0ef72ae6bc3f52a8857602b6282907
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847646"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a>更改促销实体的排序顺序


[!Include [banner](includes/banner.md)]

零售商将产品发现视为所有渠道中的主要客户互动工具。 可通过大量功能帮助客户轻松发现产品。 例如，可以浏览类别，进行搜索或使用筛选。

本文介绍与控制各种促销相关实体的显示顺序有关的概念。 还介绍了如何更改排序顺序。

## <a name="overview"></a>概览

已对为促销关联的各种实体进行排序的支持进行了增强。 此项支持现在可以更好地适应以前要求实施合作伙伴进行扩展的现有客户方案。

在低于 10.0.5 的 Retail 版本中，导航层次结构中的类别按字母排序。 促销经理可使用新的自定义排序功能为所有最终用户客户的各种促销相关实体配置排序。 这些客户包括总部 (HQ) 和呼叫中心。

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a>配置产品层次结构中的类别的显示顺序

必须先在环境中安装演示数据，才能完成此过程。

1. 转至 **Retail 和 Commerce \> 产品和类别 \> 商业产品层次结构**。
2. 单击 **编辑类别层次结构**。
3. 单击 **编辑**。
4. 在树中，展开 **所有 \> 操作排序**。
5. 在树中，展开 **所有 \> 团队排序**。
6. 在 **显示顺序** 字段中，输入一个数字。 （该数字可以是负数。）
7. 对要更改其顺序的其他任何类别重复步骤 4 到 6。

将在商业产品层次结构和按类别的已发布产品的 HQ 中体现渠道导航层次结构的显示顺序。

![使用负值排序的产品层次结构自定义。](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![基于产品层次结构按类别自定义排序的已发布产品。](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a>配置渠道导航层次结构中的类别的显示顺序

必须先在环境中安装演示数据，才能完成此过程。

1. 转到 **Retail 和 Commerce \> 产品和类别 \> 渠道导航类别**。
2. 在列表中，选择 **时尚导航** 层次结构。
3. 单击 **编辑类别层次结构**。
4. 单击 **编辑**。
5. 在树中，选择 **时尚 \> 女装 \> 女鞋**。
6. 在 **显示顺序** 字段中，输入一个数字。
7. 在树中，选择 **时尚 \> 女装 \> 上装**。

    同样，可以为子类别定义排序顺序。

8. 在树中，选择 **时尚 \> 男装 \> 休闲衬衫**。
9. 在 **显示顺序** 字段中，输入一个数字。
10. 在树中，选择 **时尚 \> 男装 \> 外套和夹克**。
11. 在 **显示顺序** 字段中，输入一个数字。
12. 对要更改其顺序的其他任何类别重复此步骤。

将在 HQ、目录和渠道中体现渠道导航层次结构的显示顺序。

![已排序渠道导航层次结构自定义。](./media/ChannelNavCustomSorted.png)

![基于渠道导航层次结构排序的目录导航层次结构自定义。](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![具有自定义排序的类别的 POS。](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> 默认情况下，已关闭自定义排序顺序。 若要了解如何开启此功能和其他功能，请参阅[功能管理](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]