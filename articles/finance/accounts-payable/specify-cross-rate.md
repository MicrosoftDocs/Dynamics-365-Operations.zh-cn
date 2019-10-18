---
title: 指定交叉汇率
description: 此主题提供有关 Microsoft Dynamics 365 Finance 中交叉汇率的一般信息。
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 146794557a3a6ba1801598fe6b814e209d9f5fc6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176665"
---
# <a name="specify-the-cross-rate"></a>指定交叉汇率

[!include [banner](../includes/banner.md)]

本主题说明了交叉汇率的目的，以及当您使用发票结算付款时如何指定交叉汇率。 在适用以下所有条件时使用交叉汇率： 
-   您正在使用发票结算付款。 
-   付款行和发票行使用不同币种。 
-   两种货币均不是记帐币种。 

交叉汇率不用于计算付款交易记录币种与付款记帐币种之间的转换。 而是检索汇率表中的汇率以计算付款交易记录币种金额和付款记帐币种金额的值。 

例如，记帐币种是 USD，发票币种是 CAD，而付款币种是 EUR。 交叉汇率使得您可以输入汇率直接在 CAD 和 EUR 之间换算而不需要通过 USD 为单位来转换。 在您选择某一发票和主付款时，可为该发票行输入交叉汇率。 交叉汇率是截止到结算日期时这些交易记录的币种之间的汇率。

1.  访问以下页面之一：
- **应收帐款 > 通用 > 客户 > 所有客户** 
- **应付帐款 > 通用 > 供应商 > 所有供应商** 
- **采购 > 通用 > 供应商 > 所有供应商**
2.  选择您要结算其未结交易记录的客户或供应商。 
3.  对于客户，在**所有客户**列表页上，转至**催款 > 结算未结交易记录**。 对于供应商，则在**所有供应商**列表页上，转至**发票 > 结算未结交易记录**。 
4.  选择作为主付款的交易记录，然后单击**标记付款**。 **标记**列中的复选框被选中，并且在**主付款**列中将出现信息图标。 
5.  在**交叉汇率**字段中，输入截止到结算日期时发票币种和付款币种之间的汇率倍数。 
