---
title: 将 TDS 税码附加到 TDS 税组并定义用于计算 TDS 的公式
description: 本文说明如何设置从源扣缴税款 (TDS) 税组以及将 TDS 税码附加到 TDS 税组。 若要计算 TDS 税组的 TDS，必须定义附加到它的 TDS 税码的公式。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3607e44bdcf7a32b156e6b4639ef907aa923cadc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853305"
---
# <a name="attach-tds-tax-codes-to-tds-tax-groups-and-define-the-formula-for-calculating-tds"></a>将 TDS 税码附加到 TDS 税组并定义用于计算 TDS 的公式

[!include [banner](../includes/banner.md)]

本文说明如何设置从源扣缴税款 (TDS) 税组以及将 TDS 税码附加到 TDS 税组。 若要计算 TDS 税组的 TDS，必须定义附加到它的 TDS 税码的公式。

按照以下步骤设置 TDS 税组，将 TDS 税码附加到它，并定义用于计算 TDS 的公式。

1. 转到 **税务 \> 间接税 \> 预缴税金 \> 预缴税金组**。

    [![预缴税金组页面。](./media/apac-ind-TDS-29.png)](./media/apac-ind-TDS-29.png)

2. 在操作窗格上，选择 **新建** 以为 TDS 创建预缴税金组，然后输入所需的详细信息。
3. 在 **税务类型** 字段中，选择 **TDS**。
4. 在 **设置** 快速选项卡上，选择 **添加** 以创建行。
5. 在 **预缴税金代码** 字段中，选择 TDS 税组的 TDS 税码。 **预缴税金名称** 字段显示 TDS 税码的名称，**值** 字段显示值。
6. 若要忽略为附加到 TDS 交易中 TDS 税码的 TDS 税种组分定义的阈值限制和异常阈值限制，请选中 **忽略阈值** 复选框。
7. 若要阻止在交易中计算税组，请选中 **免税** 复选框。
8. 在操作窗格上，选择 **设计器** 以打开公式设计器，以便您可以定义用于计算 TDS 税组的 TDS 的公式。 在 **设计器** 页面上，**税务** 选项卡显示已为 TDS 税组选择的 TDS 税码。

    [![设计器页面。](./media/apac-ind-TDS-30.png)](./media/apac-ind-TDS-30.png)

9. 在 **计算** 选项卡上，选择 **Alt+N** 以创建行。 **ID** 字段显示 TDS 计算的自动生成的优先级 ID。
10. 在 **税码** 字段中，选择要为其定义公式的 TDS 税码。 可在字段中选择已为 TDS 税组选择的所有 TDS 税码。
11. 在 **应纳税基数** 字段中，选择用于计算 TDS 的基数：

    - **总额** – 使用为税码定义的计算表达式，基于交易总额（即发票金额）计算 TDS。
    - **不含总额** – 基于为税码定义的计算表达式计算 TDS。

    > [!NOTE]
    > 对于优先级 ID 为 **1** 的 TDS 税码，**应纳税基数** 字段不能设置为 **不含总额**。

12. TDS 计算基于在 **计算表达式** 字段中为附加到 TDS 税组的每个税码定义的公式。 选择加号 (+)、减号 (-)、乘号 (\*) 或除号 (/) 按钮，在 **计算表达式** 字段中输入选定 TDS 税码的计算表达式。

    > [!NOTE]
    > 针对优先级 ID 为 **1** 的 TDS 税码，不定义任何计算表达式。

13. 若要在 **计算表达式** 字段中定义 TDS 税码的计算表达式，请添加在 **税务** 选项卡上提供的 TDS 税码。若要在 **计算表达式** 字段中添加 TDS 税码，您可以使用以下任何方法：

    - 将所需税码从 **税务** 选项卡拖动到 **计算表达式** 字段。
    - 两次点击（或双击）**税务** 选项卡上的所需税码。
    - 选择并按住（或右键单击）**税务** 选项卡上的所需税码，然后选择 **添加税码**。

    > [!NOTE]
    > 在每个 TDS 税码之前插入计算表达式。 已添加到计算表达式的 TDS 税码显示在方括号 (\[...\]) 中。

14. 若要清除在 **计算表达式** 字段中为税码定义的计算表达式，请选择 **C** 按钮。
15. 若要删除 **计算** 选项卡上的记录，请选择 **删除**。
16. 关闭该页面。
