---
title: 异步客户创建模式
description: 本文介绍 Microsoft Dynamics 365 Commerce 中的异步客户创建模式。
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 1ac1bc842d5d12ece8951ffed18157e6f9b50d14
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228715"
---
# <a name="asynchronous-customer-creation-mode"></a>异步客户创建模式

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

本文介绍 Microsoft Dynamics 365 Commerce 中的异步客户创建模式。

在 Commerce 中，有两种客户创建模式：同步和异步。 默认情况下，系统会同步创建客户。 换句话说，客户是在 Commerce Headquarters 中实时创建的。 同步客户创建模式很有用，因为可以跨渠道立即搜索新客户。 但是，它也有一个缺点。 因为它会向 Commerce Headquarters 发出 [Commerce Data Exchange：实时服务](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)请求，如果同时发出许多客户创建请求，则性能可能会受到影响。

如果在商店的功能配置文件（**Retail 和 Commerce \> 渠道设置 \> 在线商店设置 \> 功能配置文件**）中将 **以异步模式创建客户** 选项设置为 **是**，则实时服务请求不会用于在渠道数据库中创建客户记录。 异步客户创建模式不会影响 Commerce Headquarters 的性能。 临时全局唯一标识符 (GUID) 会分配给每个新的异步客户记录，并用作客户帐户 ID。 该 GUID 不会显示给销售点 (POS) 用户。 相反，这些用户看到的客户帐户 ID 为 **待同步**。

> [!IMPORTANT]
> 只要 POS 脱机，系统都将自动异步创建客户，即使禁用了异步客户创建模式也不例外。 因此，无论您选择同步客户创建还是异步客户创建，Commerce Headquarters 管理员必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业创建并计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

## <a name="async-customer-limitations"></a>异步客户限制

异步客户功能当前具有以下限制：

- 除非新客户帐户 ID 已被重新同步到渠道，否则不能将会员卡发给异步客户。

## <a name="async-customer-enhancements"></a>异步客户增强

为了帮助组织使用异步客户创建模式管理客户，并帮助减少与 Commerce Headquarters 的实时通信，已推出以下增强功能，以便在渠道中同步和异步模式之间实现均等性。 

| 功能增强 | Commerce 版本 | 功能详细信息 |
|---|---|---|
| 从渠道数据库检索客户信息时的性能改进 | 10.0.20 及更高版本 | 为了帮助改进性能，客户实体将拆分为较小的实体。 然后，系统仅从渠道数据库中检索所需信息。 |
| 能够在结帐期间异步创建地址 | 10.0.22 及更高版本 | <p>功能开关：**启用客户地址异步创建**</p><p>功能详细信息：</p><ul><li>能够在不向 Commerce Headquarters 进行实时服务调用的情况下添加地址</li><li>能够在不使用记录 ID（**RecId** 值）的情况下唯一标识渠道数据库中的地址</li><li>地址创建的跟踪时间戳</li><li>Commerce Headquarters 中的地址同步</li></ul><p>此功能将同时影响同步客户和异步客户。 若要异步编辑地址，除了异步创建地址外，您还必须启用 **在异步模式下编辑客户** 功能。</p> |
| 在同步和异步客户创建之间实现均等性。 | 10.0.24 及更高版本 | <p>功能开关：**启用增强型异步客户创建**</p><p>功能详细信息：在异步创建客户时，能够捕获其他信息，如标题、默认客户的隶属关系以及辅助联系人信息（电话号码和电子邮件地址）</p> |
| 用户友好型错误消息 | 10.0.28 及更高版本 | 如果用户在进行同步时无法立即编辑信息，则这些增强功能有助于改进用户友好型错误消息。 通过在 Commerce 站点生成器中的 **站点设置 \> 扩展** 中使用 **不允许异步客户修改某些 UI 元素** 设置，您可以启用这些增强功能。 |
| 能够异步编辑客户信息 | 10.0.29 及更高版本 | <p>功能开关：**启用在异步模式下编辑客户**</p><p>功能详细信息：能够异步编辑客户数据</p><p>有关与异步编辑客户信息相关的问题的常见问题解答，请参阅[异步客户创建模式常见问题解答](async-customer-mode-faq.md)。</p> |

### <a name="feature-switch-hierarchy"></a>开关功能层次结构

由于功能开关层次结构的缘故，在启用 **启用在异步模式下编辑客户** 功能之前，必须启用以下功能： 

- **针对客户订单和客户交易记录的性能改进** - 自 Commerce 版本 10.0.28 发布以来，此功能一直是必备功能。 
- **启用增强型异步客户创建**
- **启用客户地址异步创建**

有关常见疑难解答问题的解答，请参阅[异步客户创建模式常见问题解答](async-customer-mode-faq.md)。 

启用前面提到的功能后，您必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

### <a name="customer-creation-in-pos-offline-mode"></a>在 POS 脱机模式下创建客户

正如前面提到的，只要 POS 脱机，系统都将自动异步创建客户，即使禁用了异步客户创建模式也不例外。 因此，Commerce Headquarters 管理员必须为 **P 作业**、**从异步模式同步客户和业务合作伙伴** 作业和 **1010** 作业创建并计划一个重复执行的批处理作业，以便在 Commerce Headquarters 中将任何异步客户转换为同步客户。

> [!NOTE]
> 如果在 **商业渠道架构** 页（**Retail 和 Commerce \> Headquarters 设置 \> 商业调度 \> 渠道数据库组**）上将 **筛选共享的客户数据表** 选项设置为 **是**，则不会在 POS 联机模式下创建客户记录。 有关详细信息，请参阅[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)。

## <a name="additional-resources"></a>其他资源

[商店中的客户管理](customer-mgmt-stores.md)

[将异步客户转换为同步客户](convert-async-to-sync.md)

[客户属性](dev-itpro/customer-attributes.md)

[脱机数据排除](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
