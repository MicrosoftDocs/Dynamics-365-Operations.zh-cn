---
title: 将计算添加到产品配置模型
description: 该过程显示如何添加新计算到产品配置模型。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49d09a3544631960e3f6b292dbdd8927dd499f07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987046"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a><span data-ttu-id="b578e-103">将计算添加到产品配置模型</span><span class="sxs-lookup"><span data-stu-id="b578e-103">Add a calculation to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b578e-104">该过程显示如何添加新计算到产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="b578e-104">This procedure shows how to add a new calculation to a product configuration model.</span></span> <span data-ttu-id="b578e-105">它显示如何通过使用“If”运算符将白色扬声器高度设置为 10，将所有其他完工机柜设置为 15 来创建逻辑表达式。</span><span class="sxs-lookup"><span data-stu-id="b578e-105">It shows how you can create a logical expression using the "If" operator to set a speaker height to 10 for white speakers and 15 for all other cabinet finishes.</span></span> <span data-ttu-id="b578e-106">该过程使用演示公司 USMF 的高端扬声器组件。</span><span class="sxs-lookup"><span data-stu-id="b578e-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="add-a-calculation"></a><span data-ttu-id="b578e-107">添加一个计算</span><span class="sxs-lookup"><span data-stu-id="b578e-107">Add a calculation</span></span>

## <a name="create-calculation-expression"></a><span data-ttu-id="b578e-108">创建计算表达式</span><span class="sxs-lookup"><span data-stu-id="b578e-108">Create calculation expression</span></span>
1. <span data-ttu-id="b578e-109">单击“编辑表达式”。</span><span class="sxs-lookup"><span data-stu-id="b578e-109">Click Edit expression.</span></span>
2. <span data-ttu-id="b578e-110">在“约束体”字段中，输入“如果[完工机柜==“白色”，10, 15]”。</span><span class="sxs-lookup"><span data-stu-id="b578e-110">In the ConstraintBody field, enter 'If[CabinetFinish=="White", 10, 15]'.</span></span>
3. <span data-ttu-id="b578e-111">单击“验证”。</span><span class="sxs-lookup"><span data-stu-id="b578e-111">Click Validate.</span></span>
4. <span data-ttu-id="b578e-112">单击“关闭”。</span><span class="sxs-lookup"><span data-stu-id="b578e-112">Click Close.</span></span>
5. <span data-ttu-id="b578e-113">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="b578e-113">Click OK.</span></span>

