---
title: 设置要合并的子公司法人
description: 本主题说明如何使用合并公司的会计科目表。
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
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: fbec5ad8fa5e17b75859c07ee64a66c9568c97d3d18b6a7616a64303d3a33f10
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6727951"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>设置要合并的子公司法人

[!include [banner](../includes/banner.md)]

您准备用于合并的子公司帐户的方法取决于，一部分，在何种程度上结构在子公司中法人在合并法人中反映的会计科目表。

在开始合并作为关闭期间结束之前，完成该期间结束关闭执行准备性活动，但在合并完成前不关闭子公司帐户。 有关期间结束关闭的详细信息，请参阅[在期间结束时关闭总帐](close-general-ledger-at-period-end.md)和[关帐会计年度](tasks/close-fiscal-year.md)。

> [!NOTE]
>  我们建议您使用 Microsoft Dynamics 365 Finance 的 Management Reporter 以合并格式合并多个法人的财务结果。 通过 Management Reporter，您可以跨法人创建合并的财务报表，使用 Excel 从其他来源导入合并数据，并将金额转换为任意数量的报告货币，而无需在 Dynamics 365 Finance 中运行合并流程。

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>将子公司主科目映射到合并主科目

如果会计科目表在子公司中的法人不遵循在合并的法人会计科目表，则映射在子公司中的主帐户到在合并法人的主科目。

1. 在 *子公司法人* 中，转到 **总帐 \> 设置** \> **会计科目表 \> 会计科目表**。
2. 选择某一会计科目表。 在 **主科目** 快速选项卡上，选择一个主科目，然后选择 **编辑**。
3. 选择必须映射到合并的主科目的每个子公司主科目。 在 **常规** 快速选项卡上，在 **合并科目** 字段中，输入所选子公司主科目必须将余额或交易记录转移到的合并法人中的科目。 您可以输入若干子公司科目的相同的合并主科目。

    > [!NOTE]
    > 如果映射的子公司科目的主科目类型与合并法人中的科目的主科目类型不同，则具有 **总计** 主科目类型的科目值将在合并期间被覆盖。

4. 为合并法人准备基于财务维度的报表和财务报表。 请按照以下步骤将子公司科目中使用的财务维度映射到合并法人中的财务维度：

    1. 在 *子公司法人* 中，转到 **总帐 \> 设置 \> 财务维度 \> 财务维度**，选择一个财务维度，然后选择 **财务维度值**。
    2. 选择财务维度值以映射到合并法人中不同的财务维度值。
    3. 在 **常规** 快速选项卡上，在 **组维度** 字段中，在合并的法人中输入财务维度。 在合并期间，此财务维度将分配给在子公司法人中使用所选财务维度的交易记录和余额。 在此处输入的财务维度必须在合并的法人中使用。 您可以分配将用作为若干子公司财务维度的财务维度组的财务维度。

5. 如果您要进行在线合并，请按照以下步骤确保转移按预期进行：

    1. 在 *合并的法人* 中，转到 **总帐 \> 定期 \> 合并 \> 合并\[导出目标\]** 打开 **合并\[在线\]** 页。
    2. 在 **条件** 选项卡上，选中 **使用合并科目** 复选框。
    3. 在 **财务维度** 选项卡上，选择适当的财务维度。
    4. 对于所选的每个财务维度，请在 **段顺序** 字段中输入数字指示维度显示应该遵循的顺序。

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>在子公司和合并的法人中维护相同的会计科目表

主科目在合并的法人中时，主科目在子公司中法人可能会具有相同帐号和相同的会计科目表的结构。 在此情况下，您不必手动映射子公司中的主科目到合并的法人主科目。

在开始合并之前，请执行以下步骤。

1. 在 *合并的法人* 中，转到 **总帐 \> 定期 \> 合并 \> 合并\[导出目标\]** 打开 **合并\[在线\]** 页。
2. 选中 **使用合并科目** 复选框。 在合并期间，交易记录和余额将自动转移到正确的科目。

> [!NOTE]
> 如果科目不符，则合并将停止，并且系统将显示一条消息。

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>基于现有会计科目表创建合并的法人的会计科目表

即使尚未在合并的法人中创建会计科目表，您也可以执行合并。

- 如果您计划希望在合并的法人中使用的科目结构，您可以将子公司科目映射到此结构。
- 如果您没有任何子公司科目映射，则在子公司数据转移到合并时法人，科目将在合并的法人中自动创建。 这些科目基于主科目。 随后的数据合并的法人中累计和子公司科目具有相同的科目编号。

不论您是否映射了这些科目，在运行此类合并前，请在合并法人中的 **合并** 页上清除 **使用合并科目** 复选框。

> [!NOTE]
> 您可以使用从子公司法人的会计科目表之一的方法，在合并法人中创建会计科目表。 （有关详细信息，请参阅[合并科目组和其他合并科目](../budgeting/consolidation-account-groups-consolidation-accounts.md)。）然后将相应的合并转换原则分配给各合并主科目，并且为所有子公司法人运行合并。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]