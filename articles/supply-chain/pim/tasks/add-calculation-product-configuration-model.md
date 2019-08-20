---
title: 将计算添加到产品配置模型
description: 该过程显示如何添加新计算到产品配置模型。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39450b5aef2fb7b57492a52011f4b0db9dc8ff2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845033"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="21531-103">将计算添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="21531-103">Add a calculation to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="21531-104">该过程显示如何添加新计算到产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="21531-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="21531-105">它显示如何通过使用“If”运算符将白色扬声器高度设置为 10，将所有其他完工机柜设置为 15 来创建逻辑表达式。</span><span class="sxs-lookup"><span data-stu-id="21531-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="21531-106">该过程使用演示公司 USMF 的高端扬声器组件。</span><span class="sxs-lookup"><span data-stu-id="21531-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="21531-107">添加一个计算</span><span class="sxs-lookup"><span data-stu-id="21531-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="21531-108">创建计算表达式</span><span class="sxs-lookup"><span data-stu-id="21531-108">Create calculation expression</span></span>
1. <span data-ttu-id="21531-109">单击“编辑表达式”。</span><span class="sxs-lookup"><span data-stu-id="21531-109">Click Edit expression.</span></span>
2. <span data-ttu-id="21531-110">在“约束体”字段中，输入“如果[完工机柜==“白色”，10, 15]”。</span><span class="sxs-lookup"><span data-stu-id="21531-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="21531-111">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="21531-111">Click Validate.</span></span>
4. <span data-ttu-id="21531-112">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="21531-112">Click Close.</span></span>
5. <span data-ttu-id="21531-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="21531-113">Click OK.</span></span>

