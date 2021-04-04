---
title: 定期信用管理任务
description: 本主题描述了管理客户信用额度过程中必须进行的定期任务。
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a034d563c12c4ba8b99e13b30ea2683555a01276
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254479"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="8ac50-103">定期信用管理任务</span><span class="sxs-lookup"><span data-stu-id="8ac50-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ac50-104">本主题描述了管理客户信用额度过程中必须进行的定期任务。</span><span class="sxs-lookup"><span data-stu-id="8ac50-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="8ac50-105">更新风险分数</span><span class="sxs-lookup"><span data-stu-id="8ac50-105">Update risk scores</span></span>

<span data-ttu-id="8ac50-106">随着业务的发展和环境的变化，指定客户的信用风险也可能发生变化。</span><span class="sxs-lookup"><span data-stu-id="8ac50-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="8ac50-107">为了帮助维持适合客户的信用额度，您必须定期查看每个风险评分的标准并更新每个客户的评分。</span><span class="sxs-lookup"><span data-stu-id="8ac50-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="8ac50-108">您可以使用 **更新风险评分** 页面（**信用和收款 \> 定期任务 \> 信用管理 \> 更新风险评分**）来更新以下分数。</span><span class="sxs-lookup"><span data-stu-id="8ac50-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="8ac50-109">所有用户定义的计算也会被处理。</span><span class="sxs-lookup"><span data-stu-id="8ac50-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="8ac50-110">**平均付款天数** – 此分数是客户支付发票所用的平均天数。</span><span class="sxs-lookup"><span data-stu-id="8ac50-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="8ac50-111">**自从以下时间以来的客户** – 此分数是客户成为您组织的客户的年数。</span><span class="sxs-lookup"><span data-stu-id="8ac50-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="8ac50-112">**营业开始年份** – 此分数是客户营业的年数。</span><span class="sxs-lookup"><span data-stu-id="8ac50-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="8ac50-113">它使用 **客户** 页上的 **业务开始时间** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="8ac50-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="8ac50-114">**销售款未清天数** – 该分数基于应收帐款余额、销售收入和前 12 个月的天数。</span><span class="sxs-lookup"><span data-stu-id="8ac50-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="8ac50-115">**平均余额** – 该分数基于前 12 个月的应收帐款余额。</span><span class="sxs-lookup"><span data-stu-id="8ac50-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="8ac50-116">**信用管理组**、**帐户状态** 和 **国家/地区** – 这些分数使用来自客户的信息。</span><span class="sxs-lookup"><span data-stu-id="8ac50-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="8ac50-117">更新客户余额统计信息</span><span class="sxs-lookup"><span data-stu-id="8ac50-117">Update customer balance statistics</span></span>

<span data-ttu-id="8ac50-118">您可以运行 **更新客户余额统计信息** 流程，以更新显示在 **余额统计查询** 页上的余额统计信息计算结果。</span><span class="sxs-lookup"><span data-stu-id="8ac50-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="8ac50-119">此信息用于计算风险评分和 **客户** 页上信用统计速见表中显示的值。</span><span class="sxs-lookup"><span data-stu-id="8ac50-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="8ac50-120">运行该流程时，它将更新单个客户的客户余额统计信息。</span><span class="sxs-lookup"><span data-stu-id="8ac50-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="8ac50-121">要设置批处理作业以为多个客户运行该流程，您可以使用 **计算余额统计** 页面（**信用管理 \> 定期任务 \> 计算余额统计**）。</span><span class="sxs-lookup"><span data-stu-id="8ac50-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]