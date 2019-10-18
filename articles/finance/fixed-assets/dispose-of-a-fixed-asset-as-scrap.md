---
title: 将固定资产作为废料处置
description: 本主题介绍清除作为废料处置的固定资产交易记录的过程。
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: de105e061712540fc8e3d720a65c029f865b8948
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187283"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>将固定资产作为废料处置

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本主题介绍清除作为废料处置的固定资产交易记录的过程。 可以清除的交易记录类型包括资产的购置和累计折旧交易记录以及其他固定资产交易记录。 清除这些交易记录会影响资产负债表科目，例如购置调整、折旧调整、重估、调高和调低科目。

| 交易                                         | 借记（借） | 贷记（贷） |
|-----------------------------------------------------|-------------|--------------|
| 借记累计折旧                        | X           |              |
| 贷记固定资产损益                          |             | X            |
| 借记固定资产损益                          | X           |              |
| 贷记固定资产购置科目                 |             | X            |
| 借记固定资产损益（帐面净值 \[NBV\]） | X           |              |
| 贷记固定资产损益 (NBV)                    |             | X            |

> [!NOTE]
> 我们建议您与公司的首席财务官 (CFO) 或财务总监紧密合作，以确定每种交易记录类型应使用的正确科目，并验证处置过程及其产生的交易记录是否正确更新了这些科目。

在将固定资产作为废料处置之前，必须创建与资产的购置价值、当年的折旧、前一年的折旧以及资产的 NBV 关联的会计科目。 固定资产交易记录类型列在**固定资产过帐模板**页面上。 转到**固定资产 \> 设置 \> 固定资产过帐模板**，然后在**处置**快速选项卡上，在网格上方的字段中选择**废料**。 下图显示了**固定资产过帐模板**页面上的固定资产交易记录类型的列表。


[![作为废料处置资产，图 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

对于以下示例，固定资产于 2018 年 1 月 1 日购置，将于 2019 年 3 月 31 日报废。

- **购置价格：** 24,000.00 美元 (USD)
- **使用年限：** 两年
- **折旧方法：** 直线法
- **折旧金额：** 每月 1,000.00 美元

使用以下公式计算固定资产的 NBV：

帐面净值 = 购置价格 – 折旧

在此示例中，从 2018 年 1 月到 2019 年 3 月，固定资产购置和折旧为时 15 个月。 因此，资产的 NBV 为 9,000.00 美元（24,000.00 美元 – 15,000.00 美元）。

[![固定资产折旧示例](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


要创建处置日记帐，请转到**固定资产 \> 日记帐分录 \> 固定资产日记帐**，然后，在“操作窗格”中，选择**行**。 选择**处置 – 报废**，然后选择固定资产 ID。 要完全处置资产，请不要在**借记**字段或**贷记**字段中输入值。

[![固定资产日记帐](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

固定资产处置报废交易记录通过以下方式更改固定资产帐簿的字段值：

- 在**余额**部分，**状态**字段更新为**已报废**。
- 在**签发**部分，**处置日期**字段设置为资产报废的日期。

[![固定资产日记帐明细](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

下图显示了固定资产余额。

[![固定资产余额](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

下图显示了已过帐的凭证。

[![帐面净值](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)
