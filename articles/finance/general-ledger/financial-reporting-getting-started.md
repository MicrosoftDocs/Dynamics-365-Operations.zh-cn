---
title: 财务报告概览
description: 本主题介绍从哪里访问 Microsoft Dynamics 365 Finance 中的财务申报，以及如何使用财务申报功能。
author: aprilolson
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43ab01d36f032e36a0daed6f94897bba42f8a189
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188989"
---
# <a name="get-started-with-financial-reporting"></a>开始使用 Financial reporting 

[!include [banner](../includes/banner.md)]

本主题介绍从哪里访问财务申报，以及如何使用财务申报功能。 其中还包括提供的默认财务报表的描述。

## <a name="accessing-financial-reporting"></a>访问财务申报

您可以在以下位置找到 **财务申报** 菜单：

-   **总帐** &gt; **查询和报表**
-   **预算编制** &gt; **查询和报表** &gt; **基本预算编制**
-   **预算编制** &gt; **查询和报表** &gt; **预算计划**
-   **预算编制** &gt; **查询和报表** &gt; **预算控制**
-   合并

若要为法人创建和生成财务报表，您必须为该法人设置以下信息：

-   会计日历
-   总帐
-   会计帐户表
-   货币
-   将交易至少发布到一个帐户
-   MainAccount 在 **总帐 > 分类帐设置 > Financial Reporting 设置** 的“已选择”列中列出。

## <a name="granting-security-access-to-financial-reporting"></a>授予对 Financial Reporting 的安全访问权限
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
| 维护财务报表安全 | 维护财务报表安全并执行管理任务。 | FinancialReportsSecuritySystemMaintain |
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

在添加用户或更改角色后，用户应该在几分钟内就能访问财务报表。 

> [!NOTE]
> 将向财务申报中的所有角色添加 sysadmin 角色。

## <a name="report-deletions-and-expirations"></a>报表删除和到期
生成报表的用户可以删除他们自己的报表。 具有 **维护财务报表安全** 责任的用户可以删除其他人的报表。 

在版本 10.0.8 中，引入了到期日期的概念。 一项新的必需功能在功能管理工作区的 **所有** 页面中启用。 **财务报表保留策略** 功能包含以下更改：
* 新生成的报表将从生成之日起自动被标记为具有 90 天的有效期。
* 安装该功能之前的所有现有报表将提供 90 天的有效期。 该日期可能会在短时间内显示为空白，直到 Financial Reporting 服务运行、生成报表，并且该服务执行对具有空白到期日期的现有报表的更新。 
* 具有 **维护财务报表安全** 的用户有权使用此功能。 具有 **维护财务报表** 责任并被授予了 **维持财务报表到期** 特权的任何用户还可以修改有效期。 目前有两个保留选项可用： 
  * 90 天有效期。
  * 将报表设置为永不过期。
  
如果选择了到期时间（如 90 天），则从今天开始 90 天有效。 此行为与从生成报表时设置的原始生成日期起计算的 90 天不同。 
  
将来的功能中将考虑其他选项。 默认值为 90 天有效期，具有适当权限的用户可以在 **财务报表** 列表页上覆盖默认值。    

