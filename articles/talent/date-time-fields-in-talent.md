---
title: 在 Microsoft Dynamics 365 for Talent 中使用日期和时间
description: 了解在 Microsoft Dynamics 365 for Talent 中使用日期和时间字段时会发生什么。 清楚地了解在与 Dynamics 365 for Talent、外部源或 Common Data Service 的窗体中的日期和时间数据进行交互时可能会发生什么。
author: Darinkramer
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-06-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b4c652992272ed1a5aecbb4c78f0d11f077149d1
ms.sourcegitcommit: 46bded82aa072adfedcf443629c2adc69f512c09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/26/2019
ms.locfileid: "1791196"
---
# <a name="date-and-time-fields-in-talent"></a>Talent 中的日期和时间字段

[!include [banner](includes/banner.md)]

**日期和时间**字段是 Dynamics 365 for Talent 中的基本概念。 了解如何在 Dynamics 365 窗体、Common Data Service 和外部源中使用**日期和时间**数据非常重要。

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>了解日期与日期和时间字段数据类型之间的差异

**日期和时间**字段包含时区信息，而**日期**字段则不包含。 **日期**字段在任何位置都显示相同信息。 当您在**日期**字段中输入日期时，Talent 会将相同的日期写入数据库。

在**日期和时间**字段中显示数据时，Talent 会根据用户在**用户选项**窗体（**通用 > 设置 > 用户选项**）设置的时区调整日期和时间。 您在字段中输入的日期和时间信息可能与写入数据库的信息不同。

[![用户选项窗体](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>了解窗体中的日期和时间字段 

在**日期和时间**字段中输入数据时，如果用户的时区未设置为协调世界时 (UTC)，屏幕上显示的数据将与存储在数据库中的数据不同。 **日期和时间**字段中的数据始终存储为 UTC。

[![工作人员窗体](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>了解数据库中的日期和时间字段 

当 Talent 将**日期和时间**值写入数据库时，它以 UTC 存储数据。 这允许用户查看相对于其用户选项中定义的时区的任何**日期和时间**数据。
 
在上面的示例中，开始时间是一个时间点，而不是特定日期。 通过将登录用户的时区从 GMT +12:00 更改为 GMT UTC，刚刚创建的同一记录显示 04/30/2019 12:00:00 而不是 05/01/2019 12:00:00。
  
在下面的示例中，无论时区如何，员工 000724 的雇用都会同时变为活动状态。 该员工将于 GMT 时区的 04/30/2019 进入活动状态，与 GMT+12:00 时区的 05/01/2019 相同。 两者都指的是相同时间点而不是特定日期。 

[![工作人员窗体](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Data Management Framework、Excel、Common Data Service 和 Power BI 中的日期和时间数据 

Data Management Framework、Excel 加载项、Common Data Service 和 Power BI 报告的目的都是直接在数据库级别与数据交互。 由于没有客户端将**日期和时间**数据调整到用户的时区，因此所有**日期和时间**值均为 UTC，这可能导致在输入或查看数据时出现一些错误的假设。  
 
通过 DMF、Excel 或 Common Data Service 提交的**日期和时间**数据被数据库假定为 UTC。 当提交的**日期和时间**值未按预期显示时，这可能会导致一些混淆，因为查看数据的用户没有将其用户时区设置为 UTC。 
 
导出数据时，可能会发生相反的情况。 导出的 DMF 实体中的**日期和时间**数据可能与 Dynamics 客户端中显示的数据不同。 
 
使用 DMF 等外部源查看或创作数据时，请务必记住，**日期和时间**值默认为 UTC，无论用户计算机的时区或其当前的用户时区设置如何。 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>在不同产品区域显示的同一个记录的示例 

**用户时区设置为 UTC 的 Talent**

[![工作人员窗体](./media/worker-form3.png)](./media/worker-form3.png)

**用户时区设置为 GMT +12:00 的 Talent** 

[![工作人员窗体](./media/worker-form4.png)](./media/worker-form4.png)

**通过 OData 使用 Excel**

[![通过 OData 使用 Excel](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF 暂存**

[![DMF 暂存](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF“导出”**

[![DMF 暂存](./media/DMFexport.png)](./media/DMFexport.png)

**通过 Common Data Service 使用 Excel**

[![通过 Common Data Service 使用 Excel](./media/ExcelCDS.png)](./media/ExcelCDS.png)

### <a name="see-also"></a>请参阅

[日期和时间数据](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[用户首选时区](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 