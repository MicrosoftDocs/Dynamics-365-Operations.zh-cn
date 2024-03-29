---
title: 双重写入概览
description: 本文概括介绍双写入，其提供客户互动应用与财务和运营应用之间的近实时交互。
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 943607a3ef28db11b7bc7805257914117e6ae38c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289629"
---
# <a name="dual-write-overview"></a>双重写入概览

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>什么是双写入？

双写入是一种现成基础结构，其提供 Customer Engagement 应用与财务和运营应用之间的近实时交互。 当有关客户、产品、人员和操作的数据越过应用程序边界时，将为组织中的所有部门授权。

双写入提供财务和运营应用与 Dataverse 之间紧密耦合的双向集成。 财务和运营应用中的所有数据变化都会导致写入 Dataverse，而 Dataverse 中的所有数据变化也会导致写入财务和运营应用。 这个自动化的数据流提供了应用之间的集成用户体验。

![应用之间的数据关系。](media/dual-write-overview.jpg)

双写入有两个方面：*基础结构* 方面和 *应用程序* 方面。

### <a name="infrastructure"></a>基础结构

双写入基础结构可扩展且可靠，并且具有以下关键功能：

+ 应用程序之间的同步和双向数据流
+ 同步和播放、暂停与继续模式，用于在联机和脱机/异步模式下共同为系统提供支持。
+ 在应用程序之间同步初始数据
+ 适用于数据管理员的，合并的活动与错误日志视图
+ 配置自定义警报和阈值与订阅通知
+ 可进行筛选和转换的直观用户界面 (UI)
+ 设置和查看表依赖项和关系
+ 标准和自定义表和映射均可扩展
+ 可靠的应用程序生命周期管理
+ 适用于新客户的现成设置体验

### <a name="application"></a>应用程序

双写入在财务和运营应用中的概念与 Customer Engagement 应用中的概念之间建立映射。 此项集成支持以下方案：

+ 集成客户主数据
+ 访问客户会员卡和奖励分
+ 统一的基础产品体验
+ 感知组织层次结构
+ 集成供应商主数据
+ 访问财务和税务参考数据
+ 按需价格引擎体验
+ 集成的潜在客户到现金体验
+ 通过现场代理吹内部资产和客户资产
+ 集成的采购到付款体验
+ 客户数据和单据的集成活动和通知单
+ 查找现有库存量和详细信息
+ 项目到现金体验
+ 通过当事方概念处理多个地址和角色


## <a name="top-reasons-to-use-dual-write"></a>使用双写入的主要原因

双写入提供 Microsoft Dynamics 365 应用程序之间的数据集成。 这个强大的框架链接了环境，并让不同业务应用程序可以一起工作。 下面是为什么应该使用双写入的主要原因：

+ 双写入提供财务和运营应用与 Customer Engagement 应用之间紧密耦合的近实时双向集成。 此集成使 Microsoft Dynamics 365 成为了所有业务解决方案的一站式商店。 使用 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management，但对客户关系管理 (CRM) 使用非 Microsoft 解决方案的客户正在转向 Dynamics 365，以享受其双写入支持。
+ 客户、产品、操作、项目和物联网 (IoT) 的数据通过双写入自动流向 Dataverse。 这种连接对于对 Power Platform 扩展感兴趣的企业非常有用。
+ 双写入基础结构遵循无代码/少代码原则。 扩展标准表到表映射和包含自定义映射所需工程工作量非常少。
+ 双写入同时支持在线模式和脱机模式。 只有 Microsoft 公司同时支持在线模式和脱机模式。

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>双写入对 Customer Engagement 应用的开发人员和架构师有何意义？

双写入实现了财务和运营应用与 Customer Engagement 应用之间数据流自动化。 双写入由 Dataverse 中安装的两个 AppSource 解决方案构成。 这些解决方案扩展 Dataverse 中的表架构、插件和工作流，以使其可适应 ERP 规模。 若要成功实施，Customer Engagement 应用的开发人员和架构师必须了解这些更改，并与其对应方协作使用财务和运营应用。

为了创建与财务和运营应用程序之间的对等性，双写入在 Dataverse 架构中进行一些关键更改。 如果了解此计划，可以在将来避免一些重复性的设计和开发工作。

+ 安装了双写入 AppSource 包之后，Dataverse 将具有新概念，如公司和相关方。 这些概念可帮助基于 Dataverse 构建的应用程序（包括 Dynamics 365 Sales、Dynamics 365 Marketing、Dynamics 365 Customer Service 和 Dynamics 365 Field Service）与财务和运营应用无缝交互。

+ 活动和通知单统一且已经过扩展，同时支持 C1（系统用户）和 C2（系统客户）。

+ 若要在财务和运营应用与 Dataverse 之间传输币种时避免数据丢失，可以增加 Customer Engagement 应用中币种数据类型内的小数位数。 此功能将现有行自动转换为元数据层的新扩展状态。 在此过程中，币种值转换为十进制数据，而不是货币数据，而货币值则支持 10 个小数位数。 此功能是选择加入的，小数位数不需要超过 4 位的组织不需要选择加入。 有关详细信息，请参阅[双写入货币数据类型迁移](currrency-decimal-places.md)。

+ [日期有效性](../../dev-tools/date-effectivity.md)将添加到 Dataverse。 其将支持同一个表的过去、现在和将来的数据。

+ 产品、报价单、订单和发票支持产品[单位转换](../../../../supply-chain/pim/tasks/manage-unit-measure.md)。

有关即将推出的更改的详细信息，请参阅[双写入中新增或更改的功能](whats-new-dual-write.md)。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

