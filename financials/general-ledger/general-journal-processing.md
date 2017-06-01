---
title: "普通日记帐处理"
description: "本文介绍 Microsoft Dynamics 365 for Operations 中可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 150ca540fca154947cca47e97e45ce865ab1f507
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="general-journal-processing"></a>普通日记帐处理

[!include[banner](../includes/banner.md)]


本文介绍 Microsoft Dynamics 365 for Operations 中可以帮助使日记帐处理更加轻松以及帮助确保获取正确数据且不影响内部控制的功能。  

日记帐名称

要设置的最重要的区域之一是日记帐名称。 最好为每个用途定义特定的日记帐名称，如内部公司、应计调整和错误纠正。 您可以定制每个日记帐名称以便让每个用途的数据输入都简单且安全。 

在**“日记帐名称”**页上，您可以设置以下因素：

-   **工作流审核** - 要增强内部控制，请基于总借方金额等条件定义日记帐工作流（用于确定审查和审核步骤的重要性限制）。 您在 **总帐工作流** 页上为普通日记帐设置工作流。
-   **默认值** - 为对方科目、币种和财务维度选择的默认值。
-   **日记帐控制** - 您可以设置对公司和科目类型的限制以及对科目段值的限制。 

**示例**

日记帐名称只能用于调整。 在这种情况下，您可以指定只有**“分类帐”**科目类型在所有公司都有效。 [![日记帐控制科目类型](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

日记帐名称只能用于某个特定科目段或用于主科目的某个范围。 [![日记帐控制科目段](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

**“自动冲销”**选项可用于普通日记帐。 例如，您有一个应计调整，其中的实际单据尚未处理，如下图所示。
[![普通日记帐冲销](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

用于日记帐条目的 Microsoft Excel 加载项进一步提高了自动化水平并使数据输入更容易。 **“在 Excel 中打开行”**操作可用于**“普通日记帐”**和**日记帐凭证**页。 

在**“期间日记帐”**页上，您可以设置重复日记帐以自动执行日记帐处理。 

您可以随时使用凭证模板。 在**“普通日记帐”**页上，**“保存”**和**“选择凭证模板”**操作可在**“日志凭证”**页上找到（位于凭证行的**“功能”**下）。

## <a name="related-setup"></a>相关设置
以下设置不是特定于普通日记帐的，但有助于确保数据输入正确且容易。

### <a name="main-account"></a>主科目

主科目设置为普通日记帐处理提供了很多选项：

-   **DC/CR 需求** - 如果主科目被限制到借方或贷方交易记录，则使用此选项。 该设置在验证或过帐日记帐时验证。
-   **默认对方科目**
-   **暂停** - 在所有公司或为特定公司/法人暂停数据输入的主科目。
-   **不允许手动输入** - 防止用户为日记帐中的科目手动输入值。
-   **默认/验证币种**
-   **法人覆盖** - 此设置特定于已定义的公司/法人：
    -   **默认/验证销售税**
    -   **默认维度** - **“不固定”**或**“固定值”**。 **“固定值”**将帮助确保此主科目的所有过帐始终使用设置为**“固定”**的任何维度值。
-   **过帐验证**
    -   **用户验证** - 此选项控制允许哪些用户过帐到主科目。
    -   **过帐类型验证** - 此选项控制可对主科目使用的过帐类型。

### <a name="accounting-structures-and-advanced-rules-structures"></a>科目结构和高级规则结构

科目结构和高级规则结构对于确保在一般日记帐处理和任何单据化期间捕获财务报告所需的数据以及绩效跟踪极其重要。 科目结构和高级规则结构可让您定制数据输入体验。 您可以仅对在所有情况下都相关的财务维度允许数据输入，还可以强制实施“始终捕获必需和正确的数据”这一要求。

有关详细信息，请参阅[计划：会计科目表](plan-chart-of-accounts.md)。 




