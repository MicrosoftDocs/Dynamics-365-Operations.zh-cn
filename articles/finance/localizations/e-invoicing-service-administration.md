---
title: 电子开票管理组件
description: 本主题提供有关与电子开票的管理相关的组件的信息。
author: gionoder
ms.date: 04/29/2021
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
ms.openlocfilehash: 081d23c85d3555210b54597920a49e800ffe284b
ms.sourcegitcommit: 35fdcc6501e099c54a58583b1e3aba16f02a5ccc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2021
ms.locfileid: "5980914"
---
# <a name="electronic-invoicing-administration-components"></a>电子开票管理组件

[!include [banner](../includes/banner.md)]


本主题提供有关与电子开票的管理相关的组件的信息。 另外还提供有关如何配置电子开票服务的信息。

## <a name="azure"></a>Azure

使用 Microsoft Azure 为密钥保管库和存储帐户创建机密。 然后，在电子开票的配置中使用这些机密。

## <a name="lifecycle-services"></a>Lifecycle Services

使用 Microsoft Dynamics Lifecycle Services (LCS) 为您的 LCS 部署项目启用微服务。

> [!NOTE]
> 在 LCS 中安装微服务至少需要第 2 层虚拟机。 有关环境计划的详细信息，请参阅[环境计划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) 是用于配置电子开票的界面。 将在 RCS 中创建、维护和托管环境和电子开票功能等资源。 在资源准备就绪后，它们将发布到电子开票服务。

有关 RCS 注册的信息，请参见 [Regulatory services](https://marketing.configure.global.dynamics.com/)。

有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)

### <a name="integration-with-electronic-invoicing"></a>与电子开票的集成 

必须先配置 RCS 以允许与电子开票通信，然后才能使用 RCS 配置电子发票。 您在 **电子报告参数** 页面的 **电子开票** 选项卡上完成此配置。

#### <a name="service-endpoint"></a>服务终结点

电子开票在一些 Azure 数据中心地理区域中可用。 下表列出了每个区域的可用性。

| Azure 数据中心地理位置 |
|----------------------------|
| 美国              |
| 欧洲                     |
| 英国             |
| 亚洲                       |

### <a name="service-environments"></a>服务环境

服务环境是逻辑分区，创建这些逻辑分区以支持电子开票中电子开票功能的执行。 必须在服务环境级别配置安全机密和数字证书以及治理（即访问权限）。

客户可以根据需要创建任意数量的服务环境。 客户创建的所有服务环境都是相互独立的。

必须在 RCS 中创建和维护服务环境。 在服务环境准备就绪后，它们必须发布到电子开票。

#### <a name="service-environment-status"></a>服务环境的状态

服务环境可以通过状态进行管理。 可能的选项有：

- **未发布** – 环境已经创建，但尚未发布。
- **已发布** – 环境已发布到电子开票。
- **已更改** – 已发布环境的属性已更改，但更改尚未发布。

#### <a name="customer-secrets"></a>客户机密

电子开票服务负责将所有业务数据存储在您的公司拥有的 Azure 资源中。 若要确保服务正常运行，并且相应地访问电子开票所需和生成的所有业务数据，您必须创建两个主要 Azure 资源：

- 将存储电子发票的 Azure 存储帐户（Blob 存储）
- 将存储证书和存储帐户的统一资源标识符 (URI) 的 Azure 密钥保管库


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

若要配置服务终结点，请转到 **组织管理 \> 设置 \> 电子单据参数**，然后在 **提交服务** 选项卡上的 **电子开票 URL** 字段中，按照 **服务终结点** 部分所述的表中的说明输入 URL。

#### <a name="environments"></a>环境

在 Finance 和 Supply Chain Management 中输入的环境名称是指在 RCS 中创建并发布到电子开票的环境的名称。

必须在 **电子单据参数** 页面的 **提交服务** 选项卡上配置环境，以便让每个开具电子发票的请求都包含电子开票可以确定哪个电子开票功能必须处理请求的环境。

## <a name="additional-resources"></a>其他资源

- [在 RCS 中配置电子发票](e-invoicing-configuration-rcs.md)
- [在 Finance 和 Supply Chain Management 中开具电子发票](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
