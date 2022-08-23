---
title: 注册并安装电子开票服务
description: 本文提供有关如何注册和安装电子开票服务的信息。
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283948"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>注册并安装电子开票服务

[!include [banner](../includes/banner.md)]

本文提供有关如何注册和安装电子开票服务的信息。 此过程有四个步骤。 步骤 1 到 3 是必需的，步骤 4 是可选的。

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>步骤 1：注册 Regulatory Configuration Service

Regulatory Configuration Service (RCS) 提供用于配置电子开票的配置和设计体验。 将在 RCS 中创建、维护和管理环境和电子开票功能等资源。 在资源准备就绪后，它们将被发布到电子开票服务。

有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)。

要注册 RCS，请转到 [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) 页面。

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>步骤 2：在 Microsoft Dynamics Lifecycle Services 中安装微服务的加载项

电子开票服务是一组托管在 Microsoft 数据中心中的微服务。 默认情况下，Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的客户无权访问电子开票服务。 您必须在 Microsoft Dynamics Lifecycle Services (LCS) 中将其安装为加载项。 安装加载项时，您的 Finance 或 Supply Chain Management 环境将在允许连接到电子开票服务的应用程序的注册表中注册。

要完成此步骤，请参阅[在 Lifecycle Services 中安装微服务的加载项](e-invoicing-install-add-in-microservices-lcs.md)。

### <a name="step-3-set-up-rcs"></a>步骤 3：设置 RCS

您必须设置 RCS 和电子开票服务之间的集成。 还必须设置主要组件。

要完成此步骤，请参阅[设置 Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md)。

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>步骤 4：Microsoft Power Platform 插件管理员引用

有些场景需要在 Microsoft Power Platform 的范围内与 Dataverse 集成。

目前，如果您将电子开票解决方案用于印度尼西亚电子开票场景，此设置是强制性的。 但是，对于沙特阿拉伯电子发票场景，它是可选的。 有关详细信息，请参阅[按国家或地区划分的电子开票功能的可用性](e-invoicing-country-specific-availability.md)。

要完成此步骤，请参阅 [Microsoft Power Platform 插件管理员引用](e-invoicing-power-platform-plug-in.md)。
