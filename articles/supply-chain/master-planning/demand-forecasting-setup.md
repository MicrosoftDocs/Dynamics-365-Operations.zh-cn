---
title: 需求预测设置
description: 本文介绍为准备需求预测您必须执行的设置任务。
author: t-benebo
ms.date: 11/23/2021
ms.topic: article
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fae2ac53dec8696075e7506d979c1cf9fb277af5
ms.sourcegitcommit: d98ecbd9457197ec8f8e281f9c2f24dcce7b8269
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2022
ms.locfileid: "8960126"
---
# <a name="demand-forecasting-setup"></a>需求预测设置

[!include [banner](../includes/banner.md)]

本文介绍如何设置需求预测。  

## <a name="item-allocation-keys"></a>物料分配参数

物料分配参数建立物料组。 只有当物料是物料分配参数的一部分时，为物料及其维度计算需求预测。 此规则强制对大量的物料进行分组，以便可以更快速创建需求预测。 预测只基于历史数据创建。

如果物料分配参数在创建预测时使用，物料及其维度必须仅是这一个物料分配参数的一部分。

要创建物料分配参数并向其添加库存单位 (SKU)，请执行以下步骤。

1. 转到 **主计划 \> 设置 \> 需求预测 \> 物料分配参数**。
1. 在列表窗格中选择一个物料分配参数，或在操作窗格上选择 **新建** 来创建新参数。 在新参数或选定参数的标题上，设置以下字段：

    - **物料分配参数** – 为参数输入唯一名称。
    - **名称** – 为参数输入描述性名称。

1. 按照以下步骤之一将物料添加到选定的物料分配参数或删除物料：

    - 在 **物料分配** 快速选项卡上，使用工具栏上的 **新增** 和 **删除** 按钮根据需要添加或删除物料。 对于每一行，选择物料编号，然后根据需要在其他列中分配维度值。 选择工具栏上的 **显示维度** 更改网格中显示的维度列集。 （生成需求预测时，会忽略 **百分比** 列中的值。）
    - 如果要向参数添加大量物料，在操作窗格中选择 **分配物料** 打开一个页面，您可以在其中找到多个物料并将其分配给选定的参数。

> [!IMPORTANT]
> 请注意，仅在每个物料分配参数中包含相关物料。 在您使用 Microsoft Azure 机器学习时，不必要的物料可能导致增加成本。

## <a name="intercompany-planning-groups"></a>内部公司计划组

需求预测可以生成跨公司预测。 在 Dynamics 365 Supply Chain Management 中，一起计划的公司会被分组到同一个内部公司计划组。 要为每个公司指定哪些物料分配参数应考虑用于需求预测，将物料分配参数与内部公司计划组成员相关联。

> [!IMPORTANT]
> 计划优化当前不支持内部公司计划组。 要执行使用计划优化的内部公司计划，请设置主计划批处理作业，其中包括所有相关公司的主计划。

要设置内部公司计划组，请按照以下步骤操作。

1. 转到 **主计划 \> 设置 \> 内部公司计划组**。
1. 在列表窗格中选择一个计划组，或在操作窗格上选择 **新建** 来创建新计划组。 在新组或选定组的标题上，设置以下字段：

    - **名称** – 为计划组输入唯一名称。
    - **描述** – 为计划组输入简短描述。

1. 在 **内部公司计划组成员** 快速选项卡上，使用工具栏上的按钮为应该属于该组的每个公司（法人）添加一行。 对于每一行，设置以下字段：

    - **法人** – 选择作为所选组成员的公司（法人）的名称。
    - **计划顺序** – 分配公司相对于其他公司的处理顺序。 先处理较低的值。 当一家公司的需求影响其他公司时，此顺序可能很重要。 在这种情况下，应最后处理提供需求的公司。
    - **主计划** – 选择要为当前公司触发的主计划。
    - **自动复制到静态计划** – 选中此复选框可将计划的结果复制到静态计划。
    - **自动复制到动态计划** – 选中此复选框可将计划的结果复制到动态计划。

