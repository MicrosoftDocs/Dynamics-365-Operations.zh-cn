---
title: "跟踪生成的报表结果并将其与基准值进行比较。"
description: "本主题提供有关如何将生成的 ER 报表的结果与基准报表值进行比较的信息。"
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 1a598d0bd053c60c3f8df6b05ecb7ff15addfaa3
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2018

---

# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>跟踪生成的报表结果并将其与基准值进行比较。

[!include[banner](../includes/banner.md)]

可跟踪用于生成传出电子单据的 ER 格式的结果。 如果开启了跟踪生成（ER 用户参数**以调试模式运行**），只要运行 ER 报表，都将在 ER 格式执行日志中生成一条新的跟踪记录。 生成的每条记录中包含以下详细信息：

- 验证规则生成的所有警告
- 验证规则生成的所有错误 
- 生成的所有以跟踪记录附件形式存储的文件

可存储任何 ER 格式的单个基准申请表文件。 如果文件描述运行的报表的结果，则视为基准文件。 如果开启跟踪生成后运行的 ER 格式有基准文件，除了之前提到的详细信息，跟踪还将存储生成的电子单据与这个基准文件的比较结果。 只需单击一次，就还可以以单个 zip 文件的形式获取生成的电子单据及其基准文件。 然后可以通过使用 Windiff 之类外部工具执行详细比较。

可以评估跟踪以分析生成的电子单据中是否包含预期内容。 当代码库已更改时（如当您迁移到了应用程序的新实例，安装了修补程序包或部署了代码修改时），可以在用户接受测试 (UAT) 环境中执行此项评估。 这样就可以确保评估不会影响 所用 ER 报表的执行。 对于许多 ER 报表来说，可以以无人值守模式执行评估。

若要了解此项功能，请播放 **ER 生成报表和比较结果（第 1 部分）** 和 **ER 生成报表和比较结果（第 2 部分）** 任务指南，这些指南属于 **7.5.4.3 测试 IT 服务/解决方案 (10679)** 业务流程，可以从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。 这些任务指南可以引导您完成配置 ER 框架以使用基准文件评估生成的电子单据这一过程。

