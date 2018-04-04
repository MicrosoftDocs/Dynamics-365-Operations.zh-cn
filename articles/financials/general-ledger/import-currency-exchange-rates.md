---
title: "导入币种汇率。"
description: "如果法人收到外币发票，则必须将外币转换为本币。 这意味着需要不同币种的最新汇率。 本主题提供导入欧洲央行和俄罗斯央行等汇率提供方通过 Internet 发布的参考汇率所需设置和处理的概览。"
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: df07066371cb7d9c69976c9714b6d2fe456a0308
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="import-currency-exchange-rates"></a><span data-ttu-id="0d950-105">导入币种汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-105">Import currency exchange rates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0d950-106">如果法人收到外币发票，则必须将外币转换为本币。</span><span class="sxs-lookup"><span data-stu-id="0d950-106">If a legal entity has received invoices in foreign currencies, it’s necessary to convert the foreign currency into the local currency.</span></span> <span data-ttu-id="0d950-107">这意味着需要不同币种的最新汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-107">This means that up-to-date exchange rates for different currencies are required.</span></span> <span data-ttu-id="0d950-108">本主题提供导入欧洲央行和俄罗斯央行等汇率提供方通过 Internet 发布的参考汇率所需设置和处理的概览。</span><span class="sxs-lookup"><span data-stu-id="0d950-108">This topic provides an overview of the required settings and processing for importing foreign exchange reference rates published over the Internet by the exchange rate providers, such as the European Central Bank and the Central Bank of Russia.</span></span>

<span data-ttu-id="0d950-109">以下章节介绍用于设置和处理汇率导入的信息流。</span><span class="sxs-lookup"><span data-stu-id="0d950-109">The following sections describe the flow of information that is used for setting up and processing the import of foreign exchange rates.</span></span>

## <a name="configure-an-exchange-rate-provider"></a><span data-ttu-id="0d950-110">配置汇率提供方</span><span class="sxs-lookup"><span data-stu-id="0d950-110">Configure an exchange rate provider</span></span>
<span data-ttu-id="0d950-111">必须先设置提供汇率的提供方所需信息，才能导入汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-111">Before you can import exchange rates, you must set up the information that is required by the providers who offer the exchange rates.</span></span> <span data-ttu-id="0d950-112">请使用**配置汇率提供方**页选择汇率提供方。</span><span class="sxs-lookup"><span data-stu-id="0d950-112">Use the **Configure exchange rate providers** page to select the exchange rate providers.</span></span> <span data-ttu-id="0d950-113">Microsoft Dynamics 365 for Finance and Operations 中的演示数据随附了一些汇率提供方。</span><span class="sxs-lookup"><span data-stu-id="0d950-113">Some exchange rate providers are included with the demo data in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0d950-114">下表描述此页中的各个控件。</span><span class="sxs-lookup"><span data-stu-id="0d950-114">The following table provides descriptions for the controls on this page.</span></span>

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d950-115">**字段**</span><span class="sxs-lookup"><span data-stu-id="0d950-115">**Field**</span></span> | <span data-ttu-id="0d950-116">**描述**</span><span class="sxs-lookup"><span data-stu-id="0d950-116">**Description**</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="0d950-117">**名称**</span><span class="sxs-lookup"><span data-stu-id="0d950-117">**Name**</span></span>  | <span data-ttu-id="0d950-118">汇率提供方的名称。</span><span class="sxs-lookup"><span data-stu-id="0d950-118">The name of the exchange rate provider.</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="0d950-119">**键**</span><span class="sxs-lookup"><span data-stu-id="0d950-119">**Key**</span></span>   | <span data-ttu-id="0d950-120">提供方所需的每条配置信息的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="0d950-120">The unique identifier for each piece of configuration information that is required by the provider.</span></span> <span data-ttu-id="0d950-121">此信息为单击**添加**按钮时添加的每个汇率提供方自动添加。</span><span class="sxs-lookup"><span data-stu-id="0d950-121">This information is automatically added for each exchange rate provider that you add when you click the **Add** button.</span></span> |
| <span data-ttu-id="0d950-122">**值**</span><span class="sxs-lookup"><span data-stu-id="0d950-122">**Value**</span></span> | <span data-ttu-id="0d950-123">每个参数的信息。</span><span class="sxs-lookup"><span data-stu-id="0d950-123">Information for each key.</span></span> <span data-ttu-id="0d950-124">此信息为单击**添加**按钮时添加的每个汇率提供方添加。</span><span class="sxs-lookup"><span data-stu-id="0d950-124">This information is added for each exchange rate provider that you add when you click the **Add** button.</span></span>                                                                                         |

