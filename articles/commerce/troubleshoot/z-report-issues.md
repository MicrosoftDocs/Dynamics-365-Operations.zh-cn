---
title: Z 报告的数据对帐问题
description: 本文介绍用户在 Commerce headquarters 中对 Z 报告进行数据对帐时可能会遇到的问题。 它还描述了可能的根本原因和可能有助于防止将来发生问题的解决方案。
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832115"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Z 报告的数据对帐问题

[!include [banner](../../includes/banner.md)]

如果您在 Microsoft Dynamics 365 Commerce headquarters 中遇到 Z 报告的数据对帐问题，那么本文提供的故障排除指南可以提供帮助。 它描述了用户在进行数据对帐时可能遇到的问题、可能的根本原因以及可能有助于防止将来发生问题的解决方案。

## <a name="description"></a>Description

- Z 报告中显示的金额与计算报表中显示的总计不匹配。
- Headquarters 中的交易的行项数量不正确，或者行总计与交易总计不匹配。
- Headquarters 班次中显示的交易数量小于 Z 报表上的交易数量。
- 由于上述原因之一，报表过帐失败。

### <a name="root-cause"></a>根本原因

前面描述的症状的最常见根本原因是在渠道数据库中生成了重复的交易 ID。 由于以下原因，可能会生成重复的交易 ID：

- 现代销售点 (MPOS) 的本地数据库存储已损坏。
- MPOS 在脱机模式下有一些交易，并且使用无法访问脱机数据库的帐户重新激活。
- 与交易 ID 的生成相关的自定义存在问题。

## <a name="resolution"></a>解决方法

通常，Commerce 依靠数字序列来生成序列交易 ID。 如果系统由于任何原因而无法确定使用了编号规则，则会生成重复的交易 ID。 

要解决重复交易 ID 问题，请创建一个支持票证以检查是否可以修复交易数据。 在某些情况下，例如当 Headquarters 中没有数据丢失时，就不可能或不需要修复数据。

为帮助防止将来出现此问题，您必须在 Headquarters 中启用 **启用新交易 ID 以避免交易 ID 重复** 功能。 Commerce 版本 10.0.19 中引入了此功能。 它通过确保为每个交易创建唯一的交易 ID 来帮助防止创建序列交易 ID。 有关此功能的详细信息，请参阅[防止重复的交易 ID](../channel-setup-retail.md#ensure-unique-transaction-ids)。
