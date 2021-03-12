---
title: 在期间结束时关闭总帐
description: 本主题介绍为总帐执行定期结算时通常完成的任务。
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 944f88e65c5dbbd2acf21ebfd96c28ce477798ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975983"
---
# <a name="close-the-general-ledger-at-period-end"></a>在期间结束时关闭总帐

[!include [banner](../includes/banner.md)]

本主题介绍为总帐执行定期结算时通常完成的任务。 

在“总帐”中，您可以为期间或年度完成结转过程。 结转流程为新期间准备系统。 若要为新的一年准备系统，您必须运行年终结算流程。 每个组织有为期间结束时执行的不同的流程和步骤。 以下是期间结束的某些可选步骤：

-   完成所有其他模块的所有任务，例如应收帐款、应付帐款和库存。
-   验证所有日记帐均已过帐。
-   运行外币重估来生成所有或有损益金额。
-   结算每个会计科目的交易记录。
-   处理任何所需分配。
-   手动过帐期间结束调整。
-   将交易记录记入日记帐，并审查 **分类帐日记帐** 报表。
-   通过使用合并公司或财务报告执行合并。
-   通过使用财务报告生成期间结束财务报表。
-   设置分类帐期间为 **暂停**，以便没有进一步过帐发生。 您还可以在发生期间结束活动时限制期间到特定的用户组，以便更好地控制。 将期间设置为 **永久关闭** 不是一个好主意，因为您将无法重新打开已关闭的期间。

“财务期间结帐”工作区可用于组织和跟踪各种期间结束流程所需任务。 


有关详细信息，请参阅以下主题：
- [财务期间结帐工作区](financial-period-close-workspace.md) 
- [年终结算](Year-end-close.md)  
- [批量财务期间结帐](tasks/mass-financial-period-close.md)




