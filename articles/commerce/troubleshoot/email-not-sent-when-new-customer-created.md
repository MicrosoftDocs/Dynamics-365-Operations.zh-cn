---
title: 创建新客户时未发送欢迎电子邮件
description: 本主题提供故障排除指导，可以帮助解决在 Microsoft Dynamics 365 Commerce 中创建新客户时未发送欢迎电子邮件通知的问题。
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349939"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>创建新客户时未发送欢迎电子邮件

[!include [banner](../../includes/banner.md)]

本主题提供故障排除指导，可以帮助解决在 Microsoft Dynamics 365 Commerce 中创建新客户时未发送欢迎电子邮件通知的问题。

## <a name="description"></a>Description

在 Commerce headquarters 中创建新客户时，不会向客户发送欢迎电子邮件，即使为 **创建客户** 电子邮件通知类型配置了电子邮件通知。

## <a name="resolution"></a>解决方法

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>为“创建客户”电子邮件通知类型设置正确的电子邮件 ID 值

要在 Headquarters 中为 **创建客户** 电子邮件通知类型设置正确的 **电子邮件 ID** 值，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \> Commerce 电子邮件通知配置文件**。
1. 在左侧导航窗格中，选择电子邮件通知配置文件。
1. 在 **零售事件通知设置** 下，对于 **创建客户** 电子邮件通知类型，将 **电子邮件 ID** 字段设置为 **NewCust**。

## <a name="additional-resources"></a>其他资源

[设置电子邮件通知配置文件](../email-notification-profiles.md)
