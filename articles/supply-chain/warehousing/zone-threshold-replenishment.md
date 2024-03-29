---
title: 区域阈值补货
description: 基于区域的补货使用最小/最大补货策略，但是会评估所有仓库区域，而不仅是评估单个货位。 因此，仓库经理可以更快地确定领料区中是否需要更多库存。
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable, WHSRequestType
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 44e7dfdbc980c5df6b9426515365611bc0de45c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335936"
---
# <a name="zone-threshold-replenishment"></a>区域阈值补货

[!include [banner](../includes/banner.md)]

基于区域的补货使用最小/最大[补货](replenishment.md)策略，但是会评估所有仓库区域，而不仅是评估单个货位。 因此，仓库经理可以更快地确定领料区中是否需要更多库存。

此功能的设置类似基于货位的补货的设置。 但是，为最小/最大补货设置模板时，也可以指定应该按货位还是按区域评估阈值。 如果设置基于区域的评估，则必须向区域选择查询添加特定区域。

与基于货位的最小/最大补货一样，基于区域的最小/最大补货基于最小库存阈值的设置，该阈值触发所选物料的补货工作创建。 此补货工作将把库存最大提高到为区域指定的最大阈值。

> [!NOTE]
> 当前版本不支持产品变型的区域补货过程。


与基于货位的最小/最大补货不同，基于区域的最小/最大补货不需要固定货位即可评估货位是否应该存储特定物料。 因此，即使仓库中的每个物料或物料变型没有固定货位，基于区域的补货也允许您使用最小/最大补货。 当区域中的数量降至指定的最小阈值以下时，将创建补货工作。 货位指令决定应将库存放入哪个特定货位中。

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a>开启“区域阈值补货”功能

*区域阈值补货* 功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*仓库管理*
- **功能名称**：*区域阈值补货*

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a>设置基于区域的补货

若要设置基于区域的补货，必须配置系统的多个部分。 本节介绍各种设置，并提供在您要完成本文结尾的场景时可输入的示例数据值。

### <a name="set-up-directive-codes"></a>设置指令代码

定义工作模板中使用的货位模板时，[指令代码](control-warehouse-location-directives.md)可以提高具体程度。 每个代码建立一个公共值，可在配置各种模板时引用。

#### <a name="view-and-edit-directive-codes"></a>查看和编辑指令代码

若要查看或编辑指令代码，请转到 **仓库管理 \> 设置 \> 指令代码**。

#### <a name="prepare-demo-data-directive-codes"></a>准备演示数据指令代码

本示例说明如何准备指令代码。 如果计划完成本文结尾的场景，请使用此处提供的演示数据值。 否则，请使用您自己的值。

1. 选择法人 **USMF** 使用这些演示数据。
1. 转到 **库存管理 \> 设置 \> 指令代码**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **指令代码：**_区域补货_
    - **指令说明：**_区域补货_

1. 选择 **保存** 以保存新代码。

### <a name="set-up-replenishment-templates"></a>设置补货模板

[最小/最大补货模板](tasks/set-up-min-max-replenishment-process.md)是用于维护领料货位最佳级别的主要机制。 在这些模板中，必须设置将用于在仓库中为库存补货的规则。 模板可用于的补货中包含基于区域的补货。

#### <a name="view-and-edit-replenishment-templates"></a>查看和编辑补货模板

补货模板是控制何时和如何为货位补货的一系列规则。 选择模板以控制何时和如何进行补货。 若要查看或编辑补货模板，请转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。

#### <a name="prepare-a-demo-data-replenishment-template"></a>准备演示数据补货模板

本示例说明如何准备补货模板。 如果计划完成本文结尾的场景，请使用此处提供的演示数据值。 否则，请使用您自己的值。

1. 选择法人 **USMF** 使用这些演示数据。
1. 转到 **仓库管理 \> 设置 \> 补货 \> 补货模板**。
1. 选择 **编辑** 将页面设置为编辑模式。
1. 在操作窗格上，选择 **新建** 向 **概览** 网格添加一行。
1. 在新行中，设置以下值。 接受其他所有字段的默认值。

    - **补货模板：**_区域最小/最大补货_
    - **说明：**_区域最小/最大补货_
    - **补货类型：**_最小或最大_

