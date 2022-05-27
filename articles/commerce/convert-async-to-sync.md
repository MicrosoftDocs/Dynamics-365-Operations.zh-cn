---
title: 将异步客户转换为同步客户
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中将异步客户转换为同步客户。
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: fc1690ff6068317c748bda0d767a10f306f3debe
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691436"
---
# <a name="convert-asynchronous-customers-to-synchronous-customers"></a>将异步客户转换为同步客户

[!include [banner](includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Commerce 中将异步客户转换为同步客户。

要将异步客户转换为同步客户，请执行以下步骤。

1. 在 Commerce Headquarters 中，运行 **P 作业** 将异步客户发送到 Commerce Headquarters。
1. 运行 **从异步模式同步客户和业务合作伙伴** 作业，以创建客户帐户 ID。 （此作业以前称为 **从异步模式同步客户和业务合作伙伴**。）
1. 运行 **1010** 作业，以将新客户帐户 ID 同步到渠道。

如果订单引用尚未同步到 Commerce headquarters 的异步客户或地址，该客户或地址将作为 **同步订单** 批处理作业的一部分进行同步。 如果现金和结转交易引用异步客户或地址，该客户或地址将在日结 (EOD) 过帐之前同步。

## <a name="additional-resources"></a>其他资源

[商店中的客户管理](customer-mgmt-stores.md)

[异步客户创建模式](async-customer-mode.md)

[客户属性](dev-itpro/customer-attributes.md)

[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
