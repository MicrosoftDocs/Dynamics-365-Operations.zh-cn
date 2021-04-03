---
title: 筛选频率生成来源
description: 本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 238cd5da750d815c904090cc9002e3d1a5d2bcc7
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464566"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="83f98-103">筛选频率生成来源</span><span class="sxs-lookup"><span data-stu-id="83f98-103">Screening frequency generate from</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="83f98-104">本主题介绍 Dynamics 365 Human Resources 的筛选频率生成来源选项集。</span><span class="sxs-lookup"><span data-stu-id="83f98-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="83f98-105">物理名称：mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="83f98-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="83f98-106">此枚举提供用于确定下一次所需筛选的计算开始日期的值选项集。</span><span class="sxs-lookup"><span data-stu-id="83f98-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="83f98-107">值</span><span class="sxs-lookup"><span data-stu-id="83f98-107">Value</span></span> | <span data-ttu-id="83f98-108">标签</span><span class="sxs-lookup"><span data-stu-id="83f98-108">Label</span></span> | <span data-ttu-id="83f98-109">说明</span><span class="sxs-lookup"><span data-stu-id="83f98-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="83f98-110">200000000 未选择</span><span class="sxs-lookup"><span data-stu-id="83f98-110">200000000 Not selected</span></span> | <span data-ttu-id="83f98-111">未选择值。</span><span class="sxs-lookup"><span data-stu-id="83f98-111">No value has been selected.</span></span> |
| <span data-ttu-id="83f98-112">200000001 完成日期</span><span class="sxs-lookup"><span data-stu-id="83f98-112">200000001 Date completed</span></span> | <span data-ttu-id="83f98-113">从上一次筛选完成日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="83f98-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="83f98-114">200000002 必需日期</span><span class="sxs-lookup"><span data-stu-id="83f98-114">200000002 Date required</span></span> | <span data-ttu-id="83f98-115">从上一次必需筛选日期开始计算。</span><span class="sxs-lookup"><span data-stu-id="83f98-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="83f98-116">请参阅</span><span class="sxs-lookup"><span data-stu-id="83f98-116">See also</span></span>

[<span data-ttu-id="83f98-117">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="83f98-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="83f98-118">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="83f98-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]