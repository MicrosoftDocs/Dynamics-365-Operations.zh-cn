---
title: 创建新客户时未发送欢迎电子邮件
description: 本文提供故障排除指南，可以帮助解决在 Microsoft Dynamics 365 Commerce 中创建新客户时未发送欢迎电子邮件通知的问题。
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219396"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>创建新客户时未发送欢迎电子邮件

[!include [banner](../../includes/banner.md)]

本文提供故障排除指南，可以帮助解决在 Microsoft Dynamics 365 Commerce 中创建新客户时未发送欢迎电子邮件通知的问题。

## <a name="description"></a>Description

在 Commerce headquarters 中创建新客户时，不会向客户发送欢迎电子邮件，即使为 **创建客户** 电子邮件通知类型配置了电子邮件通知。

## <a name="resolution"></a>解决方法

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>在 Commerce 参数下关联电子邮件通知配置文件

1. 在 Headquarters 中，转到 **Retail 和 Commerce \> Headquarters 设置 \> 参数 \> Commerce 参数 \> 常规**。
2. 在 **电子邮件通知配置文件** 下拉列表中，选择电子邮件通知配置文件，其中包含客户创建的通知类型与客户创建的电子邮件模板之间的映射。  

> [!NOTE] 
> 当您启用客户创建的通知时，在法人的所有渠道中创建的客户将收到一封客户创建的电子邮件。 当前，客户创建的通知不能仅限于单个渠道。

有关详细信息，请参阅[创建交易事件的电子邮件模板](../email-templates-transactions.md)。 

## <a name="additional-resources"></a>其他资源

[设置电子邮件通知配置文件](../email-notification-profiles.md)
