---
title: 从 Excel 发布日记帐行和单据
description: 本主题说明如何从 Microsoft Excel 输入和发布普通日记帐的行。 其中包含有关您可使用的各种模板的信息，具体取决于您要输入的交易记录类型。
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0aaf5339c689af9e8748ccb25ae63dfafda8a7b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990381"
---
# <a name="publish-journal-lines-and-documents-from-excel"></a>从 Excel 发布日记帐行和单据

[!include [banner](../includes/banner.md)]

本主题说明如何从 Microsoft Excel 输入和发布普通日记帐的行。 其中包含有关您可使用的各种模板的信息，具体取决于您要输入的交易记录类型。

用户可从 Microsoft Excel 输入和发布财务日记帐的行。 用户创建日记帐之后，**在 Excel 中打开文件** 按钮将显示可用模板。 模板设计为支持特定方案，但是日记帐中并非支持科目类型的所有组合。 下表显示可用模板及其支持的科目类型。

|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **模板**             | **支持的科目类型**                                                                                             | **模板的访问方法**                                                          |
| 分类日记帐行     | 支持“科目：分类帐、客户、供应商、银行抵销科目：分类帐、客户、供应商、银行内部公司”。       | 普通日记帐                                                                         |
| 发票登记簿         | 不支持“科目：供应商抵销科目：分类帐内部公司”。                                                    | AP 发票登记簿                                                                     |
| 发票日记帐          | 支持“科目：供应商抵销科目：分类帐内部公司”。                                                      | AP 发票日记帐                                                                      |
| 供应商发票           |                                                                                                                         | 供应商发票                                                                          |
| 客户发票日记帐 | 支持“科目：客户抵销科目：分类帐内部公司”。                                                     | 普通日记帐                                                                         |
| 普通发票        |                                                                                                                         | 在 **普通发票** 页中，单击 **在 Excel 中打开**（Microsoft Office 图标）。 |
| 固定资产日记帐     | 资产到分类帐、银行、客户或供应商。 不支持“内部公司”。                                               | 固定资产日记帐                                                                     |
| 供应商付款日记帐   | 不支持“科目：供应商抵销科目：分类帐、银行内部公司”。                                                 | 供应商付款日记帐                                                                  |
| 客户付款日记帐 | 支持“科目：客户抵销科目：分类帐、银行内部公司”。                                               | 客户付款日记帐                                                                |
| 项目支出日记帐  | 支持“科目：项目、分类帐、客户、供应商抵销科目：项目、分类帐、客户、供应商、银行内部公司”。 | 普通日记帐费用（在“项目管理和会计”下）                       |

发布行时，将验证行，以便确保其符合财务日记帐中设置的规则。 发布行之后，用户可从 Dynamics 365 Finance 编辑或过帐凭证。 

若要向模板添加财务维度，需要执行更多更改。 有关详细信息，请参阅[向 Microsoft Excel 模板添加维度](../../dev-itpro/financial/add-dimensions-excel-templates.md)。 维度添加到实体之后，将在 Excel 设计器中可用，并可添加到模板。





