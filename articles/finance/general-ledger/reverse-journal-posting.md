---
title: 冲销日记帐过帐
description: 此主题介绍用于冲销凭证交易记录列表中或财务日记帐中的凭证的功能。
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248577"
---
# <a name="reverse-journal-posting"></a>冲销日记帐过帐

[!include [banner](../includes/banner.md)]

此主题介绍用于冲销整个日记帐或冲销凭证交易记录列表中的一个或多个凭证（而不考虑其来源）的 Microsoft Dynamics 365 Finance 功能。 

## <a name="reversing-journals"></a>冲销日记帐

可分别冲销日记帐行。 通过冲销日记帐过帐，也可以冲销整个财务日记帐。 若要冲销日记帐： 
- 打开财务日记帐并筛选过帐的日记帐
- 单击页面顶部的“冲销”菜单
- 将看到凭证总数和凭证行，以及正在冲销的行的总量
- 如果选择“是”，则使用现有交易记录日期，如果选择“否”，则输入新交易记录日期。 在某些情况下，原始交易记录的期间可能已关闭，您希望为冲销输入新的交易记录日期。
- 如果选择“否”，请为冲销输入交易记录日期。 
- 输入要添加到冲销交易记录的注释
- 单击“冲销”按钮

将冲销交易记录。 

如果凭证行数量超过 100 行，则将使用批处理流程运行冲销流程。 可通过查看运行的批处理作业中的注释，查看冲销结果。 将把所有失败记录到批处理作业历史记录中。

如果凭证行数量为 100 行或更少，将立即运行冲销流程。 将在对话框中提供结果，其中显示不能冲销的所有凭证和不能冲销的原因。 单击“确定”关闭该对话框。

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>冲销凭证交易记录列表中的凭证。 

也可以重新所有子分类帐的**凭证交易记录列表**中的凭证。 此外，还可以同时冲销多个凭证。 

若要冲销一个或多个凭证： 
- 单击页面顶部的“冲销”菜单
- 将看到凭证总数和凭证行，以及正在冲销的行的总量
- 如果选择“是”，则使用现有交易记录日期，如果选择“否”，则输入新交易记录日期。 在某些情况下，原始交易记录的期间可能已关闭，您希望为冲销输入新的交易记录日期。
- 如果选择“否”，请为冲销输入交易记录日期。 
- 输入要添加到冲销交易记录的注释
- 单击“冲销”按钮

将冲销交易记录。 

如果凭证行数量超过 100 行，则将使用批处理流程运行冲销流程。 可通过查看运行的批处理作业中的注释，查看冲销结果。 将把所有失败记录到批处理作业历史记录中。

如果凭证行数量为 100 行或更少，将立即运行冲销流程。 将在对话框中提供结果，其中显示不能冲销的所有凭证和不能冲销的原因。 单击“确定”关闭该对话框。

