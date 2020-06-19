---
title: 采用双写入的库存可用性
description: 本主题提供有关以双写入方式检查库存可用性的信息。
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426974"
---
# <a name="inventory-availability"></a>库存可用性

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

在 Dynamics 365 中的模型驱动应用中，使用库存可用性，您可以先检查库存，然后再将产品添加到**报价单**、**订单**或**发票**窗体。 例如，检查库存并确定履行日期是[目标客户到现金](dual-write-prospect-to-cash.md)流程的关键任务。 如果您没有足够的库存，您可以根据计划的库存收货和发货来预估交货日期。 您还可以检查产品的可承诺 (ATP) 信息，您可以在其中找到预定义时限内的 ATP 数量。

## <a name="on-hand-inventory"></a>现有库存量 

在 Dynamics 365 Sales 中的**报价单**、**订单**或**发票**窗体的标题中，添加了一个新按钮**现有库存量**。 单击此按钮时，将出现一个对话框，您可以指定要检查其现有库存量的公司和产品。 它返回 Dynamics 365 Supply Chain Management 中的库存信息，显示与[现有库存量](../../../../supply-chain/inventory/tasks/check-availability-stock.md)相同的信息。 此信息包括以下数量：

- **现有数量**
- **预留现有数量**
- **可用现有数量**
- **订购数量**
- **在单数量**
- **预留订购数量**
- **可用总数**

## <a name="atp-information"></a>ATP 信息

在 Dynamics 365 Sales 中的**报价单**、**订单**或**发票**窗体的行项上，添加了一个新按钮 **ATP 信息**。 单击此按钮时，将出现一个对话框，您可以指定公司、产品、库存站点、库存仓库和订单数量。 它返回 Supply Chain Management 中的 **ATP 信息**，并显示[订单承诺](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations)中所述的设置。 此信息包括 **ATP 数量**、**收货数量**、**发货数量**和**现有数量**。
