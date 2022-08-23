---
title: 创建款式组
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中为产品创建尺寸、样式或颜色变型组。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270092"
---
# <a name="create-a-variant-group"></a>创建款式组


[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中为产品创建尺寸、样式或颜色变型组。

## <a name="overview"></a>概览

Dynamics 365 Commerce 支持产品的多种变型。 最好是为不同的产品类别设置变型。 例如，可以为尺寸特小、较小、中等、较大和特大的 T 恤创建尺寸组，或者可以创建颜色组以包括产品的所有可用颜色。 添加产品之前，应添加变型组。

在本文中，将创建并配置一个尺寸组。 类似的过程可用于添加和配置样式组和颜色组。

## <a name="create-a-size-group"></a>创建大小组

要创建一个大小组，请执行以下步骤。
 
1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 变型组 \> 大小组**。
1. 在操作窗格上，选择 **新建**。
1. 在 **大小组** 框中，输入大小组的名称。
1. 在 **描述** 框中，输入适当的描述。
1. 在操作窗格上，选择 **保存**。

## <a name="add-attributes-to-the-size-group"></a>将属性添加到大小组

若要将属性添加到大小组，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail 和 Commerce \> 产品和类别 \> 变型组 \> 大小组**。
1. 在导航窗格中，选择一个大小组。
1. 在 **大小组行** 下面，选择 **添加**。
1. 在 **大小** 框中，输入代表大小的字符串（例如“XL”）。
1. 在 **大小名称** 框中，输入大小的名称（例如“特大号”）。
1. 在 **补货重量** 框中，输入代表补货重量的数字。
1. 在 **条码中的编号** 框中，输入代表条码的数字。
1. 在 **显示顺序** 框中，输入代表显示顺序的数字。
1. 添加完大小后，在操作窗格上选择 **保存**。

下图显示了“休闲衬衫尺寸”的大小组的示例。

![创建大小组。](media/Size-Groups.png)

## <a name="additional-resources"></a>其他资源

[产品信息概览](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[设置零售产品](set-up-retail-products.md)

[产品维度](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
