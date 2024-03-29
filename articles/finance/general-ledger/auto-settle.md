---
title: 自动化分类帐结算
description: 本文提供有关自动化分类帐结算流程的信息。
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708324"
---
# <a name="automate-ledger-settlements"></a>自动化分类帐结算

[!include [banner](../includes/banner.md)]

在 Microsoft Dynamics 365 Finance 版本 10.0.31 中， **自动化分类帐结算流程** 功能在 **功能管理** 工作区提供。 只有在您启用了 **区分分类帐结算与年终结算** 功能时，才能启用 **自动化分类帐结算流程** 功能。

分类帐结算是在总帐中匹配借方和贷方交易记录的过程。 定期执行分类帐结算活动的组织现在可以自动化此流程。 在自动化分类帐结算流程中，借方交易记录和贷方交易记录只有在记帐币种金额相等时才能自动匹配。例如，借方金额 $1.00 可以自动与贷方金额 $1.00 匹配。 但是，借方值 $1.00 不能与每个值为 $0.50 的两个贷方值自动匹配。 不支持分类帐交易金额的部分匹配。

分类帐结算自动化定义以下详细信息：

- 分类帐结算运行时间
- 哪些条件用于匹配可以自动结算的借方和贷方
- 分类帐结算信息按什么顺序处理

## <a name="define-the-occurrence-of-ledger-settlements"></a>定义分类帐结算的运行

分类帐结算自动化使用流程自动化框架。 不同的业务流程使用此框架来定义所选流程的重复执行。 要定义分类帐结算，转到  **系统管理 \> 设置 \> 流程自动化** 或 **总帐 \> 分类帐设置 \> 流程自动化**。

首先，选择 **创建新流程自动化** 选项，选择 **分类帐结算**。 然后，向导将指导您完成设置自动化的流程。

## <a name="general-page"></a>常规页面

在向导的 **常规** 页面上，输入要创建的分类帐结算运行的名称。 例如，如果您的匹配借方和贷方在星期一进行分类帐结算，输入一个描述性名称，如  **LedgerSettle\_Mon**。 您输入的名称将显示在  **分类帐结算** 页面的 **自动化规则** 列中。

此页面上的其余设置是通用的，定义此版本的分类帐结算的运行模式。 例如，如果某个运行是在星期一，您可以对其进行定义以使其每周运行一次，并且可以选择“星期一”作为它运行的星期日期。 您还可以输入较早的计划时间，如凌晨 2:00，这样流程自动化将在下一个工作日开始之前完成。 我们建议您对流程自动化进行计划，让它在您的正常工作时间之外执行。 通过这种方式，您可以帮助减少在工作日工作期间对会计人员的影响。

有关 **常规** 页面上其他字段的详细信息，请参阅流程自动化文档。

## <a name="ledger-settlements-match-criteria-page"></a>分类帐结算匹配条件页面

向导的下一页是 **分类帐结算匹配条件** 页面。 此页面用于定义流程自动化运行中包含的主科目，以及用于确定匹配借方和贷方的条件。

### <a name="account-selection"></a>科目选择

将显示您之前定义为法人分类帐结算科目的主科目。 （您在 **总帐 \> 分类帐设置 \> 总帐参数 \> 分类帐结算** 将主科目定义为分类帐结算科目。）

### <a name="main-account-and-posting-layer"></a>主科目和过帐层

 **主科目** 和 **过帐层** 值是必需的匹配条件。 在自动分类帐结算流程中，分类帐借方交易记录和贷方交易记录的 **主科目** 和 **过帐层** 值必须相等才能匹配。

### <a name="posting-type"></a>过帐类型

如果分类帐借方交易记录和贷方交易记录必须具有相同的过帐类型，以在自动分类帐结算流程中进行匹配，选择 **过帐类型** 选项。

### <a name="financial-dimensions"></a>财务维度

如果分类帐借方交易记录和贷方交易记录必须具有相同的财务维度，以在自动分类帐结算流程中进行匹配，选择 **财务维度** 选项。 选择此选项时，必须在 **可用财务维度** 列表中选择财务维度值条件。 **可用财务维度** 列表不包含主科目维度，因为将作为匹配条件的一部分自动要求提供此项。

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>查看分类帐结算自动化的结果

