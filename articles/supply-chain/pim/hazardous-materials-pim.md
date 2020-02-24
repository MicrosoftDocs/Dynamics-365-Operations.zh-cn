---
title: 危险物料
description: 本主题提供有关危险物料文档的信息以及您环境中存储的信息。
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982300"
---
# <a name="hazardous-materials"></a>危险物料

[!include [banner](../includes/banner.md)]

有关危险物料的信息在产品信息管理中设置。 此模块还提供可以通过仓库管理打印的文档。

当您运输分类为危险货物的物料时，必须在装运中提供附加文件。 危险物料功能使客户可以存储分类信息，并将其关联以发放物料。 然后，可以使用此信息来帮助准备装运文档。

> [!IMPORTANT]
> 为了帮助管理危险货物的装运，Microsoft Dynamics 365 Supply Chain Management 使您可以设置与产品相关的附加参考信息。 您还可以设置附加装运文档。 但是，系统不会自动遵守您所在国家或地区的法规。 而是充当可以帮助您实施总体计划的工具。

在使用此功能之前，需要进行以下设置：

- **产品信息管理：** 设置可应用于已发布产品的代码。
- **仓库管理：** 使用附加装运文档打印装运信息。

## <a name="product-information-management"></a>产品信息管理

在“产品信息管理”中，有一系列设置表，您可以在其中添加陆运、空运和海运危险货物清单中提供的参考信息。

以下是一些经常引用的法规：

- **ADR** – 与国际陆运危险货物有关的法规
- **CFR 49** – 美国危险货物运输法规
- **IMDG** – 国际海运危险货物 (IMDG) 法规
- **IATA** – 国际航空运输协会 (IATA) 危险货物法规

这些法规中的每一个都有包含参考代码的危险货物清单。 每种运输类型的清单在共享国际分类中合并在一起。 Supply Chain Management 为这些清单中的共享代码提供了参考表。 每个列表还包含一些可以定义的唯一代码。

要开始配置此信息，请创建可用于配置初始参数的规则。

## <a name="warehouse-management"></a>仓库管理

准备好装运后，可以打印几个新报告。 这些报告使用您在“产品信息管理”中设置的信息。
