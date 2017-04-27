---
title: "财务申报"
description: "本主题介绍从哪里访问 Microsoft Dynamics 365 for Operations 中的财务申报，以及如何使用财务申报功能。 其中包括提供的默认财务报表的描述。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>财务申报

[!include[banner](../includes/banner.md)]


本主题介绍从哪里访问 Microsoft Dynamics 365 for Operations 中的财务申报，以及如何使用财务申报功能。 其中包括提供的默认财务报表的描述。

<a name="accessing-financial-reporting"></a>访问财务申报
-----------------------------

您可以在 Dynamics 365 for Operations 中的以下位置查找**财务申报**菜单：

-   **总帐** &gt; **查询和报表**
-   **预算编制** &gt; **查询和报表** &gt; **基本预算编制**
-   **预算编制** &gt; **查询和报表** &gt; **预算计划**
-   **预算编制** &gt; **查询和报表** &gt; **预算控制**
-   合并

若要为法人创建和生成财务报表，您必须为该法人设置以下信息：

-   会计日历
-   分类帐
-   会计科目表
-   货币

财务报表功能可用于具有相应的权限和责任的用户（通过安全角色分配给他们）。 以下各节列出这些权限和责任，以及关联的角色。

### <a name="duties"></a>责任

| 责任标签                            | 描述                                                             | AOT 名称                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| 维护财务报表安全 | 维护财务报表安全并执行管理任务。 | FinancialReportsSecurityMaintain |
| 维护财务报表            | 设计并维护财务报表。                                  | FinancialReportsMaintain         |
| 生成财务报表            | 生成并刷新财务报表。                                 | FinancialReportsGenerate         |
| 审查财务绩效          | 审查并分析财务绩效。                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>特权

| 标签权限                       | 描述                                                             | AOT 名称                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| 维护财务报表安全 | 维护财务报表安全并执行管理任务。 | FinancialReportsSecurityMaintain |
| 维护财务报表            | 设计并维护财务报表。                                  | FinancialReportsMaintainReports  |
| 生成财务报表            | 生成并刷新财务报表。                                 | FinancialReportsGenerateReports  |
| 查看财务报表                | 查看财务报表。                                                 | FinancialReportsView             |

### <a name="roles"></a>角色

| 标签权限                       | 责任                                  | 角色                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| 维护财务报表安全 | 维护财务报表安全 | 安全管理员                                                          |
| 维护财务报表            | 维护财务报表            | 会计经理、会计主管、财务总监、预算经理 |
| 生成财务报表            | 生成财务报表            | CEO、CFO、会计师                                                            |
| 查看财务报表                | 审查财务绩效          | 未分配                                                                   |

在添加用户或更改角色后，用户应该在几分钟内就能访问财务报表。 **注释：**将向财务申报中的所有角色添加 sysadmin 角色。

## <a name="default-reports"></a>默认报表
财务报表提供 22 个默认财务报表。 每个报表都使用 Dynamics 365 for Operations 中的默认主科目类别。 您可以按原样使用这些报表，或者针对您的财务报表需要将其作为起点。 除了传统财务报表（例如收入报表和资产负债表）之外，这些默认报表还包括显示您可以创建的不同类型财务报表的报表。 下表中的每个报表链接到一个有关该报表的 Office Mix 演示文稿。

