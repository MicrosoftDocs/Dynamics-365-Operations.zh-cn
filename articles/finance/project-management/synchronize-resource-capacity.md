---
title: 同步资源产能
description: 此主题介绍如何在日历与项目之间同步资源的产能。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760482"
---
# <a name="synchronize-resource-capacity"></a>同步资源产能

[!include [banner](../includes/banner.md)]

资源同步流程帮助确保日历和基础日历信息深入到项目资源计划。 如果更改日历，流程对项目资源计划进行所需的更新。 因为日历的资源信息提前同步，这些流程还有助于改进性能。 因此，资源计划信息的更新更快。 我们建议您批量计划流程，而不是一次计划一个。 否则，某些员工可能忘记上次同步信息的起迄日期。 如果不使用起迄日期，可能在日期同步时发生间隔。

![日历同步](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>同步资源产能汇总

同步流程被设计为同步所有资源日历信息。 此信息包括有关对项目的资源日历产能表进行的任何更改的基本日历信息。 如果在项目中添加新的资源，同步可以帮助确保更新的日历信息可用。 此同步随时都可以进行。

我们建议您使用批次执行。 选项在同步产能预留中可用。

1. 选择**项目管理与核算** &gt; **定期** &gt; **产能同步** &gt; **同步资源产能汇总**。
2. 设置下表中的选项。

    | 选项      | 说明 |
    |-------------|-------------|
    | 期间代码 | 选择性地选择总帐日期间隔代码，以设置资源产能汇总的同步流程的开始日期和结束日期。 |
    | 入职日期  | 输入资源产能汇总的同步流程的开始日期。 |
    | 结束日期    | 输入资源产能汇总的同步流程的结束日期。 |

[![同步流程](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
