---
title: Project Service Automation
description: "此主题提供有关 Project Service Automation 到 Finance and Operations 集成解决方案的信息。 此集成解决方案使用数据集成功能，通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。"
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能，通过 Common Data Service 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。 可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance and Operations。

> [!NOTE]
> - 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。 如果必须重置会计分配，建议也安装 KB 4131710。
> - 如果在使用 Finance and Operations 7.3.0，则必须安装 KB 4074835。 然后就可以集成固定价格项目。
> - 如果在使用 Finance and Operations 7.3.0，并从 Project Service Automation 导入免费交易记录，则必须安装 KB 4345320，以便将这些费用添加到该项目发票中。
> - 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations 版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
> - 如果您正在使用 Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本，则可以同步实际值。

必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance and Operations 集成。 有关详细信息，请参阅 [Project Service Automation 集成参数](PSA-parameters.md)。

以下情况下，可通过集成解决方案直接同步：

- 在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Finance and Operations 中维护费用交易记录类别，并将其直接从 Finance and Operations 同步到 Project Service Automation。
- 在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中创建项目支出估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中创建项目时间、费用和费用实际值，并在 Project Service Automation 集成日记帐中创建项目交易记录，以便在 Finance and Operations 中过帐。

## <a name="data-synchronization"></a>数据同步

下图显示 Project Service Automation 与 Finance and Operations 之间的集成中如何同步数据。

> [!NOTE]
> 并非所有模板当前都可用。 模板将在准备好后发布。

[![Project Service Automation 与 Finance and Operations 集成](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求

若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装带平台更新 12 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation 的系统要求

若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装以下组件：

- Microsoft Dynamics 365 for Project Service Automation 版本 9.0.0.0 或更高版本
- Microsoft Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案。
- 适用于 Microsoft Dynamics 365 for Project Service Automation 的 Project Service Automation 到 Finance and Operations 解决方案版本 1.0.0.0 或更高版本

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>在 Project Service Automation 中安装 Project Service Automation 到 Finance and Operations 集成解决方案

从 [Microsoft 下载中心](https://www.microsoft.com/en-us/download/details.aspx?id=57016)下载 Project Service Automation 到 Finance and Operations 集成解决方案，然后按照该解决方案随附的说明操作。

