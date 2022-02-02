---
title: 调用流程自动化流来创建质检订单
description: 本主题以质检订单为例，提供有关使用 Power Automate 自动化业务流程的资源。
author: johanhoffmann
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fa0c9ea5a2e92ae5af7d937b5f7f16df0ee3c9ef
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985179"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a>调用流程自动化流来创建质检订单

[!include [banner](../includes/banner.md)]

组织对自动化标准业务流程，为员工提供更便捷的交互以及利用各种数据信号和系统来自动驱动业务流程的需求日益增长。 借助机器人流程自动化 (RPA) 和 Microsoft Power Automate，企业可以使用无代码体验来自动化重复流程，从而提高效率和准确性。

Supply Chain Management 的可下载自动化解决方案模板以质量订单为例展示了如何使用 Power Automate 来自动化业务流程。

您可以在[此处](https://aka.ms/D365SCMQualityOrderRPASolution)下载自动化解决方案模板。

有关此功能及其功能的概述，请参见以下视频：[在 Dynamics 365 Supply Chain Management 中利用 RPA 创建质检订单](https://www.youtube.com/watch?v=LFbzJ6-H89w)

![RPA 的自动化选项。](media/rpa-automation-options.png "RPA 的自动化选项")

Power Automate 解决方案模板包括一个云自动化流和一个桌面自动化流，它们可以在 Supply Chain Management 中自动创建质检订单。

自动化可以为响应很多事件和信号启动，包括用户输入或机器信号（包括物联网 (IoT)）。 此解决方案模板中包含了 *Q-Order* Power 应用程序示例。 它允许用户扫描物料的 QR 码，输入数量并使用相机附加图片。

包含了解决方案参数来针对生产设施中的特定用例配置自动化。

![创建质检订单。](media/rpa-create-quality-roder.png "创建质检订单")

有关如何下载、安装和使用示例解决方案来自动创建质检订单的完整的分步指南，请参阅[使用 Power Automate Desktop 通过机器人流程自动化在 Dynamics 365 Supply Chain Management 上自动创建质检订单](/power-automate/desktop-flows/dynamics365-scm-rpa)。

