---
title: 高级银行对帐概览
description: 本文介绍高级银行对帐流程的流程。 高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对账单。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b26b6e1e50e5a9b53ca6b5315de760f5bcec4769
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899389"
---
# <a name="advanced-bank-reconciliation-overview"></a><span data-ttu-id="5898c-104">高级银行对帐概览</span><span class="sxs-lookup"><span data-stu-id="5898c-104">Advanced bank reconciliation overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5898c-105">本文介绍高级银行对帐流程的流程。</span><span class="sxs-lookup"><span data-stu-id="5898c-105">This article describes the flow for the advanced bank reconciliation process.</span></span> <span data-ttu-id="5898c-106">高级银行对帐功能可以导入可从银行交易记录内自动对帐的银行对账单。</span><span class="sxs-lookup"><span data-stu-id="5898c-106">The advanced bank reconciliation feature lets you import bank statements that can be automatically reconciled from within bank transactions.</span></span>

<span data-ttu-id="5898c-107">高级银行对帐功能可以导入银行对账单。</span><span class="sxs-lookup"><span data-stu-id="5898c-107">The advanced bank reconciliation feature lets you import bank statements.</span></span> <span data-ttu-id="5898c-108">导入的银行对账单然后可以自动从银行交易记录内对帐。</span><span class="sxs-lookup"><span data-stu-id="5898c-108">The imported bank statement can then be automatically reconciled from within bank transactions.</span></span> <span data-ttu-id="5898c-109">这是高级银行对帐流的步骤。</span><span class="sxs-lookup"><span data-stu-id="5898c-109">Here are the steps in the advanced bank reconciliation flow.</span></span>

1.  <span data-ttu-id="5898c-110">设置银行对账单导入。</span><span class="sxs-lookup"><span data-stu-id="5898c-110">Set up a bank statement import.</span></span>
    -   <span data-ttu-id="5898c-111">通过数据实体框架导入银行对账单。</span><span class="sxs-lookup"><span data-stu-id="5898c-111">Import bank statements through the data entity framework.</span></span>
    -   <span data-ttu-id="5898c-112">三种典型的银行对账单构建格式：ISO20022、BAI2 和 MT940。</span><span class="sxs-lookup"><span data-stu-id="5898c-112">Three typical bank statement formats are built in: ISO20022, BAI2, and MT940.</span></span>
    -   <span data-ttu-id="5898c-113">此功能可以扩展为任意格式。</span><span class="sxs-lookup"><span data-stu-id="5898c-113">The functionality can be extended to any format.</span></span>

2.  <span data-ttu-id="5898c-114">设置高级银行对帐使用的编号规则，并且定义银行对帐匹配规则。</span><span class="sxs-lookup"><span data-stu-id="5898c-114">Set up a number sequence to use for advanced bank reconciliation, and define the bank reconciliation matching rules.</span></span>
    -   <span data-ttu-id="5898c-115">对帐匹配规则是用于在对帐过程中筛选银行对帐单行和 Microsoft Dynamics 365 Finance 银行交易记录行的一组条件。</span><span class="sxs-lookup"><span data-stu-id="5898c-115">A reconciliation matching rule is a set of criteria that are used to filter bank statement lines and Microsoft Dynamics 365 Finance bank transaction lines during the reconciliation process.</span></span> <span data-ttu-id="5898c-116">根据您的业务惯例，您可以设置多个匹配规则以自动化和优化您的对帐流程。</span><span class="sxs-lookup"><span data-stu-id="5898c-116">Depending on your business practice, you can set up more than one matching rule to automate and optimize your reconciliation process.</span></span>

3.  <span data-ttu-id="5898c-117">将银行对账单与 Finance 银行交易记录对帐。</span><span class="sxs-lookup"><span data-stu-id="5898c-117">Reconcile bank statements with Finance bank transactions.</span></span>
    -   <span data-ttu-id="5898c-118">执行自动匹配和创建对帐日记帐。</span><span class="sxs-lookup"><span data-stu-id="5898c-118">Perform automatic matching and creation of reconciliation journals.</span></span>
    -   <span data-ttu-id="5898c-119">并行查看银行对账单和 Finance 银行交易记录。</span><span class="sxs-lookup"><span data-stu-id="5898c-119">View bank statements and Finance bank transactions side by side.</span></span>
    -   <span data-ttu-id="5898c-120">如果 Finance 银行交易记录出现在银行对账单中，但不出现在 Finance 应用中，则自动过帐这些银行交易记录。</span><span class="sxs-lookup"><span data-stu-id="5898c-120">Automatically post Finance bank transactions if they appear on a bank statement but don't appear in the Finance app.</span></span>
    -   <span data-ttu-id="5898c-121">生成对账单。</span><span class="sxs-lookup"><span data-stu-id="5898c-121">Generate a reconciliation statement.</span></span>





