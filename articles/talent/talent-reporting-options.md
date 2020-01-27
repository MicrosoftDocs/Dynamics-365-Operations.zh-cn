---
title: Talent 中的报告选项
description: 本主题说明如何解决客户想要自定义 Microsoft Dynamics 365 Talent 报表或创建新报表的问题。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 05d4a2c4314b40042ae45b4f653554bad09be4fa
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897940"
---
# <a name="reporting-options-in-talent"></a>Talent 中的报告选项

**环境详细信息**

此问题适用于所有环境。

**故障**

客户想要自定义 Microsoft Dynamics 365 Talent 报表或创建新报表。

**发货**

用户无法自定义嵌入的 Microsoft Power BI 报表。

**解决方案**

- 流向 Common Data Service 的 Core HR 数据可以通过 Power Apps Common Data Service 连接器报告给 Power BI Desktop。 请注意，Common Data Service 包含 Core HR 数据的子集。 有关 Power BI 和仪表板的详细信息，请参阅[使用 Power Apps Common Data Service 创建 Power BI 报表和仪表板](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi)。
- 电子申报 (ER) 对 Talent 中的某些报表可用。 客户驱动的自定义可以通过 ER 配置选项完成。
- 数据可以使用 Talent 通过Microsoft Office 集成提供的不同数据实体导出到 Microsoft Excel 或 Microsoft Word。

**长期解决方案**

将推出更多 Power BI 选项，更多数据和实体将成为 Common Data Service 的一部分。
