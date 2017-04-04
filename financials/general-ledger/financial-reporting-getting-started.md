---
title: "财务申报"
description: "此主题的位置在 Microsoft Dynamics 365 中描述访问报告工序的财务和如何使用财务报表功能。 它包括提供默认财务报表的描述。"
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

此主题的位置在 Microsoft Dynamics 365 中描述访问报告工序的财务和如何使用财务报表功能。 它包括提供默认财务报表的描述。

<a name="accessing-financial-reporting"></a>访问财务申报
-----------------------------

**您可以找到财务报告**菜单 Dynamics 中的工序的以下位置：365

-   **总帐** &gt; ** **查询和报表
-   **预算** &gt; **查询和报告** &gt; **基本预算**
-   ** ** &gt; **预算的查询和报表** &gt; **预算计划**
-   ** ** &gt; **预算的查询和报表** &gt; **预算控制**
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
| 维护财务报表            | 维护财务报表            | 客户帐户，主管经理，财务总监，预算经理 |
| 生成财务报表            | 生成财务报表            | "首席执行官"，如首席财务官，会计                                                            |
| 查看财务报表                | 审查财务绩效          | 未分配                                                                   |

在添加用户或更改角色后，用户应该在几分钟内就能访问财务报表。 **注释：** sysadmin 角色添加到在财务报告的所有影响。

## <a name="default-reports"></a>默认报表
财务报表提供 22 个默认财务报表。 每个报表在 Dynamics 365 使用默认主科目类别的工序。 您可以按原样使用这些报表，或者针对您的财务报表需要将其作为起点。 除了传统财务报表（例如收入报表和资产负债表）之外，这些默认报表还包括显示您可以创建的不同类型财务报表的报表。 在下表的每个报表链接。有关组合办公室报表中的显示方式。

| 默认报表                                                                                         | 说明                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | 查看单列中在过去 12 个月内组织的收益率。                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | 查看每 12 个月内组织的收益率。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | 查看原始预算的所有帐户的详细余额信息，并将具有差异的已修订预算与实际进行比较。                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | 查看所有帐户的详细余额信息。 此报表按申报币种和本币显示借方和贷方余额，以及附加的交易记录信息，如用户 ID，最后修改数据的用户、最后修改的日期和日记帐 ID。 |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | 查看所有帐户的详细余额信息。 此报表显示当前期间和本年迄今的期初和期末余额以及借方和贷方余额，以及附加的交易记录信息，例如，凭证。                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | 查看组织的年度财务状况。                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | 并排查看组织的年度财务状况和收益率。                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | 了解进入和流出组织的现金。                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | 查看所有帐户的期初余额和活动信息。                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | 查看具有借方和贷方余额的所有帐户的余额信息，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | 了解前三年过去 12 个季度的费用。                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | 查看资产、负债、所有者权益、收入、支出、收益或损失财务描述的余额和活动概览。                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | 查看组织的当前期间和本年迄今收益率。                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | 查看所有帐户的详细余额信息。 此报表显示借方和贷方余额，以及，附加的交易记录信息，例如交易记录日期、日记帐编号、凭证、过帐类型和跟踪编号。                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | 查看组织的当年偿付、收益率和效率比率。                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | 了解每个过去 12 个月的费用。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | 显示组织每季度的收益率能力过去年和年初至今的。                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | 查看组织的年度财务状况。 此报告并排显示资产和负债，以及股东权益。                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | 查看具有期初和期末余额的所有帐户的余额信息，以及借方和贷方余额还有其净差额。                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | 与净其差额。显示在期初和期末余额的科目的余额信息以及贷方和借方余额当前年度以及过去或年。                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | 了解一个月内每周的销售金额和折扣。 此报告包含一个四周合计。                                                                                                                                                                                                              |
| [预算-可用的默认 https://mix.office.com/watch/15hcpezcbx7tv)] (资金                         | 显示预算修订的实际支出、预算、预留和预算资金一个比较详细可用于所有帐户                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>打开财务报表
在您单击**“财务申报”**按钮时，会显示公司的默认财务报表列表。 然后您可以打开或修改报表。 若要打开一个默认报表，请选择报表名称。 首次打开报表，它将为上个月自动生成。 例如，如果您在 2016 年 8 月第一次打开一个报表，报表生成 2016 年 7 月 31 日。 在打开报表后，可以通过深化到特定的数据部分并更改报表选项来开始探索报表。

## <a name="creating-and-modifying-financial-reports"></a>创建和修改财务报表
从财务报表列表中，您可以创建一个新的报表或修改现有的报表。 如果您具有相应的权限，则可以通过单击创建新财务报表**新**有关操作窗格。 报表设计器程序下载到您的设备。 在报表设计器中开始后稍后您可创建新报告。 在您保存新的报表后，它显示在财务报表列表中。 列表查看为公司创建的那些报表可以在 Dynamics 365 用于该工序。 创建和修改有关的详细信息。Dynamics 365 的财务报表过程的工序，请参阅这些 [] (博客过帐从 Dynamics 财务报告的 https://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/) 博客。 **注释：**您计算机上下载报表设计器客户必须具有对此安装 Microsoft .NET Framework 版本的 4.6.2。 Microsoft .NET Framework 的此版本可以从在此处下载和安装 [] (https://www.microsoft.com/en-us/download/details.aspx?id=53345)。 如果您使用镶边，必须安装 ClickOnce 扩展名以便下载报表设计器客户。 如果您在隐姓氏埋名的模式运行，请确定 ClickOnce 扩展为隐姓氏埋名的模式启用。 您还可以修改在财务报表列表中显示的报表。 当选择围绕报告名称的区域时，请在操作窗格上单击**“编辑”**。 报表设计器程序将会启动。

<a name="see-also"></a>请参阅
--------

[View financial reports](view-financial-reports.md)

[Dynamics 财务报表博客](http://blogs.msdn.com/b/dynamics_financial_reporting/)


