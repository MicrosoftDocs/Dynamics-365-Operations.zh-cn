---
title: 导入需求预测记录时，无法更新预测的单位成本
description: 当您使用数据实体导入需求预测记录时，现有记录的成本价不会更新，以与导入的数据匹配。
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c8ea8322a6c7bafe2dfcaaee3e9989f753c85e2a
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026307"
---
# <a name="you-cant-update-the-forecasted-unit-cost-when-you-import-demand-forecast-records"></a><span data-ttu-id="eed9d-103">导入需求预测记录时，无法更新预测的单位成本</span><span class="sxs-lookup"><span data-stu-id="eed9d-103">You can't update the forecasted unit cost when you import demand forecast records</span></span>

<span data-ttu-id="eed9d-104">知识库编号：4614109</span><span class="sxs-lookup"><span data-stu-id="eed9d-104">KB number: 4614109</span></span>

## <a name="symptoms"></a><span data-ttu-id="eed9d-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="eed9d-105">Symptoms</span></span>

<span data-ttu-id="eed9d-106">当您使用数据实体导入需求预测记录时，现有记录的 **预测单位成本** 值不会更新，以与导入的数据匹配。</span><span class="sxs-lookup"><span data-stu-id="eed9d-106">When you use data entities to import demand forecast records, the **Forecasted unit cost** value for existing records isn't updated so that it matches the imported data.</span></span>

## <a name="cause"></a><span data-ttu-id="eed9d-107">原因</span><span class="sxs-lookup"><span data-stu-id="eed9d-107">Cause</span></span>

<span data-ttu-id="eed9d-108">**预测单位成本** 是一个只读字段。</span><span class="sxs-lookup"><span data-stu-id="eed9d-108">**Forecasted unit cost** is a read-only field.</span></span> <span data-ttu-id="eed9d-109">此值基于产品单位成本，不能直接通过导入设置。</span><span class="sxs-lookup"><span data-stu-id="eed9d-109">The value is based on the product unit cost and can't be set directly through import.</span></span>

## <a name="resolution"></a><span data-ttu-id="eed9d-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="eed9d-110">Resolution</span></span>

<span data-ttu-id="eed9d-111">由于此字段是只读字段，因此您无法导入此字段的值。</span><span class="sxs-lookup"><span data-stu-id="eed9d-111">Because the field is read only, you can't import values for it.</span></span> <span data-ttu-id="eed9d-112">此值将根据现有业务逻辑计算得出。</span><span class="sxs-lookup"><span data-stu-id="eed9d-112">The value will be calculated according to the existing business logic.</span></span>
