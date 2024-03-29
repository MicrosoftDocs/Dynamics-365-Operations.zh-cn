---
title: 税款计算概览
description: 本文说明税务计算功能的总体范围和功能。
author: EricWangChen
ms.date: 09/08/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: cafc4c7089e0c042fc65c1e3fd21f8f1e930b785
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689876"
---
# <a name="tax-calculation-overview"></a>税款计算概览

[!include [banner](../includes/banner.md)]

税务计算是一种超级可扩展的多租户服务，使 Global Tax Engine 可以自动化并简化税务确定和计算流程。 税务引擎完全可配置。 可配置的元素包括但不限于应纳税数据模型、税码、税务适用性矩阵和税务计算公式。 税务引擎在 Microsoft Azure 核心服务平台上运行，并提供现代技术和指数可扩展性。

税务计算将 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 集成。 最终，它还将与 Dynamics 365 Project Operations、Dynamics 365 Commerce 以及其他第一方和第三方应用程序集成。

> [!IMPORTANT]
> 当您启用税款计算时，可能在数据中心（维护您的服务数据的数据中心除外）中执行对相关数据的某些操作。 在启用税款计算之前，查看[条款和条件](https://go.microsoft.com/fwlink/?linkid=2156043)。 我们非常尊重您的隐私。 要了解详细信息，请阅读我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=521839)。

税款计算是一款基于微服务的税务引擎，它提供指数级可扩展性，并且可以帮助您执行以下任务：

- 通过增强的确定机制自动确定正确的销售税组、物料销售税组和税码。
- 支持一个法人多个税务登记号，自动确定应税交易的正确税务登记号。
- 支持转移单的税务确定、计算、过帐和结算。
- 定义特定业务要求的可配置税金计算公式和条件。
- 在法人之间共享税务确定和计算解决方案，以省去维护工作并避免错误。
- 支持客户和供应商税务登记编号确定。
- 支持列表代码确定。
- 在税区级别支持税款计算参数。

若要使用税款计算，请在 Microsoft Dynamics Lifecycle Services 中从您的项目安装税款计算加载项。 然后，在 [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) 中完成设置，并在 Finance 和 Supply Chain Management 中启用税款计算。 有关详细信息，请参阅[开始使用税务服务](global-get-started-with-tax-calculation-service.md)。

## <a name="availability"></a>可用性

从版本 10.0.21 起，税款计算在生产环境中向所有客户公开发布。

将继续交付新功能。 请经常查看最新的发布计划，以了解受支持功能的覆盖率和范围。

税务计算在以下 Azure 地理区域中部署。 将根据客户需求添加更多 Azure 地理区域。

- 亚太
- 澳大利亚
- 巴西
- 加拿大
- 欧洲
- 法国
- 印度
- 日本
- 南非
- 瑞士
- 阿拉伯联合酋长国
- 英国
- 美国

> [!NOTE]
> 税款计算不支持早期版本的 Dynamics 365，例如 Dynamics AX 2012 或 Dynamics 365 的本地部署。

## <a name="versions"></a>版本
我们建议您使用与您的 Finance 或 Supply Chain Management 版本相匹配的版本导入和设置税款计算配置。

| Finance 或 Supply Chain Management 版本 | 税务配置版本               |
| --------------- | --------------------------------------- |
| 10.0.31         | 税款计算配置 40.56.240 |
| 10.0.30         | 税款计算配置 40.55.239 |
| 10.0.29         | 税款计算配置 40.55.236 |
| 10.0.28         | 税款计算配置 40.54.234 |
| 10.0.27         | 税款计算配置 40.54.234 |


## <a name="data-flow"></a>数据流

以下是税款计算的数据流流程的概述。 

1. 在 RCS 中，查看和导入应纳税单据模型配置和模型映射配置。 如果您必须扩展高级方案的配置，请参阅[在税务配置中添加数据字段](tax-service-add-data-fields-tax-configurations.md)。
2. 在 RCS 中，创建或维护税务功能。 您可以使用税务功能来维护税率和税适用性规则。
3. 完成税务功能设置后，将 RCS 中的税务配置和税务功能发布到全局存储库。
4. 在 Finance 中，选择要用于特定法人的税务功能设置版本。
5. 在 Finance 和 Supply Chain Management 中，照常操作交易。 需要税款计算时，客户端将从交易（如销售订单或采购订单）中收集信息，并将信息打包为有效负载。 然后将发送一个请求以计算税款。
6. 从客户端收到税款计算请求，并完成计算。 税务结果随后返回到客户端。
7. Dynamics 365 客户端将收到税务结果，并在销售税页面上显示税金计算结果。

## <a name="supported-transactions"></a>支持的交易

可以通过交易来启用税款计算。 

下表列出了对应版本支持的交易。

| 版本 | 交易记录 |
|---------|--------------|
| 10.0.29 | 期间日记帐 |
| 10.0.28 | 供应商付款日记帐<br> 客户付款日记帐 | 
| 10.0.26 | 普通日记帐<br> 供应商发票日记帐 |
| 10.0.23 | 普通发票 |
| 10.0.21| 销售额<br><ul><li>销售报价</li><li>销售订单</li><li>确认</li><li>领料单</li><li>装箱单</li><li>销售账单</li><li>贷方通知单</li><li>退货单</li><li>标题杂项费用</li><li>行杂项费用</li></ul>采购<br><ul><li>采购订单</li><li>确认单</li><li>收货清单</li><li>产品收货</li><li>采购账单</li><li>标题杂项费用</li><li>行杂项费用</li><li>贷方通知单</li><li>退货单</li><li>采购申请</li><li>采购申请行杂项费用</li><li>询价</li><li>询价标题杂项费用</li><li>询价行杂项费用</li></ul>库存<ul><li>转移单 – 装运</li><li>转移单 – 接收</li></ul>|

## <a name="supported-countriesregions"></a>支持的国家/地区

税款计算可以使用支持的本地化功能运行。 下表列出了法人主要地址的国家/地区。

| 版本 | 国家/地区 |
|---------|----------------|
| 10.0.26 | - 中国 <br>- 捷克共和国<br>- 西班牙 |
| 10.0.24 | 墨西哥 |
| 10.0.23 | - 泰国 <br>- 日本 <br>- 马来西亚 <br>- 新加坡 |
| 10.0.22 | - 澳大利亚<br>- 巴林 <br>- 加拿大<br>- 埃及 <br>- 香港特别行政区 <br>- 科威特 <br>- 新西兰 <br>- 阿曼 <br>- 卡塔尔 <br>- 沙特阿拉伯 <br>- 南非 <br>- 阿拉伯联合酋长国 |
| 10.0.21 | - 奥地利 <br>- 比利时 <br>- 丹麦 <br>- 爱沙尼亚 <br>- 芬兰 <br>- 法国 <br>- 德国 <br>- 匈牙利 <br>- 冰岛 <br>- 爱尔兰 <br>- 意大利 <br>- 拉脱维亚 <br>- 立陶宛 <br>- 荷兰 <br>- 挪威 <br>- 波兰 <br>- 瑞典 <br>- 瑞士 <br>- 英国 <br>- 美国 |

对于未由 Microsoft 本地化的任何国家/地区，还可以使用其他全局功能启用和运行税收计算。

## <a name="related-resources"></a>相关资源

[开始使用税务服务](./global-get-started-with-tax-calculation-service.md)

[多个增值税登记编号](./emea-multiple-vat-registration-numbers.md)

[转移单的税务功能支持](./tasks/tax-feature-support-for-transfer-order.md)

[如何在税务服务中生成扩展](./tax-service-add-data-fields-tax-integration-by-extension.md)
