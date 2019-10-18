---
title: 支出报表上的人员支出
description: 此主题介绍 Microsoft Dynamics 365 Finance 中两种处理员工个人支出的方法。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176595"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="990a0-103">支出报表上的人员支出</span><span class="sxs-lookup"><span data-stu-id="990a0-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="990a0-104">在出差期间，员工有时可能将个人支出计费到它们的公司信用卡。</span><span class="sxs-lookup"><span data-stu-id="990a0-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="990a0-105">如果不制订个人支出处理流程，则在员工提交其明细化的支出报表时，支出报表审核流程可能会中断。</span><span class="sxs-lookup"><span data-stu-id="990a0-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="990a0-106">有两种处理工作人员个人支出的方法：</span><span class="sxs-lookup"><span data-stu-id="990a0-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="990a0-107">**员工支付** - 组织不支付公司信用卡帐单上出现的个人支出。</span><span class="sxs-lookup"><span data-stu-id="990a0-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="990a0-108">相反，它创建了一个报表，该报表显示了计费到公司信用卡的个人支出和公司支出。</span><span class="sxs-lookup"><span data-stu-id="990a0-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="990a0-109">**公司支付** - 组织支付整个公司信用卡帐单，然后将个人支出借记到员工帐户中。</span><span class="sxs-lookup"><span data-stu-id="990a0-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="990a0-110">您可以在**支出管理参数**页面中选择组织使用的方法。</span><span class="sxs-lookup"><span data-stu-id="990a0-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>
