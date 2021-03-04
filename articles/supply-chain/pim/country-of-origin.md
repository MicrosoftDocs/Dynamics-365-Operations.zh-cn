---
title: 原产国家/地区
description: 许多组织向其供应商颁发证书，以确保产品符合特定的认证标准。 这些证书通常依赖于原产国家/地区。 本主题提供有关原产国家/地区功能的信息，让您可以将产品链接到其原产国家/地区并跟踪产品认证。
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0471785991a307de11147e9773d9abe1e02941d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422662"
---
# <a name="country-of-origin"></a>原产国家/地区

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

许多组织向其供应商颁发证书，以确保产品符合特定的认证标准。 这些证书通常依赖于原产国家/地区。 原产国家/地区功能让您可以将产品链接到其原产国家/地区并跟踪产品认证。

## <a name="turn-on-the-country-of-origin-feature"></a>打开原产国家/地区功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*产品信息管理*
- **功能名称**：*远程国家/地区管理功能*

## <a name="configure-source-and-destination-countries"></a>配置来源与目标国家/地区

在发放产品证书之前，必须将产品链接到其目标国家/地区和原产国家/地区。

1. 转到 **产品信息管理 \> 设置 \> 产品合规性 \> 原产国家/地区 \> 原产国家/地区规则**。
2. 选择要编辑的现有国家/地区设置，或在“操作窗格”上选择 **新建** 创建新的国家/地区设置。
3. 为所选或新国家/地区设置以下值。

    | 字段 | 说明 |
    |---|---|
    | 物料编号 | 选择产品的物料编号。 |
    | 目标国家/地区 | 选择要将产品发送到的国家/地区。 |
    | 原产国家/地区 | 选择您装运产品的国家/地区。 |

此设置的目的是帮助您生成物料清单 (BOM) 报告，报告中可以包括指定了来源和目标国家/地区的每个部件的原产国家/地区。 此报告将帮助您全面了解部件的来源和去向。

## <a name="keep-track-of-vendor-certificates"></a>跟踪供应商证书

您可以使用 **原产国家/地区供应商证书** 页面跟踪您发放给供应商的证书。

您必须确定要发放的证书文件以及如何将其报告给客户。 此功能可帮助您跟踪证书。 它还让您可以选择是否在发票、装箱单和/或订单确认单上显示相关的证书编号。

要设置您的证书信息，请按照以下步骤操作。

1. 转到 **产品信息管理 \> 设置 \> 产品合规性 \> 原产国家/地区 \> 原产国家/地区供应商证书**。
2. 选择要编辑的现有证书设置，或在“操作窗格”上选择 **新建** 创建新的证书设置。
3. 为所选或新证书设置以下设置。

    | 字段 | 说明 |
    |---|---|
    | 供应商帐户 | 选择您向其发放证书的供应商。 |
    | 物料编号 | 选择您为其发放证书的物料。 |
    | 国家/地区 | 您必须使用此证书的目标国家或地区。 |
    | 证书编号 | 输入您发放的证书的标识号。 |
    | 已生效 | 选择当前证书有效的第一个日期。|
    | 到期 | 选择当前证书有效的最后一个日期。 |
    | 打印到发票上 | 选中此复选框可在指定日期范围内在发送到指定国家/地区的发票上打印证书编号。 |
    | 打印到装箱单上 | 选中此复选框可在指定日期范围内在发送到指定国家/地区的装箱单上打印证书编号。 |
    | 打印到销售订单上 | 选中此复选框可在指定日期范围内在发送到指定国家/地区的销售订单上打印证书编号。 |

## <a name="include-the-country-of-origin-on-bom-reports"></a>在 BOM 报告中包括原产国家/地区

生成 BOM 报告时，可以为您在 **原产国家/地区规则** 页面上指定了来源和目标国家/地区的每个部件包含原产国家/地区。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择或创建一个产品以打开其 **已发放产品详细信息** 页。
1. 在“操作窗格”的 **设计** 选项卡的 **BOM** 组中，选择 **设计器**。
1. 在显示的页面上的“操作窗格”上，选择 **BOM \> 打印**。
1. 在 **物料清单行** 对话框中，将 **目标国家/地区** 字段设置为要在报告中查看的目标国家/地区。
1. 选择 **确定**。

显示有关每个部件原产国家/地区的信息的报告将生成并显示。 以下是一个报告示例。

![原产国家/地区报告](media/country-of-origin-report.png "原产国家/地区报告")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]