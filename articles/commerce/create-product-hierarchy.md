---
title: 创建新产品层次结构
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品层次结构。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c7d0c792a8590be474b05dea262ae11d15e0ada3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965194"
---
# <a name="create-a-new-product-hierarchy"></a>创建新产品层次结构


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品层次结构。

## <a name="overview"></a>概览

Dynamics 365 Commerce 支持多种零售渠道。 这些零售渠道包括在线商店、呼叫中心和零售商店（亦称实体商店）。 每个零售商店渠道都可以有自己的付款方式、价格组、销售点 (POS) 收银机、收入帐户和支出帐户以及职员。 您必须先设置所有这些元素，然后才能创建零售商店渠道。 

商业产品层次结构用于定义您的组织的整个产品层次结构。 您可以为促销活动、定价和促销、报告和分类计划使用此商业产品层次结构。 只能为每个组织分配一个商业产品层次结构。

## <a name="create-and-configure-a-product-hierarchy"></a>创建和配置产品层次结构

要创建和配置商业产品层次结构，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 商业产品层次结构**。
1. 如果还不存在层次结构，则在 **操作窗格** 上选择 **新建** 以创建层次结构的根。
1. 在 **常规** 下面：
    1. 在 **名称** 框中，输入名称。
    1. 在 **描述** 框中，输入描述。
    1. 在 **友好名称** 框中，输入友好名称。
    1. 将 **有效** 设置为 **是**。

## <a name="add-hierarchy-nodes"></a>添加层次结构节点

若要添加层次结构节点，请按照下列步骤操作。

1. 在操作窗格上选择 **编辑类别层次结构**。
1. 选择要向其添加新节点的父节点，然后选择 **新类别节点**。
1. 在 **常规** 部分中，提供 **名称**、**描述**、**友好名称** 和 **关键字**。
1. 在 **常规** 下面：
    1. 在 **名称** 框中，输入名称。
    1. 在 **描述** 框中，输入描述。
    1. 在 **友好名称** 框中，输入友好名称。
    1. 在 **关键字** 框中，输入相关关键字。
    1. 在 **显示顺序** 框中，输入显示顺序编号（可选）。
1. 在操作窗格上，选择 **保存**。
1. 重复上述步骤以添加其他节点。

下图显示了新产品层次结构节点的创建过程。

![创建产品层次结构](media/create-product-hierarchy.png)

## <a name="other-settings"></a>其他设置

类别属性组也可以根据需要分配给每个组。  

## <a name="additional-resources"></a>其他资源

[Commerce 层次结构](retail-hierarchies.md)

[管理产品类别和产品](category-management-product-creation.md)

[更改促销实体的排序顺序](custom-order-categories-nav-retail-prod-hierarchy.md)