1. 默认情况下，如果未将任何物料分配参数分配给内部公司计划组成员，则针对分配给所有公司所拥有所有物料分配参数的所有物料计算需求预测。 **生成统计基准预测** 对话框（**主计划 \> 预测 \> 需求预测 \> 生成统计基准预测**）中提供公司和物料分配参数的其他筛选选项。 要将物料分配参数分配给所选内部公司计划组中的公司，选择该公司，然后在 **内部公司计划组成员** 快速选项卡上，选择工具栏上的 **物料分配参数**。

> [!IMPORTANT]
> 请注意，在每个内部公司计划组中仅包含相关的物料分配参数。 在您使用 Azure 机器学习时，不必要的物料可能导致增加成本。

## <a name="set-up-demand-forecasting-parameters"></a><a name="parameters"></a>设置需求预测参数

使用 **需求预测参数** 页面设置多个选项，来控制需求预测在您的系统中的工作方式。

### <a name="open-the-demand-forecasting-parameters-page"></a>打开需求预测参数页面

要设置需求预测参数，转到 **主计划 \> 设置 \> 需求预测 \> 需求预测参数**。 由于需求预测跨公司运行，设置是全局的。 换言之，它将应用于所有法人（公司）。

### <a name="general-settings"></a>常规设置

使用 **需求预测参数** 页面的 **常规** 选项卡定义需求预测的常规设置。

#### <a name="demand-forecast-unit"></a>需求预测单位

需求预测生成数量形式的预测。 因此，必须在 **需求预测单位** 字段中指定应用于表示数量的度量单位。 此字段定义将用于所有需求预测的单位，不管每个产品的常用库存单位如何。 使用一致的预测单位，可以帮助确保聚合和百分比分布有意义。 有关合并和百分比分配的详细信息，请参阅[对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)。

对于用于需求预测中包含的 SKU 的每个度量单位，请确保有针对您在此处选择的度量单位和一般预测度量单位的转换规则。 当您生成预测时，不具有度量单位转换的物料列表将被记录。 因此，您可以轻松更正设置。 有关度量单位以及如何在它们之间进行转换的详细信息，请参阅[管理度量单位](../pim/tasks/manage-unit-measure.md)。

#### <a name="transaction-types"></a>交易记录类型

使用 **交易类型** 快速选项卡上的字段选择生成统计基准预测时使用的交易类型。

需求预测可用于预测相关和不相关的需求。 例如，如果只将 **销售订单** 选项设置为 *是*，并且如果为需求预测考虑的所有物料均为已售出的物料，则系统将计算不相关需求。 但是，重要子组件可以添加到物料分配参数并可以包括在需求预测中。 在这种情况下，如果 **生产订单行** 选项设置为 *是*，则计算相关的预测。

您可以使用 **物料分配参数** 选项卡替代一个或多个特定物料分配参数的交易类型。该选项卡提供相似字段。

#### <a name="choose-how-to-create-the-baseline-forecast"></a>选择如何创建基准预测

**预测生成策略** 字段可让您选择用于创建基准预测的方法。 有三种方法可用：

- *复制历史需求* – 通过复制历史数据创建预测。
- *Azure 机器学习服务* – 使用使用 Azure 机器学习服务的预测模型。 Azure 机器学习服务是 Azure 当前的机器学习解决方案。 因此，如果您想要使用预测模型，我们建议您使用它。
- *Azure 机器学习* – 使用使用 Azure 机器学习工作室（经典）的预测模型。 Azure 机器学习工作室（经典）已弃用，很快将从 Azure 中删除。 因此，如果您是第一次设置需求预测，我们建议您选择 *Azure 机器学习服务*。 如果您当前正在使用 Azure 机器学习工作室（经典），则应尽快计划切换到 Azure 机器学习服务。

您可以使用 **物料分配参数** 选项卡替代一个或多个特定物料分配参数的预测生成方法。该选项卡提供相似字段。

#### <a name="override-default-forecast-algorithm-parameters-globally"></a>全局替代默认预测算法参数

