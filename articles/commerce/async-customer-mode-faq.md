---
title: 异步客户创建模式常见问题解答
description: 本文提供 Microsoft Dynamics 365 Commerce 中异步客户创建模式的相关常见问题的解答。
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229866"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>异步客户创建模式常见问题解答

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文提供 Microsoft Dynamics 365 Commerce 中异步客户创建模式的相关常见问题的解答。

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>为什么我无法启用“启用在异步模式下编辑客户”功能？

在启用 **启用在异步模式下编辑客户** 功能之前，必须启用以下功能：

- 针对客户订单和客户交易记录的性能改进
- 启用增强型异步客户创建
- 启用客户地址异步创建

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>为什么在启用“启用在异步模式下编辑客户”功能后，我仍会看到对 Commerce Headquarters 的实时服务调用？

在未运行 Commerce Data Exchange (CDX) 作业来确保功能状态和其他渠道元数据与渠道同步时，会出现此问题。 在重试此方案之前，请确保在 Commerce Headquarters 中运行以下 CDX 作业：

- 1110（全局配置）
- 1010（客户）
- 1070（渠道配置）

在运行 CDX 作业后，在 Commerce Scale Unit (CSU) 中缓存的数据可能不会立即反映在 Commerce Headquarters 中。

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>为什么 Commerce Headquarters 不显示销售点 (POS) 或电子商务渠道中的客户创建或更新？

确保已按照此处列出的操作顺序执行了以下操作。

1. 在 Commerce Headquarters 中运行 CDX P 作业，以确保存储在 **RETAILASYNCCUSTOMERV2**、**RETAILASYNCADDRESSV2**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERAFFILIATION** 和 **RETAILASYNCCUSTOMERATTRIBUTEV2** 表中的异步客户数据在 Commerce headquarters 中可用。
1. 在 Commerce Headquarters 中运行 **同步客户和渠道请求** 批处理作业。 成功执行此批处理作业后，已从先前提及的表中成功处理的所有记录都会将 **OnlineOperationCompleted** 字段设置为 **1**。
