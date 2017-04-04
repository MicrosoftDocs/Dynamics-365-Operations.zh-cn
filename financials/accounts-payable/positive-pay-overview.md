---
title: "付款确认概览"
description: "本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 1fd606817b06a05b9abaaedf20ea9872bd7edd5d
ms.openlocfilehash: cb4806a1f023c1e60311ff9d8facb4ef5717ad94
ms.lasthandoff: 03/31/2017


---

# <a name="positive-pay-overview"></a>付款确认概览

本文提供有关付款确认的信息，其用于生成一份可以呈现给银行的支票电子列表。 

付款确认用于生成一份可以呈现给银行的支票电子列表。 付款确认文件可以帮助银行防止支票欺诈。 每次打印支票时，您设置付款确认以生成支票电子列表。 然后，当将支票提交给银行时，银行将支票与您以前提交的支票列表进行对比。 如果支票与列表中的支票相匹配，银行将清算支票。 如果支票与列表中的支票不匹配，银行将保留支票以供审查。

付款确认也称为 SafePay。 

付款确认文件可以包含有关收款人和支票金额的敏感信息。 因此，请您务必自文件生成时便使用相应的安全措施，直到它们由银行接收。 付款确认文件根据 Web 浏览器的下载说明下载。 

通过使用数据实体创建付款确认文件。 在您生成付款确认文件前，必须为将数据转换为银行可以使用的格式的 XML 设置转换格式。 

对于您想要生成付款确认信息的每个银行帐户，您必须分配付款确认格式。 在生成付款后，您可以生成用于一个法人和一个银行帐户的付款确认文件。 或者，您可以同时为多个法人和银行帐户生成付款确认文件 

当付款确认文件中列出的支票支付后，您将从银行收到一个确认编号。 您在 Microsoft Dynamics 365 中可以将工资单文件确认 (操作。 

如果您必须更改付款确认文件，您可以撤消它。 然后，对于付款确认文件中的每一张支票，将重置指示该支票是否包括在一个付款确认文件中的字段。

有关详细信息，请参阅和正设置 [则生成工资单文件] (正设置生成付薪 files.md)。


