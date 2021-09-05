---
title: 报告选项
description: 本主题介绍如何自定义 Microsoft Dynamics 365 Human Resources 报告或创建新报告。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 706e901e89fa618540067d68546be1cef1ee7148
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413365"
---
# <a name="reporting-options"></a>报告选项

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**环境详细信息**

此问题适用于所有环境。

**故障**

客户想要自定义 Microsoft Dynamics 365 Human Resources 报表或创建新报表。

**签发**

用户无法自定义嵌入的 Microsoft Power BI 报表。

**解决方案**

- 流向 Dataverse 的 Human Resources 数据可以通过 Power Apps Dataverse 连接器报告给 Power BI Desktop。 请注意，Dataverse 包含 Human Resources 数据的子集。 有关 Power BI 和仪表板的详细信息，请参阅[使用 Power Apps Common Data Service 创建 Power BI 报表和仪表板](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)。
- 电子申报 (ER) 对 Human Resources 中的某些报表可用。 客户驱动的自定义可以通过 ER 配置选项完成。
- 数据可以使用 Human Resources 通过Microsoft Office 集成提供的不同数据实体导出到 Microsoft Excel 或 Microsoft Word。

**长期解决方案**

将推出更多 Power BI 选项，更多数据和实体将成为 Dataverse 的一部分。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
