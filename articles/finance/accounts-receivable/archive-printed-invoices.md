---
title: 使用哈希编号存档打印的客户账单
description: 本主题说明如何启用存档以存储带有哈希编号的打印客户发票。
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827690"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>使用哈希编号存档打印的客户账单

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

在某些国家/地区，法律要求将计算出的哈希编号与某些文档的打印输出一起存储在系统中。 哈希编号可用于向权威机构报告以及在审核期间报告。

本主题说明如何配置存档以存储带有哈希编号的打印客户发票。

## <a name="prerequisites"></a>先决条件

- 在 **功能管理** 工作区，打开 **存档带有哈希编号的打印客户发票** 功能。 有关更多信息，请参见[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。
- 在 **打印管理** 中配置所需文档的可打印格式。

此功能适用于以下文档。

**应收账款**
- 客户账单
- 客户贷方通知单
- 普通账单
- 普通贷方通知单

**项目管理与核算**
- 项目账单
- 项目贷方通知单

## <a name="configure-customer-master-data"></a>配置客户主数据
完成以下步骤以配置客户数据，并启用自动将打印发票另存为附件的功能。

1. 转到 **应付帐款** > **所有客户**。 
2. 选择客户，然后在 **发票和交货** 快速选项卡上的 **电子发票** 部分，在 **电子发票附件** 字段中，选择 **是**。

## <a name="print-invoices"></a>打印发票
您可以为上一过程中配置的客户过帐和打印任何自由文本形式的客户和项目发票或贷方通知单。

针对打印的发票打开 **附件** 页面。 在 **附件** 快速选项卡上 **其他详细信息** 字段组内的 **文件哈希编号** 字段中，查找为打印发票计算的已存储哈希编号。

![附件哈希编号](media/attach-hash-num.jpg)

