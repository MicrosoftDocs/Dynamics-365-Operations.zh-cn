---
title: 从作业卡设备进行完工入库到牌照控制的库位
description: 此主题介绍当牌照控制库位时，完成生产订单的完工产品到库存的过程。
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572121"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>从作业卡设备进行完工入库到牌照控制的库位 

称为“完工入库”的过程用于完成生产订单中的完工产品的入库。 如果为高级仓库流程启用了成品，则将该产品报告为完工入库到称为生产输出库位的库位。 有关设置生产输出库位的信息，请参阅[生产输出库位](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)。

必须选择现有牌照编号，才能完成此任务。 如果将生产输出库位设置为由牌照跟踪，则将生产输出库位报告为完工时，必须包括牌照编号。 **作业卡设备**页上的**报告进度**中将显示**牌照**字段。 仅当报告生产订单的最后一次运行时，**报告进度**提示才显示此字段。 仅当为仓库管理流程启用了生产订单的物料，才显示此字段。 
