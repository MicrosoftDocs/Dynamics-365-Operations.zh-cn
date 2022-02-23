---
title: 子分类帐转移到总帐
description: 本主题描述 Microsoft Dynamics 365 Finance 中与总帐内的子分类帐转移过程有关的功能。
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 7addb1f26a33db84d947e6fede876be648d2c654
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645162"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>子分类帐转移到总帐

[!include [banner](../includes/banner.md)]

本主题描述 Microsoft Dynamics 365 Finance 中与用于转移子分类日记帐分录批次的规则有关的功能。

在版本 8.1 中，进行了更改以允许使用已弃用 **同步** 选项的转移规则。 有关详细信息，请参阅[已删除或弃用 Finance and Operations 的功能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20)。

以下选项可用于传输子分类帐批次。 

 - 异步 – 此选项将立即安排将子分类帐会计条目转移到总分类帐。 只要有资源可自由地在服务器上处理此请求，就会记录总帐凭证。 

- 计划批处理 – 此选项将添加要转移到总帐中的处理队列的子分类帐会计分录，在该队列中将按接收顺序处理分录。 如果有资源可自由地在服务器上处理此批处理作业，就会在计划的时间记录总帐凭证。 
 
在 10.0.8 版本中，进行了改进以增强“异步”选项的性能。 在功能名称 **子分类帐转移到总帐性能优化** 下启用了此功能。 
 
此功能改善了从子分类帐到总分类帐的数据转移。 它使流程更加高效，并将更小的交易集组合在一起进行转移。 这样可以更有效地使用批处理服务器。 此功能要求批处理服务器已设置、联机并正常运行，以使“异步转移”选项起作用。 
