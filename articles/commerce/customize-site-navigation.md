---
title: 自定义站点导航
description: 此主题介绍如何创建自定义的在线导航层次结构，以便组织产品以在 Microsoft Dynamics 365 Commerce 站点中进行浏览。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8af68fff17f2f92356ade356da0e75867ed54950d744c6cbe730ad8db4ac3975
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755874"
---
# <a name="customize-site-navigation"></a>自定义站点导航

[!include [banner](includes/banner.md)]

此主题介绍如何创建自定义的在线导航层次结构，以便组织产品以在 Microsoft Dynamics 365 Commerce 站点中进行浏览。

客户通常可使用在线店面通过浏览产品类别发现和浏览产品。 此功能通常在页面顶部的选项卡或左侧导航栏中提供。 在 Dynamics 365 Commerce 中，可创建和管理类别导航的分层结构和各类别中包含的产品。

## <a name="create-a-channel-navigation-hierarchy"></a>创建渠道导航层次结构

若要创建渠道导航层次结构，请执行以下步骤。

1. 转至 **Retail 和 Commerce \> 产品和类别 \> 类别和产品管理**。
1. 选择 **类别层次结构**，然后选择 **新建**。
1. 为层次结构命名。

    > [!NOTE]
    > 您创建的最高级别类别是根类别节点。 不会在您的站点中显示。 若要创建其中的站点上显示一个顶级节点的类别层次结构，请创建类别作为根类别的子代并为其命名。

1. 选择 **新建类别节点**，然后为类别命名。
1. 根据需要继续创建同级类别和子类别。

现在可将产品分配给顶级类别下创建的每个类别。

## <a name="customize-the-order-of-categories"></a>自定义类别顺序

默认情况下，您的站点中按字母顺序显示您定义的类别。 但是，也可以自定义类别的显示顺序。

## <a name="assign-a-category-hierarchy-type"></a>分配某个类别层次机构类型

1. 转至 **Retail 和 Commerce \> 产品和类别 \> 类别和产品管理**。
1. 选择 **类别层次结构**。
1. 在操作窗格中 **类别层次结构** 选项卡上的 **设置** 组中，选择 **关联层次结构类型**。
1. 选择 **新建**。
1. 在 **类别层次结构类型** 字段中，选择 **渠道导航层次结构**。
1. 在 **类别层次结构** 字段中，选择前面创建的渠道导航层次结构。

## <a name="publish-new-or-updated-navigation-hierarchies"></a>发布新的或更新后的导航层次结构

若要使导航层次结构可供在线店面使用，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 渠道设置 \> 渠道类别和产品属性**。
1. 在左侧树中，选择您的在线商店。
1. 选择 **发布渠道更新**。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。
1. 在列表中，找到并选择 **作业 1040**。
1. 选择 **立即运行**。
1. 对作业 1070 和 1150 重复执行步骤 5 和 6。

## <a name="show-categories-on-your-site"></a>在站点中显示类别

若要在在线店面中显示类别层次结构，必须在模板或片段中的相应位置添加导航菜单模块。 然后，如果已将导航层次结构发布到站点绑定到的渠道，导航菜单模块将显示您的导航层次结构。

> [!NOTE]
> 用户可使用模块库中包含的导航菜单模块仅导航到没有子类别的类别。 如果客户应该可以导航到有子类别的类别，则必须自定义导航菜单模块。

## <a name="add-custom-navigation-options"></a>添加自定义导航选项

在导航菜单中，可添加不属于产品类别层次结构的导航选项。 例如，可在产品类别列表结尾添加指向为站点生成的联系页的 **联系我们** 项。

若要向导航菜单添加自定义导航选项，请执行以下步骤。

1. 在要自定义的模板或片段中，选择导航菜单模块。
1. 在属性窗格中的 **数据** 选项卡上，选择 **添加项** 以创建新的内容管理系统 (CMS) 导航项。
1. 输入链接文本和 URL。
1. 重复执行步骤 2 和 3 以添加更多自定义导航选项。
1. 完成后，选择 **保存** 以保存模板或片段，然后选择 **完成编辑** 将其签入。

## <a name="additional-resources"></a>其他资源

[模板和布局概览](templates-layouts-overview.md)

[使用模板](work-with-templates.md)

[使用预设布局](work-with-layouts.md)

[使用片段](work-with-fragments.md)

[使用模块](work-with-modules.md)

[创建页面 URL](create-page-url.md)

[使用发布组](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
