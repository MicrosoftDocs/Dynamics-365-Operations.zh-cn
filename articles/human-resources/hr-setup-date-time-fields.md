---
title: 了解日期和时间字段
description: 了解在 Microsoft Dynamics 365 Human Resources 中使用日期和时间字段时会发生什么。 清楚地了解在与 Human Resources、外部源或 Common Data Service 的窗体中的日期和时间数据进行交互时可能会发生什么。
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 027e46d53fd9704f5483e90409be53c1510e8cd4
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529844"
---
# <a name="understand-date-and-time-fields"></a><span data-ttu-id="0b337-104">了解日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="0b337-104">Understand Date and Time fields</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0b337-105">**日期和时间** 字段是 Dynamics 365 Human Resources 中的基本概念。</span><span class="sxs-lookup"><span data-stu-id="0b337-105">**Date and Time** fields are a fundamental concept in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0b337-106">了解如何在 Dynamics 365 Human Resources 窗体、Common Data Service 和外部源中使用 **日期和时间** 数据非常重要。</span><span class="sxs-lookup"><span data-stu-id="0b337-106">It's important to understand how to work with **Date and Time** data in Dynamics 365 Human Resources forms, Common Data Service, and external sources.</span></span>

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a><span data-ttu-id="0b337-107">了解日期与日期和时间字段数据类型之间的差异</span><span class="sxs-lookup"><span data-stu-id="0b337-107">Understanding the difference between Date and Date and Time field data types</span></span>

<span data-ttu-id="0b337-108">**日期和时间** 字段包含时区信息，而 **日期** 字段则不包含。</span><span class="sxs-lookup"><span data-stu-id="0b337-108">**Date and Time** fields contain time zone information, while **Date** fields don't.</span></span> <span data-ttu-id="0b337-109">**日期** 字段在任何位置都显示相同信息。</span><span class="sxs-lookup"><span data-stu-id="0b337-109">**Date** fields display the same information in any location.</span></span> <span data-ttu-id="0b337-110">当您在 **日期** 字段中输入日期时，Human Resources 会将相同的日期写入数据库。</span><span class="sxs-lookup"><span data-stu-id="0b337-110">When you enter a date into a **Date** field, Human Resources writes that same date to the database.</span></span>

<span data-ttu-id="0b337-111">在 **日期和时间** 字段中显示数据时，Human Resources 会根据用户在 **用户选项** 窗体（**通用 > 设置 > 用户选项**）设置的时区调整日期和时间。</span><span class="sxs-lookup"><span data-stu-id="0b337-111">When displaying data in a **Date and Time** field, Human Resources adjusts the date and time based on the user's time zone set in the **User Options** form (**Common > Setup > User Options**).</span></span> <span data-ttu-id="0b337-112">您在字段中输入的日期和时间信息可能与写入数据库的信息不同。</span><span class="sxs-lookup"><span data-stu-id="0b337-112">The date and time information you enter in the field might not be the same as the information written to the database.</span></span>

