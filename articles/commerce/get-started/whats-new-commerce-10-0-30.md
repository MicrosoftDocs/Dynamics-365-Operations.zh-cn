---
title: Dynamics 365 Commerce 10.0.30 预览版（2022 年 11 月）
description: 本文介绍 Microsoft Dynamics 365 Commerce 10.0.30 中的新增功能或更改的功能。
author: josaw1
ms.date: 12/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: a449c7eff21c059555f9659ea932705858d26275
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831739"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Dynamics 365 Commerce 10.0.30 预览版（2022 年 11 月）

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文列出了 Microsoft Dynamics 365 Commerce 预览版 10.0.30 中的新增或更改的功能。 此版本的构建版本号为 10.0.1362，并按以下时间表提供：

- **预览版本：** 2022 年 9 月
- **版本的正式发布时间（自我更新）：** 2022 年 10 月
- **版本的正式发布时间（自动更新）：** 2022 年 11 月

## <a name="features-included-in-this-release"></a>此版本中包含的功能

下表列出了此版本中包含的功能。 我们可能会更新本文，以包含在最初发布本文之后添加到内部版本的功能。

| 特征区域 | 功能 | 更多信息… | 启用者: ，时间:  |
|---------|------------------|----------------|--------------| 
| 客户支持   | 使用 Power Virtual Agents 机器人在电子商务站点上聊天。 | 此功能将使电子商务站点用户可以选择使用 Power Virtual Agents 聊天机器人来提交支持请求。 | 由管理员/制作者为最终用户启用 |
| 见解  |  将销售点 (POS) 操作见解事件流式传输到您的 Application Insights 帐户。 | [在 Application Insights 中访问日志](../dev-itpro/operational-insights.md#enable-diagnostic-events-in-application-insights)   |  IT 专业人员/开发人员选择加入   |
|  付款  | 超过 29 天授权期的 PayPal 订单支持。 | PayPal 的最长授权期限为 29 天，之后必须生成新的授权和订单 ID。 作为替代方案，PayPal 提供了一个选项，可以将 PayPal 订单作为一般订单引用，从而允许针对同一订单 ID 进行多次授权和捕获，而不是在 29 天时生成新的授权和订单 ID）。 | 在 Commerce headquarters 中配置 PayPal 付款连接器时，已添加字段 **OrderIntent**，此字段可以有两个值：<p><p>- **Authorize** - 此配置为默认配置（如果字段留空，**Authorize** 将作为默认值）。 将 **OrderIntent** 配置为 **Authorize** 将与 **NO_INSTRUCTION** 的 PayPal **processing_instruction** 值相关。 订单将通过 PayPal 授权，使用此值时无法修改授权。<p>- **Save** - 当 **OrderIntent** 值设置为 **Save** 时，将与 **ORDER_SAVED_EXPLICITLY** 的 PayPal **processing_instruction** 值相关。 使用此值时，订单引用将保存在 PayPal 服务中。  |
| POS 登录  | [为 POS 登录启用自助诊断功能](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  此功能在销售点 (POS) 和 Commerce headquarters 中提供自助诊断功能，来帮助商店员工和经理快速发现和解决 POS 登录问题的根本原因。<p><p>- 改进了 POS 登录屏幕上显示的失败消息，以提供具体的根本原因信息，帮助使用 POS 的商店员工了解问题所在，让他们可以采取必要的措施来解决问题。<p>- Commerce headquarters 中的 **工作人员** 页面提供 **测试登录** 功能，让设置 POS 设备的商店经理可以模拟 POS 登录。 在登录失败的情况下，此功能提供可操作的故障排除指南，让经理可以检查相关配置、更正问题并验证修复。  | 默认打开 |


## <a name="additional-resources"></a>其他资源

### <a name="platform-updates-for-finance-and-operations-apps"></a>Finance and Operations 应用的平台更新

Dynamics 365 Finance 10.0.30 包括平台更新。 要了解详细信息，请参阅[财务和运营应用版本 10.0.30 的平台更新](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md)。

### <a name="bug-fixes"></a>缺陷修复

有关版本 10.0.30 中各更新内的缺陷修复的信息，请登录 Lifecycle Services (LCS)，然后查看[知识库文章](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468)。 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 和行业云：2022 版本第 2 波计划

是否对我们的任何商业应用或平台即将推出和最近发布的功能感兴趣？

查看 [Dynamics 365 和行业云：2022 版本第 2 波计划](/dynamics365-release-plan/2022wave2/)。 一个文档汇总了所有端到端、上至下的详细信息，可用其进行规划。

### <a name="removed-and-deprecated-features"></a>已删除和弃用的功能

[Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文介绍了针对 Commerce 删除或弃用的功能。

- *已移除* 的功能在产品中不再可用。
- *已弃用* 的功能在活跃的开发中不存在，而且在将来的更新中可能被移除。

从该产品中删除任何功能之前 12 个月，将在 [Dynamics 365 Commerce 中已删除或弃用的功能](removed-deprecated-features-commerce.md)一文中发布弃用通知。

对于仅影响编译时，但是与沙盒和生产环境二进制兼容的突发更改，弃用时间将低于 12 个月。 通常是需要对编译器进行的功能更新。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
