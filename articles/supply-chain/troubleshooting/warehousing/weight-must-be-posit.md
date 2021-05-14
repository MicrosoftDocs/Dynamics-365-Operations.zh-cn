---
title: 重量必须为正
description: 重量必须为正
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924295"
---
# <a name="weight-must-be-positive"></a><span data-ttu-id="1bb45-103">重量必须为正</span><span class="sxs-lookup"><span data-stu-id="1bb45-103">Weight must be positive</span></span>

<span data-ttu-id="1bb45-104">错误代码：WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="1bb45-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="1bb45-105">故障特征</span><span class="sxs-lookup"><span data-stu-id="1bb45-105">Symptoms</span></span>

<span data-ttu-id="1bb45-106">系统将显示以下错误消息：</span><span class="sxs-lookup"><span data-stu-id="1bb45-106">The system shows the following error message:</span></span>

> <span data-ttu-id="1bb45-107">重量必须为正。</span><span class="sxs-lookup"><span data-stu-id="1bb45-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="1bb45-108">原因</span><span class="sxs-lookup"><span data-stu-id="1bb45-108">Cause</span></span>

<span data-ttu-id="1bb45-109">**毛重** 字段设置为 *0*（零）或负值。</span><span class="sxs-lookup"><span data-stu-id="1bb45-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="1bb45-110">解决方法</span><span class="sxs-lookup"><span data-stu-id="1bb45-110">Resolution</span></span>

<span data-ttu-id="1bb45-111">要指定重量，请执行以下步骤之一。</span><span class="sxs-lookup"><span data-stu-id="1bb45-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="1bb45-112">在 **毛重** 字段中，设置一个值。</span><span class="sxs-lookup"><span data-stu-id="1bb45-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="1bb45-113">然后在下拉列表中选择一个单位。</span><span class="sxs-lookup"><span data-stu-id="1bb45-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="1bb45-114">选择 **获取系统重量** 来计算 **毛重** 值。</span><span class="sxs-lookup"><span data-stu-id="1bb45-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>
