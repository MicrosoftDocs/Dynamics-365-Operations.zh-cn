---
title: 记录 TDS 减免证书编号
description: 本文说明如何记录发放给供应商的从源扣缴税款 (TDS) 减免证书编号。
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
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846604"
---
# <a name="record-tds-concession-certificate-numbers"></a>记录 TDS 减免证书编号

[!include [banner](../includes/banner.md)]

本文说明如何记录发放给供应商的从源扣缴税款 (TDS) 减免证书编号。

1. 转到 **税务 \> 间接税 \> 预缴税金 \> 预缴税金减免**。
2. 在 **税务类型** 字段中，选择 **TDS** 以记录 TDS 税务类型的减免证书。
3. 在 **概述** 选项卡上，选择 **Alt+N** 以创建行。

    [![新行的标头。](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. 在 **预缴税金代码** 字段中，选择为其发放供应商减免证书的 TDS 税码。 **预缴税金代码名称** 字段显示 TDS 税码的名称。
5. 在 **开始日期** 和 **结束日期** 字段中，定义使用 TDS 税码基于减免计算供应商 TDS 的减免证书的有效期。
6. 在 **注解** 字段中，输入任何注解。
7. 在 **章节** 字段中，输入 TDS 减免证书可用的法律章节代码。

    如果章节代码为 197，表单 26Q 中的“非扣除/减低扣除的原因”列和表单 27Q 中的“非扣除/降低扣除/补偿费（如果有）的原因”列中均显示值“A”。 如果章节代码为 197A，这两个列中均显示值“B”。

8. 选择 **证书** 快速选项卡以记录供应商的 TDS 减免证书编号。
9. 在 **供应商帐户** 字段中，选择要为其发放 TDS 减免证书的供应商帐户。
10. 在 **开始日期** 和 **结束日期** 字段张，定义 TDS 减免证书的有效期。

    基于减免的 TDS 计算基于为供应商创建证书的期间。

11. 在 **证书** 字段中，输入 TDS 减免证书编号。

    [![证书快速选项卡。](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. 关闭该页面。
