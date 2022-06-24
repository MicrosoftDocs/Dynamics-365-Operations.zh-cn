---
title: 付款会在订单开发票或装运之前自动结清
description: 本文提供了故障排除指南，即使销售订单未开发票或未装运，也可以在下订单后立即在 Adyen 门户中结算付款时通过本指南获得帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c01a2fda54e198a43fa84ae83686fc1701958b6b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890261"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>付款会在订单开发票或装运之前自动结清

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，即使销售订单未开发票或未装运，也可以在下订单后立即在 Adyen 门户中结算付款时通过本指南获得帮助。

## <a name="description"></a>说明

下订单后，即使销售订单未开发票或未装运，也可以立即在 Adyen 门户中结算付款。

## <a name="resolution"></a>解决方法

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>配置手动捕获以在 Adyen 门户中进行电子商务付款

要配置手动捕获以在 Adyen 门户中进行电子商务付款，请按照下列步骤操作。

1. 登录 Adyen 门户。
1. 在右上角，为电子商务渠道选择您的商家帐户。
1. 在顶部导航栏上，选择 **帐户**，然后选择 **设置**。
1. 在 **捕获延迟** 字段中，选择 **手动**。

    ![Adyen 门户中的“捕获延迟”设置。](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>其他资源

[Adyen 付款捕获](https://docs.adyen.com/point-of-sale/capturing-payments)

[面向 Adyen 的 Dynamics 365 Payment Connector](../dev-itpro/adyen-connector.md)

[设置适用于 Dynamics 365 的 Adyen 付款连接器](https://docs.adyen.com/plugins/microsoft-dynamics)
