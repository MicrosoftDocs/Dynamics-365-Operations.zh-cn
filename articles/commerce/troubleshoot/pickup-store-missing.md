---
title: 零售店没有出现在要从中提货的商店的列表中
description: 本主题提供了故障排除指南，此指南可以在零售店没有出现在可以从中提货的商店列表中时提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ad7ddf8a17640471a2344c45eef76f682d29ef2b
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020807"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>零售店没有出现在要从中提货的商店的列表中

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，此指南可以在零售店没有出现在可以从中提货的商店列表中时提供帮助。

## <a name="description"></a>说明

零售店没有出现在可以从中提货的商店的列表中。

## <a name="resolution"></a>解决方法

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置商店地址的经度和纬度

要在 Commerce Headquarters 中配置商店地址的经度和纬度，请按照以下步骤操作。

1. 转至 **Retail 和 Commerce \> 渠道 \> 商店 \> 所有商店**。
1. 在电子商务站点上查找要出现在提货选项中的商店。 记下其 **运营单位编号** 值。
1. 转到 **组织管理 \> 组织 \> 运营单位**。
1. 搜索您先前记下的运营单位编号，然后在搜索结果中选择此运营单位。
1. 在 **地址** 快速选项卡上，选择 **更多选项**，然后选择 **高级**。
1. 在 **常规** 快速选项卡上，请确保 **经度** 和 **纬度** 字段设置正确。 作为此步骤的一部分，请确保将值正确指定为正数或负数。

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>在 Commerce Headquarters 中配置履行组

要在 Commerce Headquarters 中配置履行组，请按照下列步骤操作。

1. 转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 选择要配置的在线商店。
1. 在操作窗格上，选择 **设置**，然后选择 **履行组分配**。
1. 在 **履行组分配** 页面上，选择在线商店的履行组。
1. 在 **设置** 下面，请确保已为履行组正确配置零售店。

## <a name="additional-resources"></a>其他资源 

[创建运营单位](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[设置在线渠道](../channel-setup-online.md)