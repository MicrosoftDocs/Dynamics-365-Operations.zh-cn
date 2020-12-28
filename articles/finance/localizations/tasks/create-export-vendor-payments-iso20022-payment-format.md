---
title: 使用 ISO20022 付款格式创建和导出供应商付款
description: 此过程显示如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。
author: mrolecki
manager: AnnBe
ms.date: 01/17/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym, SysQueryForm, VendPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff8a2858bfa96eb1d4b0afa1e48ebd1b578a4431
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440853"
---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="ea1fd-103">使用 ISO20022 付款格式创建和导出供应商付款</span><span class="sxs-lookup"><span data-stu-id="ea1fd-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea1fd-104">此主题说明如何在供应商付款日记帐中创建付款行，并使用 ISO2022 贷方转帐示例生成供应商付款文件。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-104">This topic explains how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span>

<span data-ttu-id="ea1fd-105">这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第五个。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-105">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="ea1fd-106">使用 DEMF 演示数据来完成此示例。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-106">Use the DEMF demo data to complete this example.</span></span>

## <a name="example"></a><span data-ttu-id="ea1fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="ea1fd-107">Example</span></span>

1.    <span data-ttu-id="ea1fd-108">转到 **应付帐款 > 付款 > 付款日记帐**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-108">Go to **Accounts payable > Payments > Payment journal**.</span></span>
2.    <span data-ttu-id="ea1fd-109">单击 **新建**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-109">Click **New**.</span></span>
3.    <span data-ttu-id="ea1fd-110">在 **名称** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-110">In the **Name** field, enter or select a value.</span></span>
4.    <span data-ttu-id="ea1fd-111">单击 **行 > 付款方案 > 创建付款方案**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-111">Click **Lines > Payment proposal > Create payment proposal**.</span></span>
5.    <span data-ttu-id="ea1fd-112">扩展 **要包括的记录** 部分。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-112">Expand the **Records to include** section.</span></span>
6.    <span data-ttu-id="ea1fd-113">单击 **筛选器**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-113">Click **Filter**.</span></span>
7.    <span data-ttu-id="ea1fd-114">在列表中，选择 **供应商** 表和 **供应商帐户字段** 的行。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-114">In the list, select the row for **Vendors table** and **Vendor account field**.</span></span>
8.    <span data-ttu-id="ea1fd-115">在 **标准** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-115">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="ea1fd-116">您可以为选择要付款的供应商交易应用任何条件，此示例中则是将 DE-001 用作供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-116">You can apply any criteria for selecting vendor transactions to pay, for this example, use DE-001 as a vendor account.</span></span>
12.    <span data-ttu-id="ea1fd-117">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-117">Click **OK**.</span></span>
13.    <span data-ttu-id="ea1fd-118">单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-118">Click **OK**.</span></span>
14.    <span data-ttu-id="ea1fd-119">单击 **创建付款**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-119">Click **Create payments**.</span></span>
15. <span data-ttu-id="ea1fd-120">生成 ISO20022 付款文件。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-120">Generate an ISO20022 payment file.</span></span>
    1.    <span data-ttu-id="ea1fd-121">单击 **生成付款**。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-121">Click **Generate payments**.</span></span>
    2.    <span data-ttu-id="ea1fd-122">在 **付款方式** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-122">In the **Method of payment** field, enter or select a value.</span></span>
    3.    <span data-ttu-id="ea1fd-123">在 **文件名** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-123">In the **File name** field, type a value.</span></span> <span data-ttu-id="ea1fd-124">对于本例，由于 EUR 付款，生成的文件将为 SEPA 合规文件。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-124">For this example, because of the EUR payment, the generated file will be SEPA compliant.</span></span> <span data-ttu-id="ea1fd-125">ISO20022 贷方转帐以及其他供应商付款格式也可以用于生成其他币种的付款。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-125">ISO20022 credit transfer as well as other vendor payment formats can also be used for generating payments in other currencies.</span></span>
    4.    <span data-ttu-id="ea1fd-126">在 **银行帐户** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="ea1fd-126">In the **Bank account** field, enter or select a value.</span></span>