<span data-ttu-id="0b337-113">[![用户选项窗体](./media/useroptionsform.png)](./media/useroptionsform.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-113">[![User options form](./media/useroptionsform.png)](./media/useroptionsform.png)</span></span>

## <a name="understanding-date-and-time-fields-in-forms"></a><span data-ttu-id="0b337-114">了解窗体中的日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="0b337-114">Understanding Date and Time fields in forms</span></span> 

<span data-ttu-id="0b337-115">在 **日期和时间** 字段中输入数据时，如果用户的时区未设置为协调世界时 (UTC)，屏幕上显示的数据将与存储在数据库中的数据不同。</span><span class="sxs-lookup"><span data-stu-id="0b337-115">When entering data in a **Date and Time** field, the data displayed on the screen isn't the same as the data stored in the database if the user's time zone isn't set to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="0b337-116">**日期和时间** 字段中的数据始终存储为 UTC。</span><span class="sxs-lookup"><span data-stu-id="0b337-116">Data in **Date and Time** fields is always stored as UTC.</span></span>

<span data-ttu-id="0b337-117">[![工作人员窗体](./media/worker-form.png)](./media/worker-form.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-117">[![Worker form](./media/worker-form.png)](./media/worker-form.png)</span></span>

## <a name="understand-date-and-time-fields-in-the-database"></a><span data-ttu-id="0b337-118">了解数据库中的日期和时间字段</span><span class="sxs-lookup"><span data-stu-id="0b337-118">Understand Date and Time fields in the database</span></span> 

<span data-ttu-id="0b337-119">当 Human Resources 将 **日期和时间** 值写入数据库时，它以 UTC 存储数据。</span><span class="sxs-lookup"><span data-stu-id="0b337-119">When Human Resources writes a **Date and time** value to the database, it stores the data in UTC.</span></span> <span data-ttu-id="0b337-120">这允许用户查看相对于其用户选项中定义的时区的任何 **日期和时间** 数据。</span><span class="sxs-lookup"><span data-stu-id="0b337-120">This allows users to see any **Date and Time** data relative to the time zone defined in their user options.</span></span>
 
<span data-ttu-id="0b337-121">在上面的示例中，开始时间是一个时间点，而不是特定日期。</span><span class="sxs-lookup"><span data-stu-id="0b337-121">In the example above, the start time is a point in time, not a particular date.</span></span> <span data-ttu-id="0b337-122">通过将登录用户的时区从 GMT +12:00 更改为 GMT UTC，刚刚创建的同一记录显示 04/30/2019 12:00:00 而不是 05/01/2019 12:00:00。</span><span class="sxs-lookup"><span data-stu-id="0b337-122">By changing the time zone of the logged in user from GMT +12:00 to GMT UTC, the same record just created shows 04/30/2019 12:00:00 instead of 05/01/2019 12:00:00.</span></span>
  
<span data-ttu-id="0b337-123">在下面的示例中，无论时区如何，员工 000724 的雇用都会同时变为活动状态。</span><span class="sxs-lookup"><span data-stu-id="0b337-123">In the example below, employee 000724’s employment becomes active at the same time regardless of time zone.</span></span> <span data-ttu-id="0b337-124">该员工将于 GMT 时区的 04/30/2019 进入活动状态，与 GMT+12:00 时区的 05/01/2019 相同。</span><span class="sxs-lookup"><span data-stu-id="0b337-124">The employee will be active on 04/30/2019 in the GMT time zone, which is the same as 05/01/2019 in GMT+12:00 time zone.</span></span> <span data-ttu-id="0b337-125">两者都指的是相同时间点而不是特定日期。</span><span class="sxs-lookup"><span data-stu-id="0b337-125">Both refer to the same point in time and not a particular date.</span></span> 

<span data-ttu-id="0b337-126">[![工作人员窗体](./media/worker-form2.png)](./media/worker-form2.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-126">[![Worker form](./media/worker-form2.png)](./media/worker-form2.png)</span></span>

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a><span data-ttu-id="0b337-127">Data Management Framework、Excel、Common Data Service 和 Power BI 中的日期和时间数据</span><span class="sxs-lookup"><span data-stu-id="0b337-127">Date and Time data in Data Management Framework, Excel, Common Data Service, and Power BI</span></span> 

<span data-ttu-id="0b337-128">Data Management Framework、Excel 加载项、Common Data Service 和 Power BI 报告的目的都是直接在数据库级别与数据交互。</span><span class="sxs-lookup"><span data-stu-id="0b337-128">The Data Management Framework, Excel Add-In, Common Data Service, and Power BI reporting are all designed to interact with data directly on the database level.</span></span> <span data-ttu-id="0b337-129">由于没有客户端将 **日期和时间** 数据调整到用户的时区，因此所有 **日期和时间** 值均为 UTC，这可能导致在输入或查看数据时出现一些错误的假设。</span><span class="sxs-lookup"><span data-stu-id="0b337-129">Since there is no client to adjust **Date and Time** data to the time zone of the user, all **Date and Time** values are in UTC, which can lead to some incorrect assumptions when entering or viewing data.</span></span>  
 
<span data-ttu-id="0b337-130">通过 DMF、Excel 或 Common Data Service 提交的 **日期和时间** 数据被数据库假定为 UTC。</span><span class="sxs-lookup"><span data-stu-id="0b337-130">**Date and Time** data that is submitted via DMF, Excel, or Common Data Service is assumed to be in UTC by the database.</span></span> <span data-ttu-id="0b337-131">当提交的 **日期和时间** 值未按预期显示时，这可能会导致一些混淆，因为查看数据的用户没有将其用户时区设置为 UTC。</span><span class="sxs-lookup"><span data-stu-id="0b337-131">This can cause some confusion when the submitted **Date and Time** value doesn't display as expected because the user viewing the data doesn't have their user time zone  set to UTC.</span></span> 
 
<span data-ttu-id="0b337-132">导出数据时，可能会发生相反的情况。</span><span class="sxs-lookup"><span data-stu-id="0b337-132">The same thing can happen in reverse when data is exported.</span></span> <span data-ttu-id="0b337-133">导出的 DMF 实体中的 **日期和时间** 数据可能与 Dynamics 客户端中显示的数据不同。</span><span class="sxs-lookup"><span data-stu-id="0b337-133">The **Date and Time** data in the exported DMF entity can be different then what is displayed in the Dynamics client.</span></span> 
 
<span data-ttu-id="0b337-134">使用 DMF 等外部源查看或创作数据时，请务必记住，**日期和时间** 值默认为 UTC，无论用户计算机的时区或其当前的用户时区设置如何。</span><span class="sxs-lookup"><span data-stu-id="0b337-134">When using external sources like DMF to view or author data, it is important to keep in mind that the **Date and Time** values are considered by default to be in UTC regardless of the time zone of the user's computer or their current user time zone settings.</span></span> 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a><span data-ttu-id="0b337-135">在不同产品区域显示的同一个记录的示例</span><span class="sxs-lookup"><span data-stu-id="0b337-135">Examples of the same record being displayed in different product areas</span></span> 

<span data-ttu-id="0b337-136">**用户时区设置为 UTC 的 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="0b337-136">**Human Resources with user time zone set to UTC**</span></span>

<span data-ttu-id="0b337-137">[![工作人员窗体](./media/worker-form3.png)](./media/worker-form3.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-137">[![Worker form](./media/worker-form3.png)](./media/worker-form3.png)</span></span>

<span data-ttu-id="0b337-138">**用户时区设置为 GMT +12:00 的 Human Resources**</span><span class="sxs-lookup"><span data-stu-id="0b337-138">**Human Resources with user time zone set to GMT +12:00**</span></span> 

<span data-ttu-id="0b337-139">[![工作人员窗体](./media/worker-form4.png)](./media/worker-form4.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-139">[![Worker form](./media/worker-form4.png)](./media/worker-form4.png)</span></span>

<span data-ttu-id="0b337-140">**通过 OData 使用 Excel**</span><span class="sxs-lookup"><span data-stu-id="0b337-140">**Excel Via OData**</span></span>

<span data-ttu-id="0b337-141">[![通过 OData 使用 Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-141">[![Excel Via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)</span></span>

<span data-ttu-id="0b337-142">**DMF 暂存**</span><span class="sxs-lookup"><span data-stu-id="0b337-142">**DMF Staging**</span></span>

<span data-ttu-id="0b337-143">[![DMF 暂存](./media/DMFStaging.png)](./media/DMFStaging.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-143">[![DMF Staging](./media/DMFStaging.png)](./media/DMFStaging.png)</span></span>

<span data-ttu-id="0b337-144">**DMF Export**</span><span class="sxs-lookup"><span data-stu-id="0b337-144">**DMF Export**</span></span>

<span data-ttu-id="0b337-145">[![DMF 暂存](./media/DMFexport.png)](./media/DMFexport.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-145">[![DMF Staging](./media/DMFexport.png)](./media/DMFexport.png)</span></span>

<span data-ttu-id="0b337-146">**通过 Common Data Service 使用 Excel**</span><span class="sxs-lookup"><span data-stu-id="0b337-146">**Excel via Common Data Service**</span></span>

<span data-ttu-id="0b337-147">[![通过 Common Data Service 使用 Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span><span class="sxs-lookup"><span data-stu-id="0b337-147">[![Excel via Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)</span></span>

## <a name="see-also"></a><span data-ttu-id="0b337-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="0b337-148">See also</span></span>

[<span data-ttu-id="0b337-149">日期和时间数据</span><span class="sxs-lookup"><span data-stu-id="0b337-149">Date and time data</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[<span data-ttu-id="0b337-150">用户首选时区</span><span class="sxs-lookup"><span data-stu-id="0b337-150">User preferred time zones</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
