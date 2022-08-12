---
title: 子分类帐转移到总帐
description: 本文介绍与总帐内的子分类帐转移过程有关的功能。
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: a53b7834271355aaf11c13c3f1886257a97b1da8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068981"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>子分类帐转移到总帐

[!include [banner](../includes/banner.md)]

本文介绍与用于转移子分类日记帐分录批次的规则有关的功能。

在版本 8.1 中，进行了更改以允许使用已弃用 **同步** 选项的转移规则。 有关详细信息，请参阅[财务和运营的移除或弃用功能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20)。

以下选项可用于传输子分类帐批次：

- **异步** – 立即安排将子分类帐会计条目转移到总分类帐。 只要有资源可在服务器上处理此请求，就会记录总帐凭证。
- **计划批处理** – 必须转移的子分类帐会计条目被添加到总帐的处理队列中。 队列中的条目将按条目的接收顺序进行处理。 如果有资源可在服务器上处理此批处理作业，每个总帐凭证将在计划的时间更新科目。

在 10.0.8 版本中，进行了改进以增强 **异步** 选项的性能。 在功能名称 **子分类帐转移到总帐性能优化** 下启用了此功能。

异步转移子分类帐批次的功能可以帮助改进数据从子分类帐到总帐的转移。 通过对更小的一组交易进行分组，然后按组转移交易，此功能可以更高效地处理交易。 分组交易后，批处理服务器的资源将被更高效地利用。

子分类帐批次的异步转移需要批处理服务器完成设置、在线并且在工作，因为创建批处理任务是为了在批处理服务器上立即执行。 当 **子分类帐转移到总帐性能优化** 功能启用时，名为 **流程自动化轮询系统作业** 的 **流程自动化** 系统批处理作业也必须启用。 有关详细信息，请参阅[流程自动化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)。

批处理级别的效率更改对系统中的所有法人使用单个定期批处理作业。 在运行时，将创建新的批处理作业来处理尚未转移的必需记录。 更多设置可以从系统管理中的 **流程自动化** 页面进行控制。 在该页面上，您可以修改后台流程，更改频率并定义睡眠期间。

有关流程自动化设置的详细信息，请参阅[流程自动化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

