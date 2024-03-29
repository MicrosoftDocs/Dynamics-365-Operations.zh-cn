---
title: 管理帐页
description: 本文介绍如何使用帐页。 帐页通常包含每个装运的一个实体或公司的一个供应商的货物。 帐页中的货物可以在一个集装箱中，也可以分布在多个集装箱中。
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMFolioTable, ITMFolioTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ab5729cd441246a6c04ac060d5a69f949bfe47c5
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725469"
---
# <a name="manage-folios"></a>管理帐页

[!include [banner](../../includes/banner.md)]

帐页通常由海关法规确定。 它可以包含每个装运的一个实体或公司的一个供应商的货物。 帐页中的货物在一个容器中管理。

要打开 **所有帐页** 页，转到 **登陆成本 \> 帐页 \> 所有帐页**。 此页面显示所有当前帐页的列表。 您可以使用操作窗格上的按钮创建、删除和使用帐页。 在列表中选择任意帐页可以在 **帐页** 页上查看它的详细信息。

## <a name="action-pane"></a>操作窗格

**所有帐页** 和 **帐页** 页上的操作窗格提供让您可以使用选定帐页的按钮。 每个按钮执行一个操作。 操作窗格还包含选项卡，每个选项卡又提供一组相关按钮。 除非另有说明，否则以下小节中所述的所有按钮和选项卡在列表视图（即 **所有帐页** 页）和详细视图（即 **帐页** 页）中均可用。

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>直接显示在操作窗格上的按钮

下表描述了直接操作窗格上提供的按钮。

| 按钮 | 说明 |
|---|---|
| 新项 | 创建帐页。 |
| Delete | 删除打开或选择的帐页。 |
| 航行成本 | 打开 **航行成本** 页，您可以在其中查看帐页级成本并将其添加到航行中的所有货物。 将帐页成本手动添加到航行后，它们会自动添加到成本查询页面，并根据 **航行成本** 页指定的方法分摊到每个货物。 |

### <a name="buttons-on-the-manage-tab"></a>“管理”选项卡上的按钮

下表描述了操作窗格的 **管理** 选项卡上的可用按钮。

| 按钮 | 说明 |
|---|---|
| 将收货清单过帐 | 为帐页中的所有采购订单行过帐收货清单。  |
| 过帐产品收据 | 在帐页中为所有采购订单行过帐产品收货。 |
| 将发票过帐 | 为帐页中的所有采购订单行过帐发票。  |
| 装运转移单 | 过帐与相关装运中的当前帐页相关的所有转移单行的转移单。 |
| 接收转移单 | 过帐与相关装运中的当前帐页相关的所有转移单行的转移单接收。 |
| 接收在途货物 | 接收帐页中正在运输中的所有订单行。 |
| 已收到单据 | 将 **已收到单据** 选项的设置更新为 *是*。 您可以使用此按钮锁定物料和/或采购行，使其无法进一步更新。 |
| 查找自动成本 | 查找相关的航行成本。 如果已经找到或更新了这些成本，您将收到以下消息：“存在未开票成本行。 是否要覆盖它们？” 请注意，附加到帐页且已开票的航行成本不会被覆盖。 |
| 创建到达日记帐 | 使用高级仓库功能为组织生成到达日记帐。 您可以选择 **初始化数量**（建议）、**从在途货物创建** 和/或 **从采购订单创建**。 最后选项取决于是否使用了在途货物处理。 |
| 应计成本 | 当成本类型具有为借方指定的会计科目时，应计成本。 此按钮通常在存货在运输途中或货物已接收和开票时使用。 |

### <a name="buttons-on-the-general-tab"></a>“常规”选项卡上的按钮

下表描述了操作窗格的 **常规** 选项卡上的可用按钮。

| 按钮 | 说明 |
|---|---|
| 收货清单 | 为帐页中的所有采购订单行过帐收货清单。  |
| 产品收货 | 查看产品收货记录（如果使用）。 |
| 物料到达 | 查看物料到达日记帐（如果使用）。 |
| 成本查询 | 打开成本查询页查看航行的所有成本，包括装运集装箱、帐页和采购订单。 您可以使用“查看”操作调整页面的精确视图。 在成本查询页上，您可以查看任何区域，以及物料和成本类型代码。 通过删除这些物料，您可以通过将成本分组在一起来调整页面。 如果您使用尺寸和颜色，此功能可能会很有用。 您可以更改页面上显示的维度。 **成本** 页仅显示将 **过帐** 选项卡上的 **借记** 条目设置为 *物料* 的成本类型代码。 |

## <a name="header-view"></a>标头视图

要打开 **标头** 视图，打开帐页，然后选择帐页标题右上角的 **标头** 选项卡。

### <a name="settings-on-the-general-fasttab"></a>常规快速选项卡上的设置

下表描述了帐页的 **标头** 视图的 **常规** 快速选项卡上的可用字段。

