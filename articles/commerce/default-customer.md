---
title: 创建默认客户
description: 本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。
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
ms.openlocfilehash: 9e1087821b357c578993cdd5742399c5ec0ecc95
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001798"
---
# <a name="create-a-default-customer"></a>创建默认客户


[!include [banner](includes/banner.md)]

本主题描述如何创建在 Microsoft Dynamics 365 Commerce 中创建渠道时要使用的默认客户。

## <a name="overview"></a>概览

创建零售或在线渠道时，您将需要提供一个默认客户。 在首先创建客户组和客户地址簿后，可以轻松创建默认客户。

## <a name="create-a-customer-group"></a>创建客户组

如果尚不存在客户组，则可以创建一个。 示例可能是代表不同客户组（例如批发、零售、互联网、员工等）的组。

要创建客户组，请执行以下步骤。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 客户 \> 客户组**。
1. 在操作窗格上，选择**新建**。
1. 在**客户组**框中，输入客户组 ID。
1. 在**描述**框中，输入适当的描述。
1. 在**付款期限**框中，输入适当的值。
1. 在**发票到期日期与付款日期之间的时间**框中，输入适当的值。
1. 在**默认税组**框，输入税组（如果适用）。
1. 如果适用，请选中**价格包括销售税**复选框。
1. 在**默认勾销原因**框，输入适当的值（如果适用）。

下图显示了几个已配置的客户组。

![客户组](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a>新建客户通讯簿

客户需要与通讯簿相关联。 如果尚未创建，则需要创建一个。

要创建客户通讯簿，请执行以下步骤。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 渠道设置 \> 通讯簿**。
1. 在操作窗格上，选择**新建**。
1. 在**名称**框中，输入名称。
1. 在**描述**框中，输入描述。
1. 在操作窗格上，选择**保存**。

下图显示了一个通讯簿示例。

![通讯簿](media/address-book.png)

## <a name="create-a-default-customer"></a>创建默认客户

要创建默认客户，请执行以下步骤。

1. 在导航窗格中，转到**模块 \> Retail and Commerce \> 客户 \> 所有客户**。
1. 在操作窗格上，选择**新建**。
1. 在**类型**下拉列表中，选择“人员”。
1. 在**客户账户**下拉列表中，选择或输入帐号（例如，“100001”）。
1. 在**名字**下拉列表中，选择或输入名称（例如，“默认”）。
1. 在**中间名**下拉列表中，选择或输入名称（例如，“零售”）。
1. 在**姓氏**下拉列表中，选择或输入名称（例如，“客户”）。
1. 在**货币**下拉列表中，选择或输入货币（例如，“美元”）。
1. 在**货币**下拉列表中，选择先前创建的客户组。
1. 在**地址簿**下拉列表中，选择一个现有的客户通讯簿。
1. 选择**保存**以保存并返回到新客户的客户详细信息屏幕。

> [!NOTE]
> 不必为默认客户添加地址。

下图显示客户创建的示例。

![默认客户创建](media/default-customer-creation.png)

下图显示了默认的客户配置。

![客户配置示例](media/default-customer-configuration1.png)

客户详细信息屏幕上的大多数默认值都可以保留，但是应该更改两个值。

1. 在客户详细信息屏幕上，展开**销售订单默认值**。
1. 在**站点**下拉列表中，选择或输入一个预配置的站点。
1. 在**仓库**下拉列表中，选择或输入一个预配置的仓库。

下图显示客户配置示例。

![客户配置示例](media/default-customer-configuration2.png)

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[渠道设置先决条件](channels-prerequisites.md)
