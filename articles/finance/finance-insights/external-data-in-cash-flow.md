---
title: 在现金流预测中使用外部数据（预览）
description: 本主题介绍了要将外部数据输入或导入到现金流预测中必须完成的设置步骤。
author: rcarlson
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 66bdb8bd638859bb4fc5565e3f12a8f671addcff
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186682"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="26a16-103">在现金流预测中使用外部数据（预览）</span><span class="sxs-lookup"><span data-stu-id="26a16-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="26a16-104">可以将外部数据输入或导入现金流预测中。</span><span class="sxs-lookup"><span data-stu-id="26a16-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="26a16-105">本主题描述了特定于外部数据的使用和将外部数据添加到现金流预测中的设置步骤。</span><span class="sxs-lookup"><span data-stu-id="26a16-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="26a16-106">外部数据设置</span><span class="sxs-lookup"><span data-stu-id="26a16-106">External data setup</span></span>

<span data-ttu-id="26a16-107">使用 **现金流预测设置** 页面（**现金和银行管理 \> 现金流预测**）上的 **外部源** 输入支持在现金流预测中使用外部数据的设置。</span><span class="sxs-lookup"><span data-stu-id="26a16-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="26a16-108">有关此设置的详细信息，请参阅[现金流预测](../cash-bank-management/cash-flow-forecasting.md)。</span><span class="sxs-lookup"><span data-stu-id="26a16-108">For more information about the setup, see [Cash flow forecasting](../cash-bank-management/cash-flow-forecasting.md).</span></span>

<span data-ttu-id="26a16-109">要为现金流预测输入外部数据，可以使用“在 Excel 中打开”体验来输入和修改外部数据。</span><span class="sxs-lookup"><span data-stu-id="26a16-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="26a16-110">选择 **外部数据** 按钮，然后选择 **添加外部数据** 或 **编辑现有外部数据**。</span><span class="sxs-lookup"><span data-stu-id="26a16-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="26a16-111">Microsoft Excel 文件打开后，可以在以下字段中输入信息：</span><span class="sxs-lookup"><span data-stu-id="26a16-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="26a16-112">**分录 ID**</span><span class="sxs-lookup"><span data-stu-id="26a16-112">**Entry ID**</span></span>
- <span data-ttu-id="26a16-113">**描述**（可选）</span><span class="sxs-lookup"><span data-stu-id="26a16-113">**Description** (optional)</span></span>
- <span data-ttu-id="26a16-114">**外部源名称** – 在设置 Finance Insights 时定义的列表中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="26a16-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="26a16-115">**法人**</span><span class="sxs-lookup"><span data-stu-id="26a16-115">**Legal Entity**</span></span>
- <span data-ttu-id="26a16-116">**日期**</span><span class="sxs-lookup"><span data-stu-id="26a16-116">**Date**</span></span>
- <span data-ttu-id="26a16-117">**金额(交易币种)**</span><span class="sxs-lookup"><span data-stu-id="26a16-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="26a16-118">**币种代码**</span><span class="sxs-lookup"><span data-stu-id="26a16-118">**Currency Code**</span></span>
- <span data-ttu-id="26a16-119">**默认维度**（可选）</span><span class="sxs-lookup"><span data-stu-id="26a16-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="26a16-120">**文档编号**（可选）</span><span class="sxs-lookup"><span data-stu-id="26a16-120">**Document number** (optional)</span></span>
- <span data-ttu-id="26a16-121">**科目编号**（可选）</span><span class="sxs-lookup"><span data-stu-id="26a16-121">**Account number** (optional)</span></span>
- <span data-ttu-id="26a16-122">**科目名称**（可选）</span><span class="sxs-lookup"><span data-stu-id="26a16-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="26a16-123">使用数据管理框架导入外部数据</span><span class="sxs-lookup"><span data-stu-id="26a16-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="26a16-124">可以使用 **数据管理** 工作区和名称为 **现金流预测外部源输入** 的实体为现金流预测导入外部数据。</span><span class="sxs-lookup"><span data-stu-id="26a16-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="26a16-125">此外，如果必须将设置数据从一个环境移动到另一个环境，可为所需设置表使用以下实体：</span><span class="sxs-lookup"><span data-stu-id="26a16-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="26a16-126">现金流量预测外部源设置</span><span class="sxs-lookup"><span data-stu-id="26a16-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="26a16-127">现金流量预测外部源法人设置</span><span class="sxs-lookup"><span data-stu-id="26a16-127">Cash flow forecast external source legal entity setup</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
