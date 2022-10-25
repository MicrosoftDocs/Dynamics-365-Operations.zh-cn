---
title: 冲销日记帐过帐
description: 本文介绍用于冲销凭证交易记录列表中或财务日记帐中的凭证的功能。
author: kweekley
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.form: LedgerTransVoucher, LedgerJournalTable
ms.openlocfilehash: 8912409ec0d2016ea4af12843319febda98663c5
ms.sourcegitcommit: e700528679a821237e644b3e21058c36ae1323c3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2022
ms.locfileid: "9680376"
---
# <a name="reverse-journal-posting"></a>冲销日记帐过帐

[!include [banner](../includes/banner.md)]

本文介绍用于冲销整个日记帐或冲销凭证交易记录列表中的一个或多个凭证（而不考虑其来源）的 Microsoft Dynamics 365 Finance 功能。 

在使用本文介绍的功能之一之前，必须在系统中将其打开。 管理员可以使用 **功能管理** 工作区检查功能状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：
 - 模块：总帐
 - 功能名称：**批量冲销多张单据**

## <a name="reversing-journals"></a>冲销日记帐

可分别冲销日记帐行。 通过冲销日记帐过帐，也可以冲销整个财务日记帐。 若要冲销日记帐： 

- 筛选已过帐日记帐，然后打开日记帐的 **行** 视图。
- 选择页面顶部的 **冲销整个日记帐** 菜单。
- 将看到凭证总数和凭证行，以及正在冲销的行的总量。
- 如果选择 **是**，则使用现有交易记录日期，如果选择 **否**，则输入新交易记录日期。 在某些情况下，原始交易记录的期间可能已关闭，您必须为冲销输入新的交易记录日期。
- 如果选择 **否**，请为冲销输入交易记录日期。 
- 输入要添加到冲销交易记录的注释。
- 选择 **冲销** 按钮。

将冲销交易记录。 

如果凭证包含超过 100 行，则将使用批处理流程运行冲销流程。 可通过查看批处理作业中的注释查看结果。 无法冲销的所有交易记录都将在批处理作业历史记录中列出。

如果凭证包含 100 行或更少，将立即运行冲销流程。 将在对话框中提供结果，其中显示不能冲销的所有凭证，以及不能冲销的原因。 选择 **确定** 关闭对话框。

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a>冲销凭证交易记录列表中的凭证。 

也可以重新所有子分类帐的 **凭证交易记录列表** 中的凭证。 此外，还可以同时冲销多个凭证。 

若要冲销一个或多个凭证： 

- 选择页面顶部的 **冲销整个日记帐下拉列表** 菜单。
- 将显示凭证总数和凭证行，以及正在冲销的行的总量。
- 如果选择 **是**，则使用现有交易记录日期，如果选择 **否**，则输入新交易记录日期。 在某些情况下，原始交易记录的期间可能已关闭，您必须输入新的交易记录日期来冲销它。
- 如果选择 **否**，请为冲销输入交易记录日期。 
- 输入描述冲销交易的注释。
- 选择 **冲销** 按钮。

将冲销交易记录。 

如果有超过 100 个凭证行，则将使用批处理流程运行冲销流程。 可通过查看批处理作业中的注释查看结果。 无法冲销的所有交易记录都将在批处理作业历史记录中记录。

如果凭证行数量为 100 行或更少，将立即运行冲销流程。 将在对话框中显示结果，其中显示不能冲销的所有凭证，以及原因。 选择 **确定** 关闭对话框。

仅当交易记录符合进行冲销的业务规则时，才可以冲销交易记录。 使用本文中介绍的功能无法撤销供应商付款。 必须按照[冲销供应商付款](../accounts-payable/reverse-vendor-payment.md)中列出的步骤来冲销供应商付款。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
