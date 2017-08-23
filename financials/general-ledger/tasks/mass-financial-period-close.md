--- 
title: "批量财务期间结帐"
description: "此过程显示如何暂停期间，或一次性永久关闭一个期间或多个法人。"
author: aprilolson
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b176adc2cbd23647b98cf55e94829e1ea9637c95
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="mass-financial-period-close"></a>批量财务期间结帐

[!include[task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何暂停期间，或一次性永久关闭一个期间或多个法人。 此外，此任务将显示如何把用户组过帐限制到特定模块。

1. 转到“总帐”>“期间结转”>“分类帐日历”。
    * 请注意，显示的法人列表取决于该页中选择的会计日历。 将仅显示使用所选会计日历的法人。  
2. 单击“编辑”。
3. 选择要修改其状态的期间。
4. 选择要更新其状态的法人。
    * 可以通过选中网格左上方的复选标记快速选中所有法人。  
5. 选择“更新模块访问”以定义所选模块的过帐访问。
    * 也可以通过编辑网格中的记录，逐一更新模块状态。 希望快速更新多个法人记录时，此按钮非常有用。  
6. 在“应用模块”中，选择要更新状态的模块。 单击“选择”。
7. 在“访问级别”中，选择“全部”、“无”或特定用户组。 单击“选择”。
    * “所有”表示如果期间为开放状态，所有可编辑模块的用户可进行过帐。 “无”表示如果期间为开放状态，则用户不能过帐至该模块。 “特定用户组”表示如果期间为开放状态，只有组内用户能够过帐至该模块。  
8. 单击“更新”。
9. 选择另一个期间以更新状态。
10. 选择要更新其期间状态的法人。
11. 选择“更新期间状态”，然后将状态设置为“暂停”、“打开”或“永久关闭”。
    * “开放”表示期间内可进行过帐，但用户必须有访问权限。 “暂停”表示期间内不能过帐，但是可以重新打开期间。 “永久关闭”表示期间已关闭，永远不能打开。 不能过帐调整。 不建议在完成所有调整和审计前设置期间为“永久关闭”。  
12. 单击“更新”。


