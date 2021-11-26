---
title: 了解日期和时间字段
description: 本主题说明在 Microsoft Dynamics 365 Human Resources 中使用日期和时间字段时会发生什么。
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 06c783c1e4a2961f1445909ea03d557c0985064e
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728581"
---
# <a name="understand-date-and-time-fields"></a>了解日期和时间字段

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**日期和时间** 字段是 Microsoft Dynamics 365 Human Resources 中的基本概念。 了解如何在页面、Dataverse 和外部源中使用 **日期和时间** 数据非常重要。

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>了解日期与日期和时间字段数据类型之间的差异

**日期和时间** 字段包含时区信息，而 **日期** 字段则不包含。 **日期** 字段在任何位置都显示相同信息。 当您在 **日期** 字段中输入日期时，相同日期将写入数据库。

在 **日期和时间** 字段中显示数据时，日期和时间会根据在 **用户选项** 页面（**通用 \> 设置 \> 用户选项**）选择的用户时区调整。 您在字段中输入的日期和时间信息可能与写入数据库的信息不同。

[![用户选项页面。](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>了解页面上的日期和时间字段 

如果用户的时区未设置为协调世界时 (UTC)，屏幕上显示的 **日期和时间** 数据将与存储在数据库中的数据不同。 **日期和时间** 字段中的数据始终存储为 UTC。

[![工作人员页面 UTC。](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>了解数据库中的日期和时间字段 

当 **日期和时间** 值写入数据库时，数据作为 UTC 时间存储。 因此，用户可以查看相对于其用户选项中定义的时区的任何 **日期和时间** 数据。
 
在上面的示例中，开始时间是一个时间点，而不是特定日期。 通过将登录用户的时区从 GMT +12:00 更改为 GMT UTC，同一记录将显示 04/30/2019 12:00:00 而不是 05/01/2019 12:00:00。

在下面的示例中，无论时区如何，员工 000724 的雇用都会同时变为活动状态。 该员工将于 GMT 时区的 04/30/2019 进入活动状态，与 GMT+12:00 时区的 05/01/2019 相同。 两者都指的是相同时间点而不是特定日期。 

[![工作人员页面 GMT。](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Data Management Framework、Excel、Dataverse 和 Power BI 中的日期和时间数据 

Data Management Framework (DMF)、Excel 加载项、Dataverse 和 Power BI 报告的目的都是直接在数据库级别与数据交互。 由于没有客户端将 **日期和时间** 数据调整到用户的时区，因此所有 **日期和时间** 值均为 UTC，这可能导致在输入或查看数据时出现一些错误的假设。
 
通过 DMF、Excel 或 Dataverse 提交 **日期和时间** 数据时，数据库将假定为 UTC。 但是，如果查看数据的用户未将其用户时区设置为 UTC，提交的 **日期和时间** 值不会按预期显示，用户可能会感到困惑。 
 
导出数据时，可能会发生相反的情况。 导出的 DMF 实体中的 **日期和时间** 数据可能与 Dynamics 客户端中显示的数据不同。 
 
使用 DMF 等外部源查看或创作数据时，请记住，**日期和时间** 值默认为 UTC，无论用户计算机的时区或其当前的用户时区设置如何。 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>在不同产品区域显示的同一个记录的示例 

**用户时区设置为 UTC 的 Human Resources**

[![设置为 UTC 的工作人员页面。](./media/worker-form3.png)](./media/worker-form3.png)

**用户时区设置为 GMT +12:00 的 Human Resources** 

[![设置为 GMT 的工作人员页面。](./media/worker-form4.png)](./media/worker-form4.png)

**通过 OData 使用 Excel**

[![通过 OData 使用 Excel。](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF 暂存**

[![DMF 暂存。](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF Export**

[![DMF 导出。](./media/DMFExport.png)](./media/DMFExport.png)

**通过 Dataverse 使用 Excel**

[![通过 Dataverse 使用 Excel。](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>请参阅

[日期和时间数据](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[用户首选时区](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