1. 选择 **保存**。
1. **概览** 网格中的新行仍处于选中状态时，选择 **补货模板详细信息** 网格上方的 **新建** 添加与您刚才创建的 *区域最小/最大补货* 补货模板关联的行。
1. 在新行中，设置以下值：

    - **序列号：** 输入 _1_。
    - **说明：** 输入 _领料区补货_。
    - **补货单位：** 选择 _每个_。
    - **请求类型：** 将此字段保留为空。
    - **指令代码：** 此字段将补货模板与货位指令关联。 选择前面创建的演示数据指令代码（_区域补货_）。
    - **工作模板**：将此字段保留为空。
    - **最小数量：** 此字段设置触发补货的数量。 输入 _50_。
    - **最大数量：** 此字段设置某个物料在区域中可存在的最大数量。 生成的补货工作将把库存提高到此数量。 输入 _150_。
    - **单位：** 此字段设置最小值和最大值的单位。 选择 _每个_。
    - **需求增加：** 选择 _进位_。
    - **对空固定货位补货：** 选中此复选框。
    - **仅对固定货位补货：** 清除此复选框。
    - **产品查询模式：** 选择 _产品查询_。
    - **补货阈值范围：** 此字段定义模板应该按区域还是按特定货位评估。 选择 _区域_。
    - **仓库：** 选择 _61_。

1. 选择 **补货模板详细信息** 网格上方的 **选择产品**。
1. 在 **产品查询** 对话框的 **范围** 选项卡中，选择 **添加** 向网格添加一行。
1. 在新行中，设置以下值：

    - **表：**_物料_
    - **派生表：**_物料_
    - **字段：**_物料编号_
    - **条件：** _A0001_

1. 选择 **确定** 保存查询并关闭对话框。
1. 选择 **补货模板详细信息** 网格上方的 **选择要补货的区域**。
1. 在 **区域查询** 对话框的 **范围** 选项卡中，向网格添加一行。
1. 在新行中，设置以下值：

    - **表：**_仓库区域_
    - **派生表：**_仓库区域_
    - **字段：** _区域 ID_
    - **条件：**_FLOOR_

1. 选择 **确定** 保存查询并关闭对话框。

### <a name="set-up-location-directives"></a>设置货位指令

与基于货位的最小/最大补货不同，基于区域的最小/最大补货需要您同时设置领料货位指令和放置货位指令，因为系统会评估整个区域，而不仅仅是评估出库工作的领料货位。

#### <a name="view-and-edit-location-directives"></a>查看和编辑货位指令

若要查看或编辑货位指令，请转到 **仓库管理 \> 设置 \> 货位指令**。

有关显示如何使用设置创建所需领料货位指令和放置货位指令的示例，请参阅下一部分。

#### <a name="prepare-demo-data-location-directives"></a>准备演示数据货位指令

若要准备演示数据以便在本文结尾的场景中使用，必须创建两个货位指令：一个用于领料，一个用于放置。

##### <a name="create-a-replenishment-pick-directive"></a>创建补货领料指令

1. 选择法人 **USMF** 使用这些演示数据。
1. 转到 **库存管理 \> 设置 \> 位置指令**。
1. 在左窗格中，将 **工作订单类型** 设置为 _补货_。
1. 在“操作窗格”中，选择 **新建** 创建新指令。
1. 设置以下值：

    - **序列号：** 接受默认值。
    - **名称：** 输入 _区域领料_。
    - **工作类型：** 选择 _领料_。
    - **站点：** 选择 _6_。
    - **仓库：** 选择 _61_。
    - **指令代码：** 将此字段保留为空。
    - **多个 SKU：** 将此选项设置为 _否_。

