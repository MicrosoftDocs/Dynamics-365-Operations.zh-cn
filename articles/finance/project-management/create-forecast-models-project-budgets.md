---
title: 创建项目预算的预测模型
description: 本主题描述如何为剩余预算创建预测模型。
author: RadhikaRS
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 07e540f23a668b40a54906a67d87552fe991825a
ms.sourcegitcommit: 5de75c61c33e57c813944f1ab6100aceb020d432
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/29/2020
ms.locfileid: "3321771"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="835c7-103">创建项目预算的预测模型</span><span class="sxs-lookup"><span data-stu-id="835c7-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="835c7-104">本主题描述如何为剩余预算创建预测模型。</span><span class="sxs-lookup"><span data-stu-id="835c7-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="835c7-105">受预算控制的项目使用两种类型的预算：原始预算和剩余预算。</span><span class="sxs-lookup"><span data-stu-id="835c7-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="835c7-106">创建项目预算时，必须指定在**预测模型**页面中创建的原始和剩余预算预测模型。</span><span class="sxs-lookup"><span data-stu-id="835c7-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="835c7-107">当您提交项目预算时，创建基于指定模型的项目预算。</span><span class="sxs-lookup"><span data-stu-id="835c7-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="835c7-108">用于预算控制的预测模型不能具有子模型，也不能用作子模型。</span><span class="sxs-lookup"><span data-stu-id="835c7-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="835c7-109">选择**项目管理与会计** > **设置** > **预测**  > **预测模型**。</span><span class="sxs-lookup"><span data-stu-id="835c7-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="835c7-110">选择**新建**以创建新的预测模型，然后输入新模型的模型 ID 号和名称。</span><span class="sxs-lookup"><span data-stu-id="835c7-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="835c7-111">将**已停止**选项设置为**是**，以防止对预测模型的预测行进行任何更改。</span><span class="sxs-lookup"><span data-stu-id="835c7-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="835c7-112">如果与模型关联的预测行应在总账中生成现金流预测，请将**包括在现金流预测中**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="835c7-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="835c7-113">要将项目日期用作发票日期，请将**预测发票日期**设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="835c7-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="835c7-114">在**预算类型**字段中，选择以下模型类型之一：</span><span class="sxs-lookup"><span data-stu-id="835c7-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="835c7-115">**原始预算**：使用在创建和批准初始预算时承诺的原始预算金额。</span><span class="sxs-lookup"><span data-stu-id="835c7-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="835c7-116">**剩余预算**：在项目生命周期内使用剩余预算金额。</span><span class="sxs-lookup"><span data-stu-id="835c7-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="835c7-117">此预算模型的余额减去实际交易记录，它根据预算版本增加或减少。</span><span class="sxs-lookup"><span data-stu-id="835c7-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="835c7-118">**结转**：使用项目的结转预算金额。</span><span class="sxs-lookup"><span data-stu-id="835c7-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="835c7-119">结转是一个可选的流程，运行结转以将未使用的预算金额从一个会计年度转移到另一个会计年度。</span><span class="sxs-lookup"><span data-stu-id="835c7-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="835c7-120">根据需要设置以下选项：</span><span class="sxs-lookup"><span data-stu-id="835c7-120">Set the following options as required:</span></span>

   - <span data-ttu-id="835c7-121">启用**预测发票日期**以使用项目日期作为发票日期。</span><span class="sxs-lookup"><span data-stu-id="835c7-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="835c7-122">启用**根据 WIP 进行预测**以基于在建项目(WIP) 进行预测，然后选择 WIP 的类型。</span><span class="sxs-lookup"><span data-stu-id="835c7-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="835c7-123">您可以将默认的**预算类型**保留为**无**，或输入新的类型。</span><span class="sxs-lookup"><span data-stu-id="835c7-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="835c7-124">更改记录后，无法更改预算类型。</span><span class="sxs-lookup"><span data-stu-id="835c7-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="835c7-125">如果您更改默认预算类型，则所有其他选项将无法更新，并且您无法重复使用此预测模型。</span><span class="sxs-lookup"><span data-stu-id="835c7-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