默认预测算法参数和值在 **需求预测参数** 页面上分配（**主计划 \> 设置 \> 需求预测 \> 需求预测参数**）。 不过，您可以使用 **需求预测参数** 页面 **常规** 选项卡上的 **预测算法参数** 快速选项卡全局替代它们。 （您还可以使用 **需求预测参数** 页面上的 **物料分配参数** 选项卡替代特定分配参数的值。）

使用工具栏上的 **添加** 和 **删除** 按钮建立所需的参数替代集合。 对于列表中的每个参数，在 **名称** 字段中选择一个值，然后在 **值** 字段中输入相应的值。 此处未列出的所有参数将从 **需求预测参数** 页面上的设置中获取值。 有关如何使用标准参数集以及如何为其选择值的详细信息，请参阅[需求预测模型的默认参数和值](#model-parameters)一节。

### <a name="set-forecast-dimensions"></a>设置预测维度

预测维度指示针对哪个详细级别定义预测。 公司、站点和物料分配参数是必需的预测维度。 您还可以在仓库、库存状态、客户组、客户帐户、国家/地区、州/省和/或物料级别以及所有物料维度级别生成预测。 使用 **需求预测参数** 页面上的 **预测维度** 选项卡选择生成需求预测时使用的一组预测维度。

您可以随时将预测维度添加到用于需求预测的维度列表。 您还可以从列表中删除预测维度。 但是，如果您添加或删除预测维度，手动调整将丢失。

### <a name="set-up-overrides-for-specific-item-allocation-keys"></a>设置特定物料分配参数的替代

从需求预测角度，并非所有物料都以相同的方式工作。 因此，您可以为 **常规** 选项卡上定义的大多数设置建立特定于分配参数的替代。需求预测单位是一个例外。 要设置特定物料分配参数的替代，请按照这些步骤操作。

1. 在 **需求预测参数** 页面上的 **物料分配参数** 选项卡上，根据您的需要使用工具栏按钮将物料分配参数添加到左侧网格中，或删除它们。 然后选择要为其设置替代的分配参数。
1. 在 **交易类型** 快速选项卡上，启用要用于为属于所选分配参数的产品生成统计基准预测的交易类型。 这些设置的工作方式与在 **常规** 选项卡上的工作方式相同，但它们仅应用于选定的物料分配参数。 此处的所有设置（*是* 值和 *否* 值）将替代 **常规** 选项卡上的所有 **交易类型** 设置。
1. 在 **预测算法参数** 快速选项卡上，为属于所选分配参数的产品选择预测生成策略和预测算法参数替代。 这些设置的工作方式与在 **常规** 选项卡上的工作方式相同，但它们仅应用于选定的物料分配参数。 使用工具栏上的 **添加** 和 **删除** 按钮定义所需的参数替代集合。 对于列表中的每个参数，在 **名称** 字段中选择一个值，然后在 **值** 字段中输入相应的值。 有关如何使用标准参数集以及如何为其选择值的详细信息，请参阅[需求预测模型的默认参数和值](#model-parameters)一节。

### <a name="set-up-the-connection-to-the-azure-machine-learning-service"></a>设置与 Azure 机器学习服务的连接

使用 **Azure 机器学习服务** 选项卡设置与 Azure 机器学习服务的连接。 此解决方案是创建基准预测的选项之一。 此选项卡上的这些设置仅在 **预测生成策略** 字段设置为 *Azure 机器学习服务* 时生效。

有关如何设置 Azure 机器学习服务，然后使用此处的设置与它连接的详细信息，请参阅[设置 Azure 机器学习服务](#setup-amls)一节。

### <a name="set-up-the-connection-to-azure-machine-learning-studio-classic"></a>设置与 Azure 机器学习工作室的连接（经典）

> [!IMPORTANT]
> Azure 机器学习工作室（经典）已弃用。 因此，您无法再在 Azure 中为它创建新工作区。 它已被 Azure 机器学习服务取代，后者提供相似的功能以及更多功能。 如果您还未使用 Azure 机器学习，应开始使用 Azure 机器学习服务。 如果您已经有一个为 Azure 机器学习工作室（经典）创建的工作区，您可以继续使用它，直到该功能从 Azure 中完全删除。 但是，我们建议您尽快更新到 Azure 机器学习服务。 虽然应用程序会继续警告您 Azure 机器学习工作室（经典）已被弃用，但不会影响预测结果。 有关新的 Azure 机器学习服务及其设置方法的详细信息，请参阅[设置 Azure 机器学习服务](#setup-amls)一节。
>
> 只要旧的 Azure 机器学习工作室（经典）工作区仍然可用，您就可以在为 Supply Chain Management 使用新旧机器学习解决方案之间自由切换。

如果您已有可用的 Azure 机器学习工作室（经典）工作区，可以通过将其连接到 Supply Chain Management 来使用它来生成预测。 您可以使用 **需求预测参数** 页面上的 **Azure 机器学习** 选项卡建立此连接。 （此选项卡上的设置仅在 **预测生成策略** 字段设置为 *Azure 机器学习* 时生效。）输入您的 Azure 机器学习工作室（经典）工作区的以下详细信息：

- Web 服务应用程序编程接口 (API) 密钥
- Web 服务终结点 URL
- Azure 存储帐户名称
- Azure 存储帐户密钥

> [!NOTE]
> 只有当您使用的是自定义存储帐户时才需要 Azure 存储帐户名称和密钥。 如果部署本地版本，必须在 Azure 中有自定义存储帐户，以便机器学习可以访问历史数据。

## <a name="default-parameters-and-values-for-demand-forecasting-models"></a><a name="model-parameters"></a>需求预测模型的默认参数和值

当您使用机器学习生成预测计划模型时，您可以通过设置 *预测算法参数* 的值来控制机器学习选项。 这些值将从 Supply Chain Management 发送到 Azure 机器学习。 使用 **预测算法参数** 页面控制应提供哪些类型的值以及每个类型应具有哪些值。

要设置用于需求预测模型的默认参数和值，请转到 **主计划 \> 设置 \> 需求预测 \> 预测算法参数**。 已提供一组标准参数。 每个参数具有以下字段：

- **名称** – Azure 使用的参数的名称。 通常，除非已在 Azure 机器学习中自定义实验，否则不应更改此名称。
- **描述** – 参数的通用名称。 此名称用于在系统中的其他位置标识参数（例如，在 **需求预测参数** 页面上）。
- **值** – 参数的默认值。 您应该输入的值取决于您正在编辑的参数。 
- **说明** – 参数以及如何使用它的简短描述。 此描述通常包括有关 **值** 字段的有效值的建议。

默认提供以下参数。 （如果您必须恢复到此标准列表，在操作窗格中选择 **恢复**。）

- **可信度百分比** – 置信区间包含一系列用作良好的需求预测估计的值。 可信度百分比 95% 表示未来需求有 5% 的几率超出置信区间范围。
- **强制使用季节性** – 指定是否强制模型使用特定的季节性类型。 此参数仅适用于 ARIMA 和 ETS。 选项：*AUTO（默认）*、*NONE*、*ADDITIVE*、*MULTIPLICATIVE*。
- **预测模型** – 指定要使用的预测模型。 选项：*ARIMA*、*ETS*、*STL*、*ETS+ARIMA*、*ETS+STL*、*ALL*。 要选择最合适的模型，使用 *ALL*。
- **最大预测值** – 指定用于预测的最大值。 格式：+1E[n] 或数值常量。
- **最小预测值** – 指定用于预测的最小值。 格式：-1E[n] 或数值常量。
- **缺少值替换** – 指定如何填充历史数据中的差距。 选项：*（数值）*、*MEAN*、*PREVIOUS*、*INTERPOLATE LINEAR*、*INTERPOLATE POLYNOMIAL*。
- **缺少值替换范围** – 指定值替换是仅应用于每个单独的粒度属性的日期范围，还是应用于整个数据集。 以下选项可用于建立系统在填写历史数据中的空白时使用的日期范围：

    - *GLOBAL* – 系统使用所有粒度属性的完整日期范围。
    - *HISTORY_DATE_RANGE* – 系统使用 **生成统计基准预测** 对话框中 **历史区间** 部分的 **开始日期** 和 **结束日期** 字段定义的具体日期范围。
    - *GRANULARITY_ATTRIBUTE* – 系统使用当前处理的粒度属性的日期范围。

    > [!NOTE]
    > 粒度属性是针对其执行预测的预测维度的组合。 可以在 **需求预测参数** 页中定义预测维度。

- **季节性提示** – 对于季节性数据，请为预测模型提供提示以提高预测的准确性。 格式：表示需求模式自行重复的时段数的整数。 例如，对于每六个月自行重复一次的数据，请输入 *6*。
- **测试集大小百分比** – 要用作测试集以进行预测准确性计算的历史数据的百分比。

您可以通过转到 **主计划 \> 设置 \> 需求预测 \>需求预测参数** 来替代这些参数的值。 在 **需求预测参数** 页面上，您可以通过以下方式替代这些参数：

- 使用 **常规** 选项卡全局替代参数。
- 使用 **物料分配参数** 选项卡替代特定物料分配参数的参数。 针对特定物料分配参数替代的参数只影响与该物料分配参数关联的物料的预测。

> [!NOTE]
> 在 **预测算法参数** 页面上，您可以使用操作窗格上的按钮将参数添加到列表中，或从列表中删除参数。 但是，除非已在 Azure 机器学习中自定义体验，否则通常不应使用此方法。

## <a name="set-up-the-azure-machine-learning-service"></a><a name="setup-amls"></a>设置 Azure 机器学习服务

Supply Chain Management 使用 Azure 机器学习服务计算需求预测，您必须在自己的 Azure 订阅中设置和运行该服务。 本节介绍如何在 Azure 中设置 Azure 机器学习服务，然后将其连接到您的 Supply Chain Management 环境。

### <a name="enable-the-azure-machine-learning-service-in-feature-management"></a>在功能管理中启用 Azure 机器学习服务

您必须先打开 Supply Chain Management 中的一项功能来启用集成，然后才能使用 Azure 需求预测机器学习服务。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*主计划*
- **功能名称**：*Azure 需求预测机器学习服务*

### <a name="set-up-machine-learning-in-azure"></a><a name="ml-workspace"></a>在 Azure 中设置机器学习

要使 Azure 能够使用机器学习来处理您的预测，您必须为此设置一个 Azure 机器学习工作区。 您有两个选项：

- 要通过运行 Microsoft 提供的脚本来设置工作区，请按照[选项 1：运行脚本来自动设置机器学习工作区](#ml-workspace-script)一节中的说明操作，然后直接跳到[在 Supply Chain Management 中设置 Azure 机器学习服务连接参数](#demand-forecast-parameters)一节。
- 要手动设置工作区，请按照[选项 2：手动设置机器学习工作区](#ml-workspace-manual)一节中的说明操作，然后直接跳到[在 Supply Chain Management 中设置 Azure 机器学习服务连接参数](#demand-forecast-parameters)一节。 此选项需要更多时间，但它可以为您提供更多控制权。

#### <a name="option-1-run-a-script-to-automatically-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-script"></a>选项 1：运行脚本来自动设置机器学习工作区

本节介绍如何使用 Microsoft 提供的自动化脚本设置机器学习工作区。 如果您愿意，可以按照[选项 2：手动设置机器学习工作区](#ml-workspace-manual)一节中的说明手动设置所有资源。 两个选项不必全部完成。

1. 在 GitHub 上，打开[使用 Azure 机器学习进行 Dynamics 365 Supply Chain Management 需求预测的模板](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)存储库，下载以下文件：

    - quick_setup.ps1
    - sampleInput.csv
    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. 打开一个 PowerShell 窗口，运行您在上一步中下载的 **quick_setup.ps1** 脚本。 按照屏幕上的说明操作。 此脚本将设置所需的工作区、存储、默认数据存储和计算资源。 但是，您仍必须按照此过程的其余步骤创建所需的管道。 （管道提供了从 Supply Chain Management 开始预测脚本的方法。）
1. 在 Azure 机器学习工作室中，将您在步骤 1 中下载的 **sampleInput.csv** 文件上载到名为 *demplan-azureml* 的容器。 （quick_setup.ps1 脚本创建此容器。）需要此文件来发布管道和生成测试预测。 有关说明，请参阅[上载块 blob](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob)。
1. 在 Azure 机器学习工作室中，在导航器中选择 **Notebooks**。
1. 在 **文件** 结构中找到以下位置：**Users/\[当前用户\]/src**。
1. 将您在步骤 1 中下载的其余四个文件上载到您在上一步中找到的位置。
1. 选择您刚刚上载的 **api_trigger.py** 文件，然后运行它。 它将创建一个可通过 API 触发的管道。
1. 您的工作区现已设置。 直接跳到[在 Supply Chain Management 中设置 Azure 机器学习服务连接参数](#demand-forecast-parameters)一节。

#### <a name="option-2-manually-set-up-your-machine-learning-workspace"></a><a name="ml-workspace-manual"></a>选项 2：手动设置机器学习工作区

本节介绍如何手动设置机器学习工作区。 仅当您决定不运行自动设置脚本时，才必须完成本节中的过程，如[选项 1：运行脚本来自动设置机器学习工作区](#ml-workspace-script)一节所述。

##### <a name="step-1-create-a-new-workspace"></a><a name="create-workspace"></a>步骤 1：创建新工作区

使用以下过程来创建新机器学习工作区。

1. 登录 Azure 门户。
1. 打开 **机器学习** 服务。
1. 在工具栏上选择 **创建** 打开 **创建** 向导。
1. 按照屏幕说明完成向导。 操作时请记住以下几点：

    - 除非此列表中的其他要点推荐不同的设置，否则请使用默认设置。
    - 务必选择与部署 Supply Chain Management 实例的区域相匹配的地理区域。 否则，您的某些数据可能会越过区域边界。 有关详细信息，请参阅本文后面的[隐私声明](#privacy)。
    - 使用专用资源，如资源组、存储帐户、容器注册表、Azure 密钥保管库和网络资源。
    - 在向导的 **设置 Azure 机器学习服务连接参数** 页面上，您必须提供存储帐户名称。 使用专门用于需求预测的帐户。 需求预测输入和输出数据将存储在此存储帐户中。

有关详细信息，请参阅[创建工作区](/azure/machine-learning/quickstart-create-resources#create-the-workspace)。

##### <a name="step-2-configure-storage"></a><a name="config-storage"></a>步骤 2：配置存储

使用以下过程设置存储。

1. 在 GitHub 上，打开 [使用 Azure 机器学习进行 Dynamics 365 Supply Chain Management 需求预测的模板](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)存储库，下载 **sampleInput.csv** 文件。
1. 打开您在[步骤 1：创建新工作区](#create-workspace)一节中创建的存储帐户。
1. 按照 [创建容器](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container)中的说明创建一个名为 *demplan-azureml* 的容器。
1. 将您在步骤 1 中下载的 **sampleInput.csv** 文件上载到您刚才创建的容器。 发布管道和生成测试预测需要此文件。 有关说明，请参阅[上载块 blob](/azure/storage/blobs/storage-quickstart-blobs-portal#upload-a-block-blob)。

##### <a name="step-3-configure-a-default-datastore"></a>步骤 3：配置默认数据存储

使用以下过程设置默认数据存储。

1. 在 Azure 机器学习工作室中，在导航器中选择 **数据存储**。
1. 创建一个 *Azure Blob 存储* 类型的新数据存储，该数据存储指向您在 [步骤 2：配置存储](#config-storage)一节中创建的 *demplan-azureml* Blob 存储容器。 （如果新数据存储的身份验证类型为 *帐户密钥*，为创建的存储帐户提供帐户密钥。 有关说明，请参阅[管理存储帐户访问密钥](/azure/storage/common/storage-account-keys-manage?tabs=azure-portal)。）
1. 通过打开新数据存储的详细信息并选择 **设置为默认数据存储**，将新数据存储设为默认数据存储。

##### <a name="step-4-configure-compute-resources"></a><a name="config-compute-resources"></a>步骤 4：配置计算资源

使用以下过程在 Azure 机器学习工作室中设置计算资源来运行预测生成脚本。

1. 打开您在[步骤 1：创建新工作区](#create-workspace)一节中创建的机器学习工作区的详细信息页面。 找到 **工作室 Web URL** 值，选择链接将其打开。
1. 在导航窗格中选择 **计算**。
1. 在 **计算实例** 选项卡上，选择 **新建** 打开一个向导，帮助您创建新的计算实例。 按照屏幕上的说明操作。 计算实例将用于创建需求预测管道（管道发布后可以删除。）使用默认设置。
1. 在 **计算群集** 选项卡上，选择 **新建** 打开一个向导，帮助您创建新的计算群集。 按照屏幕上的说明操作。 计算群集用于生成需求预测。 它的设置会影响性能和运行的最大并行化级别。 设置以下字段，其他所有字段使用默认设置：

    - **名称** – 输入 *e2ecpucluster*。
    - **虚拟机大小** – 根据您希望用作需求预测输入的数据量调整此设置。 节点数不应超过 11，因为需要一个节点来触发需求预测生成，之后可用于生成预测的最大节点数为 10。 （您还将在[步骤 5：创建管道](#create-pipelines)一节的 parameters.py 文件中设置节点数。）在每个节点上，将有多个并行运行预测脚本的工作进程。 您的作业中的工作进程总数将为 *节点具有的核心数* × *节点数*。 例如，如果您的计算群集类型为 *Standard\_D4*（八个核心），最多 11 个节点，`nodes_count` 值在 parameters.py 文件中设置为 *10*，有效并行度级别将为 80。

##### <a name="step-5-create-pipelines"></a><a name="create-pipelines"></a>步骤 5：创建管道

管道提供了从 Supply Chain Management 开始预测脚本的方法。 使用以下过程创建所需的管道。

1. 在 GitHub 上，打开[使用 Azure 机器学习进行 Dynamics 365 Supply Chain Management 需求预测的模板](https://github.com/microsoft/Dynamics-365-Supply-Chain-Management-Demand-Forecasting-With-Azure-Machine-Learning-Service)存储库，下载以下文件：

    - src/parameters.py
    - src/api_trigger.py
    - src/run.py
    - src/REntryScript/forecast.r

1. 在 Azure 机器学习工作室中，在导航器中选择 **Notebooks**。
1. 在 **文件** 结构中找到以下位置：**Users/\[当前用户\]/src**。
1. 将您在步骤 1 中下载的四个文件上载到您在上一步中找到的位置。
1. 在 Azure 中，打开并查看您刚才上载的 **parameters.py** 文件。 确保 `nodes_count` 值比您在[步骤 4：配置计算资源](#config-compute-resources)一节中为计算群集配置的值小。 如果 `nodes_count` 值大于或等于计算群集中的节点数，管道运行可能能够启动。 但是，它会在等待所需资源时停止响应。 有关节点计数的详细信息，请参阅[步骤 4：配置计算资源](#config-compute-resources)一节。
1. 选择您刚刚上载的 **api_trigger.py** 文件，然后运行它。 它将创建一个可通过 API 触发的管道。

### <a name="set-up-a-new-active-directory-application"></a><a name="aad-app"></a>设置新 Active Directory 应用程序

需要有 Active Directory 应用程序才能使用服务主体对专门用于需求预测的资源进行身份验证。 因此，应用程序应具有生成预测所需的最低特权级别。

1. 登录 Azure 门户。
1. 在租户的 Azure Active Directory (Azure AD) 中注册一个新应用程序。 有关说明，请参阅[使用门户创建可访问资源的 Azure AD 应用程序和服务主体](/azure/active-directory/develop/howto-create-service-principal-portal)。
1. 完成向导时按照屏幕上的说明操作。 使用默认设置。
1. 为您的新 Active Directory 应用程序授予您在[在 Azure 中设置机器学习](#ml-workspace)一节中创建的以下资源的访问权限。 有关说明，请参阅[使用 Azure 门户分配 Azure 角色](/azure/role-based-access-control/role-assignments-portal?tabs=current)。 此步骤将使系统能够导入和导出预测数据，并触发从 Supply Chain Management 运行机器学习管道。

    - 机器学习工作区的参与者角色
    - 专用存储帐户的参与者角色
    - 专用存储帐户的存储 Blob 数据参与者角色

1. 在您创建的应用程序的 **证书和密码** 部分，为应用程序创建一个密码。 有关说明，请参阅[添加客户端密码](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret)。
1. 记下应用程序 ID 及其密码。 稍后在 Supply Chain Management 中设置 **需求预测参数** 页面时，您将需要此应用程序的详细信息。

### <a name="set-up-azure-machine-learning-service-connection-parameters-in-supply-chain-management"></a><a name="demand-forecast-parameters"></a>在 Supply Chain Management 中设置 Azure 机器学习服务连接参数

使用以下过程将您的 Supply Chain Management 环境连接到您刚刚在 Azure 中设置的机器学习服务。

1. 登录 Supply Chain Management。
1. 转到 **主计划 \> 设置 \> 需求预测 \> 需求预测参数**。
1. 在 **常规** 选项卡上，确保 **预测生成策略** 字段设置为 *Azure 机器学习服务*。
1. 在 **物料分配参数** 选项卡上，确保将每个应使用 Azure 需求预测机器学习服务的分配参数的 **预测生成策略** 字段设置为 *Azure 机器学习服务*。
1. 在 **Azure 机器学习服务** 选项卡上，设置以下字段：

    - **租户 ID** – 输入您的 Azure 租户的 ID。 Supply Chain Management 将使用此 ID 对 Azure 机器学习服务进行身份验证。 您可以在 Azure 门户中 Azure AD 的 **概览** 页面上找到您的租户 ID。
    - **服务主体应用程序 ID** – 输入您在 [Active Directory 应用程序](#aad-app)部分创建的应用程序的应用程序 ID。 此值用于对 Azure 机器学习服务的 API 请求授权。
    - **服务主体密码** – 输入您在 [Active Directory 应用程序](#aad-app)部分创建的应用程序的服务主体应用程序密码。 此值用于获取您为对 Azure 存储和 Azure 机器语言工作区执行授权操作而创建的安全主体的访问令牌。
    - **存储帐户名称** – 输入您在 Azure 工作区运行设置向导时指定的 Azure 存储帐户名称。 （有关详细信息，请参阅[在 Azure 中设置机器学习](#ml-workspace)一节。）
    - **管道终结点地址** – 输入 Azure 机器学习服务的管道 REST 终结点的 URL。 您[在 Azure 中设置机器学习](#ml-workspace)时作为最后一步创建了此管道。 要获取管道 URL，登录到您的 Azure 门户，在导航中选择 **管道**。 在 **管道** 选项卡上，选择名为 **TriggerDemandForecastGeneration** 的管道终结点。 然后复制显示的 REST 终结点。

    ![需求预测参数页面的 Azure 机器学习服务选项卡上的参数。](media/azure-ml-service-parameters.png "需求预测参数页面的 Azure 机器学习服务选项卡上的参数")

## <a name="privacy-notice"></a><a name="privacy"></a>隐私声明

当您选择 *Azure 机器学习服务* 作为您的预测生成策略时，Supply Chain Management 会自动发送您的历史需求客户数据，如聚合数量、产品名称及其产品维度、装运和收货位置、客户标识符以及预测参数，用于为预测将来的需求定位机器学习工作区及其链接的存储帐户所在的地理区域。 Azure 机器学习服务可能位于与部署 Supply Chain Management 的地理区域不同的区域。 一些用户可以通过在 **需求预测参数** 页面选择预测生成策略来控制是否启用此功能。

## <a name="additional-resources"></a>其他资源

- [需求预测概览](introduction-demand-forecasting.md)
- [生成统计基准预测](generate-statistical-baseline-forecast.md)
- [对基准预测进行手动调整](manual-adjustments-baseline-forecast.md)
- [网络研讨会：使用 Azure 机器学习系列进行需求预测](https://aka.ms/DemandForecastingwithAzureMachineLearningSeries)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
