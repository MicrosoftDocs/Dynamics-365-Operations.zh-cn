---
title: 提货登记模块
description: 此主题介绍提货登记模块，并说明如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937565"
---
# <a name="check-in-for-pickup-module"></a>提货登记模块

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

此主题介绍提货登记模块，并说明如何在 Microsoft Dynamics 365 Commerce 中配置此模块。

提货登记模块为使用 Dynamics 365 Commerce 客户登记功能通知商店他们已到达的客户提供了一个确认页面。 提货登记模块还允许您配置一个窗体，来从客户那里收集其他信息，推进订单交付。 这些信息包括客户的停车位号，以及其车辆的品牌和型号。 

## <a name="module-properties"></a>模块属性

| 属性名称 | 值 | 说明 |
|---------------|--------|-------------|
| 确认文本 | 文本字符串 | 登记确认页上显示的标题的内容。 |
| 显示 QR 码 | **True** 或 **False** | 当此属性设置为 **True** 时，登记确认页将显示代表订单确认 ID 的 QR 码。 |
| 其他信息标题 | 文本字符串 | 其他信息字段已配置时显示的标题的内容。 |
| 其他信息键 | 资源 ID/资源值对 | 每个键将创建一个表单域和一个关联的标签，用于从客户那里收集其他信息。 |
| 其他信息键 \> 资源 ID | 文本字符串 | 每个信息键将创建一个表单域和一个关联的标签，用于从客户那里收集其他信息。 此属性标识其他信息键。 在销售点 (POS) 创建的任务中，此属性的值在说明字段中显示为标签。 |
| 其他信息键 \> 资源值 | 文本字符串 | POS 中的任务中文本字段的标签。 |
| 其他信息键 \> 必填 | **True** 或 **False** | 此属性指定客户是否必须先填写表单域才能继续。 当此属性设置为 **True** 时，表单标签旁边将显示一个星号，将进行 null 检查来阻止客户继续（如果未输入任何值）。 |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>将提货登记模块添加到页面

提货登记模块应添加到您创建的用于登记确认的新页面。 该页面将作为在电子邮件中选择 **我在这里** 链接或按钮的客户的登记确认体验。 

## <a name="configure-the-additional-information-form"></a>配置其他信息表单

默认情况下，如果未配置其他信息键，模块将向客户显示登记确认页。 显示登记确认时，将在 POS 中为要提取订单的商店创建一个任务。

配置一个或多个其他信息键后，首先会提示客户输入信息。 当他们选择 **提交** 时，将向他们显示登记确认，并在 POS 中创建一个任务。 

## <a name="additional-resources"></a>其他资源

[在销售点 (POS) 启用客户登记通知](enable-customer-check-in.md)
