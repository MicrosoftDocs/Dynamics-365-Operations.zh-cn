---
title: 增值税申报（丹麦）
description: 本文介绍如何设置和生成丹麦预付款增值税 (VAT) 申报。
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 99c8b7a35258116adfe7433e884564d64dbf140f
ms.sourcegitcommit: 3aa3dedc3123cb079614762e2718841c2f7d7d35
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2022
ms.locfileid: "9812124"
---
# <a name="vat-declaration-denmark"></a>增值税申报（丹麦）

[!include [banner](../includes/banner.md)]

本文介绍如何设置丹麦增值税 (VAT) 申报并在 Microsoft Excel 中预览此申报。

若要自动生成报表，请先创建足够的销售税代码，以为预付款增值税申报中的每个框保留单独的增值税核算。 此外，在预付款增值税申报的电子报告 (ER) 格式的应用程序特定参数中，将销售税代码与增值税申报中框的查找结果关联。

对于丹麦，必须配置 **报表字段查找**。 有关如何设置应用程序特定参数的详细信息，请参阅本文后面的[设置增值税申报字段的应用程序特定参数](#set-up-application-specific-parameters)一节。

在以下表中，“查找结果”列显示为增值税申报格式的特定增值税申报行预配置的查找结果。 使用此信息可将销售税代码与查找结果正确关联，然后与增值税申报行正确关联。

### <a name="vat-declaration-overview"></a>增值税申报概览

丹麦增值税申报包含以下信息。

**应付 VAT**

| Description                                                  | 计税基数/税额 | 查找结果/总计                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 销项增值税                                                   | 税额          | **OutputVAT**</br> **DomesticVATUseTax**（也在“进项增值税”框中报告过）                                                                                                                                                                                                                                                                       |
| 货物增值税等 已在国外购买                           | 税额          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax**（也在“进项增值税”框中报告过）</br>**PurchaseGoodsEU**（在“框 A - 货物采购”中报告计税基数。）</br>**PurchaseGoodsEUUseTax**（也在“进项增值税”框中报告税额。 在“框 A - 货物采购”中报告计税基数。）                   |
| 境外采购的、采用逆向收费形式的服务的增值税 | 税额          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax**（也在“进项增值税”框中报告过）</br>**PurchaseServicesEU**（在“框 A - 货物采购”中报告计税基数。）</br>**PurchaseServicesEUUseTax**（也在“进项增值税”框中报告税额。 在“框 A - 服务采购”中报告计税基数。） |
| 应付款总计                                                | 税额          | 前三个框的总计                                                                                                                                                                                                                                                                                                            |

**扣缴**

| Description                                                                               | 计税基数/税额 | 查找结果/总计                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 进项增值税                                                                                 | 税额          | **InputVAT**</br> **DomesticVATUseTax**（也在“销项增值税”框中报告过）</br>**PurchaseGoodsAbroadUseTax**（也在“国外购买的货物等增值税” 框中报告过）</br>**PurchaseServicesAbroadUseTax**（“在国外购买且需要支付冲销费用的服务的增值税”框中也报告过）</br>**PurchaseGoodsEUUseTax**（也在“国外购买的货物等增值税” 框中报告过）</br> **PurchaseServicesEUUseTax**（“在国外购买且需要支付冲销费用的服务的增值税”框中也报告过） |
| 石油和罐装液化气税                                                                  | 税额          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| 能源/电力税                                                                    | 税额          | **PowerElectricityDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 天然气和城市煤气税                                                             | 税额          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| 碳税                                                                               | 税额          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | 税额          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 水费                                                                              | 税额          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 扣减总额                                                                          | 税额          | 前六个框的总计                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| 总税额(正金额 = 需付款，负金额 = 可获得退款) | 税额          | “应付款总计”-“扣缴总计”                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**补充信息**

| Description                                                                                                                                                                                                                                | 计税基数/税额 | 查找结果/总计                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| 框 A - 货物购置。 联合内部货物购置的不含增值税的值。                                                                                                                                                   | 计税基数            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| 框 A - 服务购置。 联合内部服务购置的不含增值税的值。                                                                                                                                             | 计税基数            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| 框 B - 货物供应 - 要报告到“无增值税的欧盟销售”/DK VIES。 联合内部货物供应的不含增值税的值                                                                                                           | 计税基数            | **SalesGoodsEU**                                |
| 框 B - 供应 - 将不报告到“无增值税的欧盟销售”/DK VIES。 某些联合内部供应（例如安装、装配、远程销售和非应纳税人员的新运输方式）的不含增值税的值。 | 计税基数            | **SalesInstallationAssemblyEtcEU**              |
| 框 B - 服务供应。 买方应支付增值税作为冲销费用的联合内部服务购置的不含增值税的值 - 也必须报告到“无增值税的欧盟销售”/DK VIES。                          | 计税基数            | **SalesServicesEU**                             |
| 框 C - 其他供应。 在丹麦境内向其他欧盟成员国以及第三国家/地区或第三个区域以无增值税方式提供的其他货物和服务的供应值。                                     | 计税基数            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>进项反向增值税

如果您将销售税代码配置为使用销项税过帐汇入反向增值税，请将您的销售税代码与名称中包含“UseTax”的 **报表字段查找** 的查找结果相关联。

或者，您可以配置两个单独的销售税代码：一个用于应缴增值税，一个用于增值税扣缴。 然后将每个代码与 **报表字段查找** 的相应查找结果相关联。

例如，对于应纳税的集团内部购置，您为销售税代码 **UT_S_EU** 配置了销项税，并将其与 **报表字段查找** 的 **PurchaseGoodsEUUseTax** 查找结果相关联。 在这种情况下，使用 **UT_S_EU** 销售税代码的税额会反映在“国外购买的货物等增值税” 和“进项增值税”框中。 “框 A - 货物购置”中反映了计税基数。

或者，您可以配置以下两个销售税代码：

- **VAT_S_EU**，其税率值为 -25%
- **InVAT_S_EU**，其税率值为 25%

然后，您通过以下方法将这两个代码与 **报表字段查找** 的查找结果相关联。

- 将 **VAT_S_EU** 与 **PurchaseGoodsEU** 查找结果相关联。
- 将 **InVAT_S_EU** 与 **InputVAT** 查找结果相关联。

在这种情况下，使用 **VAT_S_EU** 销售税代码的税额会反映在“国外购买的货物等增值税” 框和“框 A - 货物购置”中。 使用 **InVAT_S_EU** 销售税代码的金额会反映在“进项增值税”框中。

有关如何配置反向增值税的详细信息，请参阅[冲销费用](emea-reverse-charge.md)。

## <a name="configure-system-parameters"></a>配置系统参数

若要生成增值税申报，您必须配置增值税编号。

1. 转至 **组织管理** > **组织** > **法人**。
2. 选择法人，然后选择 **登记 ID**。
3. 选择或创建丹麦地址，然后在 **登记 ID** 快速选项卡上选择 **添加**。
4. 在 **登记类型** 字段中，选择专用于丹麦且使用 **增值税 ID** 登记类别的登记类型。
5. 在 **登记编号** 字段中，输入税号。
6. 在 **常规** 选项卡上的 **有效** 字段中，输入税号生效日期。

有关如何设置登记类别和登记类型的详细信息，请参阅[登记 ID](emea-registration-ids.md)。

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>设置丹麦增值税申报预览

### <a name="import-er-configurations"></a>导入 ER 配置

打开 **电子报告** 工作区，并导入 **增值税申报 Excel (DK)** ER 格式。

有关详细信息，请参阅[从 Configuration service 的全局知识库下载 ER 配置](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)。

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>设置增值税申报字段的应用程序特定参数

> [!NOTE]
> 我们建议您在 **功能管理** 工作区中启用 **使用先前版本的 ER 格式中的应用程序特定参数** 功能。 启用此功能后，为早期版本的 ER 格式配置的参数将自动适用于相同格式的后续版本。 如果未启用此功能，则您必须为每个格式版本显式配置特定于应用程序的参数。 从 Finance 版本 10.0.23 开始，**功能管理** 工作区中将提供 **使用先前版本的 ER 格式中的应用程序特定参数** 功能。 有关如何为每个法人设置 ER 格式参数的详细信息，请参阅[设置每个法人的 ER 格式的参数](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md)。

若要自动生成增值税申报，请关联应用程序中的销售税代码和 ER 配置中的查找结果。

按照这些步骤定义哪些销售税代码在增值税申报中生成哪些框。

1. 转到 **工作区** > **电子申报**，并选择 **报告配置**。
2. 选择 **增值税申报 Excel (DK)** 配置，然后选择 **配置 \> 应用程序特定参数设置**。
3. 在 **应用程序特定参数** 页面的 **查找** 快速选项卡上，选择 **报表字段查找**。
4. 在 **条件** 快速选项卡上，设置以下字段以关联销售税代码和报表字段。

    | 字段                  | Description                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 查找结果          | 选择报表字段的值。 有关这些值及其分配到增值税申报行的详细信息，请参阅本文前面的[增值税申报概览](#vat-declaration-overview)一节。                                                                                               |
    | 税码               | 选择要与报表字段关联的销售税代码。 使用所选销售税代码的已过帐税务交易记录将收集在适当的申报框中。 我们建议您通过以下方式来分隔销售税代码：一个销售税代码仅在一个申报框中生成金额。 |
    | 交易分类符 | 如果您创建了足以确定申报框的销售税代码，请选择 **\*非空\***。 如果未创建足够的销售税代码以便一个销售税代码仅在一个申报框中生成金额，则可以设置交易分类符。 提供了以下交易分类符：</br>-   **采购**</br>-   **PurchaseExempt**（免税购买）</br>-   **PurchaseReverseCharge**（购买冲销费用的应收税款）</br>-   **销售额**</br>-   **SalesExempt**（免税销售）</br>-   **SalesReverseCharge**（购买冲销费用或销售冲销费用的应付税款）</br>-   **销项税**。 </br>对于每个交易分类符，贷方通知单的分类符也可用。 例如，这些分类符之一是 **PurchaseCreditNote**（购买贷方通知单）。</br>请务必为每个销售税代码创建两个行：一行具有交易分类符值，另一行具有贷方通知单值的交易分类符。 |


    > [!NOTE]
    > 将所有销售税代码与查找结果关联。 如果任何销售税代码不应在增值税申报上生成值，请将销售税代码与 **其他** 查找结果关联。

    ![应用程序特定参数页面。](media/7db74920fad66a0db7fad60758698cc0.png)


5. 在 **状态** 字段中，将值更改为 **已完成**。

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>在 Excel 中为预览金额设置增值税报告格式

1. 在 **功能管理** 工作区中，找到并选择列表中的 **增值税报表格式报告** 功能，然后选择 **立即启用**。
2. 转到 **总帐** > **设置** > **总帐参数**。
3. 在 **销售税** 选项卡上的 **税选项** 快速选项卡，在 **增值税对帐单格式映射** 字段中，选择 **增值税申报 Excel (DK)** ER 格式。

   运行 **报告结算期的销售税** 时会打印此格式。 当您选择 **销售税付款** 页面上的 **打印** 时，也会打印此格式。

4. 在 **税务主管机构** 页面上，选择税务主管机构，然后在 **报表布局** 字段中选择 **默认**。

如果您要在具有[多个增值税登记](emea-reporting-for-multiple-vat-registrations.md)的法人中配置增值税申报，请按照以下步骤操作。

1. 转到 **总帐** \> **设置** \> **总帐参数**。
2. 在 **销售税** 选项卡的 **国家/地区电子报告** 快速选项卡中，在 **DNK** 行上，选择 **增值税申报 Excel (DK)** ER 格式。

## <a name="set-up-electronic-messages"></a>设置电子消息

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>下载并导入具有电子消息示例设置的数据包

数据包包含电子消息设置，这些设置用于在 Excel 中预览增值税申报。 您可以扩展这些设置或创建您自己的设置。 有关如何处理电子消息和创建您自己的设置的详细信息，请参阅[电子消息](../general-ledger/electronic-messaging.md)。

1. 在 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) 内的共用资产库中，选择 **数据包** 作为资产类型，然后下载 **DK 增值税申报包**。 下载的文件名称为 **DK VAT declaration package.zip**。
2. 在 Finance 内的 **数据管理** 工作区中，选择 **导入**。
3. 在 **导入** 快速选项卡上的 **组名称** 字段中，为作业输入一个名称。
4. 在 **选定实体** 快速选项卡上，选择 **添加文件**。
5. 在 **添加文件** 对话框中，验证 **源数据格式** 字段是否已设置为 **包**，选择 **上传并添加**，然后选择您之前下载的 zip 文件。
6. 选择 **关闭**。
7. 上传数据实体后，在操作窗格上选择 **导入**。
8. 转到 **税务** > **查询和报告** > **电子消息** > **电子消息**，并验证您导入的电子消息处理（**DK 增值税申报**）。

### <a name="configure-electronic-messages"></a>配置电子消息

1. 转到 **税务** > **设置** > **电子消息** > **填充记录操作**。
2. 选择 **DK 填充增值税退货记录** 的行，然后选择 **编辑查询**。
3. 使用筛选器指定要包括在报表中的结算期间。
4. 如果您必须在其他申报中报告其他结算期间的税务交易，请创建新的 **填充记录** 操作，并选择适当的结算期间。

## <a name="preview-the-vat-declaration-in-excel"></a>在 Excel 中预览增值税申报

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>在 Excel 中预览“报告结算期间的销售税”定期任务中的增值税申报

1. 转至 **纳税** > **定期任务** > **申报** > **销售税** > **报告结算期间的销售税**。
2. 在 **结算期间** 字段中，选择一个值。
3. 在 **销售税付款版本** 字段中，选择以下值之一：

    - **原始**：为原始销售税付款的销售税交易或在生成销售税付款之前生成报表。
    - **更正**：为该期间所有后续销售税付款的销售税交易生成报表。
    - **总计列表**：为该期间的所有销售税交易生成报表，包括原始报表和所有更正报表。

4. 在 **开始日期** 字段中，选择报告期间的开始日期。
5. 选择 **确定**，查看 Excel 报表。

### <a name="settle-and-post-sales-tax"></a>结算并过帐销售税

1. 转到 **纳税** > **定期任务** > **申报** > **销售税** > **结算和过帐销售税**。
2. 在 **结算期间** 字段中，选择一个值。
3. 在 **销售税付款版本** 字段中，选择以下值之一：

    - **原始**：生成结算期间的原始销售税付款。
    - **最新更正**：创建结算期间的原始销售税付款后，生成更正销售税付款。

4. 在 **开始日期** 字段中，选择报告期间的开始日期。
5. 选择 **确定**。

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>在 Excel 中从销售税付款预览增值税申报

1. 转到 **纳税** > **查询和报表** > **销售税查询** > **销售税付款**，并选择销售税付款行。
2. 选择 **打印报表**，然后选择 **确定**。
3. 查看为所选销售税付款行生成的 Excel 文件。

> [!NOTE]
> 仅针对选定的销售税付款行生成报表。 例如，如果您必须生成一个包含此期间的所有更正的更正申报，或一个包含原始数据和所有更正的替换申报，请使用 **报告结算期间的销售税** 定期任务。

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>通过电子消息生成增值税申报

当您使用电子消息生成报表时，您可以从多个法人收集税务数据。 有关详细信息，请参阅本文后面的[为多个法人运行增值税申报](#run-vat-declaration)一节。

以下过程适用于您以前从 LCS 共用资产库导入的电子消息处理示例。

1. 转到 **税务 \> 查询和报表 \> 电子消息 \> 电子消息**。
2. 在左窗格中，选择 **DK 增值税申报**。
3. 在 **消息** 快速选项卡上，选择 **新建**，然后在 **运行处理** 对话框中，选择 **确定**。
4. 选择创建的消息行，输入描述，然后指定申报的开始和结束日期。

   > [!NOTE]
   > 步骤 5 到 7 是可选步骤。

5. 可选：在 **消息** 快速选项卡上，选择 **收集数据**，然后选择 **确定**。 之前生成的销售税付款将添加到消息中。 有关详细信息，请参阅本文前面的[结算和过帐销售税](#settle-and-post-sales-tax)一节。 如果跳过此步骤，您仍然可以使用 **申报** 对话框中的 **纳税申报版本** 字段生成增值税申报。
6. 可选：在 **消息项** 快速选项卡上，查看转移以进行处理的销售税付款。 默认情况下，所有未包含在相同处理的任何其他消息中的所选期间所有销售税付款都包含在内。
7. 可选：选择 **原始单据** 以审查销售税付款，或选择 **删除** 以从处理中排除销售税付款。 如果跳过此步骤，您仍然可以使用 **申报** 对话框中的 **纳税申报版本** 字段生成增值税申报。
8. 在 **消息** 快速选项卡上，选择 **更新状态**。 在 **更新状态** 对话框中，选择 **准备生成**，然后选择 **确定**。 验证消息状态是否已更改为 **准备生成**。
9. 选择 **生成报表**。 要预览增值税申报金额，请在 **运行处理** 对话框中选择 **预览报表**，然后选择 **确定**。
10. 在 **电子报告参数** 对话框中，根据本文前面 [在 Excel 中预览“报告结算期间的销售税”定期任务中的增值税申报](#preview-vat-excel)一节中的描述设置字段，然后选择 **确定**。
11. 选择页面右上角的 **附件** 按钮（回形针符号），然后选择 **打开** 以打开文件。 查看 Excel 文档中的金额。

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>为多个法人运行增值税申报

要使用这些格式报告一组法人的增值税申报，您必须首先为所有必需法人的销售税代码设置 ER 格式的应用程序特定参数。

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>设置电子消息以从多个法人收集税务数据

按照以下步骤设置电子消息以从多个法人收集数据。

1. 转到 **工作区** > **功能管理**。
2. 在列表中查找并选择 **填充记录操作的跨公司查询** 功能，然后选择 **立即启用**。
3. 转到 **税务** > **设置** > **电子消息** > **填充记录操作**。
4. 在 **填充记录操作** 页面上，选择 **DK 填充增值税退税记录** 行。

   在 **数据源设置** 网格中，**公司** 字段可用。 对于现有记录，此字段会显示当前法人的标识符。

5. 在 **数据源设置** 网格中，为必须包含在报告中的每个其他法人添加一行。 对于每个新行，设置以下字段。

    | 字段                  | Description                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Name                   | 输入一个值以帮助您了解此记录的来源。 例如，输入 **子公司 1 的增值税付款**。 |
    | 消息项类型      | 选择 **增值税退税**。 此值是唯一适用于所有记录的值。                                    |
    | 帐户类型           | 选择 **全部**。                                                                                                               |
    | 主表名称      | 为所有记录指定 **TaxReportVoucher**。                                                                             |
    | 单据编号字段  | 为所有记录指定 **凭证**。                                                                                      |
    | 单据日期字段    | 为所有记录指定 **TransDate**。                                                                                    |
    | 文档帐户字段 | 为所有记录指定 **TaxPeriod**。                                                                                    |
    | 公司                | 选择法人的 ID。                                                                                            |
    | 用户查询             | 当您通过选择 **编辑查询** 定义条件时，将自动选择此复选框。                                 |

6. 对于每个新行，选择 **编辑查询**，并指定行上 **公司** 字段中指定的法人的相关结算期间。

完成设置后，**电子消息** 页面上的 **收集数据** 函数将收集您定义的所有法人的销售税付款。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
