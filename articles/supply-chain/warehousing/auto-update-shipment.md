---
title: 装运自动更新
description: 本主题概述了为装运提供自动更新的功能。
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e42e7f19311adee7cc48f0ad0b59a4d0d54df9aa
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773535"
---
# <a name="shipment-auto-updates"></a>装运自动更新

[!include [banner](../includes/banner.md)]

在将负荷发放到仓库后，自动更新装运功能会自动更新与装运关联的负荷行上的数量（增加和减少）。 此功能将保持打开状态，直到装运或负荷上的负荷行在波次中处理。 使用此功能时，订单更新可以自动流过仓库，而无需手动干预，直到仓库工作已创建。

当不使用自动更新装运功能时，只有数量减少会自动流过，直到仓库工作创建。 用户必须手动更新或删除行，然后如果订单数量增加或添加了新订单行，则他们必须重新发放行。 通过使用自动更新装运功能，企业可以无缝地向仓库提供更新，而不必担心相关的装运和负荷不会反映出订单行更新。

自动更新装运功能适用于销售订单行和转移单行，其已为特定仓库打开。 因此，公司可以根据需要在仓库之间应用不同的自动更新装运策略。 默认情况下，数量减少的自动更新装运策略适用于所有使用仓库管理流程的仓库。 使用此默认策略设置时，只有数量减少会自动流过装运和负荷，直到仓库工作创建为止。 此行为类似于在引入自动更新装运功能之前使用的行为。

## <a name="main-elements-of-the-functionality"></a>功能的主要元素

自动更新装运功能主要依靠装运状态来确定在销售订单行或转移单行上进行更改时是否应更改负荷行上的数量。 它还主要依靠装运状态来确定何时应将新负荷行自动添加到现有负荷中。 当装运状态为**已分波次**或更高时，不会发生自动更新。

自动更新也会考虑波次状态。 当与负荷行相关的波次的状态为**已持有**、**正在执行**、**已发放**、**已领料**、或**已装运**时，如果用户尝试减少负荷行上的数量（通过销售订单行或转移单行上的数量减少），则会显示以下错误消息：“已创建了依赖预留的工作，因此无法删除这些预留。” 此外，当波次具有上述波次状态之一时，如果用户尝试通过减少销售订单行或转移单行上的数量来间接增加负荷行数量，负荷行上的数量不会自动增加 。 在这种情况下，必须手动更新负荷行。

## <a name="scenarios"></a>方案

自动更新装运功能支持四个场景：添加新订单行、增加订单行上的数量、减少订单行上的数量以及删除订单行。

- **添加新订单行** – 当**仓库**页的**仓库**快速选项卡上的**自动更新装运**字段（**仓库管理 \> 设置 \> 仓库 \> 仓库**）设置为**始终**时，如果订单存在装运，并且在为销售订单创建了负荷之后新订单行已添加到销售订单或转移单中，现有负荷不会更新。 将创建一个不引用现有负荷的新负荷行，并将其与现有装运关联。 新行将添加到负荷中并发放。
- **增加订单行上的数量** – 当**自动更新装运**字段设置为**始终**时，如果订单存在装运，并且在为销售订单创建负荷后，现有销售订单行或转移单行上的数量已增加，负荷行将增加与订单行相同的数量。 如果负荷已发放，但未创建任何工作，则负荷行将增加与订单行相同的数量。
- **减少订单行上的数量** – 当**自动更新装运**字段设置为**始终**或**在数量减少时**，如果订单存在装运，并且现有销售订单行或转移单行上的数量在为销售订单创建了负荷之后减少，关联的负荷行上的数量将更新以匹配，除非该负荷行上的数量已经等于或小于订单行上的新数量。 在这种情况下，负荷行不受影响。 如果负荷已发放，但未创建任何工作，关联的负荷行上的数量将更新以匹配，除非该负荷行上的数量已经等于或小于订单行上的新数量。 在这种情况下，负荷行不受影响。
- **删除订单行** – 当**自动更新装运**字段设置为**始终**或**在数量减少时**，如果用户尝试删除负荷行存在的订单行，则会显示一条错误消息。

## <a name="example-scenario"></a>示例场景

对于此情况，必须安装演示数据，并且必须使用 **USMF** 演示数据公司。

### <a name="turn-on-the-auto-update-shipment-functionality"></a>打开自动更新装运功能

要打开自动更新装运功能，请按照以下步骤操作。

1. 转到**仓库管理 \> 设置 \> 仓库 \> 仓库**。
2. 选择仓库 **24**。
3. 在**仓库**快速选项卡上的**自动更新装运**字段中，将值从**在数量减少时**更改为**始终**。

将值更改为**始终**后，销售订单行和转移单行上数量的任何增加或减少，以及新行的任何增加，都会反映在选定仓库的装运和负荷上（假定是前面所述的更新约束）。

