---
title: 电子开票概览
description: 本文概括介绍 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中的电子开票。
author: gionoder
ms.date: 01/21/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: d219863d793c837e2346d66d6b95d38191933bcc
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709173"
---
# <a name="electronic-invoicing-overview"></a>电子开票概览

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 的电子开票是一种超级可扩展的多租户服务，可对电子发票进行可配置的处理并进行可配置的电子单据交换。 处理和集成规则完全可配置，逻辑在 Finance 和 Supply Chain Management 外部运行。 此服务主要针对企业对政府场景下的电子发票单据处理。 但可以针对其他目的进行自定义配置，如在企业到企业场景中使用不同类型的文档。

电子开票可以帮助您实现以下目标：

- 快速轻松地采用国家/地区特定要求
- 标准化实施电子开解决方案
- 增强了文档历史记录的可追溯性
- 实施周期更短
- 降低总拥有成本 (TCO)
- 可轻松调整配置，无需更改代码
- 简化配置包装
- 内置的导出、导入和集成，并可在电子发票单据处理中轻松扩展
- 在公司之间轻松重复使用相同的导出、导入和集成配置

## <a name="service-availability"></a>服务可用性

目前，Finance 和 Supply Chain Management 客户可以使用电子开票功能。 有关详细信息，请查看您的应用程序的许可条款和条件。

由于满足国家/地区特定要求的功能可能会在发行的不同阶段受到限制，因此您应该始终查看最新文档，这些文档重点介绍了受支持的国家/地区特定解决方案的覆盖范围。

电子开票在以下 Azure 地理区域部署：

- 美国
- 欧洲
- 英国
- 亚洲
- 日本
- 瑞士
- 巴西
- 阿拉伯联合酋长国
- 澳大利亚
- 加拿大
- 法国
- 印度
- 挪威
- 南非

> [!NOTE]
> 电子开票不支持本地部署。

## <a name="feature-highlights"></a>功能亮点

- 与 Finance 和 Supply Chain Management 的现成集成
- 所有国家和地区的电子发票流程的配置和监视具有一致的用户体验
- 在新的国家或地区更快、更轻松、更便宜地采用电子开票解决方案
- 通过 Regulatory Configuration Service (RCS) 和全球化功能设置来配置服务
- 使用 RCS 中定义的配置将业务数据转换为多种电子发票格式（XML、JavaScript 对象表示法 \[JSON\]、TXT 和逗号分隔值 \[CSV\]）：

    - 电子报告 (ER) 格式可用于无法配置电子发票转换的国家和地区

- 可配置向外部 Web 服务的电子发票提交，包括通过数字签名处理认证：

    - 内置、易于扩展且可配置的集成包含适用于多个国家和地区的其他内容

- 处理 Web 服务的响应，包括可配置的异常消息的处理
- 支持电子签名（例如，使用 XMLDSig 签名算法的电子签名）
- 能够将文档发送到电子邮件并将其存储在 SharePoint 中
- 批量处理电子发票消息
- 对传入文档进行可配置的转换，以及在 Finance 和 Supply Chain Management 中处理这些文档
- 能够从电子邮件和 SharePoint 等渠道接收传入文档

## <a name="privacy-notice"></a>隐私声明

启用和使用电子开票可能需要仅发送有限的数据。 此数据包括组织的税务登记 ID。 此数据将被传输到税务机构授权的第三方机构，以便使用与政府的 Web 服务集成所需的预定义格式发送电子发票。 从这些外部系统导入到此 Dynamics 365 在线服务的数据受我们的[隐私声明](https://go.microsoft.com/fwlink/?LinkId=512132)的约束。 有关详细信息，请查阅国家/地区特定功能文档中的“隐私声明”部分。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
