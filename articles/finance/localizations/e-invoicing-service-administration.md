---
title: 电子开票管理组件
description: 本主题提供有关与电子开票的管理相关的组件的信息。
author: gionoder
ms.date: 08/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d187e8a03552258099d7021ff056d0726ea60ca1
ms.sourcegitcommit: baf82100f0aa7d5f5f47c7f54bc155d8a07beab5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463866"
---
# <a name="electronic-invoicing-administration-components"></a>电子开票管理组件

[!include [banner](../includes/banner.md)]


本主题提供有关与电子开票的管理相关的组件的信息。 另外还提供有关如何配置电子开票服务的信息。

## <a name="azure"></a>Azure

使用 Microsoft Azure 为密钥保管库创建密码和设置存储帐户。 然后在电子开票的配置中使用密钥保管库密码和存储帐户 SAS 令牌。

## <a name="lifecycle-services"></a>Lifecycle Services

使用 Microsoft Dynamics Lifecycle Services (LCS) 为您的 LCS 部署项目启用电子开票加载项。

> [!NOTE]
> 在 LCS 中安装此加载项至少需要 **第 2 层环境**。 有关环境计划的详细信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) 是用于配置电子开票的界面。 将在 RCS 中创建、维护和托管环境和电子开票功能等资源。 在资源准备就绪后，它们将发布到电子开票服务。

有关 RCS 注册的信息，请参见 [Regulatory services](https://marketing.configure.global.dynamics.com/)。

有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>与电子开票的集成 

必须先配置 RCS 以允许与电子开票通信，然后才能使用 RCS 配置电子发票。 您在 **电子报告参数** 页面的 **电子开票** 选项卡上完成此配置。

#### <a name="service-endpoint"></a><a id='svc-endpoint-uris'></a>服务终结点

电子开票在一些 Azure 数据中心地理区域中可用。 下表列出了每个区域的可用性。


| 数据中心 Azure 地理位置 | 服务终结点 URI                                                       |
|----------------------------|----------------------------------------------------------------------------|
| 美国              | <p>https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing</p> |
| 欧洲                     | <p>https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| 英国             | <p>https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |
| 亚洲                       | <p>https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/</p><p>https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/</p> |

### <a name="service-environments"></a>服务环境

服务环境是逻辑分区，创建这些逻辑分区是为了支持在电子开票中执行全球化功能。 必须在服务环境级别配置安全机密和数字证书以及治理（即访问权限）。

客户可以根据需要创建任意数量的服务环境。 客户创建的所有服务环境都是相互独立的。

必须在 RCS 中创建和维护服务环境。 在服务环境准备就绪后，它们必须发布到电子开票。

#### <a name="service-environment-status"></a>服务环境的状态

服务环境可以通过状态进行管理。 可能的选项有：

- **未发布** – 环境已经创建，但尚未发布。
- **已发布** – 环境已发布到电子开票。
- **已更改** – 已发布环境的属性已更改，但更改尚未发布。

#### <a name="customer-secrets"></a>客户机密

电子开票服务负责将所有业务数据存储在您的公司拥有的 Azure 资源中。 若要确保服务正常运行，并且相应地访问电子开票所需和生成的所有业务数据，您必须创建两个主要 Azure 资源：

- 一个 Azure 存储帐户（Blob 转储），将存储电子单据，包括电子发票、单据转换结果，以及外部 Web 服务的响应。
- 将存储证书和存储帐户（SAS 令牌）的统一资源标识符 (URI) 的 Azure 密钥保管库。


必须专门分配专用的密钥保管库和客户存储帐户，以与电子开票一起使用。 有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。

若要监视密钥保管库的运行状况并接收警报，请为密钥保管库配置 Azure Monitor。 通过启用密钥保管库日志记录，您可以监视哪些人如何以及何时访问了密钥保管库。 有关详细信息，请参阅 [Azure 密钥保管库的监视和警报](/azure/key-vault/general/alert)和[如何启用密钥保管库日志记录](/azure/key-vault/general/howto-logging?tabs=azure-cli)。

最佳做法是定期轮换使用机密。 有关详细信息，请参阅[机密文档](/azure/key-vault/secrets/)。

#### <a name="users"></a>用户

每个服务环境必须在电子开票中列出可以从 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 连接的用户。

#### <a name="publication"></a>发布

服务环境必须先发布到电子开票中，然后才能使用。 仅已发布的环境可以由 Finance 和 Supply Chain Management 访问。 此外，必须在服务环境属性的任何更新在电子开票服务中生效前发布服务环境。

### <a name="connected-applications"></a>已连接的应用程序

连接的应用程序是您可能希望通过 RCS 到达的 Finance 和 Supply Chain Management 的实例。 除了应用程序 URL 及其租户外，连接的应用程序还包含让 RCS 可以连接到环境的凭证。

通过连接的应用程序，您可以在 Finance 和 Supply Chain Management 中配置电子开票功能的一部分，来让整个电子开票功能正常工作。

## <a name="finance-and-supply-chain-management"></a>Finance 和 Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>与电子开票的集成

必须先将电子开票配置为允许与服务通信，然后才能通过电子开票使用 Finance 和 Supply Chain Management 开具电子发票。

#### <a name="electronic-invoicing-integration-feature"></a>电子开票集成功能

若要启用 Finance 和 Supply Chain Management 与电子开票之间的通信，必须在 **功能管理** 工作区中打开 **电子开票集成** 功能。

#### <a name="service-endpoint"></a>服务终结点

服务终结点是电子开票所在的 URL。 必须先在 Finance 和 Supply Chain Management 配置服务终结点以允许与服务通信，然后才能够开具电子发票。

要配置服务终结点，转到 **组织管理 \> 设置 \> 电子单据参数**，然后在 **电子开票** 选项卡上的 **终结点 URL** 字段中，输入本主题前文中[服务终结点](#svc-endpoint-uris)部分中的表中的终结点 URL。

#### <a name="environments"></a>环境

在 Finance 和 Supply Chain Management 中输入的环境名称是指在 RCS 中创建并发布到电子开票的环境的名称。

必须在 **电子单据参数** 页面的 **电子开票** 选项卡中配置环境。 这样，有关颁发电子发票的每个请求中都包含满足以下条件的环境：其中的电子开票可以决定哪个电子开票功能必须处理这些请求。

## <a name="additional-resources"></a>其他资源

- [在 RCS 中配置电子发票](e-invoicing-configuration-rcs.md)
- [在 Finance 和 Supply Chain Management 中开具电子发票](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
