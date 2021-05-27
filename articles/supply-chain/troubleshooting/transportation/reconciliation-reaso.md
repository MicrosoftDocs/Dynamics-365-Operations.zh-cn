---
title: 出于对帐原因，您只能将主科目添加为货方科目
description: 在运输管理中设置对帐原因时，只能将主科目添加为货方科目。
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026289"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="fbd77-103">出于对帐原因，您只能将主科目添加为货方科目</span><span class="sxs-lookup"><span data-stu-id="fbd77-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="fbd77-104">知识库编号：4603538</span><span class="sxs-lookup"><span data-stu-id="fbd77-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="fbd77-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="fbd77-105">Symptoms</span></span>

<span data-ttu-id="fbd77-106">在运输管理中设置对帐原因时，只能将主科目添加为货方科目。</span><span class="sxs-lookup"><span data-stu-id="fbd77-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="fbd77-107">您不能将成本中心或任何其他维度添加为贷方科目。</span><span class="sxs-lookup"><span data-stu-id="fbd77-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="fbd77-108">但是，贷方科目允许您选择其他维度。</span><span class="sxs-lookup"><span data-stu-id="fbd77-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="fbd77-109">解决方法</span><span class="sxs-lookup"><span data-stu-id="fbd77-109">Resolution</span></span>

<span data-ttu-id="fbd77-110">如果对帐不是要支付供应商而是要贷记特定主科目，那么在设置对帐原因时，系统将不允许您为贷方科目选择财务维度。</span><span class="sxs-lookup"><span data-stu-id="fbd77-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="fbd77-111">如果科目结构需要贷方主科目使用特定的财务维度值，生成的供应商日记帐将由于缺少财务维度值无法自动过帐。</span><span class="sxs-lookup"><span data-stu-id="fbd77-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="fbd77-112">因此，您必须使用 **发票日记帐** 页首先手动指定贷方科目。</span><span class="sxs-lookup"><span data-stu-id="fbd77-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="fbd77-113">由于贷方科目需要维度值，因此供应商发票日记帐无法自动过帐。</span><span class="sxs-lookup"><span data-stu-id="fbd77-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="fbd77-114">在将维度值手动添加到贷方行的主科目后，您必须手动过帐。</span><span class="sxs-lookup"><span data-stu-id="fbd77-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