| 字段 | 说明 |
|---|---|
| 帐页 | 帐页的名称。 此名称在帐页创建时自动生成。|
| 航行 | 与帐页关联的航行。 |
| 关税代理 | 选择帐页的关税代理。 关税代理在供应商上定义。 它们让创建的成本可以自动确定。 |
| 内部航空运单/提单 | 指定将应用于帐页的内部航空运单或提单。 |
| 公司 | 与帐页关联的法人（公司）。 |
| 货物控制编号 | 此字段由某些国家或地区的海关部门使用。 |
| 量化指标 | 此字段支持在 **登陆成本** 模块中指定度量。 不知道商品单个体积或重量，但需要比金额或数量提供的更准确分摊的组织经常使用度量。 货运转运商将提供重量或体积度量，您可以将其放在物料或采购订单级别。 如果选择或手动输入了参数，它可以自动更新。 |
| 度量单位 | 将应用于指定度量的单位。 |
| 纸箱数量 | 帐页中纸箱的数量。 根据参数选择，此字段可以自动更新。 |
| 供应商帐户 | 选择与帐页关联的供应商。 此字段仅供参考。 它不影响任何功能。 |
| 姓名 | 所选供应商帐户的名称。 |
| 注解 | 输入与帐页相关的其他信息。 |
| 货物描述 | 选择货物描述可以帮助识别帐页。 有关详细信息，请参阅[货物的描述](shipping-information-setup.md#description-of-goods)。 |
| 估价日期 | 此字段与关税条目页相关。 **登陆成本** 模块将使用您在此处设置的日期的海关汇率。 默认值是关税条目页上的日期。 |
| 海关 ID | 输入海关 ID。 国家或地区的海关部门提供此 ID。 |
| 关税代码 | 输入要与帐页关联的关税代码。 您要装运到的国家或地区通常需要（和定义）此代码。 |

### <a name="settings-on-the-delivery-fasttab"></a>交货快速选项卡上的设置

下表描述了帐页的 **标头** 视图的 **交货** 快速选项卡上的可用设置。

| 字段 | 说明 |
|---|---|
| 帐页日期 | 选择要与帐页关联的日期。 默认值是航行的创建日期。 |
| 装运港口 ETA | 目标港口（“到达”港口）的估计到达时间 (ETA) 日期。 |
| 预计交货日期 | 通常，是货物应到达仓库的日期。 计算估计交货日期时不使用此字段。 （改为使用跟踪控制估计交货日期。）要设置此字段，使值与跟踪控制估计交货日期匹配，请使用[跟踪控制中心](delivery-information-setup.md#tracking-control-center)。 |
| 已收到原始单据 | 收到原始单据的日期。 |
| 已建议代理 | 通知代理的日期。 |
| 已发送原始提单 | 发送原始提单的日期。 |
| 已发放货物 | 发放货物的日期。 |
| 客户预约 | 客户预约日期。 |
| 已在仓库交货 | 货物交付到仓库的日期。 |
| 验证日期 | 验证日期。 |
| 交货说明 | 收到交货说明的日期。 |
| 发运港口 | 航行出发的港口。 |
| 目标港口 | 航行到达的港口。 装运集装箱可能有不同的港口，因为船可能会在多个港口停留。 |

### <a name="settings-on-the-export-fasttab"></a>出口快速选项卡上的设置

下表描述了帐页的 **标头** 视图的 **出口** 快速选项卡上的可用设置。

| 字段 | 说明 |
|---|---|
| 出口商 | 出口商可以存储在帐页上。 在国际贸易中，您可能向一个公司发送采购订单，但从另一个公司接收货物。 海关需要跟踪和记录。 出口商的名称和地址可以存储在这里。 |
| 姓名 | 所选出口商的名称。 |

## <a name="lines-view"></a>行视图

要打开 **行** 视图，打开帐页，然后选择帐页标题右上角的 **行** 选项卡。

### <a name="information-on-the-folio-fasttab"></a>帐页快速选项卡上的信息

**行** 视图中的 **帐页** 快速选项卡显示有关帐页的信息。 这些信息中的大多数还会显示在 **标头** 视图中，如本文前面所述。

### <a name="information-and-buttons-on-the-lines-fasttab"></a>行快速选项卡上的信息和按钮

**行** 视图中的 **行** 快速选项卡显示有关当前帐页中包含的每个完整或部分采购订单行的详细信息。

下表描述了 **行** 视图中的 **行** 快速选项卡上的可用按钮。

| 按钮 | 说明 |
|---|---|
| 移动 | 从航行中删除所选的采购订单行。 |
| 库存 \> 交易记录 | 查看所选采购订单行的库存交易记录。 请注意，如果您使用的是在途货物，还会显示原始订单和在途货物订单。 |
| 库存 \> 显示维度 | 打开一个对话框，您可以在其中选择针对您查看的交易记录显示的库存维度。 |
| 刷新 | 更新与所选采购订单行的行金额、重量或体积相关的信息。 |

### <a name="information-on-the-lines-details-fasttab"></a>行详细信息快速选项卡上的信息

**行** 视图中的 **行详细信息** 快速选项卡显示有关当前在 **行** 快速选项卡上选择的采购订单行的详细信息。
