---
title: 了解日期和时间字段
description: 了解在 Microsoft Dynamics 365 Human Resources 中使用日期和时间字段时会发生什么。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: efda2b54f9228ac539e6ba2d18f85bf3ad15a6ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802423"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="54cb3-103">了解日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="54cb3-103">Understand Date and Time fields</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="54cb3-104">**日期和时间** 字段是 Dynamics 365 Human Resources 中的基本概念。</span><span class="sxs-lookup"><span data-stu-id="54cb3-104">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="54cb3-105">了解如何在窗体、Dataverse 和外部源中使用 **日期和时间** 数据非常重要。</span><span class="sxs-lookup"><span data-stu-id="54cb3-105">It's important to understand how to work with **Date and Time** data in forms, Dataverse, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="54cb3-106">了解日期与日期和时间字段数据类型之间的差异</span><span class="sxs-lookup"><span data-stu-id="54cb3-106">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="54cb3-107">**日期和时间** 字段包含时区信息，而 **日期** 字段则不包含。</span><span class="sxs-lookup"><span data-stu-id="54cb3-107">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="54cb3-108">**日期** 字段在任何位置都显示相同信息。</span><span class="sxs-lookup"><span data-stu-id="54cb3-108">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="54cb3-109">当您在 **日期** 字段中输入日期时，Human Resources 会将相同的日期写入数据库。</span><span class="sxs-lookup"><span data-stu-id="54cb3-109">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="54cb3-110">在 **日期和时间** 字段中显示数据时，Human Resources 会根据用户在 **用户选项** 窗体（**通用 > 设置 > 用户选项**）设置的时区调整日期和时间。</span><span class="sxs-lookup"><span data-stu-id="54cb3-110">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="54cb3-111">您在字段中输入的日期和时间信息可能与写入数据库的信息不同。</span><span class="sxs-lookup"><span data-stu-id="54cb3-111">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="54cb3-112">[![用户选项窗体](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-112">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="54cb3-113">了解窗体中的日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="54cb3-113">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="54cb3-114">如果用户的时区未设置为协调世界时 (UTC)，屏幕上显示的 **日期和时间** 数据将与存储在数据库中的数据不同。</span><span class="sxs-lookup"><span data-stu-id="54cb3-114">**Date and Time** data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="54cb3-115">**日期和时间** 字段中的数据始终存储为 UTC。</span><span class="sxs-lookup"><span data-stu-id="54cb3-115">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="54cb3-116">[![工作人员窗体 UTC](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-116">[![Worker form UTC](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="54cb3-117">了解数据库中的日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="54cb3-117">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="54cb3-118">当 Human Resources 将 **日期和时间** 值写入数据库时，它以 UTC 存储数据。</span><span class="sxs-lookup"><span data-stu-id="54cb3-118">When Human Resources writes a **Date and Time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="54cb3-119">这允许用户查看相对于其用户选项中定义的时区的任何 **日期和时间** 数据。</span><span class="sxs-lookup"><span data-stu-id="54cb3-119">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="54cb3-120">在上面的示例中，开始时间是一个时间点，而不是特定日期。</span><span class="sxs-lookup"><span data-stu-id="54cb3-120">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="54cb3-121">通过将登录用户的时区从 GMT +12:00 更改为 GMT UTC，同一记录将显示 04/30/2019 12:00:00 而不是 05/01/2019 12:00:00。</span><span class="sxs-lookup"><span data-stu-id="54cb3-121">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="54cb3-122">在下面的示例中，无论时区如何，员工 000724 的雇用都会同时变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="54cb3-122">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="54cb3-123">该员工将于 GMT 时区的 04/30/2019 进入活动状态，与 GMT+12:00 时区的 05/01/2019 相同。</span><span class="sxs-lookup"><span data-stu-id="54cb3-123">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="54cb3-124">两者都指的是相同时间点而不是特定日期。</span><span class="sxs-lookup"><span data-stu-id="54cb3-124">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="54cb3-125">[![工作人员窗体 GMT](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-125">[![Worker form GMT](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a><span data-ttu-id="54cb3-126">Data Management Framework、Excel、Dataverse 和 Power BI 中的日期和时间数据</span><span class="sxs-lookup"><span data-stu-id="54cb3-126">Date and Time data in Data Management Framework, Excel, Dataverse, and Power BI</span></span> 

<span data-ttu-id="54cb3-127">Data Management Framework、Excel 加载项、Dataverse 和 Power BI 报告的目的都是直接在数据库级别与数据交互。</span><span class="sxs-lookup"><span data-stu-id="54cb3-127">The Data Management Framework, Excel Add-In, Dataverse, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="54cb3-128">由于没有客户端将 **日期和时间** 数据调整到用户的时区，因此所有 **日期和时间** 值均为 UTC，这可能导致在输入或查看数据时出现一些错误的假设。</span><span class="sxs-lookup"><span data-stu-id="54cb3-128">Since there's no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="54cb3-129">通过 DMF、Excel 或 Dataverse 提交的 **日期和时间** 数据被数据库假定为 UTC。</span><span class="sxs-lookup"><span data-stu-id="54cb3-129">**Date and Time** data submitted via DMF, Excel, or Dataverse is assumed to be in UTC by the database.</span></span> <span data-ttu-id="54cb3-130">当提交的 **日期和时间** 值未按预期显示时，这可能会导致一些混淆，因为查看数据的用户没有将其用户时区设置为 UTC。</span><span class="sxs-lookup"><span data-stu-id="54cb3-130">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="54cb3-131">导出数据时，可能会发生相反的情况。</span><span class="sxs-lookup"><span data-stu-id="54cb3-131">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="54cb3-132">导出的 DMF 实体中的 **日期和时间** 数据可能与 Dynamics 客户端中显示的数据不同。</span><span class="sxs-lookup"><span data-stu-id="54cb3-132">The **Date and Time** data in the exported DMF entity can be different than what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="54cb3-133">使用 DMF 等外部源查看或创作数据时，请记住，**日期和时间** 值默认为 UTC，无论用户计算机的时区或其当前的用户时区设置如何。</span><span class="sxs-lookup"><span data-stu-id="54cb3-133">When using external sources like DMF to view or author data, keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="54cb3-134">在不同产品区域显示的同一个记录的示例</span><span class="sxs-lookup"><span data-stu-id="54cb3-134">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="54cb3-135">**用户时区设置为 UTC 的 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="54cb3-135">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="54cb3-136">[![工作人员窗体设置为 UTC](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-136">[![Worker form set to UTC](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="54cb3-137">**用户时区设置为 GMT +12:00 的 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="54cb3-137">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="54cb3-138">[![工作人员窗体设置为 GMT](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-138">[![Worker form set to GMT](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="54cb3-139">**通过 OData 使用 Excel**</span><span class="sxs-lookup"><span data-stu-id="54cb3-139">**Excel Via OData**</span></span>

<span data-ttu-id="54cb3-140">[![通过 OData 使用 Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-140">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="54cb3-141">**DMF 暂存**</span><span class="sxs-lookup"><span data-stu-id="54cb3-141">**DMF Staging**</span></span>

<span data-ttu-id="54cb3-142">[![DMF 暂存](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-142">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="54cb3-143">**DMF Export**</span><span class="sxs-lookup"><span data-stu-id="54cb3-143">**DMF Export**</span></span>

<span data-ttu-id="54cb3-144">[![DMF 导出](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-144">[![DMF Export](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="54cb3-145">**通过 Dataverse 使用 Excel**</span><span class="sxs-lookup"><span data-stu-id="54cb3-145">**Excel via Dataverse**</span></span>

<span data-ttu-id="54cb3-146">[![通过 Dataverse 使用 Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="54cb3-146">[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="54cb3-147">请参阅</span><span class="sxs-lookup"><span data-stu-id="54cb3-147">See also</span></span>

[<span data-ttu-id="54cb3-148">日期和时间数据</span><span class="sxs-lookup"><span data-stu-id="54cb3-148">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="54cb3-149">用户首选时区</span><span class="sxs-lookup"><span data-stu-id="54cb3-149">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]