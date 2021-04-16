---
title: 在现金流预测中使用外部数据（预览）
description: 本主题介绍了要将外部数据输入或导入到现金流预测中必须完成的设置步骤。
author: rcarlson
ms.date: 05/01/2020
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
ms.openlocfilehash: 7d5768a6cb2b3623333fab93a42ac5840e87ec68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818601"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="50b54-103">在现金流预测中使用外部数据（预览）</span><span class="sxs-lookup"><span data-stu-id="50b54-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="50b54-104">可以将外部数据输入或导入现金流预测中。</span><span class="sxs-lookup"><span data-stu-id="50b54-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="50b54-105">本主题描述了特定于外部数据的使用和将外部数据添加到现金流预测中的设置步骤。</span><span class="sxs-lookup"><span data-stu-id="50b54-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="50b54-106">外部数据设置</span><span class="sxs-lookup"><span data-stu-id="50b54-106">External data setup</span></span>

<span data-ttu-id="50b54-107">使用 **现金流预测设置** 页面（**现金和银行管理 \> 现金流预测**）上的 **外部源** 输入支持在现金流预测中使用外部数据的设置。</span><span class="sxs-lookup"><span data-stu-id="50b54-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="50b54-108">有关此设置的详细信息，请参阅[现金流预测](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting)。</span><span class="sxs-lookup"><span data-stu-id="50b54-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="50b54-109">要为现金流预测输入外部数据，可以使用“在 Excel 中打开”体验来输入和修改外部数据。</span><span class="sxs-lookup"><span data-stu-id="50b54-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="50b54-110">选择 **外部数据** 按钮，然后选择 **添加外部数据** 或 **编辑现有外部数据**。</span><span class="sxs-lookup"><span data-stu-id="50b54-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="50b54-111">Microsoft Excel 文件打开后，可以在以下字段中输入信息：</span><span class="sxs-lookup"><span data-stu-id="50b54-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="50b54-112">**分录 ID**</span><span class="sxs-lookup"><span data-stu-id="50b54-112">**Entry ID**</span></span>
- <span data-ttu-id="50b54-113">**描述**（可选）</span><span class="sxs-lookup"><span data-stu-id="50b54-113">**Description** (optional)</span></span>
- <span data-ttu-id="50b54-114">**外部源名称** – 在设置 Finance Insights 时定义的列表中选择一个值。</span><span class="sxs-lookup"><span data-stu-id="50b54-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="50b54-115">**法人**</span><span class="sxs-lookup"><span data-stu-id="50b54-115">**Legal Entity**</span></span>
- <span data-ttu-id="50b54-116">**日期**</span><span class="sxs-lookup"><span data-stu-id="50b54-116">**Date**</span></span>
- <span data-ttu-id="50b54-117">**金额(交易币种)**</span><span class="sxs-lookup"><span data-stu-id="50b54-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="50b54-118">**币种代码**</span><span class="sxs-lookup"><span data-stu-id="50b54-118">**Currency Code**</span></span>
- <span data-ttu-id="50b54-119">**默认维度**（可选）</span><span class="sxs-lookup"><span data-stu-id="50b54-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="50b54-120">**文档编号**（可选）</span><span class="sxs-lookup"><span data-stu-id="50b54-120">**Document number** (optional)</span></span>
- <span data-ttu-id="50b54-121">**科目编号**（可选）</span><span class="sxs-lookup"><span data-stu-id="50b54-121">**Account number** (optional)</span></span>
- <span data-ttu-id="50b54-122">**科目名称**（可选）</span><span class="sxs-lookup"><span data-stu-id="50b54-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="50b54-123">使用数据管理框架导入外部数据</span><span class="sxs-lookup"><span data-stu-id="50b54-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="50b54-124">可以使用 **数据管理** 工作区和名称为 **现金流预测外部源输入** 的实体为现金流预测导入外部数据。</span><span class="sxs-lookup"><span data-stu-id="50b54-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="50b54-125">此外，如果必须将设置数据从一个环境移动到另一个环境，可为所需设置表使用以下实体：</span><span class="sxs-lookup"><span data-stu-id="50b54-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="50b54-126">现金流量预测外部源设置</span><span class="sxs-lookup"><span data-stu-id="50b54-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="50b54-127">现金流量预测外部源法人设置</span><span class="sxs-lookup"><span data-stu-id="50b54-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="50b54-128">隐私声明</span><span class="sxs-lookup"><span data-stu-id="50b54-128">Privacy notice</span></span>
<span data-ttu-id="50b54-129">预览版 (1) 采用的隐私和安全措施可能比 Dynamics 365 Finance and Operations 服务少，(2) 不包含在该服务的服务级别协议 (SLA) 中，(3) 不应用于处理应遵守法律或法规合规性要求的个人数据或其他数据，以及 (4) 享受有限支持。</span><span class="sxs-lookup"><span data-stu-id="50b54-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]