---
title: 报告选项
description: 本文说明如何解决客户想要自定义 Microsoft Dynamics 365 Human Resources 报表或创建新报表的问题。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ee6dba5e37877f1c0b3b9df8306b3194ea2f3e4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008295"
---
# <a name="reporting-options"></a>报告选项

**环境详细信息**

此问题适用于所有环境。

**故障**

客户想要自定义 Microsoft Dynamics 365 Human Resources 报表或创建新报表。

**发货**

用户无法自定义嵌入的 Microsoft Power BI 报表。

**解决方案**

- 流向 Common Data Service 的 Human Resources 数据可以通过 Power Apps Common Data Service 连接器报告给 Power BI Desktop。 请注意，Common Data Service 包含 Human Resources 数据的子集。 有关 Power BI 和仪表板的详细信息，请参阅[使用 Power Apps Common Data Service 创建 Power BI 报表和仪表板](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)。
- 电子申报 (ER) 对 Human Resources 中的某些报表可用。 客户驱动的自定义可以通过 ER 配置选项完成。
- 数据可以使用 Human Resources 通过Microsoft Office 集成提供的不同数据实体导出到 Microsoft Excel 或 Microsoft Word。

**长期解决方案**

将推出更多 Power BI 选项，更多数据和实体将成为 Common Data Service 的一部分。