1. 选择 **保存** 创建具有您迄今为止配置的设置的指令。
1. 在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **序列号：** 输入 _1_。
    - **起始数量：** 输入 _0_。
    - **截止数量：** 输入 _10000000_。
    - **单位**：保持此字段为空。
    - **查找数量：** 选择 _无_。
    - **按单位施加的限制：** 清除此复选框。
    - **进位到单位：** 清除此复选框。
    - **查找包装数量：** 清除此复选框。
    - **允许拆分：** 选中此复选框。

1. 选择 **保存** 以保存新行。
1. **行** 网格中的新行仍处于选中状态时，选择 **货位指令操作** 快速选项卡上的 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **序列号：** 输入 _1_。
    - **名称：** 输入 _批量领料_。
    - **固定货位使用情况：** 选择 _固定货位和非固定货位_。
    - **允许负库存：** 清除此复选框。
    - **批处理已启用：** 清除此复选框。
    - **策略：** 选择 _无_。

1. 选择 **保存** 以保存新操作。
1. 新操作仍处于选中状态时，选择 **货位指令操作** 网格上方的 **编辑查询**。
1. 将显示查询对话框，可在其中选择补货来源货位。 在 **范围** 选项卡中，选择 **添加** 向网格添加一行。
1. 在新行中，设置以下值：

    - **表：** _位置_
    - **派生表：**_货位_
    - **字段：** _区域 ID_
    - **条件：** _BULK_

1. 选择 **确定** 保存查询并关闭对话框。
1. 选择 **保存** 保存货位指令。

##### <a name="create-a-replenishment-put-directive"></a>创建补货放置指令

1. 在 **货位指令** 页的左窗格中，确保 **工作订单类型** 字段仍然设置为 _补货_。
1. 在“操作窗格”中，选择 **新建** 再创建一个新指令。
1. 设置以下值：

    - **序列号：** 接受默认值。
    - **名称：** 输入 _区域放置_。
    - **工作订单类型：** 选择 _放置_。
    - **站点：** 选择 _6_。
    - **仓库：** 选择 _61_。
    - **指令代码：** 选择 _区域补货_ 将此货位指令与前面使用之前创建的代码创建的补货模板链接。
    - **多个 SKU：** 将此选项设置为 _否_。

1. 选择 **保存** 创建具有您迄今为止配置的设置的指令。
1. 在 **行** 快速选项卡上，选择 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **序列号：** 输入 _1_。
    - **起始数量：** 输入 _0_。
    - **截止数量：** 输入 _10000000_。
    - **单位**：保持此字段为空。
    - **查找数量：** 选择 _无_。
    - **按单位施加的限制：** 清除此复选框。
    - **进位到单位：** 清除此复选框。
    - **查找包装数量：** 清除此复选框。
    - **允许拆分：** 选中此复选框。

1. 选择 **保存** 以保存新行。
1. **行** 网格中的新行仍处于选中状态时，选择 **货位指令操作** 快速选项卡上的 **新建** 向网格添加一行。
1. 在新行中，设置以下值：

    - **序列号：** 输入 _1_。
    - **名称：** 输入 _区域放置_。
    - **固定货位使用情况：** 选择 _固定货位和非固定货位_。
    - **允许负库存：** 清除此复选框。
    - **批处理已启用：** 清除此复选框。
    - **策略：** 选择 _合并_。

1. 选择 **保存** 以保存新操作。
1. 新操作仍处于选中状态时，选择 **货位指令操作** 网格上方的 **编辑查询**。
1. 将显示查询对话框，可在其中选择补货目标区域。 此区域应该是补货模板中指定的同一个区域。 在 **范围** 选项卡中，选择 **添加** 向网格添加一行。
1. 在新行中，设置以下值：

    - **表：** _位置_
    - **派生表：**_货位_
    - **字段：** _区域 ID_
    - **条件：**_FLOOR_

1. 选择 **确定** 保存查询并关闭对话框。
1. 选择 **保存** 保存货位指令。

## <a name="scenario"></a>应用场景

此部分提供一个示例场景，该场景演示如何使用此功能。

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a>准备示例场景所需的示例数据

开始完成此场景之前，必须按照本节中和本文前面几节中的说明激活示例数据和设置功能。

#### <a name="use-the-usmf-legal-entity"></a>使用 USMF 法人

