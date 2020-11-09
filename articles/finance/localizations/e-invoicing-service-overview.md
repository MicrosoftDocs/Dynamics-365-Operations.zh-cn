---
title: 电子开票附加产品概述
description: 本主题提供有关 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的电子开票附加产品的信息。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039738"
---
# <a name="electronic-invoicing-add-on-overview"></a>电子开票附加产品概述

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的电子开票附加产品是一种超级可扩展的多租户服务，可对电子发票单据进行可配置的处理并进行可配置的文档交换。 处理和集成规则完全可配置，逻辑在 Finance 和 Supply Chain Management 外部运行。 此服务主要针对企业对政府方案中的电子发票处理，但可以自定义配置来用于其他目的。

电子开票附加产品可以帮助您实现以下目标：

- 快速轻松地采用国家/地区特定要求
- 标准化实施电子开票附加产品解决方案
- 增强了文档历史记录的可追溯性
- 实施周期更短
- 降低总拥有成本 (TCO)
- 可轻松调整配置，无需更改代码
- 简化配置包装
- 内置的导出、导入和集成，并可在电子发票单据处理中轻松扩展
- 在公司之间轻松重复使用相同的导出、导入和集成配置

要使用电子开票附加产品，您必须从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目安装它。 接下来，按照设置过程打开与 Finance 或 Supply Chain Management 的集成。 有关详细信息，请参阅[开始使用电子开票附加产品](e-invoicing-get-started.md)。

## <a name="availability"></a>可用性

最初，电子开票附加产品可通过预览计划供指定客户使用。 之后，预览将向更多客户开放。 最终，此服务将公开发布。 由于满足国家/地区特定要求的功能可能会在发行的不同阶段受到限制，因此您应该始终查看最新文档，这些文档重点介绍了受支持的国家/地区特定解决方案的覆盖范围。

电子开票附加产品在以下 Azure 地理区域部署：

- 美国
- 欧洲

> [!NOTE]
> 电子开票附加产品不支持本地部署。

## <a name="extended-configurability"></a>扩展的可配置性

电子开票附加产品可用于必须创建电子单据并将其发送给指定方的场景。 它是专为根据接收到的数据运行可配置的处理操作流而设计的。 Finance 和 Supply Chain Management 中提供的可配置性选项仅限于文档转换。 此服务通过添加服务中提供的可配置集成来扩展这些选项。 此外，所有以前提供的电子发票功能，如巴西 Nota fiscal eletrônica (NF-e)、墨西哥 Comprobante Fiscal Digital por Internet (CFDI) 或其他西欧通用商业语言 (UBL)/泛欧洲 Public Procurement OnLine (PEPPOL) 功能，将使用配置导出和导入，以及支持与外部 Web 服务的集成。

## <a name="feature-highlights"></a>功能亮点

- 与 Finance 和 Supply Chain management 的现成集成
- 所有国家或地区的电子发票流程的配置和监视具有一致的用户体验
- 在新的国家或地区更快、更轻松、更便宜地采用电子开票附加产品解决方案
- 通过 Regulatory Configuration Service (RCS) 和全球化功能设置来配置服务
- 使用 RCS 中定义的配置将业务数据转换为多种电子发票格式（XML、JavaScript 对象表示法\[JSON\]、TXT 和逗号分隔值\[CSV\]）：

    - 电子报告格式可用于无法配置电子发票转换的国家或地区

- 可配置向外部 Web 服务的电子发票提交，包括通过数字签名处理认证：

    - 内置、易于扩展且可配置的集成包含适用于多个国家/地区的其他内容

    > [!NOTE]
    > 当前仅支持有限数量的直接提交。 有关详细信息，请参阅本主题前面的[可用性](#availability)一节。 支持会在将来扩大。

- 处理 Web 服务的响应，包括可配置的异常消息处理
- 支持电子签名（例如，使用 XMLDSig 签名算法）
- 批量处理电子发票消息

## <a name="architecture-and-data-flow"></a>体系结构和数据流

从 LCS 安装电子开票附加产品，并且在所有必需的应用程序中完成必需的设置后，安全连接已建立。 此服务当前位于美国和欧洲的数据中心。 因此，服务位置可能与相关的 Finance 或 Supply Chain Management 实例的位置不同。 在完成电子开票附加产品的设置并打开集成后，每当发送电子发票时，与特定单据相关的主数据和交易数据就会发送到电子开票附加产品。

> [!NOTE]
> 如果您的电子发票或任何其他单据包含个人数据，请验证您对此功能的使用符合《一般数据保护条例》(GDPR) 以及与个人数据传输有关的其他法规的要求。

### <a name="high-level-description-of-the-data-flow"></a>数据流的高级描述

1. 客户端将规范的业务文档发送到服务。
2. 基于从客户端接收的上下文信息，服务选择适用的处理流。
3. 服务运行处理操作。 这些操作可能包括将商业文档转换为电子发票、应用电子签名以及将文档提交给外部 Web 服务。
4. 所有接收和处理的文档都存储在客户的 Azure Blob 存储中。
5. 用于处理的所有租户密码和证书都存储在客户的 Azure 密钥保管库中。
6. 服务向客户端提供有关已发送的业务文档的处理状态的按需信息。
7. 客户端接收有关完成的处理执行的信息，并使所有日志信息可用。 同时还使在流处理运行时创建或接收的文档可用。

下图显示了数据如何流入和流出电子开票附加产品。

![电子开票附加产品的数据流](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a>隐私声明
启用和使用电子开票可能需要发送有限的数据，其中包括组织税务登记 ID。 这将被传输到税务机构授权的第三方机构，以便以与这些政府的 Web 服务集成所需的预定义格式发送电子发票。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

## <a name="additional-resources"></a>其他资源

- [开始使用电子开票附加产品](e-invoicing-get-started.md)
- [开始使用适用于巴西的电子开票附加产品](e-invoicing-bra-get-started.md)
- [开始使用适用于墨西哥的电子开票附加产品](e-invoicing-mex-get-started.md)
- [开始使用适用于意大利的电子开票附加产品](e-invoicing-ita-get-started.md)
- [设置电子开票附加产品](e-invoicing-setup.md)
