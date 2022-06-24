---
title: 按交货模式自定义事务电子邮件
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中为特定的通知类型和交货方式设置自定义电子邮件模板。
author: stuharg
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: f16bc23e3527f57bd61d73e92506946067c6eeb9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850296"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>按交货模式自定义事务电子邮件

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中为特定的通知类型和交货方式设置自定义电子邮件模板。

现在可以自定义事务电子邮件，以将通知类型（例如，**订单已创建**、**订单已包装** 或 **订单已开票**）和交货方式（例如，隔夜、店内提货或路边提货）结合在一起。 通过自定义事务电子邮件，零售商可以为客户订单提供专为订单交货方式定制的履行体验。 例如，可以自定义“订单已包装”事件，以便为选择路边提货的客户提供路边提货说明。 或者，可以为选择装运订单的客户提供装运承运人和交货信息。

> [!NOTE]
> 若要使用自定义事务电子邮件的功能，首先必须通过在 Commerce 总部中转到 **工作区 \> 功能管理** 来打开 **按交货方式自定义事务电子邮件模板** 功能。

可以针对以下通知类型按交货方式自定义电子邮件：

- **订单取消** – 此电子邮件通知类型是新的。
- **订单已创建**
- **订单已确认**
- **订单已开票** – 此电子邮件通知类型是新的。 它可以代替 **订单已装运** 通知类型，该类型将针对具有已装运交货方式（而不是提货、自提或电子交货方式）的任何发票事件发送通知。
- **订单已领料**
- **订单已包装**
- **订单可提货** – 仅在打开 **支持多个提货交货方式** 功能时才按提货方式自定义此通知类型。 在这种情况下，此通知类型在功能上等同于 **订单已包装** 通知类型。
- **付款失败**
- **已创建更换单**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>为特定的交货方式配置电子邮件模板

对于此过程，假设您已创建新的自定义电子邮件模板并将其添加到 **组织电子邮件模板** 页面。 有关如何创建和上传电子邮件模板的信息，请参阅[创建交易事件的电子邮件模板](email-templates-transactions.md)。

若要在 Commerce 总部为特定交货方式配置电子邮件模板，请按照以下步骤操作。

1. 转到 **Commerce 电子邮件通知配置文件**。
1. 在 **零售事件通知设置** 下，选择一个现有的通知类型。
1. 在通知类型保持选中时，选择 **配置交货方式**。
1. 在 **交货方式** 对话框中，选择 **新建**。
1. 在新行中，在 **交货方式** 字段中，选择交货方式。
1. 在 **电子邮件 ID** 字段中，选择要映射到交货方式的电子邮件模板。
1. 选中 **有效** 复选框。
1. 重复步骤 4 到 7 以添加更多交货方式。
1. 当您完成时，选择 **确定**。

> [!NOTE]
> - 如果销售订单的各行之间存在多种交货方式，将使用默认模板。 默认模板是在 **Commerce 电子邮件通知配置文件** 页面上映射到通知类型的模板。
> - 如果销售订单的交货方式尚未为自定义电子邮件模板配置，将使用默认电子邮件模板。

## <a name="additional-resources"></a>其他资源

[创建呼叫中心订单](tasks/create-call-center-orders.md)

[在 POS 上更改交货方式](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]