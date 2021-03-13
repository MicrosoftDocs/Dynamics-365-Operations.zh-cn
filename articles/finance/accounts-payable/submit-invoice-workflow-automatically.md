---
title: 将账单提交至工作流系统并匹配物料收货行
description: 本主题介绍了将供应商发票提交到工作流系统，并自动将过帐的物料收货行与供应商发票进行匹配的流程。
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03c9f6752a0bb9641f67d65580aca18276e43e9a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115648"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>将账单提交至工作流系统并匹配物料收货行

[!include [banner](../includes/banner.md)]

本主题介绍了将供应商发票提交到工作流系统，并自动将过帐的物料收货行与供应商发票进行匹配的流程。

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待处理的供应商发票行进行匹配

作为非接触式应付帐款开票流程的一部分，您可以让系统自动将导入的发票提交到工作流系统。 您可以在 **应付帐款参数** 页面（**应付帐款 \> 设置 \> 应付帐款参数**）的 **供应商发票自动化** 选项卡上配置将导入的发票提交到工作流系统的流程。 提交到工作流程将以您指定的频率（每小时或每天）在后台运行。

当您自动将发票提交到工作流系统时，必须从导入的发票开始。 为了确保整个发票处理流程都没有人工干预，您必须在工作流配置中包括自动化过帐任务。 可以将与采购订单 (PO) 相关的发票以及包含非 PO 采购类别和非贮存行的发票自动提交到工作流系统。 手动输入的发票必须手动提交到工作流系统。

工作流中的 **提交者** 值是在 **流程自动化** 页面上为 **将供应商发票提交到工作流** 后台任务输入的用户 ID。 具有该用户 ID 的用户将能够根据需要从工作流系统中撤回发票。

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>将过帐的物料收货与具有三向匹配政策的发票行进行匹配

作为非接触式应付帐款开票流程的一部分，系统可以自动将过帐的物料收货与发票行进行匹配。 必须为此任务定义三向匹配政策。 如果已在 **功能管理** 页面上启用了 **供应商发票自动化** 功能，则此功能可用。

该流程将一直运行，直到匹配的物料收货数量等于发票数量。 作为此流程的一部分，您可以指定系统在得出流程失败的结论之前应尝试将物料收货与发票行进行匹配的最大次数。 该流程将以每小时或每天的频率在后台运行。 您可以在将发票提交到工作流系统的流程中运行自动化匹配流程。 或者，您可以将其作为独立流程运行。 在 **应付帐款参数** 页面（**应付帐款 \> 设置 \> 应付帐款参数**）的 **供应商发票自动化** 选项卡上配置将物料收货与发票行进行匹配流程的设置。

具有三向匹配政策的发票行（匹配的收货数量小于发票数量）将包括在自动匹配到物料收货流程中。

若要查看不属于自动提交到工作流程的发票的 **最近一次匹配** 状态，请从 **供应商发票** 页面中打开发票。 当查看发票时，将更新匹配的验证信息。 **最近一次匹配** 状态可以使用 **验证发票匹配** 后台任务自动更新。 您可以在 **流程自动化** 页的 **后台流程** 选项卡上配置自动更新 **最近一次匹配** 状态的流程（**系统管理 \> 设置 \> 流程自动化**）。

如果满足以下任一条件，将从自动化流程中排除发票行：

- 发票行的 **自动化收货匹配状态** 值为 **失败**。
- 发票正在使用中。
- 发票在工作流系统中。
