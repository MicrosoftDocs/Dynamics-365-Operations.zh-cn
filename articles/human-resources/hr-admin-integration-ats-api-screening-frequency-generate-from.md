---
title: 筛选频率生成来源
description: 本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054084"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="48b49-103">筛选频率生成来源</span><span class="sxs-lookup"><span data-stu-id="48b49-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="48b49-104">本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。</span><span class="sxs-lookup"><span data-stu-id="48b49-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="48b49-105">物理名称：mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="48b49-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="48b49-106">此枚举提供用于确定下一次所需筛选的计算开始日期的值选项集。</span><span class="sxs-lookup"><span data-stu-id="48b49-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="48b49-107">值</span><span class="sxs-lookup"><span data-stu-id="48b49-107">Value</span></span> | <span data-ttu-id="48b49-108">标签</span><span class="sxs-lookup"><span data-stu-id="48b49-108">Label</span></span> | <span data-ttu-id="48b49-109">说明</span><span class="sxs-lookup"><span data-stu-id="48b49-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="48b49-110">200000000 未选择</span><span class="sxs-lookup"><span data-stu-id="48b49-110">200000000 Not selected</span></span> | <span data-ttu-id="48b49-111">未选择值。</span><span class="sxs-lookup"><span data-stu-id="48b49-111">No value has been selected.</span></span> |
| <span data-ttu-id="48b49-112">200000001 完成日期</span><span class="sxs-lookup"><span data-stu-id="48b49-112">200000001 Date completed</span></span> | <span data-ttu-id="48b49-113">从上一次筛选完成日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="48b49-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="48b49-114">200000002 必需日期</span><span class="sxs-lookup"><span data-stu-id="48b49-114">200000002 Date required</span></span> | <span data-ttu-id="48b49-115">从上一次必需筛选日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="48b49-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="48b49-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="48b49-116">See also</span></span>

[<span data-ttu-id="48b49-117">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="48b49-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="48b49-118">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="48b49-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]