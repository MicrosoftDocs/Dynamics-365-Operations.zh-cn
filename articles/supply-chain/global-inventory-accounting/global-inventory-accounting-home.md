---
title: 全球库存核算主页
description: 本主题介绍了 Microsoft Dynamics 365 Supply Chain Management 的全球库存核算加载项的主页。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3e1dbb97ba56b5910dda368b9ec15e27a683dde5
ms.sourcegitcommit: 5c0a0adeb859cc1ade6f067444f3bf08a895b35a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2021
ms.locfileid: "7557384"
---
# <a name="global-inventory-accounting-home-page"></a>全球库存核算主页

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

国际组织正面临来自当局越来越大的压力，要求其遵守当地和全球核算标准。 库存评估在确保合规性方面发挥着重要作用。 Microsoft Dynamics 365 Supply Chain Management 的全球库存核算加载项提供全面的解决方案，使组织（尤其是国际组织）能够使用多个成本计算分类帐进行库存核算。 因此，这些组织可以同时遵守多个核算标准和内部管理核算。

全球库存核算允许您通过应用适当的评估方法（标准成本、平均或特定标识）和每个实例选择的核算货币，以多种表示形式核算库存。 全球库存核算使组织能够以通常称为双估价和/或双货币的方式报告库存报表和子分类帐核算值（也称为库存余额和所售货物成本）。

库存核算在单独的分类帐中完成。 可以根据需要为组织中的每个法人创建多个全球库存核算分类帐。 因此，可以获得多个库存表示形式。 在法人中过帐的所有单据（例如采购订单、销售订单和转移单）都将在与该法人关联的所有成本计算分类帐中进行核算。

全球库存核算分类帐由以下元素的组合定义：

- 日历
- 货币
- 汇率表
- 惯例

惯例是可以与一个或多个分类帐相关联的库存核算策略的集合。 惯例使您可以在组织内共享一组通用策略。

## <a name="availability"></a>可用性

全球库存核算目前在以下 Azure 地理区域中可用：

- 美国
- 欧洲
- 英国
- 澳大利亚
- 加拿大
- 南美洲

如果您尝试从其他地理区域安装加载项，则 Microsoft Dynamics Lifecycle Services (LCS) 将显示一条消息，指明不支持您的地理区域。 全球库存核算不支持 Supply Chain Management 的本地部署。

如果您在此处列出的其中一个受支持地理区域中启用全球库存核算时有任何问题，请将包含环境 ID 的电子邮件发送到[全球库存核算团队](mailto:GlobalInvAccount@microsoft.com)以进行验证。

## <a name="licensing"></a>许可授权

全球库存核算与可用于 Supply Chain Management 的标准成本管理功能一起获得许可。 您无需购买其他许可证即可使用全球库存核算。
