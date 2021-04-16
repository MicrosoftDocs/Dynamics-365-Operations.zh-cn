---
title: 设置 ISO20022 贷方转帐的供应商及供应商银行帐户
description: 此过程可以演示如何设置供应商及其所需的特定银行帐户信息以生成 ISO20022 贷方转帐或其他任何供应商付款文件。
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47735d41fde4c5f71ec1c3209446a593e1f4180c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813411"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a><span data-ttu-id="4702a-103">设置 ISO20022 贷方转帐的供应商及供应商银行帐户</span><span class="sxs-lookup"><span data-stu-id="4702a-103">Set up vendors and vendor bank accounts for ISO20022 credit transfers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4702a-104">此过程可以演示如何设置供应商及其所需的特定银行帐户信息以生成 ISO20022 贷方转帐或其他任何供应商付款文件。</span><span class="sxs-lookup"><span data-stu-id="4702a-104">This procedure demonstrates how to set up the vendor and vendor specific bank account information required for ISO20022 Credit transfer or any other vendor payment file generation.</span></span> 

<span data-ttu-id="4702a-105">用于创建此过程的演示数据公司是 DEMF。</span><span class="sxs-lookup"><span data-stu-id="4702a-105">The demo data company used to create this procedure is DEMF.</span></span>
<span data-ttu-id="4702a-106">这是五个用于演示使用电子申报配置的供应商付款流程的流程中的第四个。</span><span class="sxs-lookup"><span data-stu-id="4702a-106">This is the fourth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="4702a-107">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="4702a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="set-up-bank-details"></a><span data-ttu-id="4702a-108">设置银行详情</span><span class="sxs-lookup"><span data-stu-id="4702a-108">Set up bank details</span></span>
1. <span data-ttu-id="4702a-109">转到“应付帐款”>“供应商”>“所有供应商”。</span><span class="sxs-lookup"><span data-stu-id="4702a-109">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="4702a-110">使用“快速筛选器”以查找记录。</span><span class="sxs-lookup"><span data-stu-id="4702a-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4702a-111">例如，在“供应商帐户”字段中筛选“DE-001”数值。</span><span class="sxs-lookup"><span data-stu-id="4702a-111">For example, filter on the Vendor account field with a value of 'DE-001'.</span></span>
3. <span data-ttu-id="4702a-112">单击 DE-001 以打开供应商详细信息。</span><span class="sxs-lookup"><span data-stu-id="4702a-112">Click DE-001 to open vendor details.</span></span>
4. <span data-ttu-id="4702a-113">在“操作窗格”上，单击“供应商”。</span><span class="sxs-lookup"><span data-stu-id="4702a-113">On the Action Pane, click Vendor.</span></span>
5. <span data-ttu-id="4702a-114">单击“银行帐户”。</span><span class="sxs-lookup"><span data-stu-id="4702a-114">Click Bank accounts.</span></span>
6. <span data-ttu-id="4702a-115">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="4702a-115">Click Edit.</span></span>
    * <span data-ttu-id="4702a-116">如果没有可用的银行帐户，您需要创建一个新帐户。</span><span class="sxs-lookup"><span data-stu-id="4702a-116">If there is no bank account available, you need to create a new one.</span></span>  
7. <span data-ttu-id="4702a-117">在“SWIFT 代码”字段中，键入 'COBADEFFXXX'。</span><span class="sxs-lookup"><span data-stu-id="4702a-117">In the SWIFT code field, type 'COBADEFFXXX'.</span></span>
8. <span data-ttu-id="4702a-118">在 'IBAN' 字段中，键入 'DE36200400000628808808'。</span><span class="sxs-lookup"><span data-stu-id="4702a-118">In the IBAN field, type 'DE36200400000628808808'.</span></span>
9. <span data-ttu-id="4702a-119">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="4702a-119">Close the page.</span></span>

## <a name="set-up-a-method-of-payment-for-the-vendor"></a><span data-ttu-id="4702a-120">为供应商设置付款方式</span><span class="sxs-lookup"><span data-stu-id="4702a-120">Set up a method of payment for the vendor</span></span>
1. <span data-ttu-id="4702a-121">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="4702a-121">Click Edit.</span></span>
2. <span data-ttu-id="4702a-122">展开或收拢付款窗口。</span><span class="sxs-lookup"><span data-stu-id="4702a-122">Expand or collapse the Payment section.</span></span>
3. <span data-ttu-id="4702a-123">在“付款方式”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="4702a-123">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4702a-124">在列表中，单击 SEPA CT 行中的链接。</span><span class="sxs-lookup"><span data-stu-id="4702a-124">In the list, click the link in the SEPA CT row.</span></span>
5. <span data-ttu-id="4702a-125">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="4702a-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]