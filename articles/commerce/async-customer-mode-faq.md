---
title: 异步客户创建模式常见问题解答
description: 本文提供 Microsoft Dynamics 365 Commerce 中异步客户创建模式的相关常见问题的解答。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690194"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>异步客户创建模式常见问题解答

[!include [banner](includes/banner.md)]

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

1. 在 Commerce Headquarters 中运行 CDX P 作业，以确保异步客户数据存储在 **RETAILASYNCCUSTOMERV2**、**RETAILASYNCADDRESSV2**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERAFFILIATION** 和 **RETAILASYNCCUSTOMERATTRIBUTEV2** 表中。
1. 在 Commerce Headquarters 中运行 **同步客户和渠道请求** 批处理作业。 成功执行此批处理作业后，已从先前提及的表中成功处理的所有记录都会将 **OnlineOperationCompleted** 字段设置为 **1**。

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>我怎样能够知道异步模式操作中的哪些客户管理失败了？如果需要，我如何进行更改？

要查看所有异步模式操作及其同步状态，在 Commerce headquarters 中，转到 **Retail 和 Commerce \> 客户 \> 客户同步状态**。 要进行更改，编辑特定操作，更新字段，选择 **保存**，然后选择 **同步** 同步更改。

