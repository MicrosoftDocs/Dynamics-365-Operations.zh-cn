---
title: 年终结算
description: 此主题描述运行总帐年终结算流程所需设置和步骤。
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3071365640eb6c012cb9af5461e885bb3f135143
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175304"
---
# <a name="year-end-close"></a>年终结算

[!include [banner](../includes/banner.md)]

此主题描述运行总帐年终结算流程所需设置和步骤。 

在某一会计年度结束时，必须运行年终结算流程将未结余额转移到新年度。 大多数组织多次运行年终结算流程。 第一次是将余额移到新会计年度。 然后可以根据需要运行任意次数的年终结算，以便将余额从调整条目移到新会计年度。 

年终结算流程期间，将创建两类可行交易记录。 将始终生成期初交易记录，并用于在新会计年度中创建期初余额。 期初交易记录显示新会计年度中的资产负债表会计科目余额，以及新会计年度中的留存利润会计科目中的损益会计科目余额中的余额。 可以选择创建期末交易记录，以便将损益科目的余额在正在结余的会计年度中降为零。

## <a name="prepare-to-run-the-year-end-close"></a>准备运行年终结算
运行年终结算流程之前，请验证以下设置： 

在**主科目**页面上：

-   验证是否为每个主科目正确定义了**主科目类型**。 主科目类型用于确定将主科目的余额作为期初余额还是结算转到期初交易记录中的留存利润。
-   年终结算期间，**期初科目**字段可用于将主科目的余额转移到新主科目。 将在**期初科目**字段中输入新主科目。 这通常在停用主科目并将新科目用于新会计年度时，用于资产负债表主科目。

在**总帐参数**页面中的**会计年度关帐**下：

-   **除年末结转交易记录**选项用于指定再次运行年终结算时，是否应删除上一年终结算中系统生成的期初交易记录。 如果此选项设置为**是**，将删除上一个期初交易记录，并根据当前余额创建新期初交易记录。 如果此选项设置为**否**，将保留上一个期初交易记录，并再创建一个期初交易记录，以便从上一个年终关帐后过帐的调整交易记录结转余额。
-   **在结转期间创建期末交易记录**选项用于在正在结算的会计年度中创建期末交易记录，以便将损益科目的余额归零。 如果此选项设置为**是**，将同时创建期初交易记录和期末交易记录。 如果此选项设置为**否**，则在下一个会计年度中仅创建期初交易记录，以便结转余额。 会计年度结尾时保留损益科目余额。
-   **将会计年度状态设置为永久关闭**选项用于将会计年度的状态设置为永久关闭。 使用此设置时请谨慎，因为不能重新打开永久关闭状态的所有期间，以防将调整过帐到会计年度。 最好是将此选项设置为**是**。
-   **必须填写凭证号**选项用于定义运行年终结算流程时是否需要凭证号。 最好需要凭证号，以便轻松识别期初交易记录。

在**会计日历**页面中：

-   运行年终结算之前，必须存在下一个会计年度。 需要下一个会计年度，才能在年初期间中创建期初余额。

在**分类帐日历**页面上：

-   可选：正在结算的会计年度的每个会计期间可以设置为**暂停**，以防输入新交易记录。 如果发现了调整条目，可以重新打开暂停期间以过帐调整条目，即使年终结算流程已在运行。

## <a name="define-year-end-close-templates"></a>定义年终结算模板
配置系统之后，可以运行年终结算流程。 在**年终结算**页面上，可以为将为其运行年终结算流程的法人组定义模板。 此模板在每个年终结算中重复使用，但是如果您的组织变动，可以修改此模板。 

首先，为模板定义**组名称**，并选择会计日历。 组名称应标识所含法人组。  例如，可以根据地理位置设置模板，并且其中包含为北美法人、EMEA 法人和 APAC 法人创建的单独组。 

