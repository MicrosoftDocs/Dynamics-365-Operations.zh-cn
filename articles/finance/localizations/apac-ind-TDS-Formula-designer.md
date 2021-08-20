---
title: TDS 计算的公式设计器
description: 本主题提供了如何基于为附加到交易的 TDS 组中每个 TDS 税码定义的公式计算从源扣缴税款 (TDS) 的示例。
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
ms.openlocfilehash: e9c97982233b1f3dc3924fa42954b5cb8d09ffcaa07d19a3892b25737a6c29c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778861"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS 计算的公式设计器

[!include [banner](../includes/banner.md)]

本主题提供了如何基于为每个 TDS 税码定义的公式计算从源扣缴税款 (TDS) 的示例。 TDS 税码在附加到交易的 TDS 组中定义。 在设计 TDS 公式之前，请完成 TDS 所需的基本设置，如以下步骤所示。 

- 使用 **预缴税金组分组** 页面设置 TDS 组分组。 
- 使用 **预缴税金组分** 页面设置 TDS 组分，并将 TDS 组分组附加到 TDS 组分。 
- 使用 **预缴税金代码** 页面设置 TDS 税码，并将 TDS 组分附加到 TDS 税码。 
- 使用 **预缴税金组** 页面设置 TDS 税组。 然后，使用 **公式设计器** 页面将 TDS 税码附加到税组，并定义公式。 

**公式示例**

在此示例中，TDS 组“租金”将附加到为供应商 A 创建的采购发票。发票金额为 $100,000。 请参考下表以查看发票的 TDS 计算。

| TDS 组                                                   | 已附加到 TDS 组的 TDS 税码 | 值              | 应纳税基数（公式设计器） | 计算表达式（公式设计器） | 基准额 | 计算的 TDS 金额 |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| 租金                                                         | TDS（TDS 组分-TDS）                | 10%                | 总额                      |                                            | 100,000      | 10,000                 |
| 附加费（TDS 组分-附加费）                         | 10%                                     | 不含总额 | +TDS                              |                   10000                    | 1,000        |                       |
| PE-Cess（TDS 组分-PE-Cess）                            | 2%                                      | 不含总额 | +TDS+附加费                    |                   11000                    | 220         |                       |
| SHE Cess（TDS 组分-SHE Cess）                          | 1%                                      | 不含总额 | +TDS+附加费                    |                   11000                    | 110         |                       |
| **针对发票计算的总 TDS** | **11,330**                               |                    |                                   |                                            |             |                       |

创建凭证条目，如下所示。

| 科目           | 借记  | 信用 |
| ----------------- | ------ | ------ |
| 租金              | 100,000 |        |
| 供应商 A          |        | 100,000 |
| 供应商 A          | 11,330  |        |
| 应付 TDS       |        | 10,000  |
| 应付附加费 |        | 1,000   |
| 应付 PE-Cess   |        | 220    |
| 应付 SHE Cess  |        | 110    |
