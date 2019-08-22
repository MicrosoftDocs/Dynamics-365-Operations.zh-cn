---
title: Project Service Automation 集成参数
description: 本主题介绍在将 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 集成时，如何配置默认数据的输入方式。
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
ms.openlocfilehash: b58d2de323395db97d1f8ea146da55bba4e0f9c6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838970"
---
# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 集成参数

[!include[banner](../includes/banner.md)]

在将 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 集成时，可在 **Project Service Automation 集成参数**页面配置默认数据的输入方式。 必须设置以下字段，才能将项目从 Project Service Automation 成功同步到 Finance and Operations 中。

> [!NOTE]
> - Microsoft Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
> - Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本中支持实际值集成。
> - 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。 如果必须重置会计分配，建议也安装 KB 4131710。

| 选项卡                    | 字段                | 说明 |
|------------------------|----------------------|-------------|
| 常规                | 默认项目类型 | 选择默认项目类型。 从 Project Service Automation 同步项目时，如果在集成模板中不提供默认值，将使用该值。 同步期间，将把新项目的**项目类型**字段设置为该值。 但是，从 Project Service Automation 同步项目联系人行时，可能更新该值。 |
|                        | 时间类别        | 选择默认时间类别。 从 Project Service Automation 同步工时估计值时使用该值。 从 Project Service Automation 同步工时估计值和工时实际值时，Finance and Operations 中的新项目工时预测的**类别**字段将设置为该值。 |
|                        | 费用类别         | 选择默认费用类别。 从 Project Service Automation 同步费用实际值时使用该值。 从 Project Service Automation 同步费用实际值时，Finance and Operations 中的新费用交易记录的**类别**字段将设置为该值。 |
| 项目组的默认值 | 项目类型         | 单击**新建**添加一行，可在该行中选择要为默认项目组设置的项目类型。 在配置中，特定项目类型只能选择一次。 |
|                        | 项目组        | 为所选项目类型选择默认项目组。 从 Project Service Automation 同步新项目时，如果尚未在集成模板中提供默认值，**项目组**字段将设置为项目类型的默认值。 |
| 计费类型默认值  | 计费类型         | 单击**新建**添加一行，可在该行中选择要为默认行属性设置的计费类型。 在配置中，特定计费类型只能选择一次。 |
|                        | 行属性        | 为所选计费类型选择默认行属性。 从 Project Service Automation 同步新工时估计值、新费用估计值或新实际值时，**行属性**字段将设置为计费类型的默认值。 |
| 功能锁定  | 不适用       | 为源自 Project Service Automation 的项目和合同选择要在 Finance and Operations 中禁用的功能。 例如，可关闭 Finance and Operations 中的编辑合同和项目，创建工作分解结构以及输入工时单功能。 将继续启用与核算有关的字段，即使根据参数设置这些字段不可用也不例外。 默认情况下，将启用所有功能。 |
