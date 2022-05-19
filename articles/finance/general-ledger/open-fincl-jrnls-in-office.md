---
title: 在 Office 中打开财务日记帐模板
description: 本主题介绍了使用 Microsoft Excel 模板创建自定义财务日记帐时可能发生的问题。
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 099d3c0074a86913b79b732a4c2a34b6e6488672
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723069"
---
# <a name="open-financial-journal-templates-in-office"></a>在 Office 中打开财务日记帐模板

[!include [banner](../includes/banner.md)]

本主题介绍了使用 Microsoft Excel 模板创建自定义财务日记帐时可能发生的问题。

## <a name="symptom"></a>问题

您创建了财务日记帐的自定义 Excel 模板，但该模板未显示在 **在 Excel 中打开行** 菜单上。 或者，它确实显示在菜单上，但是当您选中该模板时，打开的却是另一个模板。

## <a name="resolution"></a>解决方法

默认情况下，“在 Excel 中打开”功能使用当前页面的根数据源（表）来确定哪些 Office 模板或数据实体在 **在 Excel 中打开** 菜单上显示为选项。 这一方法并不适用于财务日记帐，因为财务日记帐使用相同的表（LedgerJournalTable 和 LedgerJournalTrans）作为许多其他类型日记帐的根数据源。

对于财务日记帐，“在 Excel 中打开行”功能旨在显示针对您当前正在其上下文中操作的日记帐而设计的模板，例如普通日记帐或付款日记帐。 例如，与供应商付款日记帐结合使用的模板设计用于将您的主帐户强制用作供应商帐户。

如果您想要升级模板，使其在 **在 Excel 中打开行** 和 **在 Excel 中打开** 菜单中可用，开发人员可以通过实现 **LedgerIJournalExcelTemplate** 界面并扩展 **DocuTemplateRegistrationBase** 类来轻松实现该操作。 此方法已在系统中实现，且有许多示例。 可供参考的一个示例是为普通日记帐（或日常记帐）创建的 **LedgerDailyJournalExcelTemplate** 界面。

已为您的模板实现了 **LedgerIJournalExcelTemplate** 界面，**在 Excel 中打开行** 菜单将按您的日记帐类型筛选模板，并仅显示可用于该日记帐的模板。 该界面还提供了一种验证方法，可确保只有满足帐户类型要求才可打开可用于该日记帐的模板。 例如，您可以指定帐户类型必须为 **供应商** 或者 **分类帐**。

有关此功能的更多信息，请参阅[将模板添加到“在 Excel 中打开行”菜单中](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md)。
