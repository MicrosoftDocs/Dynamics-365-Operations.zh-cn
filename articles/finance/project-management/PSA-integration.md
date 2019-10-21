---
title: Project Service Automation 概览
description: 本主题提供有关 Dynamics 365 Project Service Automation 到 Dynamics 365 Finance 集成解决方案的信息。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250545"
---
# <a name="project-service-automation-overview"></a>Project Service Automation 概览

[!include[banner](../includes/banner.md)]

Project Service Automation 到 Finance 集成解决方案使用数据集成功能，通过 Common Data Service 跨 Dynamics 365 Finance 和 Dynamics 365 Project Service Automation 的实例同步数据。 可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance。

> [!NOTE]
> - 如果在使用版本 7.3.0，则必须安装 KB 4074835。 然后就可以集成固定价格项目。
> - 如果在使用版本 7.3.0，并从 Project Service Automation 导入免费交易记录，则必须安装 KB 4345320，以便将这些费用添加到该项目发票中。
> - 如果您正在使用版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
> - 如果您正在使用版本 8.0.1 或更高版本，则可以同步实际值。

必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance 集成。 有关详细信息，请参阅 [Project Service Automation 集成参数](PSA-parameters.md)。

以下情况下，可通过集成解决方案直接同步：

- 在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Finance 中维护费用交易记录类别，并将其直接从 Finance 同步到 Project Service Automation。
- 在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中创建项目费用估计值，并将其直接从 Project Service Automation 同步到 Finance。
- 在 Project Service Automation 中创建项目时间、费用和费用实际值，并在 Project Service Automation 集成日记帐中创建项目交易记录，以便在 Finance 中过帐。

## <a name="data-synchronization"></a>数据同步

下图显示 Project Service Automation 与 Finance 之间的集成中如何同步数据。

> [!NOTE]
> 并非所有模板当前都可用。 模板将在准备好后发布。

[![Project Service Automation 与 Finance 集成](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Finance 的系统要求

若要使用 Project Service Automation 到 Finance 集成解决方案，必须安装带平台更新 12 或更高版本的 Enterprise Edition 7.3。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation 的系统要求

若要使用 Project Service Automation 到 Finance 集成解决方案，必须安装以下组件：

- Dynamics 365 Project Service Automation 版本 9.0.0.0 或更高版本
- Dynamics 365 Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案
- 适用于 Dynamics 365 Project Service Automation 版本 1.0.0.0 或更高版本的 Project Service Automation 到 Finance 解决方案

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>在 Project Service Automation 中安装 Project Service Automation 到 Finance 集成解决方案

从 [Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=57016)下载 Project Service Automation 到 Finance 集成解决方案，然后按照该解决方案随附的说明操作。
