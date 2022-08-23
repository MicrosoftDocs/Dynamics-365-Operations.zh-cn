---
title: 渠道概览
description: 本文概述 Microsoft Dynamics 365 Commerce 中的渠道。
author: samjarawan
ms.date: 01/27/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.assetid: ''
ms.openlocfilehash: ad31f466563aeb38f28f9761828e6708895005b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280412"
---
# <a name="channels-overview"></a>渠道概览


[!include [banner](includes/banner.md)]

本文概述 Microsoft Dynamics 365 Commerce 中的渠道。 它包含有关在设置每个渠道前后必须完成的任务的信息。

## <a name="types-of-channels"></a>渠道类型

Dynamics 365 Commerce 支持以下三种不同的渠道类型：零售、呼叫中心和在线渠道。

### <a name="retail-channels"></a>零售渠道

零售渠道代表标准的实体商店。 每个商店可以有自己的销售点 (POS) 收银机、收入帐户和支出帐户以及职员。 

### <a name="call-center-channels"></a>呼叫中心渠道

呼叫中心渠道代表呼叫中心订单和客户管理。

### <a name="online-channels"></a>在线渠道

在线渠道代表在线电子商务店面。 创建在线渠道后，必须使用 Microsoft Dynamics 365 Commerce 站点构建器工具或其他第三方电子商务解决方案创建站点。

## <a name="channel-setup-basics"></a>渠道设置基础知识

渠道设置是在 Commerce 工具中执行的。 每个渠道可以有自己的付款方式、价格组、产品层次结构、分类和产品集。 在创建渠道后，分配您希望其提供和销售的产品。 每种渠道类型都有可能需要配置的一组独特功能。 例如，零售渠道需要分配的员工、收银机和客户。 创建新渠道后，需要将其分配给组织层次结构。

## <a name="channel-setup-prerequisites"></a>渠道设置先决条件

在设置渠道之前，必须根据渠道类型完成一些先决条件任务。 有关更多信息，请参见[渠道设置先决条件](channels-prerequisites.md)。

## <a name="set-up-a-channel"></a>设置渠道

完成先决条件任务后，请使用以下链接以获取详细设置说明。

- [设置零售渠道](channel-setup-retail.md)
- [设置呼叫中心渠道](channel-setup-callcenter.md)
- [设置在线渠道](channel-setup-online.md)

<!--
## Post-channel configuration

After you create a channel, you may need to complete some of the below tasks:

- [Add channel to an organizational hierarchy](add-channel-org-hierarchy.md)
- Set up fulfillment groups. (LINK TBD)
- Configure the POS registers for the store. (LINK TBD)
- Assign product assortments to the store. (LINK TBD)
- Process assortments to generate the list of products that are included in the assortment and to make the products available in the retail store. (LINK TBD)
- Send data such as number sequences, hardware profiles, and POS screen layouts to the Retail POS registers.(LINK TBD)
- Publish the retail store to send store data to Retail POS. (LINK TBD)
- Run the jobs to send the store data to Retail POS. (LINK TBD)
-->

## <a name="additional-resources"></a>其他资源

[渠道设置先决条件](channels-prerequisites.md)

[设置零售渠道](channel-setup-retail.md)
    
[设置在线渠道](channel-setup-online.md)

[设置呼叫中心渠道](channel-setup-callcenter.md)

[设置组织层次结构](channels-org-hierarchies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
