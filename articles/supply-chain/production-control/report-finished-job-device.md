---
title: 从作业卡设备进行完工入库到牌照控制的库位
description: 此主题介绍当牌照控制库位时，完成生产订单的完工产品到库存的过程。
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 5f61c1abfb115f02e6ff314f6a3e42bb1d3b543f
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092560"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>从作业卡设备进行完工入库到牌照控制的库位 

称为“完工入库”的过程用于完成生产订单中的完工产品的入库。 如果为高级仓库流程启用了成品，则将该产品报告为完工入库到称为生产输出库位的库位。 有关设置生产输出库位的信息，请参阅[生产输出库位](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)。

如果生产输出位置是牌照控制的，则必须在完工入库时提供牌照。 **作业卡设备**页上的**报告进度**中将显示**牌照**字段。 仅当报告生产订单的上一次操作并且为仓库管理流程启用了生产订单的物料时，此字段才会在**报告进度**提示上可见。 

提供牌照有两种选择
- 用户正在牌照字段中选择现有的牌照。
- 牌照从编号规则自动生成，并默认为牌照字段。

另一个选择是通过选择**配置设备的作业卡**页面上的选项**生成牌照**来配置自动生成牌照。
