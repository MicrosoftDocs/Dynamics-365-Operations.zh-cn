---
title: Project Service Automation 集成参数
description: 本主题介绍在将 Microsoft Dynamics 365 for Project Service Automation 与 Dynamics 365 Finance 集成时，如何配置默认数据的输入方式。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: f7cef5384812e0dcb7d5e084ddd7668a7687a259
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174768"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 集成参数

[!include[banner](../includes/banner.md)]

在将 Dynamics 365 Project Service Automation 与 Dynamics 365 Finance 集成时，可在 **Project Service Automation 集成参数**页面配置默认数据的输入方式。 必须设置以下字段，才能将项目从 Project Service Automation 成功同步到 Finance 中。

> [!NOTE]
> - 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
> - 版本 8.0.1 或更高版本中支持实际值集成。


| Tab                    | 字段                | 说明 |
|------------------------|----------------------|-------------|
| 常规                | 默认项目类型 | 选择默认项目类型。 从 Project Service Automation 同步项目时，如果在集成模板中不提供默认值，将使用该值。 同步期间，将把新项目的**项目类型**字段设置为该值。 但是，从 Project Service Automation 同步项目联系人行时，可能更新该值。 |
|                        | 时间类别        | 选择默认时间类别。 从 Project Service Automation 同步工时估计值时使用该值。 从 Project Service Automation 同步工时估计值和工时实际值时，Finance 中的新项目工时预测的**类别**字段将设置为该值。 |
|                        | 费用类别         | 选择默认费用类别。 从 Project Service Automation 同步费用实际值时使用该值。 从 Project Service Automation 同步费用实际值时，Finance 中的新费用交易记录的**类别**字段将设置为该值。 |
| 项目组的默认值 | 项目类型         | 单击**新建**添加一行，可在该行中选择要为默认项目组设置的项目类型。 在配置中，特定项目类型只能选择一次。 |
|                        | 项目组        | 为所选项目类型选择默认项目组。 从 Project Service Automation 同步新项目时，如果尚未在集成模板中提供默认值，**项目组**字段将设置为项目类型的默认值。 |
| 计费类型默认值  | 计费类型         | 单击**新建**添加一行，可在该行中选择要为默认行属性设置的计费类型。 在配置中，特定计费类型只能选择一次。 |
|                        | 行属性        | 为所选计费类型选择默认行属性。 从 Project Service Automation 同步新工时估计值、新费用估计值或新实际值时，**行属性**字段将设置为计费类型的默认值。 |
| 功能锁定  | 不适用       | 为源自 Project Service Automation 的项目和合同选择要在 Finance 中禁用的功能。 例如，可关闭 Finance 中的编辑合同和项目，创建工作分解结构以及输入工时单功能。 将继续启用与核算有关的字段，即使根据参数设置这些字段不可用也不例外。 默认情况下，将启用所有功能。 |
