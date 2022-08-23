---
title: 配置渠道以使用渠道导航层次结构
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置渠道以使用渠道导航层次结构。
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
ms.openlocfilehash: b15e6eee86880f0315f42b34056385f718cc6bf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280385"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>配置渠道以使用渠道导航层次结构


[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中配置渠道以使用渠道导航层次结构。

## <a name="overview"></a>概览

渠道导航层次结构按类别组织产品，以便可以在电子商务站点或销售点 (POS) 上浏览产品。 对于渠道导航层次结构，必须配置零售和在线渠道。

## <a name="configure-the-channel"></a>配置渠道

要配置渠道以使用渠道导航层次结构，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 渠道类别和产品属性**。
1. 选择要配置的渠道。
1. 在操作窗格上，选择 **设置属性元数据**。
1. 在 **类别层次结构** 下拉列表中，选择合适的渠道导航层次结构。
1. 在操作窗格上，选择 **保存**。
1. 在 **属性组** 下面，添加将成为所有节点的全局属性的所有属性组。

下图显示了如何配置渠道以使用渠道导航层次结构。

![渠道配置示例。](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>设置属性元数据

设置属性元数据将允许在每个节点上配置属性。

要设置属性元数据，请按照以下步骤操作。

1. 在操作窗格上，选择 **设置属性元数据**。
1. 对于每个节点，请选择 **渠道产品属性**。
1. 将 **在渠道上显示属性** 设置为 **是**，将 **可细化** 设置为 **是**，以在该渠道上启用优化器。
1. 根据需要配置每个节点后，在 **操作窗格** 上，选择 **保存** 按钮进行保存。
1. 选择右上角中的 **X** 以将此屏幕退回到 **渠道类别和产品属性** 页。

下图显示了在渠道类别节点上配置的一组渠道产品属性的示例。

![渠道类别节点上的渠道属性。](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>发布更改

若要让更改生效，则需要发布这些更改。

若要发布更改，请执行以下步骤。

1. 在操作窗格上，选择 **发布渠道更新**。
1. 在 **发布渠道更新** 窗格中，选择 **确定**。

下图显示了如何发布渠道更新。

![发布渠道更新。](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>其他资源

[创建渠道导航层次结构](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
