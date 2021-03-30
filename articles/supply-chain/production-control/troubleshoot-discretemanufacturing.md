---
title: 离散制造疑难解答
description: 此主题介绍如何解决使用离散制造时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2004a48455939855df54c3087a11c8003d825566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222745"
---
# <a name="troubleshoot-discrete-manufacturing"></a>离散制造疑难解答

此主题介绍如何解决使用离散制造时可能遇到的问题。

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>我收到以下错误消息：“仓库管理流程当前正在使用。 如果工作行尚未登记，您可以取消创建的工作以及所有负荷或装运行，然后继续领料或装运流程。”

### <a name="issue-description"></a>问题描述

如果您尝试预留或下达某个行的工作，但库存交易的状态为 *已领料*（指示物料已领取），这时会发生此问题。

### <a name="issue-resolution"></a>解决问题

若要解决此问题，请按照以下其中一个步骤操作。

- 将生产订单的状态更改回 *已估计* 或 *已下达*。
- 打开相关生产订单的详细信息页面。 在操作窗格上的 **仓库** 选项卡上，在 **停止** 组中，选择 **停止并取消领料** 取消所有已领料交易的领料。 然后选择 **删除停止** 以处理生产订单。

这里是对 *取消领料* 和 *停止* 功能的说明：

- **取消领料** – 此功能撤消状态从 *已领料* 一直到 *在单* 的物料清单 (BOM) 行和配方行的库存交易状态。 原材料领料工作完成后，行的状态将设置为 *已领料*。 此状态防止将生产订单重置为 *已创建* 状态。 在这种情况下，您可以使用 *取消领料* 功能从 *已领料* 状态恢复交易，然后将生产订单重置为 *已创建* 状态。
- **停止** – 此功能在生产订单上设置 **已停止** 标记，以防止对订单进行任何状态更新。 您可以在生产订单详细信息页的 **仓库** 快速选项卡上找到 **已停止** 标记。

> [!NOTE]
>
> - 仅当为仓库流程启用的物料创建生产订单时，按钮才可见。
> - **停止** 组仅在生产订单详细信息页的操作窗格上的 **仓库** 选项卡上可见。 在 **生产订单** 列表页的 **仓库** 快速选项卡上不可见。

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>我在全球通讯簿中更改工作人员姓名后，匹配的资源姓名不更新。

### <a name="issue-description"></a>问题描述

如果您在全球通讯簿中更改工作人员姓名，匹配的资源姓名不会在主资源组中更新。

### <a name="issue-resolution"></a>解决问题

当前不支持此场景。 若要解决此问题，您必须手动更新资源姓名。

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>我在创建新生产订单时，没有收到以下消息：“插入物料清单和工艺路线的有效版本？”

### <a name="issue-description"></a>问题描述

创建新的生产订单时，输入物料编号后，**站点** 和 **仓库** 字段将自动设置为在成品物料的 **默认订单设置** 页上定义的默认站点和仓库。 此外，有效的物料清单编号和工艺路线编号也将自动输入。 您不会收到以下提示您输入这些值的消息：

> 插入物料清单和工艺路线的有效版本？

### <a name="issue-resolution"></a>解决问题

如果您选择了在 **默认订单设置** 页上为其定义了站点和仓库的产品，则不会提示您插入物料清单和工艺路线编号。 只有在没有为所选产品定义这些值时，才会提示您。

## <a name="production-orders-arent-shown-on-the-marking-page"></a>生产订单没有显示在“标记”页上。

### <a name="issue-description"></a>问题描述

有些生产订单不会显示在 **标记** 页上。

### <a name="issue-resolution"></a>解决问题

具有以下配置的产品不能进行标记。 因此，它们不会显示在 **标记** 页上：

- 这些产品定义为 *实际称重* 类型的产品。
- 它们已启用高级仓库流程。
- 它们被配置为由 *标准成本* 原则控制。

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>当我尝试结束生产订单时，收到以下错误消息：“计算的物料清单 consumptionCost 值在从库存发货时必须为负。”

此问题在版本 10.0.15 中已修复。

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>当生产订单的状态从“完工入库”更改为“结束”时，我收到以下错误消息：“更新冲突。 标准成本与更新后的财务库存值不匹配”和“InventCostMovement.checkVariance 函数中发生严重错误”。

发生此问题的原因是基础数据被另一个流程更改。 此流程最多会尝试更新数据五次。 如果五次尝试后冲突仍然存在，您将收到以下错误消息：

> 更新冲突。 标准成本在更新后与财务库存值不匹配。

> 函数 InventCostMovement.checkVariance 中发生严重错误。

此为有意行为。 要缓解此问题，请继续批处理作业。 它应该完成运行。

如果批处理作业在您恢复后持续失败，请验证分类帐默认货币的舍入精度是否符合应用于 InventSum 表中的值的舍入要求。 如果舍入精度更改为不符合要求的值，您可能必须将其重新更改为符合要求的值。 查找 **ModifiedDateTime**。 在这种情况下，此值通常会显示舍入精度最近已更改。

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>当我下达到仓库时，我收到以下错误消息：“物料 RM 无法完整预留。 请确保全部数量都可用，或者如果物料清单行上的“预留”字段设置为“手动”或“已开始”，则手动预留物料。 无法将订单下达到仓库，因为某些材料无法预留。” 但是，状态会更新为“已下达”。

### <a name="issue-description"></a>问题描述

如果在下达生产订单时，不是所有物料清单行项实际都可用，当生产订单上的 **发放到仓库** 策略设置为 *需要全部预留* 时，您将收到以下错误消息：

> 物料 RM 无法完全预留。 请确保全部数量都可用，或者如果物料清单行上的“预留”字段设置为“手动”或“已开始”，则手动预留物料。 无法将订单发放到仓库，因为某些材料无法预留。

### <a name="issue-resolution"></a>解决问题

此行为是有意设计的，属于正常工作。

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>当我尝试结束生产订单并报告完工入库时，我收到以下错误消息：“生产报告为完工入库的总计完好数量将是 %1。 最后一道工序的反馈总计为 0.00 个。”

### <a name="issue-description"></a>问题描述

当您尝试在生产订单上过帐完工入库日记帐时，会收到以下错误消息：

> 生产完工入库的完好数量合计将是 %1。 最后一道工序的反馈总计为 0.00 个。

### <a name="possible-cause"></a>可能原因

如果最后工序中过帐的数量不正确，将发生此问题。 例如，如果生产已开始，但未分配必须开始的数量，工艺卡日记帐在过帐时将没有任何行。 要确认情况，请打开生产订单，然后在操作窗格上的 **视图** 选项卡上，选择 **工艺卡**。

### <a name="workaround"></a>解决方法

您可以通过为日记帐未正确过帐的操作过帐其他日记帐来解决此问题。 重新启动生产订单，然后选择过帐其他日记帐。 此操作不会启动生产订单，但会过帐日记帐。 然后，工艺卡应会显示已过帐的数量，您应该能够成功结束生产订单。

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>我可以在报告错误数量时将生产订单报告为完工入库，但在报告时间或物料数量时不这样报告吗？

您不能报告生产订单上的错误数量，除非您同时也报告了完好数量。 **不** 支持此场景。 完工入库更新会在您尝试结束生产订单时最终失败，您将收到以下错误消息：

> 缺少报告为完工入库的数量。

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>我可以根据消耗品的序列号跟踪成品的序列号吗？

您不能根据生产订单生产这些成品所消耗的物料的序列号来跟踪成品的序列号。 当前不支持此场景。 解决方法是创建数量为 1 的生产订单。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]