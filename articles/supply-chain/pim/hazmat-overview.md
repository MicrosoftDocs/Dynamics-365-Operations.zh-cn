---
title: 危险物料概述
description: 本主题概括介绍与在产品信息管理和仓库管理期间处理和记录危险物料有关的功能。
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 22e1b0838160378f3ff9484faaf87c9aec6e8964
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570673"
---
# <a name="hazardous-materials-overview"></a>危险物料概述

[!include [banner](../includes/banner.md)]

为了始终遵守装运和运输法规，装运被分类为危险货物的物料的组织必须在装运中提供其他文件。 危险物料功能使客户可以存储与已发布物料有关的信息。 然后，可以使用此信息来帮助准备装运文档。 装运危险货物的组织必须有自己的流程和程序来管理装运流程。 Microsoft Dynamics 365 Supply Chain Management 只是可以帮助生成所需文档的工具。

下图说明了设置和使用危险物料功能所需的步骤。

![设置和使用危险物料功能。](media/hazmat-overview.png "设置和使用危险物料功能")

危险物料功能在“产品信息管理”中设置，提供可通过“仓库管理”打印的文档。 因此，从广义上讲，以下区域是您将检查、设置和使用此功能的功能的两个主要区域：

- **产品信息管理** – 设置将应用于已发布产品的代码。
- **仓库管理** – 处理将要为装运打印的其他装运文档。

> [!IMPORTANT]
> Supply Chain Management 中的危险物料功能提供了一组有用的产品信息字段和相关功能，可以帮助您记录和引用与危险物料有关的信息。 这些功能还可以帮助您设计和打印包含有关您所装运的任何危险物料的某些信息的装运文档。 但是，系统不会自动使您遵守您所在国家或地区的所有适用法规。 虽然这些工具的目的是帮助您遵守常见法规，但它们本身并不足够，也不能保证一定合规。 您的组织有责任了解所有适用法规，并采取所有必要的步骤来遵守这些法规。

## <a name="product-information-management"></a>产品信息管理

“产品信息管理”提供一系列设置表，您可以在其中为各个陆运、空运和海运危险货物清单输入参考信息。

开发此功能时，参考了以下常见法规：

- **ADR** – 与国际陆运危险货物有关的法规
- **CFR 49** – 美国危险货物运输法规
- **IMDG** – 国际海运危险货物 (IMDG) 法规
- **IATA** – 国际航空运输协会 (IATA) 危险货物法规

每组法规均提供危险货物和参考代码的标准化列表。 因此，Supply Chain Management 为这些列表中的通用代码提供了参考表。 每个列表还包含一些可以定义的唯一代码。

有关如何为危险物料设置法规和值以及如何将值分配给相关产品的详细信息，请参阅以下主题：

- [设置危险物料](hazmat-setup.md)
- [产品、订单、装运和负荷中的危险物料](hazmat-items.md)

## <a name="warehouse-management"></a>仓库管理

在“仓库管理”中准备装运时，您能够打印使用您在“产品信息管理”中设置的信息的多个新报表。 有关可用报表以及如何使用它们的详细信息，请参阅[危险物料查询和报表](hazmat-reports.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]