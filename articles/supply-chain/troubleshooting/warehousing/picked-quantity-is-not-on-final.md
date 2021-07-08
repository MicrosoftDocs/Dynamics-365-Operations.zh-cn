---
title: 您无法确认装运，因为物料尚未领取
description: 您无法确认装运，因为物料尚未领取
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301297"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>您无法确认装运，因为物料尚未领取

错误代码：LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>故障特征

当您尝试确认装运时，系统显示以下错误消息：

> 负荷 %1 所需的部分物料尚未领料并且已移至最终装运库位。

因此，您无法确认负荷的装运。

## <a name="cause"></a>原因

负荷或装运无法在其当前状态下确认，因为可能存在以下其中一种情况：

- 相关工作尚未领取并被移至最终装运位置。
- 领取的工作数量与负荷行上创建的工作数量不匹配。
- 在使用波次模板集装化时，库位指令已配置为作为最终装运库位的包装库位。

## <a name="resolution"></a>解决方法

负荷或装运当前处于装运确认失败的状态。 要解决此问题，请完成以下任务之一：

- 查看您的负荷行并确保所有相关工作已在最终装运库位完成，并且数量匹配。
- 取消使用包装库位作为最终装运库位创建的工作 ID，重新配置库位指令，并重新发放负荷。

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>查看您的负荷行并确保所有相关工作已在最终装运库位完成，并且数量匹配

使用以下过程查看您的负荷行，并确保所有相关工作已在最终装运库位完成，并且数量匹配。

1. 转到 **仓库管理 \> 负荷 \> 所有负荷**。
1. 选择无法确认装运的负荷。
1. 在 **负荷行** 快速选项卡上，选择负荷行。
1. 记下 **创建的工作数量** 字段的值。
1. 在操作窗格的 **负荷** 选项卡上的 **相关信息** 组中，选择 **工作**。
1. 验证工作已在最终装运位置完成，并且所领取的工作数量与负荷行上创建的工作数量匹配。
1. 对所有负荷行重复此过程，确保满足所有条件。

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>取消使用包装库位作为最终装运库位创建的工作 ID，重新配置库位指令，并重新发放负荷

使用以下过程取消使用包装库位作为最终放置库位并采用自动集装化的工作 ID。

1. 转到 **仓库管理 \> 定期任务 \> 清理 \> 取消工作**。
1. 将打开 **取消工作** 对话框。 在 **工作 ID** 字段中，指定要取消的工作的 ID。 选定的工作 ID 必须具有 *打开*、*进行中*、*已取消*、*已合并* 或 *已关闭* 的 **工作状态** 值。
1. 选择 **确定**。
1. 选择 **是** 确认要取消该工作。
1. 根据需要对其他工作 ID 重复此过程。

有关详细信息，请参阅[取消要进行异常处理的仓库工作](../../warehousing/cancel-warehouse-work.md)。

使用以下过程重新配置库位指令，以便在为波次模板设置自动集装化时不会使用包装库位作为最终装运库位。

1. 转到 **库存管理 \> 设置 \> 位置指令**。
1. 在 **工作订单类型** 字段中，选择 *销售订单*。
1. 选择用于自动集装化的库位指令。
1. 在 **库位指令操作** 快速选项卡工具栏上，选择 **编辑查询**。
1. 在查询编辑器对话框中的 **范围** 选项卡上，找到 **字段** 设置为 *库位配置文件* 的行，验证该行的 **条件** 字段未设置为 **库位类型** 为 *包装* 的库位配置文件。 调整 **条件** 字段以更正最终放置库位。

使用以下过程重新发放负荷并创建具有正确最终装运库位的工作 ID。

1. 转到 **仓库管理 \> 装载 \> 装载计划工作台**。
1. 在 **负荷** 部分中，查找需要发放的负荷。
1. 在 **负荷** 部分工具栏上，选择 **发放 \> 发放到仓库** 以将选定负荷发放到仓库。
1. 根据需要对其他负荷重复此过程。