## <a name="default-reports"></a>默认报表
财务报表提供 22 个默认财务报表。 每个报表使用默认主科目类别。 您可以按原样使用这些报表，或者针对您的财务报表需要将其作为起点。 除了传统财务报表（例如收入报表和资产负债表）之外，这些默认报表还包括显示您可以创建的不同类型财务报表的报表。 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| 默认报表                                                                                         | 描述                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 个月累积单列收入报表 – 默认 | 查看单列中在过去 12 个月内组织的收益率。                                                                                                                                                                                                                                      |
| 12 个月趋势收入报表 – 默认                 | 查看每 12 个月内组织的收益率。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                             |
| 实际与预算 – 默认                                | 查看原始预算的所有帐户的详细余额信息，并将具有差异的已修订预算与实际进行比较。                                                                                                                                                                          |
| 审计详细信息 – 默认                                  | 查看所有帐户的详细余额信息。 此报表按申报币种和本币显示借方和贷方余额，以及附加的交易记录信息，如用户 ID，最后修改数据的用户、最后修改的日期和日记帐 ID。 |
| 余额表 – 默认                                   | 查看所有帐户的详细余额信息。 此报表显示当前期间和本年迄今的期初和期末余额以及借方和贷方余额，以及附加的交易记录信息，例如，凭证。                                                                    |
| 资产负债表 – 默认                                   | 查看组织的年度财务状况。                                                                                                                                                                                                                                                             |
| 资产负债表和收入报表并排 - 默认 | 并排查看组织的年度财务状况和收益率。                                                                                                                                                                                                                              |
| 现金流量 – 默认                                       | 了解进入和流出组织的现金。                                                                                                                                                                                                                                   |
| 详细 JE 和 TB 审查 – 默认                      | 查看所有帐户的期初余额和活动信息。                                                                                                                                                                                                                                                      |
| [试算平衡表(明细) - 默认](trial-balance-financial-reports.md)| 查看具有借方和贷方余额的所有帐户的余额信息，以及这些余额的净值，还有交易记录日期、凭证和日记帐描述。                                                                                                                                  |
| 三年每季度趋势费用 – 默认             | 了解前三年过去 12 个季度的费用。                                                                                                                                                                                                                                   |
| 财务描述 JE 和 TB 审查 – 默认            | 查看资产、负债、所有者权益、收入、支出、收益或损失财务描述的余额和活动概览。                                                                                                                                                                           |
| [收入报表 – 默认](income-statement-financial-report.md)| 查看组织的当前期间和本年迄今收益率。                                                                                                                                                                                                                                   |
| 科目交易记录列表 – 默认                        | 查看所有帐户的详细余额信息。 此报表显示借方和贷方余额，以及，附加的交易记录信息，例如交易记录日期、日记帐编号、凭证、过帐类型和跟踪编号。                                                                            |
| 比率 – 默认                                          | 查看组织的当年偿付、收益率和效率比率。                                                                                                                                                                                                                           |
| 累计 12 个月费用 – 默认                       | 了解每个过去 12 个月的费用。 这 12 个月可以跨多个会计年度。                                                                                                                                                                                                       |
| 累计季度收入报表 – 默认               | 按过去年度每个季度以及本年迄今查看组织的收益率。                                                                                                                                                                                                                   |
| 并排资产负债表 – 默认                      | 查看组织的年度财务状况。 此报告并排显示资产和负债，以及股东权益。                                                                                                                                                                                |
| [试算平衡表汇总 – 默认](trial-balance-financial-reports.md)| 查看具有期初和期末余额的所有帐户的余额信息，以及借方和贷方余额还有其净差额。                                                                                                                                                                  |
| [各年汇总试算余额表 – 默认](trial-balance-financial-reports.md)| 查看具有期初和期末余额的所有帐户的余额信息，以及借方和贷方余额还有当年和过去一年的净差额。                                                                                                                           |
| 每周销售和折扣 - 默认                     | 了解一个月内每周的销售金额和折扣。 此报告包含一个四周合计。                                                                                                                                                                                                              |
| 可用预算资金 - 默认                         | 查看所有科目的修订预算、实际支出、预算预留和预算资金的详细比较                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>打开财务报表
在您选择 **财务申报** 菜单时，会显示公司的默认财务报表列表。 然后您可以打开或修改报表。 若要打开一个默认报表，请选择报表名称。 首次打开报表，它将为上个月自动生成。 例如，如果在 2019 年 8 月首次打开报表，将为 2019 年 7 月 31 日生成报表。 在打开报表后，可以通过深化到特定的数据部分并更改报表选项来开始探索报表。

## <a name="creating-and-modifying-financial-reports"></a>创建和修改财务报表
从财务报表列表中，您可以创建一个新的报表或修改现有的报表。 如果您具有相应的权限，则可以通过选择“操作窗格”上的 **新建** 以创建新财务报表 。 报表设计器程序将下载到您的设备。 报表设计器启动之后，您就可以创建新报表。 在您保存新的报表后，它显示在财务报表列表中。 此列表仅显示为您在 Dynamics 365 Finance 中使用的公司创建的报表。 

## <a name="reporting-tree-definitions"></a>报告树定义 
用于生成财务报表的组件之一是报告树定义。 报告结构树定义帮助定义您组织的结构和层次结构。 这是基于财务数据中的维度关系的跨维层次结构。 它在报告单位级别和摘要级别为结构树中的所有单位提供信息。

