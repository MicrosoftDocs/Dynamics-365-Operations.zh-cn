---
title: 付款确认概览
description: 本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: thweeloc
ms.custom:
- "88463"
- intro-internal
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: f25dfaaa2e52b58c7b6971b4d277ef315de431a0
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715740"
---
# <a name="positive-pay-overview"></a>付款确认概览

[!include [banner](../includes/banner.md)]

本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。 

付款确认用于生成一份可以呈现给银行的支票电子列表。 付款确认文件可以帮助银行防止支票欺诈。 每次打印支票时，您设置付款确认以生成支票电子列表。 然后，当将支票提交给银行时，银行将支票与您以前提交的支票列表进行对比。 如果支票与列表中的支票相匹配，银行将清算支票。 如果支票与列表中的支票不匹配，银行将保留支票以供审查。

付款确认也称为 SafePay。 

付款确认文件可以包含有关收款人和支票金额的敏感信息。 因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。 付款确认文件根据 Web 浏览器的下载说明下载。 

通过使用数据实体创建付款确认文件。 在您生成付款确认文件前，必须为将数据转换为银行可以使用的格式的 XML 设置转换格式。 

对于您想要生成付款确认信息的每个银行帐户，您必须分配付款确认格式。 在生成付款后，您可以生成用于一个法人和一个银行帐户的付款确认文件。 或者，您可以同时为多个法人和银行帐户生成付款确认文件 

当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。 然后，您可以在系统中确认付款确认文件。 

如果您必须更改付款确认文件，您可以撤消它。 然后，对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。

有关详细信息，请参阅[设置和生成先对单再支付文件](set-up-generate-positive-pay-files.md)。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
