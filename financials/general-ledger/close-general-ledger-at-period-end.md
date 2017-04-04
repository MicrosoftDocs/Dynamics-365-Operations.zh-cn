---
title: "在期间结束时关闭总帐"
description: "此主题描述完成通常，当执行总帐时的期间结转的任务。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: a7b72dfa98758b14d303d09890bd46729b1cdbe9
ms.lasthandoff: 03/31/2017


---

# <a name="close-the-general-ledger-at-period-end"></a>在期间结束时关闭总帐

此主题描述完成通常，当执行总帐时的期间结转的任务。 

在“总帐”中，您可以为期间或年度完成结转过程。 结转流程为新期间准备系统。 系统要为新年准备，您必须运行年度结转过程。 每个组织具有为期间的结束日期不同的过程和执行的步骤。 这是期间结束的某些选项步骤：

-   完成所有其他模块的所有任务，例如应收帐款、应付帐款和库存。
-   验证所有日记帐均已过帐。
-   运行外币重估来生成所有或有损益金额。
-   结算每个会计科目的交易记录。
-   处理任何所需分配。
-   手动过帐期间结束调整。
-   将交易记录记入日记帐，并审查**分类帐日记帐**报表。
-   通过使用合并公司或财务报告执行合并。
-   通过使用财务报告生成期间结束财务报表。
-   设置分类帐期间为**暂停**，以便没有进一步过帐发生。 您还可以在发生期间结束活动时限制期间到特定的用户组，以便更好地控制。 它并非完全好设置期间**永久已关闭**，因为不能重新打开已关闭的期间。

财务期间结帐工作区可用于组织。各种期间结束跟踪和处理所需的任务。 参考 [财务期间结帐工作区] (财务期间结帐 workspace.md) 和年末结转的 [] (年度结束 close.md) 主题详细信息。 




