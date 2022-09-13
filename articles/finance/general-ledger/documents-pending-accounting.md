---
title: 单据的待定会计
description: 本文将介绍如何使用“单据的待定会计”页面上的功能。
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: e915c248abd1c842f8f01490a49db9b824644a29
ms.sourcegitcommit: 07ed6f04dcf92a2154777333651fefe3206a817a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2022
ms.locfileid: "9424357"
---
# <a name="documents-pending-accounting"></a>单据的待定会计

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

本文将介绍如何使用 **单据的待定会计** 页面上的功能。

Microsoft Dynamics 365 Finance 10.0.30 推出了 **增强的原始单据会计框架性能** 功能。 此功能改进了原始单据（已启用单据过帐）的过帐流程，从普通发票的过帐流程开始。

启用此功能后，子分类帐单据的过帐会与创建传输到总帐的完整会计明细的会计生成或 *分录* 流程分开进行。 例如，在普通发票过帐流程中，首先记录 **应收帐款** 模块中的客户发票后，然后生成完整会计。 而使用此增强的性能功能，即使会计生成延迟，也能更快地记录客户发票。

**单据的待定会计** 页面提供以下按钮。

- **生成会计** - 提交当前正在等待生成会计以进行分录的单据。
- **查看分配** - 查看列表中选定单据的会计分配。
- **查看错误日志** - 查看会计状态显示错误的单据的错误消息详情。 您也可以通过选择单据行上的 **错误日志** 链接查看错误消息详情。

会计生成由名为 **会计框架处理器** 的流程自动化后台流程实现。 有关所有流程自动化设置和配置的更多信息，请参阅[流程自动化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
