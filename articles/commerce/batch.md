---
title: 改进了批量跟踪物料的处理
description: 本主题介绍了 Microsoft Dynamics 365 Commerce 中对于对帐单过帐流程中批量跟踪物料处理的改进。
author: josaw1
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 513b6ca84fa71e851a5a3e4275e0b6572789e1eb
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485775"
---
# <a name="improved-handling-of-batch-tracked-items"></a>改进了批量跟踪物料的处理

[!include [banner](includes/banner.md)]

本主题介绍了 Microsoft Dynamics 365 Commerce 中对于对帐单过帐流程中批量跟踪物料处理的改进。

在 Dynamics 365 Commerce 销售点 (POS) 中，无法在销售时捕获批量跟踪物料的批处理号。 但是，对于特定配置，在 Commerce Headquarters 中通过客户订单或对帐单过帐来过帐销售额时，Commerce 要求批量跟踪物料具备有效的批处理号，这些编号在开票流程中使用。

如果有效的批处理号对产品可用，则来自对帐单过帐的客户订单开票流程和销售订单开票流程均会使用这些编号。 如果有效的批处理号对产品不可用，则客户订单开票流程无法过帐，POS 用户将收到错误消息。 对帐单过帐随后会进入错误状态，即使为产品启用了负库存，也会如此。

对 Commerce 所做的改进可帮助确保在为批量跟踪物料启用了负库存时，如果库存为 0（零）或者批处理号不可用，不会阻止这些物料通过对帐单过帐进行客户订单开票和销售订单开票。 批处理号不可用时，改进的功能会使用销售行的默认批处理 ID。

## <a name="define-the-default-batch-id-that-is-used-for-customer-orders"></a>定义为客户订单使用的默认批处理 ID

要定义为客户订单使用的默认批处理 ID，请按照下列步骤操作。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。
1. 在 **客户订单** 选项卡的 **订单** 快速选项卡上，在 **默认批处理 ID** 字段中输入值。

## <a name="define-the-default-batch-id-that-is-used-for-sales-order-invoicing-through-statement-posting"></a>定义为通过对帐单过帐进行的销售订单开票使用的默认批处理 ID

要定义为通过对帐单过帐进行的销售订单开票使用的默认批处理 ID，请按照下列步骤操作。

1. 在 Commerce Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数**。
1. 在 **过帐** 选项卡的 **库存更新** 快速选项卡上，在 **默认批处理 ID** 字段中输入值。

> [!NOTE]
> - 只有为特定商店仓库和物料启用了高级仓储时，默认批处理 ID 功能才可用。 在未来的版本中，未启用高级仓库管理的方案也将支持默认批处理 ID 功能。
> - Commerce 版本 10.0.5 中推出了在对非高级仓库管理方案进行对帐单过帐期间，对批量跟踪物料处理的改进的支持。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
