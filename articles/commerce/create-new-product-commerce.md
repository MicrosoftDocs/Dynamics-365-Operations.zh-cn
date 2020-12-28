---
title: 在 Commerce 中创建新产品
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: eb2dd36c6149f2aa40305cd57eac060b232b09e5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410444"
---
# <a name="create-a-new-product-in-commerce"></a>在 Commerce 中创建新产品


[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中创建新产品。

## <a name="overview"></a>概览

产品主要由产品编号、名称和描述定义。 但是也需要其他数据以描述产品或服务：

## <a name="create-a-new-product"></a>创建新产品

1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 产品(按类别)**。
1. 在操作窗格上，选择 **新建**。
1. 在 **产品类别** 下拉列表中，选择 **项目** 或 **服务**。
1. 在 **产品子类型** 下拉列表中，选择 **产品**（如果产品没有任何变型）或 **基础产品**（如果产品将有变型）。
1. 在 **产品编号** 框中，输入产品编号（如果尚未预先填充）。
1. 在 **产品名称** 框中，输入产品名称。
1. 在 **搜索名称** 框中，输入搜索名称。
1. 在 **零售类别** 下拉列表中，选择适当的类别。
1. 如果产品是套件，请针对 **产品套件** 选择 **是**。
1. 如果产品子类型是基础产品，请设置 **产品维度组** 以包括支持的变型。 选项包括 **颜色**、**大小**、**样式** 和 **配置**。 如果需要，您可能需要创建其他产品维度组。
1. 在 **配置技术** 下拉列表中，选择适当的选项。
1. 选择 **确定**。

下图显示了添加的产品示例。

![创建产品](media/create-new-product.png)

添加产品后，可以为其设置其他数据，例如 **产品描述**、**变型组**、**维度组**、**产品属性** 和 **相关产品**。

下图显示了产品的其他详细信息。

![产品详细信息](media/create-new-product-2.png)

### <a name="create-product-variants"></a>创建产品变型

如果产品子类型是 **基础产品**，则需要创建特定变型。 

要创建产品变型，请执行以下步骤。

1. 在操作窗格上，选择 **产品变型**。
1. 如果在操作窗格上选择了变型组，请选择**变型建议*。
1. 选择您要为该产品支持的变型。
1. 选择 **创建**。

## <a name="release-a-product"></a>发布产品

要销售产品，必须先将其发布给法人。

1. 从产品页面中，选择 **发布产品**。

    ![发布产品](media/create-new-product-3.png)

1. 选择要发布的产品，然后选择 **下一个**。

    ![选择要发布的产品](media/create-new-product-4.png)

1. 选择要发布的产品变型集，然后选择 **下一个**。

    ![选择要发布的变型](media/create-new-product-5.png)

1. 选择法人，然后选择 **下一个**。

    ![选择法人](media/create-new-product-6.png)

1. 选择 **完成**。

    ![完成产品发布](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>配置发布的产品

发布产品后，将需要进一步的配置，包括为产品添加价格。

1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 已发布的产品(按类别)**。
1. 选择已发布产品的产品类别节点，然后从产品列表中选择产品。
1. 在操作窗格上，选择 **编辑**。
1. 在 **采购** 部分，配置所有必需的属性，包括 **单位**、**价钱** 和 **数量**。
1. 在操作窗格上，选择 **验证** 以确保没有报告字段缺失错误。
1. 在操作窗格上，选择 **保存**。

下图显示了一个已发布产品的配置示例。

![配置发布的产品](media/create-new-product-8.png)

## <a name="additional-resources"></a>其他资源

[创建法人](channels-legal-entities.md)

[创建变型组](create-variant-group.md) 
