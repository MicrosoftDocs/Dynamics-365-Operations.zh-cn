---
title: 供应计划
description: 本主题提供有关供应计划页面及其功能的信息。
author: ChristianRytt
ms.date: 9/3/2021
ms.topic: article
ms.search.form: ReqSupplyDemandSchedule, ReqSupplyDemandScheduleFilters, ReqSupplyDemandItemDetails, ReqTransFuturesActionsPart, ReqSupplyDemandOverviewLegendPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 0d2f0f38d86ae307ef80bd02901e19a08d5e30ae
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578360"
---
# <a name="supply-schedule"></a>供应计划

[!include [banner](../includes/banner.md)]

**供应计划** 页面显示产品或产品系列的供应和需求的全面概览。 信息按位置、主计划和期间筛选。 您还可以使用此页面创建新订单、修改现有计划订单以及运行主计划。

## <a name="open-the-supply-schedule-page"></a>打开供应计划页

您可以通过以下任何方式打开 **供应计划** 页面：

- 转到 **主计划 \> 主计划 \> 供应计划**。 在 **修改筛选器** 对话框中，通过在提供的字段中输入筛选器值指定您要查找的计划和产品。 （在本主题的其余部分，您输入的筛选器值集合称为“筛选器”或“当前筛选器”。）完成后，选择 **确定**。
- 转到 **产品信息管理 \> 产品 \> 已发布产品**。 选择或打开一个产品。 然后，在操作窗格中 **计划** 选项卡上的 **视图** 组中，选择 **供应计划**。
- 转到 **主计划 \> 设置 \> 需求预测 \> 物料分配参数**。 选择用作产品系列的物料分配参数。 然后，在操作窗格上，选择 **供应计划**。
- 转到 **主计划 \> 主计划 \> 计划订单**。 选择或打开计划订单。 然后，在操作窗格中 **视图** 选项卡上的 **视图** 组中，选择 **供应计划**。

> [!NOTE]
> 当您从产品、产品系列或计划订单打开 **供应计划** 页面时，不必输入筛选器值。 系统将使用默认期间模板。

## <a name="use-the-supply-schedule-page"></a>使用供应计划页

**供应计划** 页面包含一个上半部分、**期间结束库存** 快速选项卡、一个额外的快速选项卡，该选项卡基于在上半部分中选择的行显示，以及速见表窗格。 （要打开速见表窗格，查看速见表，选择页面右边缘的 **相关信息**。）

### <a name="upper-section"></a>上半部分

**供应计划** 页面的上半部分包含一个网格，显示产品或产品系列的以下数据。 此数据按筛选器中的 **期间模板** 值定义的期间细分。

- **期间开始库存** – 如果系统中的所有订单都发生，此行显示期间开始时的预期库存余额。
- **期间结束库存** – 如果系统中的所有订单都发生，此行显示期间结束时的预期库存余额。
- **期间结束限定库存** – 此行显示根据未来需求限定的期间结束时的库存量。
- **期间净供应** – 此行显示期间内供应和需求之间的差值。
- **最小库存量** – 此节点显示产品或产品系列的安全存货。 要展开或折叠此节点，选择它，然后选择工具栏上的 **展开** 或 **折叠**。 仅当产品或产品系列有安全存货时才会显示此节点。
- **需求** – 此节点显示产品或产品系列的需求。 需求按交易类型分组。 要展开或折叠此节点，选择它，然后选择工具栏上的 **展开** 或 **折叠**。 需求交易类型包括销售、转移和库存日记帐。 仅当产品或产品系列有需求时才会显示此节点。
- **供应** – 此节点显示产品或产品系列的供应。 供应按交易类型分组。 要展开或折叠此节点，选择它，然后选择工具栏上的 **展开** 或 **折叠**。 供应交易类型包括生产、采购和转移。 仅当产品或产品系列有供应时才会显示此节点。

很多可用的工具栏按钮、速见表显示和快速选项卡显示取决于您在上半部分中的选择。 通常，您将通过选择 **供应** 或 **需求** 节点下的其中一个行来选择交易类型。 然后，您将通过为所选行选择特定列来选择一个期间。

**供应计划** 页面上半部分中网格上方的工具栏提供以下按钮：

- **展开/折叠** – 展开或折叠所选节点，如 **需求** 节点、**供应** 节点及其子节点。 （节点显示 **\[+\]** 或 **\[-\]** 前缀来指示它们当前是折叠还是展开。）
- **新** – 将打开一个菜单，其中每个命令依次打开一个对话框或页面，让您可以为选择添加特定类型的物料。 可用命令包括 **预测供应**、**计划订单**、**计划看板**、**新建生产订单**、**采购订单** 和 **转移单**。
- **主计划** – 运行主计划。 将出现一个对话框，您可以在其中指定要运行的计划。 默认情况下，**主计划** 字段设置为匹配当前筛选器。
- **完工入库的最大量** – 打开当前筛选器中定义的产品的 **完工入库的最大量** 页面。
- **更新计划订单** – 打开 **计划订单** 页面，该页面显示当前筛选器中定义的产品或产品系列的计划订单。
- **级别** – 根据出现的对话框中的设置展开计划订单。
- **按位置划分的材料计划策略** – 打开当前筛选器中定义的产品的 **物料覆盖范围** 页面。
- **看板规则** – 打开当前筛选器中定义的产品的 **看板规则** 页面。

### <a name="fasttabs"></a>快速选项卡

**供应计划** 页面可能包含以下快速选项卡：

- **期间结束库存** – 此快速选项卡以图形格式显示期间结束库存数据。
- **供应概况** – 此快速选项卡以图形格式显示供应数据。 当您在上半部分选择 **供应** 节点或其下方的一行时，它将可见。
- **摘要** – 此快速选项卡显示与您在上半部分选择的交易类型相关的摘要详细信息。 例如，如果您在 **需求** 节点下选择 **销售**，此快速选项卡将显示与销售订单相关的字段，如 **请求的销售订单行** 或 **总金额**。 如果您在 **供应** 节点的 **生产** 子节点下选择 **生产订单**，此快速选项卡将显示与生产订单相关的字段，如 **已计划生产订单** 或 **已计划总计**。 字段值取决于您在上半部分选择的期间。 
- **\[交易类型\] - \[期间\]** – 此快速选项卡显示您在上半部分选择的交易类型和期间的订单。 此快速选项卡的名称会反映这些选择。 例如，它可能被命名为 **销售订单 - 订货** 或 **生产订单 - 第 37 周**。

### <a name="action-pane"></a>操作窗格

操作窗格上提供以下按钮：

- **修改筛选器** – 打开 **修改筛选器** 对话框，您可以在其中更新筛选器值，然后重新打开 **供应计划** 页面，该页面反映更新的筛选器设置。
- **显示延迟** – 如果该交易类型存在延迟订单，将突出显示上半部分的相关行。

### <a name="factbox-pane"></a>速见表窗格

要打开速见表窗格，查看速见表，选择页面右边缘的 **相关信息**。 **供应计划** 页上有以下速见表：

- **物料详细信息** – 此速见表显示有关当前筛选器中定义的产品的基本信息。 如果您在筛选器中定义了产品系列，此项为空。
- **操作** – 此速见表显示您在上半部分选择的交易类型的订单的操作。
- **延迟** – 此速见表显示您在上半部分选择的交易类型的订单的延迟。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]