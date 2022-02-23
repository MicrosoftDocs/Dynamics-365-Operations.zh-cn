---
title: 设置仓库
description: 本主题描述如何在 Microsoft Dynamics 365 Commerce 中设置要与新渠道一起使用的仓库。
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
ms.openlocfilehash: 6da72ae612f0520965a2b11a21123d4642303ac3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410478"
---
# <a name="warehouse-set-up"></a>仓库设置


[!include [banner](includes/banner.md)]

本主题描述如何在 Microsoft Dynamics 365 Commerce 中设置要与新渠道一起使用的仓库。

## <a name="overview"></a>概览

每个商业渠道都需要一个与之关联已配置仓库。 以下过程提供了为商业渠道设置仓库所需的最低配置。 有关仓库设置的更多信息，请参见[仓库管理概览](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)。

## <a name="configure-a-warehouse-site"></a>配置仓库站点

在设置仓库之前，您需要配置仓库站点。

要配置仓库站点，请按照下列步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 站点**。
1. 在操作窗格上，选择 **新建**。
1. 在 **站点** 字段中，输入一个值。
1. 在 **名称** 字段中，输入一个值。
1. 在 **常规** 部分中，设置适当的 **时区**。
1. 在 **地址** 部分中，输入地址。
1. 在操作窗格上，选择 **保存**。

下图显示了一个仓库站点示例。

![仓库站点示例](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>设置仓库

若要设置仓库，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。
1. 在操作窗格上，选择 **新建**。
1. 在 **仓库** 字段中，输入一个值。  如果这是到商店的 1:1 映射，请考虑使用商店名称或区域分销中心的名称。
1. 在 **名称** 字段中，输入一个值。
1. 在 **站点** 下拉列表中，选择先前创建的仓库站点。
1. 在 **类型** 字段中，选择 **默认**。
    - 如果要设置 **检验仓库**，首先，您需要按照以下步骤创建一个额外的仓库，其中 **类型** 设定为 **检验**。
    - 如果要设置 **中转仓库**，首先，您需要按照以下步骤创建一个额外的仓库，其中 **类型** 设定为 **中转**。
1. 在操作窗格上，选择 **保存**。

## <a name="set-up-inventory-aisles"></a>设置库存通道

要设置库存通道，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 位置设置 \> 库存通道**。
1. 在操作窗格上，选择 **新建**。
1. 在 **仓库** 下拉列表中，选择先前创建的仓库。
1. 在 **通道** 字段中，输入名称（例如“默认”）。
1. 在 **名称** 字段中，输入名称（例如“默认通道”）。
1. 在操作窗格上，选择 **保存**。

## <a name="set-up-warehouse-inventory-locations"></a>设置仓库库位

要为标准、损坏和退货库存设置仓库库存库存，请按照以下步骤操作。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。
1. 选择您之前创建的仓库。
1. 在操作窗格上，选择 **编辑**。
1. 在操作窗格上，选择 **仓库**，然后选择 **库存库位**。
1. 在操作窗格上，选择 **新建**。 **仓库** 下拉列表应默认为您的新仓库。
    1. 在 **通道** 框中，输入您先前指定的通道的名称。 
    1. 将 **手动更新** 设置至 **是**
    1. 在 **库位** 框中，输入仓库的名称。
    1. 在操作窗格上，选择 **保存**。
 1. 在操作窗格上，选择 **新建**。  **仓库** 下拉列表应默认为您的新仓库。
    1. 在 **通道** 框中，输入您先前指定的通道的名称。  
    1. 将 **手动更新** 设置至 **是**
    1. 在 **库位** 框中，输入“已损坏”。
    1. 在操作窗格上，选择 **保存**。
 1. 在操作窗格上，选择 **新建**。  **仓库** 下拉列表应默认为您的新仓库。
    1. 在 **通道** 框中，输入您先前指定的通道的名称。 
    1. 将 **手动更新** 设置至 **是**
    1. 在 **位置** 框中，输入“退货”。
    1. 在操作窗格上，选择 **保存**。
    
下图显示了旧金山仓库库存库位设置过程。

![库存库位设置示例](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>完成仓库设置

若要完成仓库设置，请遵循这些步骤。

1. 在导航窗格中，转到 **模块 \> Retail and Commerce \> 渠道设置 \> 仓库**。
1. 选择您之前创建的仓库。
1. 在操作窗格上，选择 **编辑**。
1. 在 **库存和仓库管理** 下面：
    1. 将 **默认收货库位** 设置为上面创建的默认库位。
    1. 将 **默认发货库位** 设置为上面创建的默认库位。
1. 在 **地址** 部分下面，输入仓库地址。
1. 在 **零售** 部分下面： 
    1. 在 **默认退货位置** 框中，输入先前创建的退货位置。
    1. 将 **商店** 设置为 **是**。
    1. 将 **重量** 设置为 **1.00**。 
    1. 在 **存储维度** 框中，输入先前创建的默认位置。
1. 在 **仓库** 部分下面，将 **实际负库存** 设置为 **是**。
1. 在操作窗格上，选择 **保存**。

下图显示了已配置仓库的详细信息。

![已配置仓库示例](media/warehouse-sample.png)

## <a name="additional-resources"></a>其他资源

[仓库管理概览](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)

[设置零售渠道](channel-setup-retail.md)
    
[设置在线渠道](channel-setup-online.md)

[设置呼叫中心渠道](channel-setup-callcenter.md)