创建分类帐结算自动化系列后，每个分类帐结算的运行将显示在流程自动化周视图中。 此外，还会显示每个执行的状态。 使用以下状态：

- **已计划**  – 自动化已计划，但尚未运行。
- **正在执行** – 自动化当前正在运行。
- **错误**  – 自动化已运行，但发生错误。 您可以选择 **查看结果** 按钮来查看错误。
- **已完成**  – 自动化已成功运行。 您可以在 **分类帐结算** 页面查看结算结果。

要查看匹配结果，转到 **总帐 \> 定期任务 \> 分类帐结算**。 **分类帐结算** 页面的 **自动化规则** 字段显示用于结算交易记录的自动分类帐结算计划任务的名称。 不成功的结算尝试不会更新 **自动化规则** 值。 如果您手动冲销以前通过自动化流程成功结算的交易记录，**自动化规则** 值将被删除。

匹配记录的 **结算日期** 字段显示执行自动化流程的日期。

## <a name="editing-a-ledger-settlement-automation"></a>编辑分类帐结算自动化

使用流程自动化框架，您可以编辑系列以及为分类帐结算创建的运行。 系列可以从 **流程自动化** 页面或流程自动化周视图进行编辑。 例如，如果经理决定在星期三而不是星期一执行分类帐结算，他们可以在周视图中找到一个运行，然后选择 **查看/编辑 – 系列**。

如果编辑系列，系统会提示您指定是对所有现有执行还是仅对新执行进行更改。 状态为 **已完成** 的历史运行，或 **错误** 状态的运行不会被更改。

您还可以添加新执行或更改现有执行。 例如，下一次分类帐结算运行计划在 1 月 1 日（星期三）运行，但是此日期是假日。 您可以从 **流程自动化** 页面或流程自动化周视图更改此运行。 一个页面将打开，显示计划详细信息和匹配条件。 在这里，您可以编辑计划的时间和日期。 如果需要更改，您还可以编辑匹配条件。 

您还可以禁用执行或系列。 要禁用执行并暂停它的处理，请在流程自动化周视图中选择它，然后选择 **禁用**。 您可以在 **流程自动化** 页面禁用系列。

## <a name="security-for-ledger-settlement-automation"></a>分类帐结算自动化的安全性

**维护分类帐结算自动化系列设置** 责任已添加到会计经理和会计主管角色，**查看分类帐结算自动化系列设置** 责任已添加到会计师、会计经理和会计主管角色，用于执行分类帐结算自动化。 这些责任是默认的安全设置，但可以根据组织的要求进行更改。

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>分类帐结算自动化的总帐参数

**结算典型余额** 字段指示自动分类帐结算的处理顺序。 要设置或查看 **结算典型余额** 值，转到 **总帐 \> 设置 \> 总帐参数**，选择 **分类帐结算** 选项卡。

如果选择 **借方**，自动分类帐结算流程将在借方开始，搜索相应的贷方。 如果选择 **贷方**，自动分类帐结算流程将在贷方开始，搜索相应的借方。 此选项应反映主科目的典型余额。

## <a name="processing-a-ledger-settlement-automation"></a>处理分类帐结算自动化

运行自动化时，系统会为为流程自动化系列定义的主科目选择分类帐交易记录。 将使用从会计年度开始到流程自动化运行日期期间的日期范围按日期对交易记录进行排序。 将根据指定的匹配条件进行匹配。 借方和贷方的记帐币种金额的绝对值必须匹配才能结算。

当主科目通过运行分类帐结算自动化处理时，您无法在 **分类帐结算** 页面显示它。 您必须等到自动化流程完成。 我们建议您将流程自动化计划在工作时间以外运行，以帮助防止冲突。

自动化流程将包括符合条件的所有交易记录，已在 **分类帐结算** 页面手动标记为结算的交易记录除外。

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>由自动化流程结算的交易记录冲销

您可以冲销通过自动分类帐结算流程进行的结算。 冲销通过自动化流程结算的交易记录时，**自动化规则** 值将被删除。
