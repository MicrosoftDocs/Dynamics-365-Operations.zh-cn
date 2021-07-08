---
title: 全球库存核算分类帐
description: 本主题介绍了全球库存核算分类帐，这些分类帐由货币、日历、惯例以及与法人的关联的组合定义。
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273118"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="7bb8b-103">全球库存核算分类帐</span><span class="sxs-lookup"><span data-stu-id="7bb8b-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7bb8b-104">全球库存核算具有自己的一组分类帐。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="7bb8b-105">每次为相关法人处理与库存相关的交易时，系统都可以根据需要在任意数量的全球库存核算分类帐中对该交易进行核算。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="7bb8b-106">分类帐是借方和贷方度量的登记。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="7bb8b-107">这些度量通过使用成本元素和子分类帐科目进行分类。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="7bb8b-108">全球库存核算分类帐由其货币、日历、惯例以及与法人的关联的组合定义。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="7bb8b-109">若要设置您的全球库存核算分类帐，请转到 **全球库存核算 \> 设置 \> 全球库存核算分类帐**。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="7bb8b-110">对于每个分类帐，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="7bb8b-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="7bb8b-111">**名称** – 输入分类帐的名称。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="7bb8b-112">**描述** – 输入分类帐的描述。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="7bb8b-113">**会计日历** – 指定分类帐的会计日历。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="7bb8b-114">**货币和汇率类型** – 使用此快速选项卡上的字段选择分类帐使用的记帐币种和汇率类型。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="7bb8b-115">您选择的货币可能与法人使用的货币不同。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="7bb8b-116">在全球库存核算中，用户可以根据需要定义尽可能多的成本计算分类帐。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="7bb8b-117">全球库存核算支持多种货币和多种估价的库存核算。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="7bb8b-118">设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="7bb8b-118">Set the following fields:</span></span>

    - <span data-ttu-id="7bb8b-119">**货币** – 选择用于维护与库存相关的值的成本计算货币。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="7bb8b-120">这些值包括库存价值、所售货物成本、在途库存和各种差异。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="7bb8b-121">**汇率类型** – 选择系统应用于以交易货币和物料的标准成本将交易金额转换为成本计算货币的汇率。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="7bb8b-122">**惯例名称** – 指定惯例。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="7bb8b-123">惯例是一系列策略，用于确定如何在此分类帐中核算成本。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="7bb8b-124">**法人** – 分类帐将对过帐到选定法人的单据进行核算。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="7bb8b-125">**启动** – 选择是否应根据分类帐中的货币和惯例处理在创建分类帐之前创建的库存交易。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="7bb8b-126">选择以下值之一：</span><span class="sxs-lookup"><span data-stu-id="7bb8b-126">Select one of the following values:</span></span>

    - <span data-ttu-id="7bb8b-127">**已启用** – 分类帐应处理在创建分类帐之前创建的交易。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="7bb8b-128">**已停用** – 分类帐应仅处理在创建分类帐之后创建的交易。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7bb8b-129">在输入新单据后，您将 **无法** 返回并设置此字段。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="7bb8b-130">**状态** – 系统自动将新创建的分类帐状态设置为 *准备*。</span><span class="sxs-lookup"><span data-stu-id="7bb8b-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
