---
title: 租赁终止方案
description: 本主题说明如何建议要终止的租赁。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ff3795f26ab10ac19cc3a0dd00dca65095118f45
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207295"
---
# <a name="propose-a-lease-for-termination"></a>建议要终止的租赁

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

如果租赁提前终止，“资产租赁”可以记录终止日记帐条目，以勾销租赁负债、使用权 (ROU) 资产和累计折旧，并计入损益。 提前终止流程将终止租赁及其关联的租赁帐簿。 不会终止单个租赁帐簿。 本主题介绍让您可以建议要终止的租赁并处理租赁终止日记帐条目的功能。

如果租赁未分类为延期租金处理租赁且未与固定资产关联，资产租赁将生成以下终止日记帐条目。

| 交易                           | 借记（借） | 贷记（贷） |
|---------------------------------------|-------------|--------------|
| 借记租赁负债                   | X           |              |
| 借记累计折旧          | X           |              |
| 借记租赁修改的损（益） | X           |              |
| 贷记租赁资产                       |             | X            |
| 贷记租赁修改的损（益） |             | X            |

如果租赁帐簿被分类为延期租金帐簿，条目会将终止之前延期租金的余额勾销到收益科目或损失科目，如此处所示。

| 交易                           | 借记（借） | 贷记（贷） | 
|---------------------------------------|-------------|--------------|
| 借记延期租金                     | X           |              |
| 贷记租赁修改的损（益） |             | X            |
| 贷记延期租金                     |             | X            |
| 借记租赁修改的损（益） | X           |              |

如果租赁帐簿连接到固定资产，使用权资产将计入固定资产。 此会计包括要提前终止的会计。 资产租赁生成以下日记帐条目以勾销租赁负债。

| 交易                           | 借记（借） | 贷记（贷） |
|---------------------------------------|-------------|--------------|
| 借记租赁负债                   | X           |              |
| 贷记租赁修改的损（益） |             | X            |

有关处置使用权资产的正确方法的信息，请参阅[将固定资产作为废料处置](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md)。

## <a name="propose-a-lease-for-termination"></a>建议要终止的租赁

1. 转到必须终止的租赁，然后在操作窗格上，选择 **终止方案**。

    > [!NOTE]
    > 如果针对任何帐簿有任何未过帐的日记帐条目，**终止方案** 按钮将不可用。 您必须先过帐或删除针对租赁创建的所有日记帐条目，然后才能够终止租赁。

2. 在出现的对话框中，为终止日记帐条目设置 **生效日期** 和 **过帐日期** 字段。
3. 选择 **终止方案** 可以建议要终止的租赁。
4. 选择 **过帐租赁终止** 可以自动过帐租赁终止日记帐条目。
5. 在 **租赁终止** 页上，选择您建议终止的租赁的租赁 ID 来查看终止行。 终止行显示使用权资产、租赁负债、累计折旧、延期租金（如果适用）以及在租赁终止时必须确认的损益的结转值。

租赁现在可以终止了。 租赁帐簿的 **终止状态** 字段的值将更改为 **可以终止**。 此时，您不能再针对该租赁过帐日记帐条目，也不能对其进行调整或减损。 

## <a name="process-leases-that-are-ready-for-termination"></a>处理准备好终止的租赁

要处理准备好终止的租赁并过帐终止日记帐条目，请按照下列步骤操作。

1. 在 **租赁终止** 页上，选择要处理的租赁，然后选择 **终止**。
2. 在显示的对话框中，选择 **确定**。

系统将过帐终止日记帐条目。 租赁帐簿的 **租赁状态** 字段将设置为 **已终止**，**终止方案状态** 字段将设置为 **已完成**。

## <a name="reverse-a-lease-termination"></a>冲销租赁终止

要冲销租赁终止日记帐条目并打开终止的租赁，请执行以下步骤。

- 在 **租赁终止** 页上，选择要冲销的终止的租赁，然后选择 **冲销终止**。