若要使用此处指定的示例记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)。 此外，开始前，还必须选择 **USMF** 法人。

#### <a name="prepare-additional-sample-data"></a>准备其他示例数据

选择法人 **USMF** 之后，请按照本文前面[设置基于区域的补货](#setup)一节中的说明添加需要的更多示例数据。

#### <a name="check-your-on-hand-inventory"></a>检查现有库存

执行以下步骤确保系统中有足够库存来支持示例场景。

1. 确保补货模板中指定的领料区 (*FLOOR*) 的两个不同货位内有物料 *A0001* 的现成库存。 但是，库存总量应小于补货模板中指定的最小必需数量 (*50*)。 这样，就可以模拟如何为整个区域进行计算，而不是模拟仅为单个货位进行计算。 **根据需要使用任何仓库流程调整库存。**
1. 确保区域领料货位指令中指定的堆放货位（此处补货工作应该从区域 ID *BULK* 领取物料）处有物料 *A0001* 的充足库存。 库存总量必须大于补货模板中指定的最大必需数量 (*150*)。
1. 可选，但是建议：执行以下步骤创建库存调整日记帐：

    1. 转到 **库存管理 \> 日记帐条目 \> 物料 \> 库存调整**。
    1. 选择 **新建**。
    1. 在 **创建库存日记帐** 对话框的 **仓库** 字段中，选择 *61*。
    1. 选择 **确定**。
    1. 在 **日记帐行** 快速选项卡中，使用 **新建** 按钮向网格添加三行，然后设置以下值。 每行设置完毕之后，选择 **保存**。

        - **行 1：**

            - **物料编号：***A0001*
            - **站点**：*6*
            - **仓库**：*61*
            - **货位**：*02A01R1S1B*
            - **牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。
            - **数量：** *1000*

        - **行 2：**

            - **物料编号：***A0001*
            - **站点**：*6*
            - **仓库**：*61*
            - **货位**：*07A01R2S1B*
            - **牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。
            - **数量：** *15*

        - **行 3：**

            - **物料编号：***A0001*
            - **站点**：*6*
            - **仓库**：*61*
            - **货位**：*07A01R1S1B*
            - **牌照：** 在列表中选择一个现有牌照，或创建一个新的牌照。
            - **数量：** *10*

    1. 在操作窗格上，选择 **验证**。 前往下一步之前，解决发现的所有错误。
    1. 在操作窗格上，选择 **过帐** 将库存过帐到仓库。

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a>示例场景：运行基于区域的最小/最大补货

准备好所有先决示例数据之后，可以执行以下步骤触发补货。

1. 转到 **仓库管理 \> 补货 \> 补货**。
1. 在 **补货** 对话框的 **要包括的记录** 快速选项卡上，选择 **筛选器**。
1. 在 **查询** 对话框的 **范围** 选项卡中，按照以下方式编辑默认表行：

    - **表：** 选择 _补货模板_。
    - **派生表：** 选择 _补货模板_。
    - **字段：** 选择 _补货模板_。
    - **条件：** 选择 _区域最小/最大补货_。 此补货模板是您在为此场景准备演示数据时创建的补货模板。

1. 选择 **确定** 保存查询并回到 **补货** 对话框。
1. 选择 **确定** 运行补货模板。

现在已创建了补货工作，以便从 *BULK* 区域领取库存，然后将其补给 *FLOOR* 区域。

## <a name="notes-and-tips"></a>说明和提示

下面是有关使用此功能的一些说明和提示：

- 若要设置针对所需区域的补货工作，可以按照下面的一种方法链接补货模板行和货位指令：

    - 编辑货位指令标题查询，然后筛选所选补货模板行。
    - 使用补货模板行中的指令代码，然后将其与放置货位指令比对。

- 如果使用动态货位，并且将货位指令操作设置为使用 **合并** 策略，将为第一个可用货位或为已经包含库存的货位创建补货工作。
- 如果使用固定货位而不是区域，则应使用[标准最小/最大补货](tasks/set-up-min-max-replenishment-process.md)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]