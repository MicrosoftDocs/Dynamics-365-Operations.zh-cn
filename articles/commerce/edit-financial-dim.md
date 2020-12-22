---
title: 编辑零售交易记录的财务维度
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录的财务维度。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: e26bd4eb53fa44330f15c7cda004cb3d19dfec6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458566"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a><span data-ttu-id="07155-103">编辑零售交易记录的财务维度</span><span class="sxs-lookup"><span data-stu-id="07155-103">Edit financial dimensions for retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07155-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中编辑零售交易记录的财务维度。</span><span class="sxs-lookup"><span data-stu-id="07155-104">This topic describes how to edit financial dimensions for retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="edit-financial-dimensions"></a><span data-ttu-id="07155-105">编辑财务维度</span><span class="sxs-lookup"><span data-stu-id="07155-105">Edit financial dimensions</span></span>

<span data-ttu-id="07155-106">要在 Commerce Headquarters 中编辑零售交易记录的财务维度，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="07155-106">To edit financial dimensions for retail transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="07155-107">打开 **用于集成应用程序的财务维度配置** 页面。</span><span class="sxs-lookup"><span data-stu-id="07155-107">Open the **Financial dimensions configuration for integrating applications** page.</span></span>
1. <span data-ttu-id="07155-108">选择有效的 **默认维度集成** 记录。</span><span class="sxs-lookup"><span data-stu-id="07155-108">Select the active **Default dimensions integration** record.</span></span>
1. <span data-ttu-id="07155-109">在 **财务维度** 快速选项卡上，确保您要在 Excel 工作表中编辑的所有维度都存在于 **已选择** 列表中。</span><span class="sxs-lookup"><span data-stu-id="07155-109">On the **Financial dimensions** FastTab, make sure that all the dimensions that you want to edit in the Excel worksheet are present in the **Selected** list.</span></span> <span data-ttu-id="07155-110">有关详细信息，请参阅[数据实体](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities)。</span><span class="sxs-lookup"><span data-stu-id="07155-110">For more information, see [Data entities](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).</span></span>
1. <span data-ttu-id="07155-111">从 **商店财务** 工作区的 **对帐单** 页面、**零售交易记录** 页面或 **交易记录验证失败** 磁贴中下载并打开 Excel 文件。</span><span class="sxs-lookup"><span data-stu-id="07155-111">Download and open the Excel file from the **Statements** page, the **Retail transactions** page, or the **Transaction validation failures** tile in the **Store financials** workspace.</span></span>
1. <span data-ttu-id="07155-112">要更改交易记录财务维度，请选择 **设计**，然后选择 **交易记录（可审计）** 行旁边的铅笔符号。</span><span class="sxs-lookup"><span data-stu-id="07155-112">To change the transaction financial dimension, select **Design**, and then select the pencil symbol next to the **Transaction (auditable)** row.</span></span>
1. <span data-ttu-id="07155-113">找到并选择 **FinancialDimensionDisplayValue** 字段，在 Excel 工作表的标头部分中选择一个单元格，然后选择 **添加标签**。</span><span class="sxs-lookup"><span data-stu-id="07155-113">Find and select the **FinancialDimensionDisplayValue** field, select a cell in the header part of the Excel worksheet, and then select **Add label**.</span></span>
1. <span data-ttu-id="07155-114">选择在上一步中选择的单元格下方的一个单元格，选择 **添加值**，然后选择 **刷新**。</span><span class="sxs-lookup"><span data-stu-id="07155-114">Select a cell below the cell that you selected in the previous step, select **Add Value**, and then select **Refresh**.</span></span> <span data-ttu-id="07155-115">将财务维度添加到 Excel 工作表中，然后可以对其进行编辑并发布。</span><span class="sxs-lookup"><span data-stu-id="07155-115">The financial dimensions are added to the Excel worksheet, and they can then be edited and published.</span></span>
1. <span data-ttu-id="07155-116">要更改交易记录行上的维度，请选择 **销售交易记录（可审计）** 行，选择铅笔符号，然后重复步骤 6 和 7。</span><span class="sxs-lookup"><span data-stu-id="07155-116">To change the dimensions on the transaction lines, select the **Sales transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>
1. <span data-ttu-id="07155-117">要更改付款行上的维度，请选择 **付款交易记录（可审计）** 行，选择铅笔符号，然后重复步骤 6 和 7。</span><span class="sxs-lookup"><span data-stu-id="07155-117">To change the dimensions on the payment lines, select the **Payment transactions (auditable)** row, select the pencil symbol, and then repeat steps 6 and 7.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="07155-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="07155-118">Additional resources</span></span>

[<span data-ttu-id="07155-119">编辑并审计现金和结转及现金管理交易记录</span><span class="sxs-lookup"><span data-stu-id="07155-119">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="07155-120">编辑并审计在线订单和异步客户订单交易记录</span><span class="sxs-lookup"><span data-stu-id="07155-120">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="07155-121">创建 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="07155-121">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="07155-122">将字段添加到 Excel 工作簿以编辑零售交易记录</span><span class="sxs-lookup"><span data-stu-id="07155-122">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
