---
title: 年终结算缺少期初余额
description: 本主题介绍了进行年终结算时为什么可能会缺少期初余额，以及缺少期初余额时如何重新生成这些余额。
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 582363ba6c5f6e63e695d41e73ee2f0b382cf26e
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727163"
---
# <a name="year-end-close-missing-opening-balances"></a>年终结算缺少期初余额

[!include [banner](../includes/banner.md)]

本主题介绍了进行年终结算时为什么可能会缺少期初余额，以及缺少期初余额时如何重新生成这些余额。

### <a name="symptom"></a>问题

为什么运行总帐年终结算之后没有期初余额？ 

### <a name="resolution"></a>解决方法

如果您进行总帐年终结算，但生成的试算平衡表未显示下一会计年度的期初余额，可以检查下面几个方面：

如果 **撤消上一次结算** 字段设置为 **是**，将冲销同一会计年度的上一次年终结算。 运行冲销年终结算的流程时，将删除有关期末余额和期初余额的所有条目，好像从未进行年终结算一样。 此外，还将删除凭证。 将不会自动重新运行年终结算流程。 您必须重新启动该流程，此时会将 **撤消上一次结算** 选项更新为 **否**。

年终结算常见问题解答主题中介绍了此情况。 有关详细信息，请参阅[年终活动常见问题解答](faq-year-end-activities.md)。

### <a name="symptom"></a>问题

我在 **撤消上一次结算** 选项设置为 **否** 的情况下运行了年终结算，但我的会计年度仍没有期初余额。

### <a name="resolution"></a>解决方法

请首先检查批处理作业的状态。 年终结算包括多项单独的任务，但是最关键的步骤是批处理任务，**步骤 5.0.0** 中提供了相关任务说明。 在此步骤期间中，会将期初交易记录和可选的期末交易记录过帐到总帐。 

[![批处理历史记录列表。](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)

如果此步骤成功完成，但您在 **试算平衡表查询** 页面上看不到期初余额（**总帐 > 查询和报表 > 试算平衡表**），请查看年终结算批处理作业的结果，以了解是否已成功完成“重新生成余额”步骤。

[![年终结算批处理作业的结果。](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)

如果此步骤由于任何原因而失败，则可能已成功过帐期初（和可选的期末）交易记录。 您可以使用 **凭证交易记录查询** 页面来验证是否已成功过帐总帐交易记录，方法是为所结算的年份指定年终结算对话框上提供的凭证编号和日期（**总帐 > 查询和报表 > 凭证交易记录**）。

[![凭证交易记录查询。](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)

如果存在期初（和可选的期末）凭证，则无需再次运行年终结算。 请参阅下一部分了解有关如何继续的信息。

### <a name="symptom"></a>问题

年终结算中的“重新生成余额”步骤失败，我是否需要重新运行整个年终结算流程？

### <a name="resolution"></a>解决方法

“重新生成余额”步骤会更新在生成试算平衡表查询时使用的总帐余额。  这是年终结算流程中的最后一步。  如果此步骤是唯一失败的步骤，则说明已成功过帐总帐交易记录。  无需再次运行年终结算。 您可以运行该流程以使用 **财务维度集** 页面（**总帐 > 会计科目表 > 维度 > 财务维度集**）手动重新生成余额。

[![“财务维度集”页面上的“重新生成余额”按钮。](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)

如果此步骤需要较长的时间才能完成，我们建议您按照[更新财务维度集的最佳实践](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets)中所述查看财务维度集的最佳实践。 

