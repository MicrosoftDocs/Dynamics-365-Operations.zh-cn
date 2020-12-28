---
title: 在资产租赁中过帐转换调整日记帐条目
description: 本主题介绍使您可以将租赁组合转换到会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 这两种新的租赁会计标准的功能。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2020
ms.locfileid: "4440969"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="2d4bb-103">在资产租赁中过帐转换调整日记帐条目</span><span class="sxs-lookup"><span data-stu-id="2d4bb-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d4bb-104">本主题介绍使您可以将租赁组合转换到会计准则编纂专题 842 (ASC 842)（这是美国公认会计准则 (US GAAP) 中的准则）和国际财务报告准则 16 (IFRS 16) 这两种新的租赁会计标准的功能。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="2d4bb-105">有关如何设置帐簿以转换到新标准的信息，请参阅[设置租赁帐簿](set-up-lease-books.md)。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="2d4bb-106">创建转换调整日记帐条目时，将生成日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="2d4bb-107">该条目反映在该日期根据新准则记录租赁对资产负债表的影响。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="2d4bb-108">将为该日期的帐面金额借记相应资产科目，并贷记负债科目。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="2d4bb-109">差值将借记或贷记到保留收益。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="2d4bb-110">要按照新记帐准则过帐转换调整，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="2d4bb-111">在 **租赁摘要** 页上，选择租赁，然后选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="2d4bb-112">在帐簿中，选择 **付款计划**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="2d4bb-113">在 **付款计划** 对话框中，选择 **确认**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="2d4bb-114">然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="2d4bb-115">选择 **转换调整**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2d4bb-116">只能为分配给 **转换帐簿** 字段可用的帐簿分配的租赁帐簿创建转换调整。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="2d4bb-117">如果 **租赁开始** 字段中的值晚于转换日期，将不更新 **转换调整** 字段中的值。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="2d4bb-118">要查看日记帐条目，请选择 **资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="2d4bb-119">选择新日记帐，然后选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="2d4bb-119">Select the new journal, and then select **Post**.</span></span>
