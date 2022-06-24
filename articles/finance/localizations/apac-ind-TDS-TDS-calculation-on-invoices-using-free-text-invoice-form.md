---
title: 从普通发票页面中根据发票的 TDS 计算
description: 本文说明如何使用普通发票页面根据发票计算从源扣缴税款 (TDS)。
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
ms.openlocfilehash: b1cf0f5366315884e75a6fee25b88a3aac7d62de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856602"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>从普通发票页面中根据发票的 TDS 计算

[!include [banner](../includes/banner.md)]

本文说明如何使用 **普通发票** 页面根据发票计算从源扣缴税款 (TDS)。

1. 转到 **应收帐款 \> 发票 \> 所有普通发票**。

    [![普通发票页面。](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. 选择 **新建** 以创建普通发票，并输入所需的详细信息。
3. 选择 **发票** 选项卡。在 **预缴税金组** 部分中，**评估对象的性质** 字段显示客户的评估对象类别的性质。
4. 在 **TDS 组** 字段中，查看或更改为客户定义的默认 TDS 组。

    > [!NOTE]
    > 当在 **TDS 组** 字段中选择值时，**TCS 组** 字段变得不可用。 仅在 **所有客户** 页面上为客户将 **计算预缴税金** 选项设置为 **是** 时，才计算 TDS。

5. 在 **税务信息** 选项卡的 **公司信息** 部分中，在 **名称** 字段中，针对已为公司设置的备用地址选择公司名称。

    在 **预缴税金** 部分中，**税务帐号 (TAN)** 字段显示选定公司的税务帐号 (TAN)。

6. 在 **发票行** 选项卡上，创建发票行，然后输入所需的详细信息。

    在 **预缴税金组** 部分中，**税务帐号 (TAN)** 字段显示 TAN，**TDS 组** 字段显示 TDS 组。

7. 选择 **预缴税金** 以打开 **临时预缴税金交易** 页面。 此页面的上部具有以下字段：

    - **预缴税金总金额** – 已为 TDS 组的交易计算的总 TDS。
    - **值** – 已用于计算交易的 TDS 的总百分比。 总百分比基于为 TDS 税码定义和附加到 TDS 组的公式。
    - **调整后预缴税金总金额** – TDS 组中所有税码的调整后 TDS 总金额。
    - **TDS** – 选中的复选框指示 TDS 组已附加到交易。

    **概述**、**常规** 和 **调整** 选项卡上的字段为附加到 TDS 组的每个 TDS 税码显示计算的 TDS 金额和调整的 TDS 金额详细信息。

8. 选择 **阈值** 以打开 **阈值** 页面，您可以在该页面中查看为附加到特定 TDS 税码的 TDS 税种组分定义的阈值限制。
9. 选择 **公式设计器** 以打开 **公式设计器** 页面，您可以在该页面中查看为特定 TDS 税码定义的公式。
10. 过帐普通发票。 为普通发票计算的 TDS 金额将过帐到为 TDS 组中每个 TDS 税码定义的应收帐款。 TDS 税码的应收帐款在 **预缴税金代码** 页面上定义。
11. 选择 **过帐的预缴税金** 以打开 **预缴税金交易** 页面。 **值** 字段显示用于计算交易的 TDS 的总百分比。

    **概述**、**常规** 和 **金额** 选项卡上的字段显示已针对发票行计算的 TDS 金额。

12. 查看附加到 TDS 组的每个 TDS 税码的 TDS 计算信息。
