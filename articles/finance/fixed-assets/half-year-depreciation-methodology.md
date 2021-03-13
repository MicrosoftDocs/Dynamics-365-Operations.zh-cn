---
title: 半年折旧惯例方法
description: 本主题介绍固定资产用于计算使用半年惯例的折旧的方法，即计算资产第一年到最后一年服务期间的六个月折旧。
author: moaamer
manager: Ann Beebe
ms.date: 08/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-17
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 6ec4c3a0bd86e15ee015fc2e2c49c92b035243b6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009285"
---
# <a name="half-year-depreciation-convention-methodology"></a><span data-ttu-id="681a4-103">半年折旧惯例方法</span><span class="sxs-lookup"><span data-stu-id="681a4-103">Half-year depreciation convention methodology</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="681a4-104">此主题介绍固定资产中用于计算使用半年惯例的折旧的方法。</span><span class="sxs-lookup"><span data-stu-id="681a4-104">This topic describes the method that is used in fixed assets to calculate depreciation using the half-year convention.</span></span> <span data-ttu-id="681a4-105">半年惯例计算资产第一年到最后一年服务期间的六个月折旧。</span><span class="sxs-lookup"><span data-stu-id="681a4-105">The half-year convention calculates six months of depreciation during an asset’s first and last year of service.</span></span> <span data-ttu-id="681a4-106">有关折旧惯例的详细信息，请参阅[折旧法和惯例](Fixed-asset-depreciation-conventions.md)。</span><span class="sxs-lookup"><span data-stu-id="681a4-106">For more information about depreciation conventions, see [Depreciation methods and conventions](Fixed-asset-depreciation-conventions.md).</span></span> 

<span data-ttu-id="681a4-107">当您使用六个月折旧惯例时，系统使用购置年份或资产开始服务的年份，然后计算从该年开始的五年折旧，然后增加六个月。</span><span class="sxs-lookup"><span data-stu-id="681a4-107">When you use the six-month depreciation convention, the system uses the acquisition year or the year that the asset was placed in service, then calculates five years of depreciation from that year, and then adds six months.</span></span> <span data-ttu-id="681a4-108">为了阐释此过程，假设一个资产的购置价格为 50,000，服务时间为 2020 年 4 月。</span><span class="sxs-lookup"><span data-stu-id="681a4-108">To illustrate this process, consider an asset that was acquired for the price of 50,000, and placed in service in April 2020.</span></span> <span data-ttu-id="681a4-109">再假设资产的服务寿命为五年。</span><span class="sxs-lookup"><span data-stu-id="681a4-109">Also assume that the asset has a five-year service life.</span></span>

<span data-ttu-id="681a4-110">第一个服务年份在 2020 年 12 月结束，这意味着资产的前五年服务寿命结束时间为 2024 年 12 月。</span><span class="sxs-lookup"><span data-stu-id="681a4-110">The first year of service will conclude in December 2020, which means the end of the asset’s five-year service life will be December 2024.</span></span> <span data-ttu-id="681a4-111">半年折旧惯例将向资产的寿命添加六个月，这意味着其服务将在 2025 年 6 月结束。</span><span class="sxs-lookup"><span data-stu-id="681a4-111">The half-year depreciation convention will add six months to the asset’s life, which means its service life will end in June 2025.</span></span> 

> <span data-ttu-id="681a4-112">年折旧 50,000/5 = 10,000，月折旧 10,000/12 = 833.33</span><span class="sxs-lookup"><span data-stu-id="681a4-112">Yearly depreciation 50,000/5 = 10,000 monthly depreciation 10,000/12 = 833.33</span></span> <br>
> <span data-ttu-id="681a4-113">第一年折旧 10,000/2 = 5,000，后续月折旧 5,000/9 = 555.56</span><span class="sxs-lookup"><span data-stu-id="681a4-113">First year depreciation 10,000/2 = 5,000  and the subsequent monthly depreciation 5,000/9 = 555.56</span></span>

   <span data-ttu-id="681a4-114">[![半年折旧惯例的折旧计划](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span><span class="sxs-lookup"><span data-stu-id="681a4-114">[![Depreciation schedule for half-year depreciation convention](./media/half-yr-dprectn-cnvntn.png)](./media/half-yr-dprectn-cnvntn.png)</span></span>

<span data-ttu-id="681a4-115">半年惯例增加的延长后折旧期的折旧分配更精确。</span><span class="sxs-lookup"><span data-stu-id="681a4-115">The extended depreciation periods that are added by the half-year convention provide more accurate allocation of depreciation.</span></span> <span data-ttu-id="681a4-116">六个月惯例提供的折旧费用更平均，这对损益表中的报告非常有用。</span><span class="sxs-lookup"><span data-stu-id="681a4-116">The six-month convention represents depreciation expenses more equally, which is useful for reporting on the profit and loss statement.</span></span>
