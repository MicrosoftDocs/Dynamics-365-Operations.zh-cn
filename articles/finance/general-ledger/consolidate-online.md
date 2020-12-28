---
title: 在线财务合并
description: 此主题介绍总帐中的在线财务合并。
author: aprilolson
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 86be6d4cc0af3f2fd92523d4ecd3825f2383fc48
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440748"
---
# <a name="online-financial-consolidations"></a>在线财务合并

[!include [banner](../includes/banner.md)]

此主题介绍总帐中的在线财务合并。 阅读此主题之前，务必阅读[财务合并和货币折算概述](financial-consolidations-currency-translation.md)主题。

完成设置后，在 **[在线] 合并** 页中输入合并的详细信息。 完成后，可单击 **确定** 或 **批处理** 处理合并。

## <a name="criteria"></a>条件
在 **[在线] 合并** 页的 **条件** 选项卡上，定义合并的金额、期间和数据类型。

![“条件”选项卡](./media/criteria-consolidate-online.png "“条件”选项卡")

下面是此选项卡上的各字段的说明：

- **说明** – 输入要合并的期间的精确说明。
- **主科目** – 此部分中的字段用于定义将处理的主科目。

    - **从** 和 **到** – 指定要处理的科目范围。 如果将这些字段保留为空，将把所有公司的所有科目移到合并公司。 因此，如果要合并四个公司，每个公司有一个不同的会计科目表，将在合并公司中创建所有四个公司的所有科目。
    - **使用合并科目** – 如果将此选项设置为 **是**，**选择合并科目的来源** 字段将可用。 在此字段中，选择应将所有科目合并到 **主科目** 页中设置的合并科目，还是要从一个合并科目组选择科目。
    - **合并科目组** – 选择要用于合并的主科目映射的组。

- **合并期间** – 此部分中的字段用于定义合并期间。

    - **从** 和 **到** – 指定合并的日期范围。 如果将这些字段留空，将为公司的分类帐日历中定义的所有期间处理合并。 我们建议您不要将这些字段留空。
    - **包括实际金额** – 如果将此选项设置为 **是**，将合并实际数据。
    - **包括预算金额** – 如果将此选项设置为 **是**，将合并预算登记的数据。
    - **在合并过程中重新生成余额** – 建议不要将此选项设置为 **是**。 而是以单独的批处理作业的形式重新生成余额。

- **预算模型** – 如果已选择合并预算数据，请使用此部分中的选项定义预算模型。

    - **从** 和 **到** – 指定要使用的模型范围。
    - **预算汇率类型** – 选择要用于对预算数据进行货币折算的预算汇率类型。

## <a name="financial-dimensions"></a>财务维度
在 **财务维度** 选项卡上，定义合并公司中应包含的维度。 若要选择维度，请将 **说明** 字段设置为 **维度**，然后定义合并公司中的维度顺序。

![“财务维度”选项卡](./media/financial-dimensions-cons.png "“财务维度”选项卡")

无论定义哪种顺序，**主科目** 始终是第一个科目段。

## <a name="legal-entities"></a>法人
在 **法人** 选项卡上，定义合并公司中应包含的公司。 也可以定义这些公司的所有权百分比。 如果指定的所有权低于 100%，将把指定的这个百分比汇总到合并公司。 对于任何折算差额，**折算差额的科目类型** 字段用于从 **自动交易记录科目** 页中的设置选择主科目。

![“法人”选项卡](./media/legal-entities-cons.png "“法人”选项卡")

![自动交易记录帐户页面](./media/accounts-for-automatic-cons.png "自动交易记录帐户页面")

## <a name="elimination"></a>清除
在 **清除** 选项卡上，有三个用于处理清除的选项：

- 设置清除规则，然后在 **方案选项** 字段中选择 **仅方案**。 此选项将在合并过程中处理清除，但是不会在一个步骤中进行所有过帐。 可以在以后过帐日记帐。
- 设置清除规则，然后在 **方案选项** 字段中选择 **仅过帐**。 此选项将在合并过程中处理清除，并将在一个步骤中进行所有过帐。
- 通过使用清除日记帐与合并过程分开运行清除方案。

![“清除”选项卡](./media/elimination-cons-onl.png "“清除”选项卡")

有关清除的详细信息，请参阅[清除规则](./elimination-rules.md)。

## <a name="currency-translation"></a>货币折算
在 **货币折算** 选项卡中，可定义法人、科目和汇率类型，以及汇率。 **应用来自以下对象的汇率** 字段中有三个选项：

- **合并日期** – 将把合并的日期用于获取汇率。 此汇率等同于即期汇率或月底汇率。 将看到汇率的预览，但是不能进行编辑。
- **交易记录日期**  – 每个交易记录的日期将用于选择汇率。 此选项最常用于固定资产，通常称为历史汇率。 不能查看此汇率的预览，因为科目范围的各交易记录有大量汇率。
- **用户定义的汇率** – 选择此选项之后，可以输入所需汇率。 此选项可能对于平均汇率很有用，如果要针对固定汇率进行合并，也可能很有用。

![“货币折算”选项卡](./media/currency-translation-cons-online.png "“货币折算”选项卡")

## <a name="additional-resources"></a>其他资源

有关合并和货币折算的详细信息，请参阅此主题的父主题，即[财务合并和货币折算概述](./financial-consolidations-currency-translation.md)。

有关可以生成财务报表的方案的信息，请参阅[生成合并的财务报表](./generating-consolidated-financial-statements.md)。