## <a name="import-currency-exchange-rates"></a><span data-ttu-id="0d950-125">导入币种汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-125">Import currency exchange rates</span></span>
<span data-ttu-id="0d950-126">可以从汇率提供方源导入汇率，然后在**汇率**页面中设置导入的汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-126">You can import exchange rates from the exchange rate providers source, and set them up in the **Currency exchange rates** page.</span></span> <span data-ttu-id="0d950-127">可使用**导入汇率**页导入汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-127">Use the **Import currency exchange rates** page to import the exchange rates.</span></span> <span data-ttu-id="0d950-128">下表介绍成功完成导入过程所需字段。</span><span class="sxs-lookup"><span data-stu-id="0d950-128">The following table provides descriptions the fields that are required to successfully complete the import process.</span></span>

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d950-129">**字段**</span><span class="sxs-lookup"><span data-stu-id="0d950-129">**Field**</span></span>                              | <span data-ttu-id="0d950-130">**描述**</span><span class="sxs-lookup"><span data-stu-id="0d950-130">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0d950-131">**汇率类型**</span><span class="sxs-lookup"><span data-stu-id="0d950-131">**Exchange rate type**</span></span>                 | <span data-ttu-id="0d950-132">汇率类型。</span><span class="sxs-lookup"><span data-stu-id="0d950-132">An exchange rate type.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="0d950-133">**汇率提供方**</span><span class="sxs-lookup"><span data-stu-id="0d950-133">**Exchange rate provider**</span></span>             | <span data-ttu-id="0d950-134">汇率提供方。</span><span class="sxs-lookup"><span data-stu-id="0d950-134">An exchange rate provider.</span></span>                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="0d950-135">**导入起始日期**</span><span class="sxs-lookup"><span data-stu-id="0d950-135">**Import as of**</span></span>                       | <span data-ttu-id="0d950-136">此参数管理导入当天汇率还是某个日期范围的汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-136">This parameter manages whether to import as of today’s date or for a date range.</span></span> <span data-ttu-id="0d950-137">如果要使用日期范围，请输入或选择开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="0d950-137">If you want to use a date range, enter or select starting and ending dates.</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="0d950-138">**创建必需的币种对**</span><span class="sxs-lookup"><span data-stu-id="0d950-138">**Create necessary currency pairs**</span></span>    | <span data-ttu-id="0d950-139">如果导入的币种对不存在，此复选框管理币种对的自动创建。</span><span class="sxs-lookup"><span data-stu-id="0d950-139">This check box manages the automatic creation of currency pairs, if the currency pairs that are imported do not exist.</span></span> <span data-ttu-id="0d950-140">此选项可能对某些提供方不可用。</span><span class="sxs-lookup"><span data-stu-id="0d950-140">This option might not be available for some providers.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="0d950-141">**重写现有汇率**</span><span class="sxs-lookup"><span data-stu-id="0d950-141">**Override existing exchange rates**</span></span>   | <span data-ttu-id="0d950-142">已存在特定日期的汇率时，此复选框管理汇率对的现有汇率更新。</span><span class="sxs-lookup"><span data-stu-id="0d950-142">This check box manages the update of the existing exchange rate for a currency pair when the exchange rate for a specific date already exists.</span></span> <span data-ttu-id="0d950-143">如果不选中此复选框，则已存在另一个汇率时，不导入指定日期的汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-143">If you do not select this check box, the exchange rate for the specific dates is not imported if another exchange rate already exists.</span></span>                                                                                       |
| <span data-ttu-id="0d950-144">**禁止在法定假日导入**</span><span class="sxs-lookup"><span data-stu-id="0d950-144">**Prevent import on national holiday**</span></span> | <span data-ttu-id="0d950-145">此复选框管理假日的汇率导入。</span><span class="sxs-lookup"><span data-stu-id="0d950-145">This check box manages the import of the exchange rate for a date that is a public holiday.</span></span> <span data-ttu-id="0d950-146">例如，如果选中此复选框并使用欧洲央行作为汇率提供方，系统将不更新与当前法人有关的假日的汇率。</span><span class="sxs-lookup"><span data-stu-id="0d950-146">For example, if you select this check box and use the European Central Bank as the exchange rate provider, the system will not update the exchange rate on a public holiday that is related to the current legal entity.</span></span> <span data-ttu-id="0d950-147">此选项可能对某些提供方不可用。</span><span class="sxs-lookup"><span data-stu-id="0d950-147">This option might not be available for some providers.</span></span> |






