---
title: 管理配方及其成分的更改
description: 本主题介绍如何执行配方管理以及如何管理对处理制造主数据的更改。
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 825cc5b9355695a648c857e5197b5b93a21fdb43
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115167"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>管理配方及其成分的更改

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

如果您使用的是 Microsoft Dynamics 365 Supply Chain Management 的处理制造功能，您还可以使用相关的配方管理功能来管理以下更改：

- **配方和计划物料：** 管理配方中的成分及其联产品和副产品的更改。
- **联产品和副产品：** 编辑配方中联产品和副产品的数量和其他信息。
- **实际称重物料：** 管理对实际称重物料的更改。

## <a name="turn-on-this-feature-in-your-system"></a>在系统中开启此功能

要使用此功能，必须完成以下任务：

1. 启用 *工程更改管理* 功能及其配置密钥，如[工程更改管理概述](product-engineering-overview.md)中所述。 如该主题中提到的，请确保您还启用了 **处理制造的更改管理** 许可证密钥，它嵌套在主 **工程更改管理** 许可证密钥下。
1. 在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开 *管理配方及其成分的更改* 功能。

## <a name="feature-naming-conventions"></a>功能命名约定

在 Supply Chain Management 用户界面 (UI) 和文档中，更改管理功能通常称为 *工程更改管理*，可管理的产品通常称为 *工程产品*。 虽然此术语通常与处理制造的配方的管理无关，但您应将工程更改管理视为简单的更改管理，将工程产品视为版本化产品。

## <a name="work-with-formula-change-management-features"></a>使用配方更改管理功能

以下列表总结了工程更改管理功能如何应用于配方管理。 另外还提供了指向更多信息的链接。 由于配方更改管理利用工程更改管理功能，因此您应该了解工程更改管理的总体工作原理，以便可以使用它来管理您的配方及其成分。

- **集中式产品数据管理** – 通过托管发布流程设置一个组织，该组织确保整个企业的用户都可以使用准确且相关的产品数据。 有关详细信息，请参阅[工程公司和数据所有权规则](engineering-org-data-ownership-rules.md)。
- **产品版本控制** – 通过产品版本跟踪对产品的更改，在供应链的所有阶段控制产品。 这样，您可以跟踪配方的更改。 有关详细信息，请参阅[工程版本和工程产品类别](engineering-versions-product-category.md)。
- **产品生命周期管理** – 管理整个组织的产品数据的可见性，控制供应链各阶段产品版本的可用性。 您可以详细控制某个产品版本何时可以在特定业务流程中使用，并可以创建自己的生命周期状态来满足您的业务需求。 有关详细信息，请参阅[产品生命周期状态和交易](product-lifecycle-state-transactions.md)。
- **配方更改管理** – 整个组织的用户都可以请求更改配方。 使用更改订单评估和记录建议更改的影响。 添加工作流来管理产品及其配方的更改流程以及新版本的发布。 有关详细信息，请参阅[管理工程产品的更改](engineering-change-management.md)。
- **准备控制** – 使用系统检查和用户指南（调查表和清单）确保在发布产品之前已完全输入所有必需的产品数据。 有关详细信息，请参阅[产品准备](product-readiness.md)。
- **增强的产品发布功能** – 将组织（法人）中的产品及其配方的完整定义版本发布到其他法人。 您甚至可以决定在发布之前是否必须查看或编辑产品信息。 有关详细信息，请参阅[发布产品结构](release-product-structure.md)。

请注意，上一个列表中链接的大多数主题提供的是基于物料清单 (BOM) 的示例。 不过，配方的工作方式相似。 以下是另外一些可以帮助了解您何时使用更改管理（或仅使用配方更改管理）来管理配方和物料清单的概念：

- 对于每个[产品工程类别](engineering-versions-product-category.md)，您可以指定生产类型（物料清单、配方或计划物料）。 您还可以指定使用该类别的产品是否需要实际称重支持。
- 联产品和副产品不是工程产品。 因此，它们未版本化。 如果必须更改它们，只需创建一个新产品。 这种方法让维护更加容易。
- 您可以管理作为物料清单且具有子配方物料的最终物料。 此功能适用于包含配方的物料清单和/或包含物料清单的配方的任何组合。
