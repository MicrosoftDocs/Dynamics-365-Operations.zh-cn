---
title: Project Service Automation
description: "此解决方案使用数据集成功能，通过 Common Data Service (CDS) 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Project Service Automation 到 Finance and Operations 集成解决方案使用数据集成功能，通过 Common Data Service (CDS) 跨 Microsoft Dynamics 365 for Finance and Operations 和 Microsoft Dynamics 365 for Project Service Automation 的实例同步数据。 可通过数据集成功能提供的集成模板将项目、项目合同、项目合同行、项目合同行里程碑、项目任务、费用交易记录类别、工时估计值和费用估计值从 Project Service Automation 传输到 Finance and Operations。

> [!NOTE] 
> 如果您正在使用 Dynamics 365 for Finance and Operations Enterprise Edition 7.300，您必须安装 KB 4074835。 这样就可以集成固定价格项目。
>
> 如果您正在使用 Dynamics 365 for Finance and Operations 版本 8.0，则可以使用项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。
>
> 如果您正在使用 Dynamics 365 for Finance and Operations 版本 8.0.1，则可以同步实际值。
>
> 如果您正在使用 Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。 如果必须重置会计分配，建议也安装 KB 4131710。

必须先配置 Project Service Automation 集成参数，才能将 Project Service Automation 与 Finance and Operations 集成。 有关详细信息，请参阅“Project Service Automation 集成参数”。

以下情况下，可通过集成解决方案直接同步：

- 在 Project Service Automation 中维护项目合同，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中创建项目，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目合同行，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目合同行里程碑，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中维护项目任务，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Finance and Operations 中维护费用交易记录类别，并将其直接从 Finance and Operations 同步到 Project Service Automation。
- 在 Project Service Automation 中创建项目工时估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。
- 在 Project Service Automation 中创建项目支出估计值，并将其直接从 Project Service Automation 同步到 Finance and Operations。

## <a name="data-synchronization"></a>数据同步
下图显示 Project Service Automation 与 Finance and Operations 之间的集成中如何同步数据。

> [!NOTE]
> 并非所有模板当前都可用。 模板将在准备好后发布。

[![Project Service Automation 与 Finance and Operations 集成](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Finance and Operations 的系统要求

若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装带平台更新 12 或更高版本的 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3。

## <a name="system-requirements-for-project-service-automation"></a>Project Service Automation 的系统要求

若要使用 Project Service Automation 到 Finance and Operations 集成解决方案，必须安装以下组件：

- Microsoft Dynamics 365 for Project Service Automation 版本 9.0.0.0 或更高版本。
- Dynamics 365 for Sales 版本 1.14.0.0 (v14) 或更高版本的从目标客户到现金解决方案。
- 适用于 Dynamics 365 for Project Service Automation 的 Project Service Automation 到 Operations 解决方案版本 1.0.0.0 或更高版本。

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>在 Project Service Automation 中安装 Project Service Automation 到 Finance and Operations 集成解决方案



