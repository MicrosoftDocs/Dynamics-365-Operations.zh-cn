---
title: 创建渠道导航层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e43c4c00545dfecb2f9a2192f81cd25300e3d6e6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352462"
---
# <a name="create-a-channel-navigation-hierarchy"></a>创建渠道导航层次结构


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建渠道导航层次结构。

## <a name="overview"></a>概览

渠道导航层次结构用于按类别归组和组织产品，以便可以在线或在销售点 (POS) 中浏览产品。

## <a name="create-a-channel-navigation-hierarchy"></a>创建渠道导航层次结构

若要创建渠道导航层次结构，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 渠道导航类别**。
1. 在操作窗格上，选择 **新建**。
1. 在 **名称** 框中，输入名称。
1. 在 **描述** 框中，输入描述。
1. 选择 **创建**。
1. 在操作窗格中，选择 **新类别节点** 以创建根节点。
1. 在 **名称** 框中，输入名称。
1. 在 **描述** 框中，输入描述。
1. 在 **友好名称** 框中，输入友好名称。
1. 在操作窗格上，选择 **保存**。

下图显示了根节点示例。

![示例根节点。](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>创建导航类别节点

若要创建任何其他导航类别节点以表示渠道上的产品类别，请按照下列步骤操作。

1. 在导航窗格中，选择要将类别添加到的父节点。
1. 在操作窗格上选择 **新建类别模式**。
1. 在 **名称** 框中，输入名称。
1. 在 **描述** 框中，输入描述。
1. 在 **友好名称** 框中，输入友好名称。
1. 在 **显示顺序** 框中，输入显示顺序（可选）。
1. 在操作窗格上，选择 **保存**。

下图显示了完成的渠道导航层次结构的示例。

![示例渠道层次结构。](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>向类别节点添加产品

要将产品添加到类别节点，请按照下列步骤操作。

1. 选择类别节点。
1. 在 **产品** 下面，选择 **添加**。
1. 使用产品编号或产品名称找到要添加的新产品，然后选择 **确定**。
1. 在操作窗格上，选择 **保存**。

> [!NOTE]
> 将产品添加到渠道导航层次结构内的节点并不能让产品在所选渠道上显示，这些产品也必须归类为某个渠道。 有关分类的详细信息，请参阅[分类管理](assortments.md)。

下图显示了添加有产品的节点示例。

![添加到类别节点的产品。](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>将产品属性组添加到类别节点

> [!NOTE]
> 必须先创建属性组，然后才能将其添加到渠道导航层次结构内的节点。

要将产品属性组添加到类别节点，请执行以下步骤。

1. 选择类别节点。
1. 在 **产品属性组** 下面，选择 **添加**。
1. 找到您要添加的属性组，然后选择 **确定**。
1. 在操作窗格上，选择 **保存**。

下图显示了添加有产品属性组的示例节点。

![节点上的产品属性组。](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>其他资源

[设置分类](set-up-assortments.md)

[管理属性和属性组](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
