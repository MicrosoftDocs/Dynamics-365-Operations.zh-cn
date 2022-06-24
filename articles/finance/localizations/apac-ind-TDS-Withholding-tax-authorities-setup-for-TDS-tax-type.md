---
title: 设置 TDS 税务类型的预缴税金主管机构
description: 本文说明如何设置从源扣缴税款 (TDS) 主管机构。
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
ms.openlocfilehash: 43562381bab93d2f143788b8dc61f2b13d05db3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864204"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>设置 TDS 税务类型的预缴税金主管机构

[!include [banner](../includes/banner.md)]

本文说明如何设置从源扣缴税款 (TDS) 主管机构。

1. 转到 **税 \> 间接税 \> 预缴税金主管机构**。

    [![预缴税金主管机构页面。](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)

2. 在 **税务类型** 字段中，选择 **TDS** 为 TDS 税务类型设置预缴税金主管机构。
3. 在“操作窗格”中，选择 **新建** 创建一行。
4. 在 **预缴税金主管机构** 字段中，为 TDS 主管机构输入名称。
5. 在 **描述** 字段中，输入描述。
6. 在 **常规** 快速选项卡上，在 **供应商帐户** 字段中，选择 TDS 主管机构的供应商帐户。

    > [!NOTE]
    > 您必须定义欠 TDS 主管机构供应商的资金将存入的银行的名称。 银行的名称在 **银行帐户** 页（**应付帐款 \> 所有供应商 \> 供应商 \> 设置 \> 银行帐户**）上定义。

7. 关闭该页面。