系统将冲销终止日记帐条目。 租赁帐簿的 **租赁状态** 字段将设置为 **打开**。 此租赁不会再出现在 **租赁终止** 页上，可以再次建议终止。

## <a name="example-of-a-lease-termination"></a>租赁终止示例

在此示例中，租赁与非专用资产关联，不会转移资产所有权或授予承租人购买资产的选择权。

### <a name="setup"></a>设置

下面的表显示了在 **常规** 和 **付款计划行** 选项卡中为此示例中使用的租赁设置的值。

**常规选项卡**

| 字段                      | 值            |
|----------------------------|------------------|
| 资产的公平价值    | 600,000          |
| 货币                   | USD              |
| 初始直接成本       | 1,000            |
| 增量借贷利率 | 7%               |
| 复合间隔       | 每年         |
| 资产使用年限(月数) | 600              |
| 年金类型               | 普通年金 |
| 开始日期          | 1/1/2019         |

**付款计划行选项卡**

| 字段             | 值      |
|-------------------|------------|
| 开始日期        | 1/1/2019   |
| 期间间隔   | 月度    |
| 期间           | 120        |
| 结束日期          | 12/31/2028 |
| 付款频率 | 每年   |
| 付款金额    | 10,000     |

### <a name="steps-for-terminating-the-lease"></a>终止租赁的步骤

1. 按照本主题前面所述创建租赁后，转到租赁帐簿，并确认付款计划。 然后过帐初始确认日记帐条目。 初始使用权资产为 71,235.81 美元，租赁负债应为 70,235.81 美元。 对于此示例，根据会计准则编纂专题 842 (ASC 842)，租赁被分类为经营性租赁。
2. 运行批处理日记帐流程三遍，模拟三年的租赁付款、利息费用和折旧费用过程。
3. 运行完所有三个批处理作业后，回到租赁帐簿，然后打开负债和资产交易表以查看使用权资产和租赁负债的当前帐面价值。 三年后，负债的价值应该为大约 -53,893.00 美元，资产的价值应该大约为 54,593.00 美元。

    三年过去后，企业和出租人相互同意终止租赁。 因此，您现在必须终止租赁。

4. 转到必须终止的租赁，然后在操作窗格上，选择 **终止方案**。 
5. 在出现的对话框中，在 **生效日期** 和 **过帐日期** 字段中，输入 **1/1/2021**。
6. 选择 **终止方案** 可以建议要终止的租赁。

    **租赁终止** 页将出现，显示将要终止的租赁。

7. 要查看终止行，选择您建议终止的租赁的租赁 ID。 终止行显示租赁的结转值。 下表显示了这些值在此示例中会呈现的值。 

    | 字段                                                 | 值      |
    |-------------------------------------------------------|------------|
    | 以交易货币表示的负债结转余额 | 53,892.89 美元 |
    | 以交易货币表示的使用权资产            | 71,235.81 美元 |
    | 以交易货币表示的累计折旧      | 16,642.92 美元 |
    | 以交易货币表示的损（益）                   | 700.00 美元   |

8. 要过帐终止日记帐条目，在 **租赁终止** 页上选择租赁，然后选择 **终止**。
9. 在显示的对话框中，选择 **确定**。
10. 要查看已创建并过帐的终止日记帐条目，转到租赁帐簿中资产的租赁日记帐。 下表显示了此条目在此示例中会呈现的样子。

    | 交易                           | 借记（借） | 贷记（贷） |
    |---------------------------------------|-------------|--------------|
    | 借记租赁负债                   | 53,892.89   |              |
    | 借记累计折旧          | 16,642.92   |              |
    | 借记租赁修改的损（益） | 700.00      |              |
    | 贷记租赁资产                       |             | 71,235.81    |

11. 要查看使用权资产和租赁负债为 0（零）的终止的实际影响，打开负债和资产交易表。

租赁状态现在应为 **已终止**。 除非终止被冲销，否则不会针对此租赁过帐其他日记帐条目。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]