### <a name="change-the-wave-template-so-that-load-lines-arent-automatically-processed"></a>更改波次模板，以使负荷行不会自动处理

要配置波次模板，使其不自动处理负荷行，请按照以下步骤操作。

1. 转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。
2. 选择波次模板 **24 装运默认**。
3. 选择**编辑**。
4. 在**常规**快速选项卡上，将**自动波次创建**选项设置为**是**，并确保将所有其他选项设置为**否**。

在波次创建过程中，不自动创建和发放任何工作，这一点很重要。 在创建与为销售订单行创建的负荷行相关的工作之后，如果更改了销售订单行上的数量，则负荷行将不再自动更新。

### <a name="create-a-sales-order"></a>创建销售订单

要创建销售订单，请按照下面的步骤操作。

1. 转到**销售和营销 \> 销售订单 \> 所有销售订单**。
2. 选择客户 **US-003**。
3. 为物料编号 **A0001** 创建一行。
4. 输入数量 **10**。 （确保您使用的是仓库 **24**。）
5. 选择**保存**。
6. 在“操作窗格”上的**仓库**选项卡上，在**操作**组中，选择**发放到仓库**。 装运和波次已创建。

由于您在上一过程中更改了波次模板，因此不会创建任何负荷或工作。 装运状态为**打开**，波次状态为**已创建**。

### <a name="decrease-the-quantity-on-a-sales-order-line"></a>减少销售订单行上的数量

要减少销售订单行上的数量，请按照下列步骤操作。

1. 转到**销售和营销 \> 销售订单 \> 所有销售订单**。
2. 选择您刚刚发放到仓库的销售订单。
3. 选择销售订单行。 在**数量**字段中，将值从 **10** 更改为 **8**。
4. 在销售订单行中，选择**仓库 \> 装运详细信息**。 在**装运详细信息**页面上的**负荷行**快速选项卡上，数量反映了销售订单行上的更改。

### <a name="increase-the-quantity-on-a-sales-order-line"></a>增加销售订单行上的数量

要增加销售订单行上的数量，请按照下列步骤操作。

1. 转到**销售和营销 \> 销售订单 \> 所有销售订单**。
2. 选择您之前发放到仓库的销售订单。
3. 将行数量从**8** 改为 **12**。
4. 选择**保存**。
5. 返回**所有销售订单**页，两次选择该销售订单。
5. 在“操作窗格”的**仓库**选项卡上的**相关信息**组中，选择**装运详细信息**。 在**装运详细信息**页面上的**负荷行**快速选项卡上，数量反映了销售订单行上的更改。

尽管负荷行上的数量从 8 增加到了 12，但除非打开了自动预留功能，否则只有八个物料会预留。 由于尚未预留添加到现有装运的数量，因此，如果此时在未预留的情况下处理波次，则仅为已预留的数量创建工作。

> [!NOTE]
> 当订单行上的数量减少时，如果负荷行上的数量已经等于或小于订单行上的新数量，则此数量不会受到影响。 当增加订单行上的数量时，负荷行将增加与订单行相同的数量。 如果订单行上的数量与负荷行上的数量不同，差额将保持不变。

### <a name="add-a-sales-order-line"></a>添加销售订单行

若要添加销售订单行，请执行以下步骤。

1. 转到**销售和营销 \> 销售订单 \> 所有销售订单**。
2. 选择您之前发放到仓库的销售订单。
3. 为物料编号 **A0002** 创建一行。
4. 在**数量**字段中，输入 **10**。 （请确保您使用的是仓库 **24**。）新行将自动添加到现有装运中。
5. 选择**保存**。
6. 返回**所有销售订单**页，两次选择该销售订单。
7. 在“操作窗格”的**仓库**选项卡上的**相关信息**组中，选择**装运详细信息**。 在**装运详细信息**页面上的**负荷行**快速选项卡上，注意第二个负荷行。

由于尚未预留刚刚添加到现有装运的销售订单行，因此，如果此时处理了波次，则仅为第一个销售订单行和第一个负荷行上的数量创建工作。

### <a name="process-a-wave"></a>处理波次

若要处理波次，请遵循以下步骤。

1. 转到**仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。
2. 选择您之前创建的波次。
3. 在“操作窗格”的**波次**选项卡的**波次**组中，选择**处理**。

波次将被处理，并为负荷行上的预留数量创建工作。 装运状态将从**打开**更新为**已分波次**。 当装运状态更新为**已分波次**时，发生的任何更改（例如行数量减少或增加，或向销售订单添加新行）都不会影响与已分波次装运关联的现有负荷行。

如果装运的状态为**已分波次**或更高，则不会在与该装运关联的负荷行上反映或根据其验证销售订单行上的数量更新。 必须直接在负荷行上更改负荷行上的数量。

验证将在为负荷行创建工作并进行预留之后进行。 然后，根据工作行预留验证销售订单行上数量的减少。