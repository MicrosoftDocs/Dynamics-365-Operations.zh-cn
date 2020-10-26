---
title: 查看试验的状态
description: 本主题说明了试验在 Dynamics 365 Commerce 的试验生命周期中有哪些状态。
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 097206c0aa487e14499bdf3907465e17b7d337e2
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930145"
---
# <a name="review-the-status-of-an-experiment"></a>查看试验的状态
在 Dynamics 365 Commerce 中设置和运行试验涉及许多步骤。 有关试验生命周期的信息，请参阅 [Dynamics 365 Commerce 中的试验](experimentation-overview.md)。

若要了解试验在生命周期中的位置，请转到站点构建器中的**试验**选项卡。 将显示试验列表，其中包含 Commerce 和用于创建试验、分配变体和分析数据的第三方服务中每个试验的状态。

在 **Commerce 状态**列中，可能会显示以下值。 
- **草稿** - 试验已连接到 Commerce 中的一个页面或片段，将进行编辑。
- **已发布** - 试验变体已准备好在您的网站上显示。 如果试验在第三方服务中运行，则网站用户将看到由第三方服务选择的页面或片段变体。
- **取消发布** - 试验在您的网站上不再可用。 即使试验在第三方服务中运行，网站用户也只能看到默认版本的页面或片段。
- **已完成** - 试验已经完成，并推广了变体以供所有网站用户使用。

同样，在**第三方状态**列中，可能会显示以下值，以指示试验在第三方服务中有哪些状态。
- **草稿** - 试验在第三方服务中设置，但尚未启动。
- **运行** - 试验已在第三方服务中启动，正在收集数据。
- **已暂停** - 试验已暂停且未在收集数据。 您必须恢复试验才能再次收集数据。
- **已存档** - 试验已经完成，并已归类在第三方服务中以供将来引用。

下图显示了两种状态以及它们之间的关系。

[![试验状态](./media/experimentation_statuses.svg)](./media/experimentation_statuses.svg#lightbox)
