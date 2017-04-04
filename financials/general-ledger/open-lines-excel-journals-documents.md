---
title: "过帐日志行和文档从 Excel"
description: "本主题说明如何输入和过帐普通记帐日志中的行将从 Microsoft Excel。 它根据您输入的交易记录类型包括与您可以使用的不同，模板的信息。"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>过帐日志行和文档从 Excel

本主题说明如何输入和过帐普通记帐日志中的行将从 Microsoft Excel。 它根据您输入的交易记录类型包括与您可以使用的不同，模板的信息。

用户可以输入和过帐财务日志中的行将从 Microsoft Excel。 在用户创建日志后，在 Excel 的**未结行**按显示可用的模板。 模板支持特定设计方案，但不指明，科目类型的每个组合日志中支持。 下表显示可用的模板和这些支持哪些科目类型。
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **支持的科目类型**                                                                                             | **如何访问**模板                                                          |
| 分类日记帐行     | 帐户：会计，客户，供应商，银行对方科目：会计，客户，供应商，银行支持内部公司。       | 普通日记帐                                                                         |
| 发票登记簿         | 帐户：供应商对方科目：内部公司的会计不支持。                                                    | AP 发票登记簿                                                                     |
| 发票日记帐          | 帐户：供应商对方科目：内部公司会计的支持。                                                      | AP 发票日记帐                                                                      |
| 供应商发票           |                                                                                                                         | 供应商发票                                                                          |
| 客户发票日记帐 | 帐户：客户：对方科目内部公司会计的支持。                                                     | 普通日记帐                                                                         |
| 普通发票        |                                                                                                                         | **在普通发票** **页，请单击打开在** Microsoft Office Excel (图标)。 |
| 固定资产日记帐     | 到会计、银行、客户或供应商的资产。 内部公司并不只支持。                                               | 固定资产日记帐                                                                     |
| 供应商付款日记帐   | 帐户：供应商对方科目：会计，内部公司的银行支持。                                                 | 供应商付款日记帐                                                                  |
| 客户付款日记帐 | 帐户：客户：对方科目会计，内部公司的银行支持。                                               | 客户付款日记帐                                                                |
| 项目支出日记帐  | 帐户：项目，会计，客户，供应商对方科目：项目，会计，客户，内部公司的供应商支持。 | 普通记帐日志的支出 (项目管理与核算下)                       |

行在发布时，其验证，以确保它们符合在财务日志设置的规则。 行在发布后，用户才能编辑或过帐从 Microsoft Dynamics 365 的凭证的工序。 

若要加上财务维度，附加到模板的更改需要。 有关其他信息，请参阅《[到 Microsoft Excel 模板中添加维度 dev] (\ \ \ itpro 财务维度将维度添加 Excel 模板)。 在维度添加实体后，他们可以在 Excel 设计器，可以添加到模板。




