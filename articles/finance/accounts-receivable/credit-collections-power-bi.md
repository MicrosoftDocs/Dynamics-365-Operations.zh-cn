---
title: 信用和收款管理 Power BI 内容
description: 此主题介绍信用和收款管理 Power BI 内容中的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。
author: ShivamPandey-msft
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 65423f49ba106a152f58c92533c4f1a16d47a318982cfe69bb23f9091fa09846
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763206"
---
# <a name="credit-and-collections-management-power-bi-content"></a>信用和收款管理 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍 **信用和收款管理** Microsoft Power BI 内容中所包含的内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="overview"></a>概览

**信用和收款管理** Power BI 内容是为信用和收款经理和收款职员而创建的。 它提供关键信用和收款指标，例如销售款未清天数、逾期余额、信用曝光和超出信用额度的客户。 它使用交易记录数据，并且提供跨所有公司的信用和收款的聚合视图。 它还提供各公司、客户组和客户的明细。

此 Power BI 内容包括 10 个报表页：

- 两个概览页（一页用于信用概览，另一页用于收款概览）
- 八个详细信息页，提供跨不同维度划分和细分的信用和收款指标的详细信息。

所有金额均以系统币种显示。 您可以在 **系统参数** 页设置系统币种。

默认情况下，显示当前公司的信用和收款数据。 要查看跨所有公司的数据，请将 **CustCollectionsBICrossCompany** 责任分配到角色。

## <a name="setup-needed-to-view-power-bi-content"></a>查看 Power BI 内容所需设置

需要完成以下设置，才能在 **客户信用和收款** Power BI 视觉对象中显示数据。

1. 转到 **系统管理 > 设置 > 系统参数** 以设置 **系统币种** 和 **系统汇率**。
2. 转到 **总帐 > 日历 > 会计日历** 验证分配到有效时段的会计日历日期。
3. 转到 **总帐 > 设置 > 分类帐** 并设置 **记帐币种** 和 **汇率类型**。
4. 定义交易币种与记帐币种和记帐币种与系统币种之间的汇率。 方法是，转到 **总帐 > 币种 > 币种汇率**。
5. 转到 **系统管理 > 设置 > 实体商店** 刷新 **CustCollectionsBIMeasurementsV2** 聚合度量。

>[!NOTE] 
> 必须在 **应收帐款参数 > 收款 > 收款默认** 中设置帐龄期间定义，才能在 Power BI 内容中启用帐龄数据。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容

**信用和收款管理** Power BI 内容显示在 **客户信用和收款** 工作区。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>此 Power BI 内容中包含的报表

**CustCollectionsBICrossCompany** Power BI 内容包括一个含有一组指标的报表。 这些指标显示为图表、磁贴和表。 下表概要介绍 **CustCollectionsBICrossCompany** Power BI 内容中的可视化。

| 报表页                 | 可视化 |
|-----------------------------|---------------|
| 收款概览        | <ul><li>客户过期</li><li>客户超出信用额度</li><li>DSO 30 天</li><li>未结案例</li><li>关闭案例的平均天数</li><li>未结活动</li><li>关闭活动的平均天数</li><li>未结利息单</li><li>未结催款单</li><li>客户暂停</li><li>销售暂停</li><li>帐龄余额</li><li>收款状态金额</li><li>收款代码金额</li><li>按原因勾销</li><li>结欠金额(按地区)</li><li>预期付款</li></ul> |
| 信用概览             | <ul><li>客户过期</li><li>信用额度与结欠金额</li><li>客户超出信用额度网格</li><li>每个公司的超出信用额度的客户</li><li>已使用信用额与总信用额度</li><li>信用额度与已使用信用额（按地区）</li><li>每种信用等级的客户</li></ul> |
| 信用额度                | <ul><li>信用额度</li><li>信用额度明细</li><li>信用额度（按客户）</li><li>每个客户组的信用额度</li><li>每个公司的每种信用等级的信用额度</li><li>信用额度与已用贷款(按地区)</li></ul> |
| 客户超出信用额度 | <ul><li>客户超出信用额度</li><li>客户超出信用额度明细</li><li>每个公司的超出信用额度的客户</li><li>超出信用额度的客户（按客户组）</li><li>超出信用额度的客户(按地区)</li></ul> |
| 客户过期          | <ul><li>客户过期</li><li>客户过期明细</li><li>客户过期（按公司）</li><li>客户过期（按客户组）</li><li>客户过期（按地区）</li></ul> |
| 帐龄余额               | <ul><li>帐龄余额</li><li>帐龄余额明细</li><li>每个公司的帐龄较长的余额</li><li>每个客户组的帐龄较长的余额</li></ul> |
| 预期付款           | <ul><li>预期付款</li><li>预期付款明细</li><li>每个公司的预期付款</li><li>每个客户组的预期付款</li><li>预期付款(按地区)</li></ul> |
| 勾销                  | <ul><li>勾销（按地区）</li><li>勾销明细</li><li>勾销（按主科目）</li><li>勾销（按公司）</li><li>勾销（按客户组）</li><li>勾销（按地区）</li></ul> |
| 收款状态          | <ul><li>争议</li><li>承诺付款已中断</li><li>承诺付款</li><li>收款状态明细</li><li>收款状态金额</li><li>未结案例</li><li>未结活动</li></ul> |
| 催款单         | <ul><li>收款代码金额</li><li>收款代码金额明细</li><li>催款单金额（按公司）</li><li>催款单金额（按客户组）</li><li>催款单金额（按地区）</li></ul> |

所有这些报表中的图表和磁贴均可以筛选和并固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/)。 您还可以使用导出基础数据功能导出在可视化中汇总的基础数据。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]