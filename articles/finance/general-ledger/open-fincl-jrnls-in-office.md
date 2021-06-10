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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089449"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="2a81c-103">在 Office 中打开财务日记帐模板</span><span class="sxs-lookup"><span data-stu-id="2a81c-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a81c-104">本主题介绍了使用 Microsoft Excel 模板创建自定义财务日记帐时可能发生的问题。</span><span class="sxs-lookup"><span data-stu-id="2a81c-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="2a81c-105">问题</span><span class="sxs-lookup"><span data-stu-id="2a81c-105">Symptom</span></span>

<span data-ttu-id="2a81c-106">您创建了财务日记帐的自定义 Excel 模板，但该模板未显示在 **在 Excel 中打开行** 菜单上。</span><span class="sxs-lookup"><span data-stu-id="2a81c-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="2a81c-107">或者，它确实显示在菜单上，但是当您选中该模板时，打开的却是另一个模板。</span><span class="sxs-lookup"><span data-stu-id="2a81c-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="2a81c-108">解决方法</span><span class="sxs-lookup"><span data-stu-id="2a81c-108">Resolution</span></span>

<span data-ttu-id="2a81c-109">默认情况下，“在 Excel 中打开”功能使用当前页面的根数据源（表）来确定哪些 Office 模板或数据实体在 **在 Excel 中打开** 菜单上显示为选项。</span><span class="sxs-lookup"><span data-stu-id="2a81c-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="2a81c-110">这一方法并不适用于财务日记帐，因为财务日记帐使用相同的表（LedgerJournalTable 和 LedgerJournalTrans）作为许多其他类型日记帐的根数据源。</span><span class="sxs-lookup"><span data-stu-id="2a81c-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="2a81c-111">对于财务日记帐，“在 Excel 中打开行”功能旨在显示针对您当前正在其上下文中操作的日记帐而设计的模板，例如普通日记帐或付款日记帐。</span><span class="sxs-lookup"><span data-stu-id="2a81c-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="2a81c-112">例如，与供应商付款日记帐结合使用的模板设计用于将您的主帐户强制用作供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="2a81c-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="2a81c-113">如果您想要升级模板，使其在 **在 Excel 中打开行** 和 **在 Excel 中打开** 菜单中可用，开发人员可以通过实现 **LedgerIJournalExcelTemplate** 界面并扩展 **DocuTemplateRegistrationBase** 类来轻松实现该操作。</span><span class="sxs-lookup"><span data-stu-id="2a81c-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="2a81c-114">此方法已在系统中实现，且有许多示例。</span><span class="sxs-lookup"><span data-stu-id="2a81c-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="2a81c-115">可供参考的一个示例是为普通日记帐（或日常记帐）创建的 **LedgerDailyJournalExcelTemplate** 界面。</span><span class="sxs-lookup"><span data-stu-id="2a81c-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="2a81c-116">已为您的模板实现了 **LedgerIJournalExcelTemplate** 界面，**在 Excel 中打开行** 菜单将按您的日记帐类型筛选模板，并仅显示可用于该日记帐的模板。</span><span class="sxs-lookup"><span data-stu-id="2a81c-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="2a81c-117">该界面还提供了一种验证方法，可确保只有满足帐户类型要求才可打开可用于该日记帐的模板。</span><span class="sxs-lookup"><span data-stu-id="2a81c-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="2a81c-118">例如，您可以指定帐户类型必须为 **供应商** 或者 **分类帐**。</span><span class="sxs-lookup"><span data-stu-id="2a81c-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="2a81c-119">有关此功能的更多信息，请参阅[将模板添加到“在 Excel 中打开行”菜单中](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md)。</span><span class="sxs-lookup"><span data-stu-id="2a81c-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