| 默认报表                                                                                         | 说明                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 个月累积单列收入报表 – 默认](https://mix.office.com/watch/76kc7bm3wnt1) | 查看单列中在过去 12 个月内组织的收益率。                                                                                                                                                                                                                                      |
| [12 个月趋势收入报表 – 默认](https://mix.office.com/watch/12brmfge5p8r)                 | 查看每 12 个月内组织的收益率。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                             |
| [实际与预算 – 默认](https://mix.office.com/watch/fi439lkwr0no)                                | 查看原始预算的所有帐户的详细余额信息，并将具有差异的已修订预算与实际进行比较。                                                                                                                                                                          |
| [审计详细信息 – 默认](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | 查看所有帐户的详细余额信息。 此报表按申报币种和本币显示借方和贷方余额，以及附加的交易记录信息，如用户 ID，最后修改数据的用户、最后修改的日期和日记帐 ID。 |
| [余额表 – 默认](https://mix.office.com/watch/1kezwu2a10fq4)                                   | 查看所有帐户的详细余额信息。 此报表显示当前期间和本年迄今的期初和期末余额以及借方和贷方余额，以及附加的交易记录信息，例如，凭证。                                                                    |
| [资产负债表 – 默认](https://mix.office.com/watch/zkgq0u7visw9)                                   | 查看组织的年度财务状况。                                                                                                                                                                                                                                                             |
| [资产负债表和收入报表并排 - 默认](https://mix.office.com/watch/zkgq0u7visw9) | 并排查看组织的年度财务状况和收益率。                                                                                                                                                                                                                              |
| [现金流量 – 默认](https://mix.office.com/watch/jd3go9pz6390)                                       | 了解进入和流出组织的现金。                                                                                                                                                                                                                                   |
| [详细 JE 和 TB 审查 – 默认](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | 查看所有帐户的期初余额和活动信息。                                                                                                                                                                                                                                                      |
| [试算平衡表(明细) - 默认](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | 查看具有借方和贷方余额的所有帐户的余额信息，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。                                                                                                                                  |
| [三年每季度趋势费用 – 默认](https://mix.office.com/watch/gwm4zu7tmtj8)             | 了解前三年过去 12 个季度的费用。                                                                                                                                                                                                                                   |
| [财务描述 JE 和 TB 审查 – 默认](https://mix.office.com/watch/1sw9fmtwgjb1f)            | 查看资产、负债、所有者权益、收入、支出、收益或损失财务描述的余额和活动概览。                                                                                                                                                                           |
| [收入报表 – 默认](https://mix.office.com/watch/sbuhgl5hzuhi)                                | 查看组织的当前期间和本年迄今收益率。                                                                                                                                                                                                                                   |
| [科目交易记录列表 – 默认](https://mix.office.com/watch/19h9v2rmh48vy)                        | 查看所有帐户的详细余额信息。 此报表显示借方和贷方余额，以及，附加的交易记录信息，例如交易记录日期、日记帐编号、凭证、过帐类型和跟踪编号。                                                                            |
| [比率 – 默认](https://mix.office.com/watch/b08hfc5h92me)                                          | 查看组织的当年偿付、收益率和效率比率。                                                                                                                                                                                                                           |
| [累计 12 个月费用 – 默认](https://mix.office.com/watch/iywod5qmqhz7)                       | 了解每个过去 12 个月的费用。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                                       |
| [累计季度收入报表 – 默认](https://mix.office.com/watch/1k4yl6a6oyxqc)               | 按过去年度每个季度以及本年迄今查看组织的收益率。                                                                                                                                                                                                                   |
| [并排资产负债表 – 默认](https://mix.office.com/watch/zkgq0u7visw9)                      | 查看组织的年度财务状况。 此报告并排显示资产和负债，以及股东权益。                                                                                                                                                                                |
| [试算平衡表汇总 – 默认](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | 查看具有期初和期末余额的所有帐户的余额信息，以及借方和贷方余额还有其净差额。                                                                                                                                                                  |
| [各年汇总试算余额表 – 默认](https://mix.office.com/watch/1ewwgbpv0iwrl)           | 查看具有期初和期末余额的所有帐户的余额信息，以及借方和贷方余额还有当年和过去一年的净差额。                                                                                                                           |
| [每周销售和折扣 - 默认](https://mix.office.com/watch/112ng0hy5de0j)                     | 了解一个月内每周的销售金额和折扣。 此报告包含一个四周合计。                                                                                                                                                                                                              |
| [可用预算资金 - 默认](https://mix.office.com/watch/15hcpezcbx7tv)                         | 查看所有科目的修订预算、实际支出、预算预留和预算资金的详细比较                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>打开财务报表
在您单击**“财务申报”**按钮时，会显示公司的默认财务报表列表。 然后您可以打开或修改报表。 若要打开一个默认报表，请选择报表名称。 首次打开报表，它将为上个月自动生成。 例如，如果在 2016 年 8 月首次打开报表，将为 2016 年 7 月 31 日生成报表。 在打开报表后，可以通过深化到特定的数据部分并更改报表选项来开始探索报表。

## <a name="creating-and-modifying-financial-reports"></a>创建和修改财务报表
从财务报表列表中，您可以创建一个新的报表或修改现有的报表。 如果您具有相应的权限，则可以通过单击操作窗格上的**新建**以创建新财务报表 。 报表设计器程序将下载到您的设备。 报表设计器启动之后，您就可以创建新报表。 在您保存新的报表后，它显示在财务报表列表中。 此列表仅显示为您在 Dynamics 365 for Operations 中使用的公司创建的报表。 有关在 Dynamics 365 for Operations 中创建和修改财务报表的过程的详细信息，请参阅 Dynamics 财务申报博客中的[博客文章](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/)。 **注释：**您用于下载报表设计器客户端的计算机上必须已安装了 Microsoft .NET Framework 版本 4.6.2。 可从[此处](https://www.microsoft.com/en-us/download/details.aspx?id=53345)下载和安装此版本的 Microsoft .NET Framework。 如果使用的是 Chrome，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。 如果以匿名模式运行，请确保为匿名模式启用了 ClickOnce 扩展。 您还可以修改在财务报表列表中显示的报表。 当选择围绕报告名称的区域时，请在操作窗格上单击**“编辑”**。 报表设计器程序将会启动。

<a name="see-also"></a>请参阅
--------

[查看财务报表](view-financial-reports.md)

[Dynamics 财务报表博客](http://blogs.msdn.com/b/dynamics_financial_reporting/)




