---
title: 礼品卡跨公司数据共享
description: 本文介绍如何配置 Microsoft Dynamics 365 Commerce 来跨数据区域使用 Dynamics 365 Finance 数据共享功能同步礼品卡数据。
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473923"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>礼品卡跨公司数据共享

[!include [banner](../includes/banner.md)]

本文介绍如何配置 Microsoft Dynamics 365 Commerce 来使用 Dynamics 365 Finance 数据共享功能同步礼品卡数据。 然后可以使用数据记录共享功能在两个数据区域之间跨公司共享数据。 这样，Commerce 内部礼品表可以在两个公司实体之间共享数据。 有关 Dynamics 365 Finance 跨公司数据共享的详细信息，请参阅[跨公司数据共享](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing)。

## <a name="key-terms"></a>重要术语

| 条款 | Description |
|---|---|
| 公司 | Dynamics 365 Finance 环境中的法人。 |
| 礼品卡 | Dynamics 365 Commerce 内部礼品卡产品。 |

## <a name="prerequisites"></a>先决条件

用户必须按照[跨公司数据共享](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing)中的说明配置环境来进行跨公司数据共享。

**RetailGiftCardTable** 必须将 **DataSharingType** 字段设置为 **重复** 才能为礼品卡表启用重复记录共享 (DRS)。 有关详细信息，请参阅[面向开发人员的跨公司数据共享](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev)。

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>配置礼品卡跨公司数据共享

要配置礼品卡跨公司数据共享，请执行以下步骤。

1. 在 Commerce headquarters 中，转到 **系统管理 \> 设置 \> 配置跨公司数据共享**。
1. 在操作窗格上，选择 **新建** 添加数据共享记录。
1. 在 **名称** 字段中，为数据共享记录输入名称（例如，**礼品卡**）。
1. 在 **要共享的表和字段** 部分，选择 **添加**。
1. 在 **共享新表** 对话框的 **表名称** 字段中，输入 **RETAILGIFTCARDTABLE**（零售礼品卡表）。 **表标签** 字段应会自动设置为 **礼品卡表**。
1. 确保 **按公司保存数据**、**具有唯一索引** 和 **尚未共享** 复选框均处于选中状态。 选择这些复选框会触发与数据共享功能相关的验证。
1. 选择 **添加表**。 **礼品卡表 (RetailGiftCardTable)** 记录现在应会出现在 **要共享的表和字段** 下。 选择插入符号 (^) 查看所有自动与表关联以进行共享的表字段。
1. 在 **共享这些表中的记录的公司** 部分，选择 **添加** 添加要与之共享数据的公司。
1. 在 **公司** 下的行中，从下拉列表中选择一家公司。
1. 在 **名称** 字段中，输入公司名称。
1. 重复步骤 8 到 10 添加更多公司行。
1. 添加完公司行后，在操作窗格上选择 **启用**。
1. 您会收到一条警告消息，指出“建议仅在非工作时间执行此操作。 对于策略中的表，任何并发事务操作都将失败。 是否要继续?” 选择 **是** 同意。
1. 您会收到一条警告消息，显示“您现在是否要跨所有共享公司复制全部现有数据?” 选择 **是** 同意。

您同意这两条消息后，表将开始跨配置的公司复制数据。 然后，一家公司礼品卡的余额将对另一家公司可见。

## <a name="additional-resources"></a>其他资源

[付款常见问题](payments-retail.md)

[结帐模块](../add-checkout-module.md)

[付款模块](../payment-module.md)