接下来，可以将这些法人添加到模板。 可通过选择组织层次结构或通过选择法人来添加法人。 如果选择组织层次结构，则仅将层次结构内使用所选会计日历的法人添加到模板。 如果使用要添加到模板的法人，则仅可添加具有相同会计日历的法人。 需要相同会计日历，因为年终结算是通过选择会计年度运行的，而各日历的年终结算可能各不相同。 

添加法人之后，请为每个法人定义留存利润主科目。 只要为法人运行年终结算，都将更新**上一年终结算日期**字段。 

**财务维度**选项卡用于定义在期初交易记录中使用哪些财务维度。 请注意，要定义的设置仅与**法人**网格中选择的法人有关。 将为网格中的每个法人重复此设置。 

**转移资产负债表维度**用于定义是否应在期初交易记录中维护过帐到资产负债表科目的交易记录中的财务维度。 最好是将此选项设置为**是**。 **转移损益维度**用于定义是否将过帐到损益科目的交易记录中的财务维度转移到留存利润主科目。 首先，确定与所选法人有关的财务维度。 其中包括该年中针对其过帐的任何财务维度，即使该财务维度不属于有效科目结构也不例外。 然后，将每个维度定义为**结算单个**或**结算全部**。  默认值为**结算全部**，这将维护来自已过帐交易记录的原始财务维度值，并将其用于为留存利润科目创建期初余额。 将为财务维度值的每个唯一组合创建单独的留存利润期初余额。 如果选择**结算单个**，**关闭单个**之后，将把使用该财务维度过帐的所有交易记录汇总到该字段中输入的维度值的留存利润期初余额中。 例如，假设使用“主科目 - 部门”的科目结构过帐了会计年度的所有交易记录。 在模板中的“部门”财务维度中，将选择**结算单个**，并输入值 100。 如果过帐到部门 200、300 和 400 的所有交易记录的总收入为 100,000 美元，则将为“留存利润 - 100”创建一个期初余额。 如果选择**结算单个**并将财务维度值保留为空，将使用为空的维度值把所有交易记录过帐到留存利润。 

年终结算流程不遵循科目结构。 这是因为科目结构在会计年度中可能改变，并且这些更改导致并非始终可以标识相关科目结构。  创建期初交易记录时，将按照年终结算模板中的定义使用财务维度结转余额。 在当前科目结构以及在当前科目结构中不再有效的段落组合中，期初余额条目内不再刻意包含财务维度。 如果您的组织希望排除留存利润期初余额的财务维度，请将该财务维度设置为**结算单个**，并将维度值保留为空。

## <a name="run-the-year-end-close-process"></a>运行年终结算流程
创建年终结算模板支护，可通过在操作窗格中选择**运行会计年度**启动年终结算流程。 从模板中选择要对其运行年终结算的所有法人或一小组法人。 在会计年度中首次运行年终结算时，刻意选择所有法人，以便为所有法人创建期初余额。 如果再次运行年终结算，刻意仅为过帐了其调整条目的法人运行此流程。 

选择要对其运行年终结算流程的会计年度。 如果会计年度的最后一个期间有多个期末期间，并且定义了设置以创建期末交易记录，**期间名称**将变为可用，这样您就可以选择哪个期末期间过帐期末交易记录。 

输入凭证号，是否需要凭证号取决于总帐参数中的设置。 同一凭证号将用于为年终结算流程选择的所有法人。 凭证号不是使用编号规则生成的。 最好输入凭证号，即使不需要。 如果输入凭证号，更容易在新会计年度中找到期初交易记录。 如果不输入凭证号，期初交易记录的凭证将为空。 

如果要取消所选会计年度的上一个年终结算，请将**撤销上一次结算**设置为**是**。 将撤销该年终结算，但是随时可以运行此流程。 如果撤销年终结算，**上一年终结算日期**将不可用。 

年终结算流程默认以批处理模式运行。 最好以批处理模式运行流程，以便允许用户返回到其他活动。 年终结算流程完成后，将使用会话日期更新**上一年终结算日期**。

有关详细信息，请参阅[在期间结束时关闭总帐](close-general-ledger-at-period-end.md)和[关帐会计年度](tasks/close-fiscal-year.md)。


