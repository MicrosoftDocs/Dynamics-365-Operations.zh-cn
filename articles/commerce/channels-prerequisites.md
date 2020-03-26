---
title: 渠道设置先决条件
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的渠道设置先决条件。
author: samjarawan
manager: annbe
ms.date: 02/21/2020
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
ms.openlocfilehash: 0da0457240cf12686fff2fa929c7fb510c11f242
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113774"
---
# <a name="channel-setup-prerequisites"></a>渠道设置先决条件


[!include [banner](includes/banner.md)]

此主题概述 Microsoft Dynamics 365 Commerce 中的渠道设置先决条件。

## <a name="overview"></a>概览

在可以创建 Dynamics 365 Commerce 通道之前，必须完成几个先决条件任务。 以下先决条件任务列表按渠道类型进行组织。

> [!NOTE]
> 一些文档仍在编写中，链接将随着新内容的发布而更新。

## <a name="initialization"></a>初始化

- [初始化种子数据](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>所有渠道类型所需的全局先决条件

- [定义和配置法人结构](channels-legal-entities.md) 
- [配置组织层次结构](channels-org-hierarchies.md)
- [设置仓库](channels-setup-warehouse.md)
- [配置销售税](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [设置电子邮件通知配置文件](email-notification-profiles.md)
- [设置编号规则](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [设置默认客户和通讯簿](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>零售渠道先决条件

- [信息代码和信息代码组](info-codes-retail.md)
- [设置零售功能配置文件](retail-functionality-profile.md)
- [设置员工通讯簿](new-address-book.md)
- [设置屏幕布局](pos-screen-layouts.md)
- [设置硬件工作站](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a>呼叫中心渠道先决条件

- 呼叫中心参数
- [呼叫中心订单和退款付款方式](work-with-payments.md)
- [呼叫中心交货方式和费用](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a>在线渠道先决条件

- [创建在线功能配置文件](online-functionality-profile.md)

## <a name="additional-resources"></a>其他资源

[渠道概览](channels-overview.md)

[组织和组织层次结构概览](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[设置组织层次结构](channels-org-hierarchies.md)

[创建法人](channels-legal-entities.md)

[设置零售渠道](channel-setup-retail.md)
    
[设置在线渠道](channel-setup-online.md)
