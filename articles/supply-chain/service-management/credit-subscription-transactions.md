---
title: 贷方预订交易记录
description: 本主题演示如何创建预订交易记录。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a136489b663a066b853344844ad28a14670c8d66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202506"
---
# <a name="credit-subscription-transactions"></a><span data-ttu-id="2ab40-103">贷方预订交易记录</span><span class="sxs-lookup"><span data-stu-id="2ab40-103">Credit subscription transactions</span></span> 

[!include [banner](../includes/banner.md)]


## <a name="credit-subscription-transactions"></a><span data-ttu-id="2ab40-104">贷方预订交易记录</span><span class="sxs-lookup"><span data-stu-id="2ab40-104">Credit subscription transactions</span></span>

1.  <span data-ttu-id="2ab40-105">单击**服务管理** \> **常用** \> **服务预订** \> **所有服务预订**。</span><span class="sxs-lookup"><span data-stu-id="2ab40-105">Click **Service management** \> **Common** \> **Service subscriptions** \> **All service subscriptions**.</span></span>

2.  <span data-ttu-id="2ab40-106">选择附加到您要为其创建贷方通知单的预订交易记录的预订。</span><span class="sxs-lookup"><span data-stu-id="2ab40-106">Select the subscription attached to the subscription transaction for which you want to create a credit note.</span></span>

3.  <span data-ttu-id="2ab40-107">选择**分析**选项卡，然后在“操作窗格”上单击**费用交易记录**按钮。</span><span class="sxs-lookup"><span data-stu-id="2ab40-107">Select the **Analyze** tab, and then click the **Fee transactions** button on the Action Pane.</span></span>

4.  <span data-ttu-id="2ab40-108">从**费用交易记录**窗体中选择您想为其创建贷方通知单的交易记录。</span><span class="sxs-lookup"><span data-stu-id="2ab40-108">From the **Fee transactions** form, select the transaction for which you want to create a credit note.</span></span>

5.  <span data-ttu-id="2ab40-109">单击**功能** \> **为贷方通知单选择**。</span><span class="sxs-lookup"><span data-stu-id="2ab40-109">Click **Functions** \> **Select for credit note**.</span></span>

6.  <span data-ttu-id="2ab40-110">从**为贷方通知单选择**窗体中，选择您要贷记的交易记录，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="2ab40-110">From the **Select for credit note** form, select the transaction that you want to credit and then click **OK**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2ab40-111">当您创建贷方通知单时，请确保您选择了<STRONG>贷方通知单</STRONG>。</span><span class="sxs-lookup"><span data-stu-id="2ab40-111">When you create the credit note, make sure that you select <STRONG>Credit notes</STRONG>.</span></span> <span data-ttu-id="2ab40-112">这是在<STRONG>创建发票</STRONG>对话框中的<STRONG>开票方法</STRONG>列表中找到的。</span><span class="sxs-lookup"><span data-stu-id="2ab40-112">This is found in the <STRONG>Invoicing method</STRONG> list in the <STRONG>Create invoice</STRONG> dialog box.</span></span></P>

<span data-ttu-id="2ab40-113">如果**服务管理参数**窗体中的**冲销贷记的应计项目**字段设置为**手动**，则您必须首先单独冲销每个应计收入交易记录，然后才能为该交易记录创建贷方通知单方案。</span><span class="sxs-lookup"><span data-stu-id="2ab40-113">If the **Reverse accruals on crediting** field in the **Service management parameters** form is set to **Manual**, you have to reverse each accrued revenue transaction individually before you create a credit note proposal for the transaction.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ab40-114">请参阅</span><span class="sxs-lookup"><span data-stu-id="2ab40-114">See also</span></span>

[<span data-ttu-id="2ab40-115">发票预订交易记录</span><span class="sxs-lookup"><span data-stu-id="2ab40-115">Invoice subscription transactions</span></span>](invoice-subscription-transactions.md)


 
