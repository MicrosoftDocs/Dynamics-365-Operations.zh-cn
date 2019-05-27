---
title: 导入 ISO20022 贷方转帐配置
description: 此过程显示如何导入供应商付款电子申报配置。
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fbd2e39f488696ebe8db5579ed88595e246ce97
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573109"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="46887-103">导入 ISO20022 贷方转帐配置</span><span class="sxs-lookup"><span data-stu-id="46887-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46887-104">此过程显示如何导入供应商付款电子申报配置。</span><span class="sxs-lookup"><span data-stu-id="46887-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="46887-105">以德国 ISO 20022 贷方转帐格式为例。</span><span class="sxs-lookup"><span data-stu-id="46887-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="46887-106">此过程可用于其他可用电子申报格式。</span><span class="sxs-lookup"><span data-stu-id="46887-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="46887-107">此任务是使用演示数据公司 DEMF 创建的，但是您可以使用任何演示数据公司完成此任务。</span><span class="sxs-lookup"><span data-stu-id="46887-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="46887-108">这是五个共同用于演示使用电子申报配置的供应商付款流程的任务中的第一个。</span><span class="sxs-lookup"><span data-stu-id="46887-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="46887-109">此过程针对 Dynamics 365 for Operations 版本 1611 中增加的一项功能。</span><span class="sxs-lookup"><span data-stu-id="46887-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="46887-110">转到“组织管理”>“工作区”>“电子申报”。</span><span class="sxs-lookup"><span data-stu-id="46887-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="46887-111">在可用配置提供商列表中，选择“Microsoft”。</span><span class="sxs-lookup"><span data-stu-id="46887-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="46887-112">单击“设置有效”。</span><span class="sxs-lookup"><span data-stu-id="46887-112">Click Set active.</span></span>
4. <span data-ttu-id="46887-113">单击“存储库”。</span><span class="sxs-lookup"><span data-stu-id="46887-113">Click Repositories.</span></span>
5. <span data-ttu-id="46887-114">单击“打开”。</span><span class="sxs-lookup"><span data-stu-id="46887-114">Click Open.</span></span>
6. <span data-ttu-id="46887-115">单击“显示筛选器”。</span><span class="sxs-lookup"><span data-stu-id="46887-115">Click Show filters.</span></span>
7. <span data-ttu-id="46887-116">应用以下筛选器：使用“开头为”筛选器运算符在“配置名称”字段中输入筛选器值“ISO20022 贷方转帐（德国）”。</span><span class="sxs-lookup"><span data-stu-id="46887-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="46887-117">也可以在列表中查找配置，选择该配置，然后将其移至“导入任务”。</span><span class="sxs-lookup"><span data-stu-id="46887-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="46887-118">单击“导入”。</span><span class="sxs-lookup"><span data-stu-id="46887-118">Click Import.</span></span>
    * <span data-ttu-id="46887-119">如果导入按钮没出现，表示该配置文件已经被导入了。</span><span class="sxs-lookup"><span data-stu-id="46887-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="46887-120">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="46887-120">Click Yes.</span></span>

