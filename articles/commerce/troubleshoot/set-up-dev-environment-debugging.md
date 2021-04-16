---
title: 设置电子商务开发环境以针对 1 级零售服务器虚拟机进行调试
description: 本主题介绍如何设置电子商务开发环境以针对 1 级零售服务器虚拟机 (VM) 进行调试。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 5ef286aa28ff459befb72b0178f308e5fb85ec44
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801475"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>设置电子商务开发环境以针对 1 级零售服务器虚拟机进行调试

[!include [banner](../../includes/banner.md)]

本主题介绍如何设置电子商务开发环境以针对 1 级零售服务器虚拟机 (VM) 进行调试。

## <a name="description"></a>说明

通常会为 Commerce Runtime (CRT) 和销售点 (POS) 扩展开发部署 Microsoft Dynamics 365 Commerce 1 级环境。 它们是独立的环境。 由于架构具有服务型软件 (SaaS) 性质，因此它们不包含电子商务组件。

在某些情况下，您可能希望在 1 级环境中测试对扩展的调用，以便可以调试电子商务组件中的扩展。 有关一般说明，请参阅[针对 1 级商业开发环境进行调试](../e-commerce-extensibility/debug-tier-1.md)。

当您针对 1 级环境进行调试时，由于该站点现在会调用另一台零售服务器，因此跨服务器调用可能会导致与内容安全策略相关的各种错误。

下图显示了在产品详细信息页面上选择变体时可能会发生的错误的示例。

![在产品详细信息页面上选择变体时出错](media/unhandled-rejection-error.jpg)

下图显示了浏览器的调试器工具（F12 开发人员工具）中类似错误的示例。 该错误消息提到违反内容安全策略指令。

![调试器工具错误](media/debugger-tools-error.JPG)

## <a name="resolution"></a>解决方法

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>在 Commerce 站点构建器中对站点禁用内容安全策略

1. 选择您正在处理的站点。
1. 选择 **设置**，然后选择 **扩展**。
1. 在 **内容安全策略** 选项卡上，选择 **禁用内容安全策略**。
1. 选择 **保存并发布**。

> [!NOTE]
> 企业对消费者 (B2C) 登录在本地开发环境中不起作用。 但是，您可以根据需要使用来宾结帐或构建页面模拟来模拟用户登录。

## <a name="additional-resources"></a>其他资源

[电子商务在线可扩展性开发入门](../e-commerce-extensibility/sdk-getting-started.md)

[在电子商务站点上管理内容安全策略 (CSP)](../manage-csp.md)
