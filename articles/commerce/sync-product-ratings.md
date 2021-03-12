---
title: 在 Dynamics 365 Commerce 中同步产品评分
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中同步产品评分。
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7318d53535a93352425f811ec90572e65aeb696
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006277"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a>在 Dynamics 365 Commerce 中同步产品评分

[!include [banner](includes/banner.md)]

此主题介绍如何在 Microsoft Dynamics 365 Commerce 中同步产品评分。

## <a name="overview"></a>概览

若要在全渠道（如销售点 (POS)）中和在呼叫中心中使用产品评分，必须将评分和评价服务中的产品评分导入到 Commerce 渠道数据库中。 当产品评分在全渠道中可用时，可以在客户与销售助理交互时，直接帮助客户。

此主题介绍以下任务：

1. 将 **产品评分同步作业** 配置为批处理作业来同步来自 **评分和评价服务** 的产品评分。
1. 验证产品评分同步的批处理作业是否成功。
1. 使产品评分在 POS 可用。

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a>配置批处理作业以同步产品评分

> [!IMPORTANT]
> 首先，确保安装 Dynamics 365 Commerce 版本 10.0.6 或更高版本。

### <a name="initialize-the-commerce-scheduler"></a>初始化商业调度

若要初始化商业调度，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 初始化商业调度**。 也可以搜索“初始化商业调度”。
1. 在 **初始化商业调度** 对话框中，确保 **删除现有配置** 选项设置为 **否**，然后选择 **确定**。

### <a name="verify-the-retailproductrating-subjob"></a>验证 RetailProductRating 子作业

若要验证是否存在 **RetailProductRating** 子作业，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 调度子作业**。 也可以搜索“调度子作业”。
1. 在子作业列表中，找到或搜索 **RetailProductRating** 子作业。

下图显示 Commerce 中的子作业详细信息的示例。

![RetailProductRating 子作业的详细信息](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> 如果找不到 **RetailProductRating** 子作业，说明在初始化商业调度之前，您可能已运行了 **同步产品评分** 作业和 **1040 CDX** 作业。 在此情况下，请执行以下步骤运行 **完全数据同步** 作业。

> 1. 转到 **Retail 和 Commerce \> Headquarters 设置 \>  商业调度 \> 渠道数据库**。 也可以搜索“渠道数据库”。
> 1. 选择要同步的渠道数据库。
> 1. 在操作窗格中，选择 **完全数据同步**。
> 1. 在 **选择配送计划** 下拉对话框中，选择 **1040 - 产品**，然后选择 **确定**。
> 1. 重复上一过程的步骤，以便验证是否已创建了 **RetailProductRating** 子作业。

### <a name="import-product-ratings"></a>导入产品评分

若要将产品评分从评分和评价服务导入到 Commerce 中，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 总部设置 \> 商业调度 \> 同步产品评分作业**。 也可以搜索“同步产品评分作业”。
1. 在 **提取产品评分** 对话框的 **在后台运行** 快速选项卡中，选择 **重复执行**。
1. 在 **定义重复项** 对话框中，设置重复执行模式。 （建议值为两小时。）安排的重复周期不应低于一小时。
1. 选择 **确定**。
1. 将 **批处理** 选项设置为 **是**。 此设置可帮助确保您可以审核日志和验证批处理作业的运行状态。
1. 选择 **确定** 安排批处理作业。

下图显示 Commerce 中的批处理作业配置的示例。

![配置同步产品评分批处理作业](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>验证产品评分同步批处理作业是否成功

若要验证 **同步产品评分** 批处理作业是否成功，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> 系统管理员 \> 查询 \> 批处理作业**，如果您在使用纯 Commerce 库存单位 (SKU)，则改为转到 **Retail 和 Commerce \> 查询和报表 \> 批处理作业**。 也可以搜索“批处理作业”。
1. 若要查看批处理作业的详细信息，请在批处理作业列表的 **作业描述** 列中，搜索包含“提取产品评分”的描述。
1. 选择作业 ID 以查看批处理作业详细信息，如计划的开始日期/时间和重复文本。

下图显示当安排批处理作业以两小时的间隔运行时，Commerce 中的批处理作业详细信息的示例。

![同步产品评分批处理作业的详细信息](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>使产品评分在 POS 可用

Dynamics 365 Commerce 中的评分和评价解决方案是全渠道解决方案。 但是，默认情况下，POS 中不显示产品评分。 若要在销售助理帮助店内客户时，帮助客户查看评分和评价，必须在 POS 中开启产品评分。

若要在 POS 中开启产品评分，请执行以下步骤。

1. 转到 **Retail 和 Commerce \> Commerce 设置 \> 参数 \> 商业参数**。 也可以搜索“商业参数”。
1. 在 **配置参数** 选项卡中，选择 **新建**。
1. 输入名称（如 **RatingsAndReviews.EnableProductRatingsForRetailStores**），然后将值设置为 **true**。
1. 选择 **保存**。
1. 转到 **Retail 和 Commerce \> Retail 和 Commerce IT \> 分配计划**。 也可以搜索“配送计划”。
1. 在作业列表中，选择 **1110**（**全局配置**），然后选择 **立即运行**。
1. 作业成功运行之后，验证 POS 中现在是否显示产品评分。

下图显示要在 POS 中开启产品评分所需商业参数配置的示例。

![POS 中产品评分的商业参数配置](media/rnr-hq-enable-ratings-in-pos.png)

下图显示 POS 中的产品评分的示例。

![POS 中的产品评分](media/rnr-pos-catalog-ratings.png)

下图显示呼叫中心渠道中的产品评分的示例。

![呼叫中心渠道中的产品评分](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[管理评分和评价](manage-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)
