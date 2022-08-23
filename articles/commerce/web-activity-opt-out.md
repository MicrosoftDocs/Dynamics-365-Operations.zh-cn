---
title: 选择退出 Web 活动事件收集
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中让网站的访问者选择不收集 Web 活动事件。
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286717"
---
# <a name="opt-out-of-web-activity-event-collection"></a>选择退出 Web 活动事件收集
[!include [banner](includes/banner.md)]

本文说明如何在 Microsoft Dynamics 365 Commerce 中让客户选择不收集 Web 活动事件。

站点管理员可通过 Dynamics 365 Commerce 分析其电子商务站点用户的 Web 活动。 这样，就可以更好地了解其站点的使用方式，并且可以优化站点以提供更出色的用户体验和满足业务目标。


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>管理员实施选择退出体验的方法

管理员可以通过三种方法实现选择退出体验。

### <a name="opt-out-on-behalf-of-users"></a>代表用户选择退出

在 Commerce Headquarters (HQ) 的“帐户管理”中，管理员可以代表用户选择退出。

1. 在 HQ 客户端的 **所有客户** 页中，搜索和选择客户。
1. 在客户详细信息页的 **零售** 快速选项卡上 **隐私** 部分中，将 **不跟踪 Web 活动** 选项设置为 **是**。

    ![隐私设置。](media/Disablepersonalizationpart2.png)

1. 选择 **保存**，然后关闭页面。

### <a name="module-based-opt-out-experience"></a>基于模块的退出体验

管理员可以让已通过身份验证的用户自行选择不收集 Web 活动事件。 要提供这种退出体验，请将用户退出模块添加到客户帐户的个人资料页面。

### <a name="custom-extensions"></a>自定义扩展

管理员可以创建自己的扩展来管理用户的退出体验。 有关详细信息，请参阅[调用 Retail Server API](e-commerce-extensibility/call-retail-server-apis.md) 和[在线渠道可扩展性](e-commerce-extensibility/overview.md)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
