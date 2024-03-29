---
title: 解决适用于 Adyen 的 Dynamics 365 付款连接器问题
description: 本文提供了故障排除指南，当您遇到适用于 Adyen 的 Microsoft Dynamics 365 付款连接器问题，此指南可以帮助您获得支持。
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
ms.openlocfilehash: 687f2fdff5e29cc25fae911b015164f0d90aee88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268857"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>解决适用于 Adyen 的 Dynamics 365 付款连接器问题

[!include [banner](../../includes/banner.md)]

本文提供了故障排除指南，当您遇到适用于 Adyen 的 Microsoft Dynamics 365 付款连接器问题，此指南可以帮助您获得支持。

## <a name="description"></a>说明

在以下方面，您遇到有关适用于 Adyen 的 Dynamics 365 付款连接器 的问题，并且需要 Adyen 团队的支持：

- 销售点 (POS)、现代销售点 (MPOS)、呼叫中心或 Dynamics 365 Commerce 的配置
- Adyen 付款服务提供商 (PSP) 参考号（例如，如果您对拒绝有疑问，包括手动关键条目 \[MKE\] 拒绝）
- 在测试或实时商家环境中无法正常工作的所有项

## <a name="resolution"></a>解决方法

使用以下电子邮件模板开始执行 Adyen 团队支持流程。 为了加快故障排除速度，请确保电子邮件包含所有必需的详细信息。

| 字段        | 值 |
|--------------|-------|
| 结束日期           | `support@adyen.com` |
| 抄送           | |
| 主题行 | Microsoft Dynamics 支持请求 |
| 正文         | <p>支持人员，你好：</p><p>请对以下问题提供支持：</p><ul><li>商户帐户</li><li>环境（测试/生产）</li><li>渠道（POS/呼叫中心/Commerce 电子商务）</li><li>PSP 参考号（如果问题涉及特定交易）（您可以在收据上、在 Adyen 客户区域中或在 POS 终端的交易菜单上找到 PSP 参考号。）</li><li>错误消息的屏幕截图或照片（如适用）</li><li>事件查看器日志（.txt 格式）</li><li>问题说明和尝试的故障排除步骤</li></ul> |

## <a name="additional-resources"></a>其他资源

[使用适用于 Dynamics 365 Commerce 的 Adyen 连接器接受付款](https://www.adyen.com/partners/dynamics-365-commerce)

[适用于 Adyen 的 Dynamics 365 付款连接器](../dev-itpro/adyen-connector.md)

[设置适用于 Dynamics 365 的 Adyen 付款连接器](https://docs.adyen.com/plugins/microsoft-dynamics)
