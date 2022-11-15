---
title: 取消计划作业
description: 本文说明如何取消使用“计划优化”功能的活动计划作业。
author: t-benebo
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741168"
---
# <a name="cancel-a-planning-job"></a>取消计划作业

[!include [banner](../../includes/banner.md)]

在 Microsoft Dynamics 365 Supply Chain Management 中，您可以取消使用“计划优化”功能的活动计划作业。 如果在直接从用户界面（而不是后台）触发了计划优化作业后在对话框中选择 **取消**，不会取消该计划优化作业。 即使收到“已取消操作”之类警告，您仍然需要通过以下步骤通过计划优化取消计划作业。

要取消活动的计划作业，请按照下列步骤操作。

> [!NOTE]
> 仅活动作业可以取消。

1. 转到 **主计划 \> 设置 \> 计划**。
2. 为计划运行选择适当的计划。
3. 选择 **历史记录**。
4. 选择要取消的计划作业。
5. 选择 **取消**。

作业状态将为 **正在取消**，直到计划优化服务确认该作业已被取消。 然后，状态将更改为 **已取消**。

> [!NOTE]
> 要查看状态更改，您必须通过选择 **刷新** 按钮刷新页面。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]