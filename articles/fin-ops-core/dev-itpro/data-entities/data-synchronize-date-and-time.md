---
title: 同步导入作业中的日期和时间
description: 在导入作业中使用 UTC 时区来避免时区转换出现问题。
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748661"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a>同步导入作业中的日期和时间

[!include [banner](../includes/banner.md)]

将导入作业的时区设置为协调世界时 (UTC) 很重要。 如果使用其他设置，您可能会在导入的数据中看到意外的日期和时间。 没有正确的设置，导入流程会将 UTC 日期转换为本地格式，然后系统设置会将其再次转换。

这种双重转换会导致日期在应用程序之间更改。 例如，由于本地时区的差异，双重转换可能导致 Dynamics 365 Human Resources 和 Dynamics 365 Finance 之间的员工开始日期不同。 将导入作业设置为 UTC 可以解决此问题。

1. 在 Dynamics 365 Finance and Operations 中，选择 **数据管理**。

2. 选择 **导入项目**，然后选择项目。

3. 在 **源日期格式** 下，选择 **CSV-Unicode**。

   [![将源日期格式更改为 UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)

4. 将 **时区** 更改为 **协调世界时区**，将 **语言** 更改为 **En-US**。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]