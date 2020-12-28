---
title: 使用外币记录租赁
description: 本主题说明如何使用非记帐币种或申报币种记录租赁。
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
ms.openlocfilehash: 92177d4f808bfec88dabe9277c3d584ed02e401e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440948"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="24b67-103">使用外币记录租赁</span><span class="sxs-lookup"><span data-stu-id="24b67-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24b67-104">采用非记帐币种或申报币种的租赁的资产租赁科目是在 **分类帐设置** 页上建立的。</span><span class="sxs-lookup"><span data-stu-id="24b67-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="24b67-105">所有租赁均应以其交易币种输入。</span><span class="sxs-lookup"><span data-stu-id="24b67-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="24b67-106">换句话说，应使用租赁合同中指定的币种输入。</span><span class="sxs-lookup"><span data-stu-id="24b67-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="24b67-107">本主题说明如何使用非记帐币种或申报币种记录租赁。</span><span class="sxs-lookup"><span data-stu-id="24b67-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="24b67-108">如果您以外币形式输入租赁，则使用权 (ROU) 资产会以记帐币种和申报币种折旧。</span><span class="sxs-lookup"><span data-stu-id="24b67-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="24b67-109">这些币种在 **分类帐设置** 页中配置。</span><span class="sxs-lookup"><span data-stu-id="24b67-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="24b67-110">固定资产中也使用此行为。</span><span class="sxs-lookup"><span data-stu-id="24b67-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="24b67-111">当您以外币创建租赁时，请在 **币种** 字段中选择交易币种。</span><span class="sxs-lookup"><span data-stu-id="24b67-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="24b67-112">记帐币种的汇率是 **记帐币种汇率** 字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="24b67-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="24b67-113">申报币种的汇率是 **申报币种汇率** 字段中的默认值。</span><span class="sxs-lookup"><span data-stu-id="24b67-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="24b67-114">这些汇率自租赁开始之日起生效。</span><span class="sxs-lookup"><span data-stu-id="24b67-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="24b67-115">**记帐币种汇率** 和 **申报币种汇率** 字段位于 **租赁详细信息** 页面的 **财务和申报汇率信息** 快速选项卡中。</span><span class="sxs-lookup"><span data-stu-id="24b67-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="24b67-116">选中 **固定利率** 复选框以覆盖自动输入的汇率，然后输入新汇率。</span><span class="sxs-lookup"><span data-stu-id="24b67-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="24b67-117">在其他字段中，输入租赁所需的信息，然后选择 **创建计划**。</span><span class="sxs-lookup"><span data-stu-id="24b67-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="24b67-118">在新的 **租赁详细信息** 页面上，选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="24b67-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="24b67-119">在 **租赁帐簿** 页面上的 **财务和申报交换信息** 选项卡上，验证 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="24b67-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="24b67-120">这些字段中的每个字段均以相应币种显示折算后的使用权资产余额。</span><span class="sxs-lookup"><span data-stu-id="24b67-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="24b67-121">只要您更改任何财务信息，这些字段就会更新。</span><span class="sxs-lookup"><span data-stu-id="24b67-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="24b67-122">在确认付款计划之前，请选择 **创建计划**。</span><span class="sxs-lookup"><span data-stu-id="24b67-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="24b67-123">初始确认日记帐条目记录使用租赁中列出的货币汇率的使用权资产。</span><span class="sxs-lookup"><span data-stu-id="24b67-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="24b67-124">日记帐条目还包括 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="24b67-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="24b67-125">外币租赁的后续计量</span><span class="sxs-lookup"><span data-stu-id="24b67-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="24b67-126">折旧计划以申报币种、记帐币种和交易币种显示预期的折旧费用金额。</span><span class="sxs-lookup"><span data-stu-id="24b67-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="24b67-127">要以申报币种或记帐币种查看使用权资产余额和折旧金额，请打开 **资产折旧计划** 页，然后选中 **显示记帐币种金额** 或 **显示申报币种金额** 复选框。</span><span class="sxs-lookup"><span data-stu-id="24b67-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="24b67-128">当您针对以外币计价的租赁创建折旧费用日记帐条目时，该条目将使用租赁中列出的汇率。</span><span class="sxs-lookup"><span data-stu-id="24b67-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="24b67-129">还使用 **记帐币种初始使用权资产** 和 **申报币种初始使用权资产** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="24b67-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="24b67-130">最终折旧费用金额可以通过使用稍微不同的汇率来计算，因此使用权资产可以以记帐货币和申报币种完全折旧。</span><span class="sxs-lookup"><span data-stu-id="24b67-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="24b67-131">如果租赁已重新分类为 **延期租金**，系统会自动清除记帐币种和申报币种的汇率（如果已定义）。</span><span class="sxs-lookup"><span data-stu-id="24b67-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>
