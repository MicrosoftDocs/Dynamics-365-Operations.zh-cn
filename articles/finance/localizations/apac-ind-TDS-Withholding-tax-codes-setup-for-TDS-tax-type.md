---
title: 设置 TDS 税务类型的预缴税金代码
description: 本主题说明如何设置从源扣缴税款 (TDS) 的税代码。
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
ms.openlocfilehash: add91eaef2ad091df7fd45e3de2dfe3993e6d62fdcbbcfcf95a7fc4953189239
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754871"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>设置 TDS 税务类型的预缴税金代码

[!include [banner](../includes/banner.md)]

本主题说明如何设置从源扣缴税款 (TDS) 的税代码。

1. 转到 **税 \> 间接税 \> 预缴税金 \> 预缴税金代码**。

    [![预缴税金代码页面。](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. 在操作窗格上，选择 **新建** 为 TDS 创建预缴税金代码，然后输入所需的详细信息。
3. 在 **常规** 快速选项卡上，在 **税务类型** 字段中，选择 **TDS** 将税代码分类为 TDS 税代码。
4. 在 **结算期间** 字段中，选择 TDS 税代码的 TDS 结算期间。
5. 在 **主科目** 字段中，选择应将 TDS 金额过帐到的会计科目。
6. 在 **应收帐款** 字段中，选择应将销售交易中扣除的 TDS 金额过帐到的应收帐款。

    **源** 字段将自动设置为 **总额百分比**，此值无法更改。

    > [!NOTE]
    > 对于 TDS 税务类型的税代码，不能将来源设置为 **净额百分比**。

7. 在 **预缴税金组分** 字段中，选择 TDS 税代码的 TDS 税种组分。
8. 在操作窗格上，选择 **值** 打开 **预缴税金值** 页。
9. 在 **开始日期** 字段中，输入 TDS 值的开始日期。 在 **结束日期** 字段中，输入结束日期。

    > [!NOTE]
    > **下限**、**上限** 和 **排除 %** 字段对 TDS 税务类型的税代码不可用。

10. 在 **值** 字段中，输入 TDS 税代码的 TDS 百分比。
11. 关闭 **预缴税金值** 页返回 **预缴税金代码** 页。

    > [!NOTE]
    > **预缴税金代码** 页上的 **限额** 按钮对 TDS 税务类型的税代码不可用。

12. 关闭该页面。
