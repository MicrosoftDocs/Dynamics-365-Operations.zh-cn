---
title: 为合并流程准备法人
description: 在合并过程中，您将来自若干法人帐户组的交易记录汇集到单组法人帐户中。 本主题说明如何为合并准备法人。
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a1ffbf79cdccab457b1aee1bc0f1d963bca49b3e390187c6be5da475f278a3d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720494"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>为合并流程准备法人

[!include [banner](../includes/banner.md)]

在合并过程中，您将来自若干法人帐户组的交易记录汇集到单组法人帐户中。 本主题说明如何为合并准备法人。

> [!NOTE]
> 我们建议您使用 Microsoft Dynamics 365 Finance 的 Management Reporter 以合并格式合并多个法人的财务结果。 通过 Management Reporter，您可以跨法人创建合并的财务报表，使用 Excel 从其他来源导入合并数据，并将金额转换为任意数量的报告货币，而无需在 Dynamics 365 Finance 中运行合并流程。

您可以从合并的法人打印报表，例如财务报表。 但是，您不能为每日交易记录使用合并的法人。

您可以合并使用与合并的法人不同数据库的法人的数据。 此合并过程称作 *导入合并*。 或者，法人实体可以将相同数据卡用作合并的法人。 此合并过程称作 *在线合并*。

合并的法人收集子公司的结果和余额。 若要为一个合并准备合并的法人，请执行以下步骤。

1. 转到 **总帐 \> 设置 \> 组织 \> 法人**。
2. 选择 **新建** 创建将成为合并的法人的法人。
3. 选中 **用于财务合并流程** 复选框，然后输入有关合并的法人的信息。 请确保输入与您希望出现在合并的法人的财务报表中的相同的信息。
4. 关闭该页面。
5. 在页面右上角的字段中选择合并的法人，然后选择 **确定**。
6. 转到 **总帐 \> 设置 \> 分类帐**。
7. 为合并的法人选择会计科目表、会计日历、记帐币种、一个可选申报币种和默认汇率类型。 
8. 转到 **总帐 \> 设置 \> 货币 \> 货币汇率**。
9. 为子公司法人的货币设置相关期间中的货币汇率。
10. 关闭该页面。
11. 如果合并的法人有使用外币的子公司，请按照以下步骤操作：

    1. 转到 **总帐 \> 设置 \> 过帐 \> 自动交易记录帐户**。
    2. 在 **过帐类型** 字段中，选择适当的科目：

        - 如果法人有在财务或运营上与母法人相互依赖的外国子公司，则为 **合并差异的损益科目** 过帐类型选择适当的科目。
        - 如果您合并财务和运营上从母法人独立的子公司，或包含财务和运营上从母法人独立的若干子公司的结果的法人，且如果您使用转换方法合并数据，则为 **合并差异的资产负债科目** 过帐类型选择适当的科目。

    3. 在 **主科目** 字段中，选择应用于外币重估调整的主科目。
    4. 关闭该页面。

    如果您在该期间的早期创建合并的法人，则您可以在合并期间汇率发生变化时，重估外币金额。

合并的法人现在为 **合并** 定期作业进行设置。 您可以执行导入合并或在线合并。

- 要进行导入合并，转到 **总帐 \> 定期 \> 合并 \> 合并\[导入来源\]**。
- 要进行在线合并，转到 **总帐 \> 定期 \> 合并 \> 合并\[在线\]**。

> [!NOTE]
> 在您可以处理合并前，必须准备用于合并的子公司法人。 有关详细信息，请参阅[设置要合并的子公司法人](set-up-subsidiary-company-for-consolidation.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]