您可以创建数量不限的报告结构树来以各种方式显示组织的数据。 每个报告树可以包含部门和汇总单位的任意组合，但是报表定义一次只能链接到一个报告树。 


## <a name="troubleshooting-issues-opening-report-designer"></a>解决打开报表设计器存在的问题
打开报表设计器时，有一些常见问题可能会导致出现故障。 这些问题及其解决步骤如下。

问题 1：选择 **新建** 或 **编辑** 时，报表设计器不启动。

* 在 Internet Explorer 中，选择 **设置**，然后选择 **Internet 选项**。 选择 **安全** 选项卡。选择“受信任站点”，然后选择 **站点**。 在 **将此网站添加到区域** 中，输入“\*\.dynamics.com”（不带引号），然后选择 **添加**。 
* 在 Internet Explorer 中，选择 **设置**，然后选择 **Internet 选项**。 选择 **安全** 选项卡。选择“受信任站点”。 在标有此区域的安全级别区域中，将此选项更改为 **中-低**。
* 在浏览器中禁用弹出窗口阻止程序。
* 工作站需要安装 Microsoft .NET Framework 4.6.2 或更高版本。 可从 [Microsoft 下载中心](https://www.microsoft.com/download/details.aspx?id=53345)下载和安装此版本的 Microsoft .NET Framework。
* 如果使用的是 Chrome 浏览器，则必须安装 ClickOnce 扩展才能下载报表设计器客户端。 如果以匿名模式运行 Chrome，请确保为匿名模式启用了 ClickOnce 扩展。 有关 Chrome ClickOnce 扩展的详细信息，请参阅[云部署的系统要求](../../fin-ops-core/fin-ops/get-started/system-requirements.md)。
* 如果您正在通过 Chrome 浏览器使用 Microsoft Edge，则无需为 Edge Chromium 安装 ClickOnce 扩展。 但是，必须启用 ClickOnce 选项以下载报表设计器客户端。 如果以匿名模式运行，请确保为匿名模式启用了 ClickOnce 扩展。
     1. 在 Microsoft Edge 中打开新浏览器。
     2. 输入 **edge://flags**，然后选择 **输入**。
     3. 搜索 **ClickOnce 支持** 选项或使用此直接链接：**edge://flags/#edge-click-once**。
     4. 将下拉菜单选项设置为 **已启用**。
     5. 选择 **重启浏览器**。

问题 2：未为用户分配使用 Financial Reporting 所需的权限。 

* 要验证用户是否没有权限，请在此错误上选择 **是**：“无法连接到 Financial Reporting 服务器。 如果要继续并指定其他服务器地址，请选择‘是’。” 然后选择 **测试连接**。 如果您没有权限，您将看到一条消息，显示“连接尝试失败。 用户没有适当的权限连接到服务器。 请与系统管理员联系。”
* 所需权限在上面的[授予对 Financial Reporting 的安全访问权限](#granting-security-access-to-financial-reporting)中列出。 Financial Reporting 中的安全性基于这些权限。 除非将这些权限（或包含这些权限的另一个安全角色）分配给您，否则您将无权访问。 
* **公司用户提供程序到公司** 集成任务（也负责并称为用户集成）每隔 5 分钟运行一次。 任何权限更改最多可能需要 10 分钟在 Financial Reporting 中生效。 
  如果另一个用户可以打开报表设计器，请选择 **工具**，然后选择 **集成状态**。 验证集成映射“公司用户提供程序到公司”是否已成功运行，因为已为您分配了使用 Financial Reporting 的权限。 
* 可能是另一个错误阻止了 **Dynamics 用户到 Financial Reporting 用户的集成** 完成。 或者可能是由于已启动但尚未完成数据市场重置，或者发生了另一个系统错误。 请稍后再次尝试运行此流程。 如果问题仍然存在，请与系统管理员联系。

问题 3：您可以从 ClickOnce 报表设计器登录页面继续访问，但无法在报表设计器中完成登录。 

* 输入登录凭据时，在本地计算机上设置的时间必须在 Financial Reporting 服务器上时间的五分钟之内。 如果相差超过五分钟，系统将不允许登录。 
* 在这种情况下，我们建议启用 Windows 选项来自动设置您的 PC 时间。 

## <a name="additional-resources"></a>其他资源
- [查看财务报表](view-financial-reports.md)
- [财务报表中的报告结构树定义](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]