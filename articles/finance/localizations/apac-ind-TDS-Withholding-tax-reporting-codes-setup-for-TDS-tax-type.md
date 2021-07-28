---
title: 设置 TDS 税务类型的预缴税金申报代码
description: 预缴税金申报代码用于为从源扣缴税款 (TDS) 生成表格 26Q 和表格 27Q 报表。 本主题说明设置预缴税金申报代码的步骤，让您可以设置 TDS 申报代码。
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
ms.openlocfilehash: c74132af95f088ea88155b722a8270861fba50e7
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361278"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>设置 TDS 税务类型的预缴税金申报代码

[!include [banner](../includes/banner.md)]

预缴税金申报代码用于为从源扣缴税款 (TDS) 生成表格 26Q 和表格 27Q 报表。 本主题说明设置预缴税金申报代码的步骤，让您可以设置 TDS 申报代码。

1. 转到 **税 \> 设置 \> 预缴税金 \> 预缴税金申报代码**。

    [![预缴税金申报代码页面。](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. 在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型定义预缴税金申报代码。
3. 在 **预缴税金组分** 字段中，选择要为其定义预缴税金申报代码的 TDS 组分。 **预缴税金组分组** 字段显示为您要定义的 TDS 组分定义的 TDS 组分组。

    **常规** 快速选项卡上的 **地区代码** 字段显示附加到 TDS 组分组的地区代码。

4. 在 **常规** 快速选项卡上，在 **申报代码** 字段中，选择 TDS 申报代码：

    - TDS
    - TCS
    - 附加费
    - PE\_Cess
    - SHE\_Cess

5. 关闭该页面。
