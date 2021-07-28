---
title: 为 TDS 税务类型设置税种组分
description: 本主题说明如何为从源扣缴税款 (TDS) 税务类型设置预缴税金组分。 它还说明如何定义用于计算每个 TDS 组分的 TDS 的阈值限制。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 70e57a928ecd3f5d10ebd3d0fc3f52870d40fcd9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358162"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>为 TDS 税务类型设置税种组分

[!include [banner](../includes/banner.md)]

本主题说明如何为从源扣缴税款 (TDS) 税务类型设置预缴税金组分。 TDS 组分是 TDS、附加费、PE-Cess 和 SHE Cess。 本主题还说明如何定义用于计算每个 TDS 组分的 TDS 的阈值。 此外，您可以定义一个异常阈值，用于计算每个 TDS 组分的 TDS。

按照以下步骤设置 TDS 组分。

1. 转到 **税务 \> 设置 \> 预缴税金 \> 预缴税金组分**。

    [![预缴税金组分页面。](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. 在 **税务类型** 字段中，选择 **TDS** 以为 TDS 税务类型设置预缴税金组分。
3. 在“操作窗格”中，选择 **新建** 创建一行。
4. 在 **预缴税金组分** 字段中，为 TDS 组分输入名称。
5. 在 **预缴税金组分组** 字段中，选择 TDS 组分要附加到的 TDS 预缴税金组分组。
6. 在 **常规** 快速选项卡上，在 **描述** 字段中，输入 TDS 组分的描述。
7. 在操作窗格上，选择 **阈值** 以打开 **阈值** 页面，以便您可以定义用于为 TDS 组分计算 TDS 的阈值。
8. 使用 **开始日期** 和 **结束日期** 字段定义阈值适用的期间。
9. 在 **常规** 快速选项卡上，在 **阈值** 字段中，输入用于为 TDS 组分计算 TDS 的阈值金额。 仅在累计发票金额超过阈值时，才从源扣除税款。

    例如，如果阈值金额为 10,000，则在累计发票金额超过 10,000（换言之，当金额为 10,001 或更高）后计算 TDS。

10. 在 **异常阈值** 字段中，输入用于为 TDS 组分计算 TDS 的异常阈值金额。 仅在金额超过异常阈值时，才从源扣除发票行上的税款。

    例如，如果异常阈值金额为 5,000，则如果发票行金额超过 5,000（换言之，如果金额为 5,001 或更高），将根据特定发票行计算 TDS。

    [![阈值页面。](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > 异常阈值金额必须小于或等于阈值金额。
    >
    > 如果交易金额超过异常阈值，即使累计发票金额未超过在 **阈值** 字段中指定的阈值，也扣除交易的税款。

11. 关闭 **阈值** 页面以返回到 **预缴税金组分** 页面。
12. 在操作窗格上，选择 **复制** 以打开 **复制预缴税金组分** 对话框，以便您可以将为一个 TDS 组分组设置的 TDS 组分复制到另一个 TDS 组分组。
13. 在 **从** 字段中，选择要从中复制 TDS 组分的 TDS 组分组。 在 **至** 字段中，选择要将 TDS 组分复制到的预缴税金组分组。

    > [!NOTE]
    > 不复制附加到这两个 TDS 组分组的常见 TDS 组分。

14. 选择 **确定** 以在 **预缴税金组分** 页面上为其他 TDS 组分组复制和创建 TDS 组分。

    [![复制预缴税金组分对话框。](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. 关闭该页面。
