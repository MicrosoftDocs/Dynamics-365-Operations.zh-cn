---
title: 自动化供应商开票流程概述
description: 本主题描述了自动化供应商发票处理的功能以及使用自动化流程的好处。
author: abruer
manager: AnnBe
ms.date: 08/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 187b3c4f1a8b2c9ec6df95c19b261756ec4562dc
ms.sourcegitcommit: 6ffbae02de2eee1f3be9bab2da37a3771aae8bec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/30/2020
ms.locfileid: "3904999"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>自动化供应商开票流程概述

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题描述了自动化供应商发票处理的功能以及使用自动化流程的好处。 此功能包含在功能管理中启用的功能。 这些功能仅适用于供应商发票，不适用于通过**发票日记帐**或**发票登记薄日记帐**页面处理的发票。

组织通常与第三方合作，使用光学字符识别 (OCR) 服务提供商处理纸质发票。 服务提供商返回机器可读的发票元数据。 为了帮助实现自动化，应付帐款自动化功能使您可以从应付帐款中使用这些项目。

您可以自动化某些应付帐款供应商开票流程。 这些流程包括将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待定供应商发票行进行匹配。 自动化流程会显示有关供应商发票在每个流程中的进度信息。 此功能可以帮助应付帐款职员和经理更有效地处理供应商发票。 它还有助于减少手动输入和处理信息时可能发生的错误，并提高效率。

自动化流程可用于执行以下任务：

- 自动将导入的发票提交到工作流系统。
- 将物料收货与待定供应商发票行进行匹配。
- 在过帐供应商发票之前模拟过帐。
- 快速有效地查看工作流历史记录。
- 查看和分析自动化供应商发票处理的结果。

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>供应商发票自动化 – 将导入的供应商发票提交到工作流系统

作为非接触式应付帐款开票流程的一部分，您可以让系统自动将导入的发票提交到工作流系统。 该流程将以您指定的频率（每小时或每天）在后台运行。 自动将导入的发票提交到工作流系统的功能要求您的流程以导入的发票开始。 为了确保整个发票处理流程都没有人工干预，工作流配置中必须包括自动化过帐任务。

可以将与采购订单 (PO) 相关的发票以及包含非 PO 采购类别和非贮存行的发票自动提交到工作流系统。 手动输入的发票和通过**供应商协作开票**工作区创建的发票必须手动提交到工作流系统。

自动化功能提供了一个灵活的框架，可让您定义公司特定的规则，以将导入的供应商发票提交到工作流系统，并将过帐的物料收货行与待定供应商发票行进行匹配。

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>供应商发票自动化 – 将物料收货与具有三向匹配政策的发票行进行匹配

系统可以自动将过帐的物料收货与定义了三向匹配政策的发票行进行匹配。 该流程将一直运行，直到匹配的物料收货数量等于发票数量。 作为此流程的一部分，您可以指定系统在得出流程失败的结论之前应尝试将物料收货与发票行进行匹配的最大次数。 该流程将以每小时或每天的频率在后台运行。 您可以在将发票提交到工作流系统的流程中运行自动化匹配流程。 或者，您可以将其作为独立流程运行。

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>供应商发票自动化 – 预验证供应商发票过帐

过帐模拟完成了供应商发票过帐流程中完成的验证步骤，但是没有更新任何帐户。 若要运行该流程，您可以在**待定供应商发票**页面上选择一个或多个发票。

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>供应商发票自动化 – 用于查看供应商发票的工作流历史信息的增强体验

提供了易于阅读的供应商发票工作流历史记录视图。 可以直接从供应商发票访问供应商发票工作流历史记录。 因此，只需较少的点击即可找到该信息。

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>供应商发票自动化 – 分析和指标

通过**供应商发票条目**工作区，您可以专注于未通过自动化流程完成的供应商发票。 工作区上的磁贴列出了有关未成功提交到工作流系统，未导入或未与产品收据进行匹配的供应商发票的信息。 还提供了 Microsoft Power BI 指标，以使应付帐款经理可以洞悉供应商发票自动化的效率。
