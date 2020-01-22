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
ms.openlocfilehash: 63073035941cd2ef343c65364536fe76a9b71430
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935114"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="b9e1d-103">从作业卡设备进行完工入库到牌照控制的库位</span><span class="sxs-lookup"><span data-stu-id="b9e1d-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="b9e1d-104">称为“完工入库”的过程用于完成生产订单中的完工产品的入库。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="b9e1d-105">如果为高级仓库流程启用了成品，则将该产品报告为完工入库到称为生产输出库位的库位。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="b9e1d-106">有关设置生产输出库位的信息，请参阅[生产输出库位](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location)。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="b9e1d-107">如果生产输出位置是牌照控制的，则必须在完工入库时提供牌照。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="b9e1d-108">**作业卡设备**页上的**报告进度**中将显示**牌照**字段。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="b9e1d-109">仅当报告生产订单的上一次操作并且为仓库管理流程启用了生产订单的物料时，此字段才会在**报告进度**提示上可见。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="b9e1d-110">提供牌照有两种选择</span><span class="sxs-lookup"><span data-stu-id="b9e1d-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="b9e1d-111">用户正在牌照字段中选择现有的牌照。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="b9e1d-112">牌照从编号规则自动生成，并默认为牌照字段。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="b9e1d-113">另一个选择是通过选择**配置设备的作业卡**页面上的选项**生成牌照**来配置自动生成牌照。</span><span class="sxs-lookup"><span data-stu-id="b9e1d-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
