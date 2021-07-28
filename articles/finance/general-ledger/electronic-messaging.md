---
title: 电子消息
description: 此主题提供 Microsoft Dynamics 365 Finance 中电子消息的概述和设置信息。
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433711"
---
# <a name="electronic-messaging"></a>电子消息

[!include [banner](../includes/banner.md)]

本主题提供 **电子消息** (EM) 功能的概述和设置信息。

最近，全世界各个国家和地区的政府与立法机构对在这些国家或地区注册的公司实施了报告要求。 要求的目的是支持数据以电子格式从这些公司、直接从具有、存储和处理数据的系统获取。

Microsoft Dynamics 365 Finance 中的 EM 功能支持在 Finance 与政府和立法机构为报告、提交和接收官方信息提供的系统之间进行各种电子互操作流程。

EM 功能与 **电子申报** (ER) 模块集成。 您可以为电子消息设置 ER 格式。 有关详细信息，请参阅[电子报告 (ER)](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting)。

## <a name="basic-concepts-for-em-functionality"></a>EM 功能的基本概念

EM 功能基于以下实体：

- **电子消息** – 应在内部报告或传输的报表或声明，例如发送给税务局的报表。
- **电子消息项** – 应包括在报告的消息中的记录。
- **电子消息处理** – 应运行以收集所需的数据、生成报表、在 Azure Blob 存储中存储数据、在系统之外传输报表、接收系统外部的响应以及基于收到的信息更新数据库的操作链。 链中的操作可以已链接，也可以取消链接。

下图显示 EM 的数据流。

![电子消息数据流。](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>EM 功能支持的场景

EM 功能支持以下场景：

- 手动创建消息和生成基于各种类型的关联导出 ER 格式的报表。 这些类型包括 Microsoft Excel、XML、JavaScript 对象表示法 (JSON)、PDF、文本和 Microsoft Word。
- 自动创建和处理基于通过使用关联导入 ER 格式从当局请求和接收的信息的消息。
- 作为消息项收集和处理来自数据源的信息。 数据源是一个 Finance 表。
- 存储附加信息，并通过调用有关消息或消息项的专门定义的可执行类评估不同值。
- 聚合在消息项中收集的信息，按消息拆分该信息，然后生成关联导出 ER 格式的报表。
- 传输使用存储在 Azure Key Vault 中的安全信息生成到 Web 服务的报表。
- 接收 Web 服务的响应、解释响应、根据需要更新 Finance 中的数据。
- 存储和查看生成的所有报表。
- 存储和查看与为消息或消息项运行的行动有关的所有日志信息。
- 通过各个消息状态和消息项状态控制处理。

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>EM 功能支持的特定于国家/地区的监管功能

下表提供了有关 EM 功能支持的特定于某些国家/地区的监管功能的信息。

| 国家/地区     | 功能名称 | 功能演示记录 |
|-------------|--------------|------------------------|
| 西班牙       | [立即提供增值税信息 (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| 匈牙利     | [在线开票系统](../localizations/emea-hun-online-invoicing.md) | |
| 英国 | [税数字化 (MTD) – 增值税对帐单提交](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations：英国数字税 - Dynamics 365 中的增值税申报](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| 立陶宛   | [i.SAF 报告](../localizations/emea-ltu-isaf.md) | |
| 波兰      | [增值税申报与登记（JPK_V7M、VDEK）](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance：SAF/JPK 增值税审计登记](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| 荷兰 | [荷兰增值税申报](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| 捷克共和国 | [增值税申报](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| 巴西      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| 俄罗斯      | [增值税申报](../localizations/rus-vat-declaration.md) | |
| 俄罗斯      | [电子格式的会计报表](../localizations/rus-accounting-reporting.md) | |
| 俄罗斯      | [利润税申报](../localizations/rus-profit-tax-declaration.md) | |
| 俄罗斯      | [估定税申报](../localizations/rus-assessed-tax-declaration.md) | |
| 俄罗斯      | [运输税申报](../localizations/rus-transport-tax-declaration.md) | |
| 俄罗斯      | [土地税申报](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

