---
title: 下达生产订单
description: 下达的生产订单是已授权进行生产的订单。 “已下达”一词用于描述生产订单生命周期中的状态，在其中，生产订单可用于生产车间和仓库流程的执行。
author: johanhoffmann
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdParmRelease
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2414
ms.assetid: 50c2257b-2924-44f5-b7c1-11f498092053
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 118b0d6300647135b22e42cc84a79f07e48d7ef4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811694"
---
# <a name="release-production-orders"></a>下达生产订单

[!include [banner](../includes/banner.md)]

下达的生产订单是已授权进行生产的订单。 “已下达”一词用于描述生产订单生命周期中的状态，在其中，生产订单可用于生产车间和仓库流程的执行。

## <a name="characteristics-of-the-released-state"></a>“已下达”状态的特征

**已下达** 状态为生产订单生命周期的一个状态。 在状态 **下达** 中的生产订单可用于车间中的执行和仓库流程。 **已下达** 状态具有以下特征：

- 生产订单可以从生产订单或通过使用批处理更改为 **已下达** 状态。 生产订单还可以从使用 **主计划** 页的 **确定时限** 字段确定的计划生产订单自动更新。
- **已下达** 状态是向车间操作员发出信号以开始在车间执行生产作业。
- 生产单，例如工艺卡、工艺路线作业和作业卡提供有关生产作业的信息，并且可以分派。
- 对于实际预留的物料，生成仓库工作以领取生产订单的物料。

## <a name="releasing-jobs-to-the-shop-floor"></a>将作业下达到车间

在下达生产订单后，与该订单相关的生产作业将可见并可供登记。 操作员可为作业登记，例如开始、停止和完成，在 **作业卡终端** 页或 **作业卡设备** 页。 登记的时间和数量将自动从登记页转移到生产日记帐以跟踪所用的时间和数量。

## <a name="route-cards"></a>工艺卡

工艺卡提供来自工艺路线和工序设置以及工序级和作业级排产法的信息的概览。

## <a name="route-jobs"></a>工艺路线作业

工艺路线作业详细列出工序的每个作业，包括设置、处理、排队和运输时间。 例如，喷漆之类的工序可能要求一些单独作业，例如设置时间、运行时间（用于喷漆流程）和排队时间（用于干燥）。

## <a name="job-cards"></a>作业卡

作业卡列出了特定工序的单独作业编号。 每页一个作业。 在作业卡上包括的作业及其预估时间来自工艺路线和工序设置信息。 从作业卡，您可以打开 **生产日记帐行**，**作业卡** 页。 运行运营资源的人员可提供有关生产流程的反馈。 存在一些您可以输入消耗量统计和信息（例如残次数量）的字段。

## <a name="warehouse-work-for-raw-material-picking"></a>物料消耗的仓库工作

原材料领料工作在下达期间生成。 工作只为在下达订单前为生产订单实际预留的物料数量生成。 为原材料领料生成仓库工作需要以下设置：

- 确定在哪个仓库库位领取物料的原材料领料的库位指令
- 原材料的波次模板，在其中配置执行仓库工作的策略
- 确定物料放入位置的生产输入位置

当使用牌照控制位置时，您可以选择在处理原材料领料工作时，是应领取订购数量还是物料可用的全部数量。 要设置此选项：

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**，打开相关物料。
1. 展开 **仓库** 快速选项卡。
1. 为 **牌照位置的材料领取** 字段选择以下选项之一：
    - *订单领料*：应仅领取订购的数量。
    - *暂存*：只要有可能，应领取牌照可用的全部数量。 为了让工作人员能够领取全部牌照数量，牌照不能包含混合物料，且不能有混合维度。 如果牌照包含混合维度或物料，领料将像将像设置为 *订单领料* 一样进行。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]