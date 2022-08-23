---
title: 出站集装箱装箱和装运处理的包装工作
description: 本文介绍“装箱”工作订单类型，该类型管理集装箱的装箱工作，在库存物料仍未装箱时，该类型支持与负荷相关的已装箱集装箱的部分装运。
author: perlynne
ms.date: 7/13/2022
ms.topic: article
ms.search.form: WHSPackingWorkLocationSetup, WHSPack, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 34a7087df7e7768d0012ea4f534aa109654af8fa
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220524"
---
# <a name="packing-work-for-packing-outbound-containers-and-processing-shipments"></a>出站集装箱装箱和装运处理的包装工作

[!include [banner](../../includes/banner.md)]

本文介绍 *装箱* 工作订单类型，该类型管理集装箱的装箱工作，在库存物料仍未装箱时，该类型支持与负荷相关的已装箱集装箱的部分装运。 装箱工作允许您使用[确认和转移](confirm-and-transfer.md)功能来确认与集装箱关联的出站装运。

将与原始单据工作相关的库存放入 *装箱库位类型* 的库位时，将自动创建装箱工作。 该工作由两行组成，一行用于 *领料*，一行用于 *放置*，并作为集装箱关闭/重新打开流程的一部分自动维护。

有关如何设置和使用集装箱装箱流程的详细信息，请参阅[装入集装箱以进行装运](packing-containers.md)。

## <a name="turn-on-the-feature"></a>开启功能

如果您的系统尚未包含本文中所述的功能，请转到[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，按以下顺序打开以下功能。 这两个功能都是 **仓库管理** 模块的一部分。

1. *确认并转移*
1. *装箱工作站的装箱工作*

## <a name="set-up-a-location-for-packing-work"></a>设置装箱工作的库位

使用以下过程设置装箱库位。 对于每个库位，您可以选择系统是否自动创建装箱工作。

1. 转到 **仓库管理 \> 设置 \> 装箱 \> 装箱工作站设置**。
1. 在操作窗格上，选择 **新建** 以添加装箱工作站设置记录。
1. 在新记录中，设置以下字段：

    - **仓库** – 选择或输入装箱库位所在的仓库。
    - **库位** - 选择或输入装箱库位。 必须将此库位分配给使用库位类型的库位配置文件，此库位类型在 **仓库管理参数** 页上被配置为贵公司的装箱库位类型。 有关详细信息，请参阅[装入集装箱以进行装运](packing-containers.md)。
    - **创建装箱工作** - 选中此复选框可在每次将物料交付到装箱库位时创建装箱工作。 该工作将包括指向相关负荷行的链接，以便可以装箱和装运部分负荷。

## <a name="example-scenario"></a>示例场景

此示例方案显示如何通过装箱集装箱和装运部分负荷来处理出站销售订单流。

### <a name="make-sample-data-available"></a>提供示例数据

若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)。 此外，开始前，还必须选择 **USMF** 法人。

您还可以将此方案用作在生产系统上使用此功能的指导。 但是，如果是这样，您必须替换这里介绍的每个设置中的自己的值。

### <a name="configure-packing-work-for-warehouse-packing-location"></a>配置仓库装箱库位的装箱工作

首先，您必须为特定仓库和库位配置 *装箱* 工作流程。

1. 转到 **仓库管理 \> 设置 \> 装箱 \> 装箱工作站设置**。
1. 在操作窗格上，选择 **新建** 以添加设置记录。
1. 在新记录中，设置以下值：

    - **仓库**：*62*
    - **位置**：*装箱*
    - **创建装箱工作**：*是*

1. 关闭 **装箱工作站设置** 页面。

### <a name="create-a-load-template-that-allows-partial-shipping"></a>创建允许部分装运的负荷模板

若要使负荷在多个装运中交货，您必须将其与允许部分装运的负荷模板关联。 请执行以下步骤以创建所需的模板。

1. 转到 **仓库管理 \> 设置 \> 负荷 \> 负荷模板**。
1. 在操作窗格上，选择 **新建** 以添加设置记录。
1. 在新记录中，设置以下值：

    - **负荷模板 ID**：*部分*
    - **允许负荷在装运确认期间拆分**：*是*

1. 关闭 **负荷模板** 页面。

有关详细信息，请参阅[确认并转移](Confirm-and-transfer.md)。

### <a name="process-a-sales-order"></a>处理销售订单

按照这些步骤处理销售订单并对销售订单进行部分装运。

1. 完成[装入集装箱以进行装运](packing-containers.md#scenario)中提供的[示例方案](packing-containers.md)。 在此方案中，您将为一个物料的两个部分创建销售订单。 然后，您将仅将其中一个部件装箱到集装箱中并封闭此集装箱。 您应根据方案中的指示记录所创建的装运 ID。
1. 转到 **仓库管理 \> 工作 \> 所有工作**。
1. 在筛选器区域中，选中 **显示已结束的工作** 复选框。 然后，在 **筛选器** 字段中输入装运 ID，并选择以按 **装运 ID** 值进行筛选。 您现在应看到三个工作标题。 一个用于销售订单领料工作，其状态为 *已关闭*。 两个用于装箱流程：一个与已封闭集装箱相关，并且状态为 *已关闭*，另一个与未装箱的剩余物料相关，并且状态为 *打开*。
1. 选择任何工作标题的 **负荷 ID** 值，以打开负荷的 **负荷详细信息** 页。
1. 切换到 **标题** 视图。
1. 在 **常规** 快速选项卡上，选择 **负荷模板 ID** 字段的 **编辑** 按钮。 然后，选择您为此方案创建的部分装运负荷模板（*部分*）。
1. 在操作窗格上 **装运和接收** 选项卡上 **确认** 组中，选择 **出站装运**。
1. 在 **装运确认** 对话框中，选择 **已将数量拆分至新负荷** 选项。
1. 选择 **确定**。

您现在已装运一个与原始负荷相关的集装箱，并且系统已为仍必须装入集装箱的剩余物料创建了新负荷。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
