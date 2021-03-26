---
title: 创建具有空白状态的支票
description: 本主题介绍了如何在“支票”页面中为银行帐户创建空白支票。
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 94d3a4ac8a3906e48f5a6053c031001c111549ad
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254027"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="d1428-103">创建具有空白状态的支票</span><span class="sxs-lookup"><span data-stu-id="d1428-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1428-104">本主题介绍了如何创建空白支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="d1428-105">例如，您可以创建一个空白支票以记录已损坏并且不能用于付款的支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="d1428-106">在 **支票** 页面上，可对支票执行维护任务。</span><span class="sxs-lookup"><span data-stu-id="d1428-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="d1428-107">例如，您可以创建新支票编号以及删除支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="d1428-108">您也可以创建具有 **空白** 状态的支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="d1428-109">在创建空白支票之后，将无法在系统中删除或重用这些支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="d1428-110">仅当在 **功能管理** 页面中启用 **在“支票”页面中创建具有空白状态的支票** 功能时，此功能才在 **支票** 页面中可用。</span><span class="sxs-lookup"><span data-stu-id="d1428-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="d1428-111">如果未启用该功能，则只能在应付帐款的付款生成流程期间从 **支票付款** 对话框创建具有 **空白** 状态的支票。</span><span class="sxs-lookup"><span data-stu-id="d1428-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="d1428-112">若要打开 **支票** 页面，请转到 **现金和银行管理 \> 银行账户 \> 银行账户**，然后在操作窗格的 **管理付款** 选项卡的 **相关信息** 组中，选择 **支票**。</span><span class="sxs-lookup"><span data-stu-id="d1428-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="d1428-113">或者，请转到 **现金和银行管理 \> 查询和报表 \> 支票**。</span><span class="sxs-lookup"><span data-stu-id="d1428-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="d1428-114">然后，若要创建具有 **空白** 状态的支票，请在操作窗格中选择 **创建空白支票**。</span><span class="sxs-lookup"><span data-stu-id="d1428-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="d1428-115">当系统创建空白支票时，关联的银行帐户将会暂时禁用。</span><span class="sxs-lookup"><span data-stu-id="d1428-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="d1428-116">此行为将会降低在创建空白支票时生成付款的风险。</span><span class="sxs-lookup"><span data-stu-id="d1428-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="d1428-117">处理完成后，关联的银行帐户将重新激活。</span><span class="sxs-lookup"><span data-stu-id="d1428-117">When the processing is completed, the associated bank account is reactivated.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]