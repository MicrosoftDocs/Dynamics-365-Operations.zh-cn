---
title: “保存以用于下一次付款”选项未显示
description: 本文提供了故障排除指南，当电子商务站点结帐页面上的“付款方式”下面未出现“保存以用于下一次付款”复选框时，该指南可以提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287476"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>“保存以用于下一次付款”选项未显示

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，当电子商务站点结帐页面上的 **付款方式** 下面未出现 **保存以用于下一次付款** 复选框时，该指南可以提供帮助。

## <a name="description"></a>说明

此 **保存以用于下一次付款** 复选框没有出现在电子商务网站的结帐页面上的 **付款方式** 部分中。

下图显示了一个结帐页面的示例，其中包括 **保存以用于下一次付款** 复选框。

![“付款”模块中的“保存以用于下一次付款”复选框。](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>解决方法

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>验证是否在 Commerce Headquarters 中正确配置了适用于 Adyen 的 Dynamics 365 付款连接器

若要验证是否在 Commerce Headquarters 中正确配置了适用于 Adyen 的 Dynamics 365 付款连接器，请执行以下步骤。

1. 转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 选择在线商店。
1. 在 **付款帐户** 快速选项卡上，请确保 **允许在电子商务中保存付款信息** 字段设置为 **真**。

![允许在 Commerce Headquarters 的电子商务字段中保存付款信息。](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>其他资源

[付款模块](../payment-module.md)

[使用 Adyen 连接器保存在线付款方式](../dev-itpro/adyen-connector-listPI.md)
