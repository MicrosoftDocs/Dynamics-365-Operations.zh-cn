---
title: 电子开票附加产品管理组件
description: 本主题提供有关与电子开票附加产品的管理相关的组件的信息。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104350"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>电子开票附加产品管理组件

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

本主题提供有关与电子开票附加产品的管理相关的组件的信息。 另外还提供有关如何配置电子开票附加产品服务的信息。

## <a name="azure"></a>Azure

使用 Microsoft Azure 为密钥保管库和存储帐户创建机密。 然后在电子开票附加产品的配置中使用这些机密。

## <a name="lifecycle-services"></a>Lifecycle Services

使用 Microsoft Dynamics Lifecycle Services (LCS) 为您的 LCS 部署项目启用微服务附加产品。

在 LCS 中，选择 **预览功能管理** 磁贴，然后打开 **电子开票服务** 功能。

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) 是用于配置电子开票附加产品的界面。 将在 RCS 中创建、维护和托管环境和电子开票功能等资源。 当资源准备好后，它们将被发布到电子开票附加产品服务。

有关 RCS 的详细信息，请参阅 [Regulatory Configuration Services (RCS) - 全球化功能](rcs-globalization-feature.md)

### <a name="integration-with-the-electronic-invoicing-add-on"></a>与电子开票附加产品集成

必须先配置 RCS 以允许与电子开票附加产品通信，然后才能够使用 RCS 配置电子发票。 您在 **电子报告参数** 页的 **电子开票附加产品** 选项卡上完成此配置。

#### <a name="service-endpoint"></a>服务终结点

电子开票附加产品终结点的 URL 可能根据 Azure 数据中心的地理位置发生变化。 下表列出了每个区域的可用性：

| Azure 数据中心地理位置 | 服务终结点 URL                                                       |
|----------------------------|----------------------------------------------------------------------------|
| 美国东部                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| 美国西部                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| 欧洲北部                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| 欧洲西部                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>申请 ID

应用程序 ID 是电子开票附加产品应用程序的 ID。 在此例中，此值是固定的：**0cdb527f-a8d1-4bf8-9436-b352c68682b2**。

#### <a name="lcs-environment-id"></a>LCS 环境 ID

LCS 环境 ID 是您组织的 LCS 订阅的 ID。

### <a name="service-environments"></a>服务环境

服务环境是逻辑分区，创建这些逻辑分区用以支持电子开票附加产品中电子开票功能的执行。 必须在服务环境级别配置安全机密和数字证书以及治理（即访问权限）。

客户可以根据需要创建任意数量的服务环境。 客户创建的所有服务环境都是相互独立的。

必须在 RCS 中创建和维护服务环境。 当服务环境准备好后，它们必须被发布到电子开票附加产品。

#### <a name="service-environment-status"></a>服务环境的状态

服务环境可以通过状态进行管理。 可能的选项有：

- **未发布** – 环境已经创建，但尚未发布。
- **已发布** – 环境已发布到电子开票附加产品。
- **已更改** – 已发布环境的属性已更改，但更改尚未发布。

#### <a name="customer-secrets"></a>客户机密

电子开票附加产品服务负责将所有业务数据存储在您的公司拥有的 Azure 资源中。 为确保服务正常运行，并且仅电子开票附加产品能够访问此附加产品所需的和生成的所有业务数据，您必须创建两个主要的 Azure 资源：

- 将存储电子发票的 Azure 存储帐户（Blob 存储）
- 将存储证书和存储帐户的统一资源标识符 (URI) 的 Azure 密钥保管库

> [!NOTE]
> 必须专门分配专用的密钥保管库和客户存储帐户，以与电子开票附加产品一起使用。

有关详细信息，请参阅[创建 Azure 存储帐户和密钥保管库](e-invoicing-create-azure-storage-account-key-vault.md)。

#### <a name="users"></a>用户

每个服务环境必须在电子开票附加产品中列出可以从 Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 连接的用户。

#### <a name="publication"></a>发布

服务环境必须先发布到电子开票附加产品中，然后才能使用。 仅已发布的环境可以由 Finance 和 Supply Chain Management 访问。 此外，必须在服务环境属性的任何更新在电子开票服务中生效前发布服务环境。

### <a name="connected-applications"></a>已连接的应用程序

连接的应用程序是您可能希望通过 RCS 到达的 Finance 和 Supply Chain Management 的实例。 除了应用程序 URL 及其租户外，连接的应用程序还包含让 RCS 可以连接到环境的凭证。

通过连接的应用程序，您可以在 Finance 和 Supply Chain Management 中配置电子开票功能的一部分，来让整个电子开票功能正常工作。

## <a name="finance-and-supply-chain-management"></a>Finance 和 Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>与电子开票附加产品集成

必须先将电子开票附加产品配置为允许与服务通信，然后才能够通过电子开票附加产品使用 Finance 和 Supply Chain Management 开具电子发票。

#### <a name="electronic-invoicing-add-on-integration-feature"></a>电子开票附加产品集成功能

要启用 Finance 和 Supply Chain Management 与电子开票附加产品之间的通信，必须在 **功能管理** 工作区打开 **电子开票附加产品集成** 功能。

#### <a name="service-endpoint"></a>服务终结点

服务终结点是电子开票附加产品所在的 URL。 必须先在 Finance 和 Supply Chain Management 配置服务终结点以允许与服务通信，然后才能够开具电子发票。

要配置服务终结点，转到 **组织管理 \> 设置 \> 电子单据参数**，然后在 **提交服务** 选项卡上的 **电子开票附加产品 URL** 字段中，按照 **服务终结点** 一节所述的表中的说明输入 URL。

#### <a name="environments"></a>环境

在 Finance 和 Supply Chain Management 中输入的环境名称是指在 RCS 中创建并发布到电子开票附加产品的环境的名称。

必须在 **电子单据参数** 页的 **提交服务** 选项卡上配置环境，让每个开具电子发票的请求都包含电子开票附加产品可以确定哪个电子开票功能必须处理请求的环境。

## <a name="additional-resources"></a>其他资源

- [在 RCS 中配置电子发票](e-invoicing-configuration-rcs.md)
- [在 Finance 和 Supply Chain Management 中开具电子发票](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
