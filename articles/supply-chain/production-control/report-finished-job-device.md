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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="f4cae-103">从作业卡设备进行完工入库到牌照控制的库位</span><span class="sxs-lookup"><span data-stu-id="f4cae-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="f4cae-104">称为“完工入库”的过程用于完成生产订单中的完工产品的入库。</span><span class="sxs-lookup"><span data-stu-id="f4cae-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="f4cae-105">如果为高级仓库流程启用了成品，则将该产品报告为完工入库到称为生产输出库位的库位。</span><span class="sxs-lookup"><span data-stu-id="f4cae-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="f4cae-106">有关设置生产输出库位的信息，请参阅[生产输出库位](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)。</span><span class="sxs-lookup"><span data-stu-id="f4cae-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="f4cae-107">必须选择现有牌照编号，才能完成此任务。</span><span class="sxs-lookup"><span data-stu-id="f4cae-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="f4cae-108">如果将生产输出库位设置为由牌照跟踪，则将生产输出库位报告为完工时，必须包括牌照编号。</span><span class="sxs-lookup"><span data-stu-id="f4cae-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="f4cae-109">**作业卡设备**页上的**报告进度**中将显示**牌照**字段。</span><span class="sxs-lookup"><span data-stu-id="f4cae-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="f4cae-110">仅当报告生产订单的最后一次运行时，**报告进度**提示才显示此字段。</span><span class="sxs-lookup"><span data-stu-id="f4cae-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="f4cae-111">仅当为仓库管理流程启用了生产订单的物料，才显示此字段。</span><span class="sxs-lookup"><span data-stu-id="f4cae-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
