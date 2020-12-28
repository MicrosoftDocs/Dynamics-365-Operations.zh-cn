---
title: 调整 ER 格式以生成自定义电子单据
description: 本主题说明如何调整 Microsoft 提供的电子申报 (ER) 格式，以便生成自定义电子单据。
author: NickSelin
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7a32ac5f6ab21f89ed3c11c64458286864c9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680162"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>调整 ER 格式以生成自定义电子单据

[!include[banner](../includes/banner.md)]

本主题中的过程介绍系统管理员或电子申报功能顾问角色的用户如何执行以下任务：

- 配置[电子申报 (ER) 框架](general-electronic-reporting.md)的参数。
- 导入由 Microsoft 提供并在处理[供应商付款](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md)期间用于生成付款文件的 ER 配置。
- 创建 Microsoft 提供的标准 ER 格式配置的自定义版本。
- 修改自定义 ER 格式配置，以使其生成满足特定银行要求的付款文件。
- 在自定义 ER 格式配置中应用对标准 ER 格式配置所做的更改。

以下所有过程均可在 **GBSI** 公司中完成。 无需进行编码。

- [配置 ER 框架](#ConfigureFramework)

    - [配置 ER 参数](#ConfigureParameters)
    - [激活 ER 配置提供程序](#ActivateProvider)

        - [查看 ER 配置提供程序列表](#ReviewProvidersList)
        - [添加新 ER 配置提供程序](#ActivateProvider)
        - [激活 ER 配置提供程序](#ActivateAddedProvider)

- [导入标准 ER 格式配置](#ImportERSolution1)

    - [导入标准 ER 配置](#ImportERFormat1)
    - [查看导入的 ER 配置](#ReviewImportedERSolution)

- [准备要处理的供应商付款](#PrepareVendorPayment)

    - [添加供应商帐户的银行信息](#AddBankAccount)
    - [输入供应商付款](#EnterVendorPayment)

- [使用标准 ER 格式处理供应商付款](#ProcessVendorPayment1)

    - [设置电子付款方式](#ConfigureMethodOfPayment1)
    - [处理供应商付款](#ProcessPayment1)

- [自定义标准 ER 格式](#CustomizeProvidedFormat)

    - [创建自定义格式](#DeriveProvidedFormat)
    - [编辑自定义格式](#ConfigureDerivedFormat)
    - [将自定义格式标记为可运行](#MarkFormatRunnable)

- [使用自定义 ER 格式处理供应商付款](#ProcessVendorPayment2)

    - [设置电子付款方式](#ConfigureMethodOfPayment2)
    - [处理供应商付款](#ProcessPayment2)

- [导入标准 ER 格式配置的新版本](#ImportERSolution2)

    - [导入标准 ER 配置的新版本](#ImportERFormat2)
    - [查看导入的 ER 格式配置](#ReviewImportedERFormat)

- [在自定义格式中采用在所导入格式的新版本中进行的更改](#AdoptNewBaseVersion)

    - [完成自定义格式的当前草稿版本](#CompleteDerivedFormat)
    - [将自定义格式重定为新基本版本](#RebaseDerivedFormat)
    - [使用重定 ER 格式处理供应商付款](#ProcessPayment3)

- [其他资源](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>配置 ER 框架

作为电子申报功能顾问角色的用户，您必须至少配置一小组 ER 参数，才能开始使用 ER 框架设计标准 ER 格式的自定义版本。

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>配置 ER 参数

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **电子申报参数**。
3. 在 **电子申报参数** 页上，在 **常规** 选项卡上，将 **启用设计模式** 选项设置为 **是**。
4. 在 **附件** 选项卡上，设置以下参数：

    - 在 **配置** 字段中，选择 **USMF** 公司的 **文件** 类型。
    - 在 **作业存档**、**临时**、**基准** 和 **其他** 字段中，选择 **文件** 类型。

有关 ER 参数的详细信息，请参阅[配置 ER 框架](electronic-reporting-er-configure-parameters.md)。

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>激活 ER 配置提供程序

将把添加的每个 ER 配置标记为由 ER 配置提供程序负责。 在 **电子申报** 工作区中激活的 ER 配置提供程序用于此目的。 因此，必须先在 **电子申报** 工作区中激活 ER 配置提供程序，才能开始添加或编辑 ER 配置。

> [!NOTE]
> 只有 ER 配置的负责人才能对其进行编辑。 因此，必须先在 **电子申报** 工作区中激活相应 ER 配置提供程序，才能编辑 ER 配置。

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>查看 ER 配置提供程序列表

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序表** 页面中，每条提供程序记录都有唯一名称和 URL。 查看此页面的内容。 如果已有 **Litware, Inc.** (`https://www.litware.com`) 的记录，请跳过下一过程，即[添加新 ER 配置提供程序](#ActivateProvider)。

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>添加新 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **相关链接** 部分中，选择 **配置提供程序**。
3. 在 **配置提供程序** 页面上，选择 **新建**。
4. 在 **名称** 字段中，输入 **Litware, Inc.**
5. 在 **Internet 地址** 字段中，输入 `https://www.litware.com`。
6. 选择 **保存**。

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>激活 ER 配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Litware, Inc.** 磁贴，然后选择 **设置有效**。

有关 ER 配置提供程序的详细信息，请参阅[创建配置提供程序并将其标记为有效](tasks/er-configuration-provider-mark-it-active-2016-11.md)。

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>导入标准 ER 格式配置

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>导入标准 ER 配置

若要向当前 Microsoft Dynamics 365 Finance 实例添加标准 ER 配置，必须从为该实例配置的 ER [存储库](general-electronic-reporting.md#Repository)导入这些配置。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。
3. 在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。 如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。
4. 在 **配置存储库** 页面左侧窗格的配置树中，选择 **BACS (UK)** 格式配置。
5. 在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **1.1**。
6. 选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。

![配置存储库页面](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> 如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 Microsoft Dynamics Lifecycle Services (LCS)[ 下载配置](download-electronic-reporting-configuration-lcs.md)。

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>查看导入的 ER 配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**。
4. 请注意，除了所选 **BACS (UK)** ER 格式，还导入了其他必需的 ER 配置。 请确保配置树中有以下 ER 配置：

    - **付款模型** – 此配置中包含[数据模型](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于表示付款业务域的数据结构。
    - **付款模型映射 1611** – 此配置中包含[模型映射](general-electronic-reporting.md#data-model-and-model-mapping-components) ER 组件，用于描述如何在运行时使用应用程序数据填充数据模型。
    - **BACS (UK)** – 此配置中包含[格式](general-electronic-reporting.md#FormatComponentOutbound)和格式映射 ER 组件。 格式组件指定报表布局。 格式映射组件中包含模型数据源，并指定如何在运行时使用此数据源填充报表布局。

![配置页面](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>准备要处理的供应商付款

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>添加供应商帐户的银行信息

必须在等记付款中添加后文将引用的供应商帐户的银行信息。

1. 转到 **应付帐款** \> **供应商** \> **所有供应商**。
2. 在 **所有供应商** 页面中，选择 **GB_SI_000001** 供应商帐户，然后在操作窗格中 **供应商** 选项卡上的 **设置** 组中，选择 **银行帐户**。
3. 在 **供应商银行帐户** 页面上，选择 **新建**，然后输入以下信息：

    1. 在 **银行帐户** 字段中，输入 **GBP OPER**。
    2. 在 **银行组** 字段中，选择 **BankGBP**。
    3. 在 **银行帐号** 字段中，输入 **202015**。
    4. 在 **SWIFT 代码** 字段中，输入 <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**。
    5. 在 **IBAN** 字段中，输入 **GB33BUKB20201555555555**。
    6. 在 **银行代号** 字段中，保留默认值 <a id="DefineRoutingNumber"></a>**123456**。

    ![“供应商银行帐户”页面](./media/er-quick-start2-bank-account.png)

4. 选择 **保存**。
5. 关闭该页面。
6. 在 **所有供应商** 页面中，打开 **GB_SI_000001** 供应商帐户。
7. 在供应商详细信息页面上，选择 **编辑** 使页面可编辑（如果需要）。
8. 在 **付款** 快速选项卡的 **银行帐户** 字段中，选择 **GBP OPER**。

    ![供应商详细信息页面](./media/er-quick-start2-bank-account-reference.png)

9. 选择 **保存**。
10. 关闭该页面。

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>输入供应商付款

必须使用[付款方案](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal)创建新的供应商付款。

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 在 **供应商付款日记帐** 页面上，选择 **新建**。
3. 在 **名称** 字段中，选择 **VendPay**。
4. 选择 **行**。
5. 选择 **付款方案** \> **创建付款方案**。
6. 在 **供应商付款方案** 对话框中，将条件配置为仅筛选 **GB_SI_000001** 供应商帐户的记录，然后选择 **确定**。
7. 选择发票 **00000007_Inv** 的行，然后选择 **创建付款**。

    ![供应商付款方案对话框](./media/er-quick-start2-payment-proposal.png)

8. 验证是否将输入的付款配置为使用 **电子** 付款方式。

    ![供应商付款页面](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>使用标准 ER 格式处理供应商付款

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>设置电子付款方式

必须使用电子付款方式，以使其使用导入的 ER 格式配置。

1. 转到 **应付帐款** \> **付款设置** \> **付款方式**。
2. 在 **付款方式 - 供应商** 页面中，在左侧窗格中选择 **电子** 付款方式。
3. 选择 **编辑**。
4. 在 **文件格式** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。
5. 在 **导出格式配置** 字段中，选择 **BACS (UK)** 格式配置。

    ![付款方式 - 供应商页面](./media/er-quick-start2-method-of-payment1.png)

6. 选择 **保存**。

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>处理供应商付款

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 在 **供应商付款日记帐** 页面上，选择您先前添加的付款日记帐，然后选择 **行**。
3. 在 **供应商付款** 页面上，选择 **生成付款**。
4. 在 **生成付款** 对话框中，输入以下信息：

    - 在 **付款方式** 字段中，选择 **电子**。
    - 在 **银行帐户** 字段中，选择 **GBSI OPER**。

5. 选择 **确定**。
6. 在 **电子报表参数** 对话框中，将 **打印控制报表** 选项设置为 **是**，然后选择 **确定**。

    ![“电子报表参数对话框”页面](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > 除了付款文件，现在还可以生成控制报表。

7. 下载 zip 文件，然后从中提取以下文件：

    - Excel 格式的控制报表
    - TXT 格式的付款文件

        请注意，按照提供的 ER 格式的[结构](#PositionRoutingNumber)，生成的文件中的付款行以为配置的用户帐户[定义的](#DefineRoutingNumber)银行代号开始。

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>自定义标准 ER 格式

对于此部分中显示的示例，需要使用 Microsoft 提供的 ER 配置生成 BACS 格式的供应商付款文件，但是必须添加自定义来支持特定银行的要求。 还需要可以在新的 ER 配置版本可用时升级自定义格式。 但是，您希望可以以最低成本进行升级。

在此情况下，作为 Litware, Inc. 的代表，您必须以 **BACS (UK)** Microsoft 提供的配置为基础创建（派生）新 ER 格式配置。

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>创建自定义格式

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS (UK)**。 Litware, Inc. 将把此 ER 格式配置的版本 1.1 用作自定义版本的基础。
3. 选择 **创建配置**，以打开下拉对话框。 可使用此对话框创建自定义付款格式的新配置。
4. 在 **新建** 字段组中，选择 **从以下名称派生: BACS (UK), Microsoft** 选项。
5. 在 **名称** 字段中，输入 **BACS（UK 自定义）**。

    ![“创建配置”下拉对话框](./media/er-quick-start2-add-derived-format.png)

6. 选择 **创建配置**。

将创建 **BACS（UK 自定义）** ER 格式配置的版本 1.1.1。 此版本的 [状态](general-electronic-reporting.md#component-versioning)为 **草稿**，可以编辑。 自定义 ER 格式的当前内容与 Microsoft 提供的格式的内容匹配。

![配置页面](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>编辑自定义格式

必须配置自定义格式，使其满足银行的特定要求。 例如，一家银行可能要求生成的付款文件中包含银行的国际银行金融电信协会 (SWIFT) 代码，该代码为银行分配所处理供应商付款中的代理角色。 SWIFT 代码是用于在全球识别特定银行的国际银行代码。 也称为银行标识符代码 (BIC)。 SWIFT 代码的长度必须为 11 个字符，并且必须在生成的付款文件中每个付款行开始处输入。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS（UK 自定义）**。
3. 在 **版本** 快速选项卡上，选择所选配置的版本 **1.1.1**。
4. 选择 **设计器**。
5. 在 **格式设计器** 页面中，选择 **显示详细信息** 查看有关格式元素的详细信息。
6. 展开并查看以下元素：

    - **文件夹** 类型的 **BACSReportsFolder** 元素。 此元素用于生成 ZIP 格式的输出。
    - **文件** 类型的 **file** 元素。 此元素用于生成 TXT 格式的付款文件。
    - **序列** 类型的 **transactions** 元素。 此元素用于在付款文件中生成单个付款行。
    - **序列** 类型的 **transaction** 元素。 此元素用于生成单个付款行的各字段。

7. 选择 **transaction** 元素。

    ![ER Operations 设计器中的 transaction 元素](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > 将配置提供的报表，使<a id="PositionRoutingNumber"></a>每个付款行以银行代号开头。 **vendBankRouteNum** 格式元素用于此目的。 

8. 选择 **添加**，然后选择添加的格式元素的 **Text\\String** 类型：

    1. 在 **名称** 字段中，输入 **vendBankSWIFT**。
    2. 在 **最小长度** 字段中，输入 **11**。
    3. 在 **最大长度** 字段中，输入 **11**。
    4. 选择 **确定**。

    > [!NOTE]
    > **vendBankSWIFT** 元素将用于在生成的文件中输入供应商银行的 SWIFT 代码。

9. 在格式结构树中，选择 **vendBankSWIFT**。
10. 选择 **上移** 将所选格式元素上移一级。 重复此步骤，直到 **vendBankSWIFT** 元素成为父 **transaction** 元素下的<a id="PositionSWIFTCode"></a>第一个元素。

    ![VendBankSWIFT 为 ER Operations 设计器中 transaction 下的第一个元素](./media/er-quick-start2-derived-format1.png)

11. 格式结构树中 **vendBankSWIFT** 仍处于选中状态时，选择 **映射** 选项卡，然后展开 **模型** 数据源。
12. 展开 **model.Payment** \> **model.Payment.CreditorAgent**，然后选择 **model.Payment.CreditorAgent.BICFI** 数据源字段。 此数据源字段显示供应商银行的 SWIFT 代码，该代码在处理的供应商付款中为银行分配代理角色。
13. 选择 **绑定**。 **vendBankSWIFT** 格式元素现在已经与 **model.Payment.CreditorAgent.BICFI** 数据源字段绑定，因此将在生成的付款文件中输入 SWIFT 代码。

    ![ER Operations 设计器中 vendBankSWIFT 格式元素与 model.Payment.CreditorAgent.BICFI 数据源字段绑定](./media/er-quick-start2-derived-format2.png)

14. 选择 **保存**。
15. 关闭设计器页面。

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>将自定义格式标记为可运行

已创建自定义格式的第一个版本，并且其状态为 **操作**，您可以针对测试用途运行该版本。 若要运行此报表，必须使用引用自定义 ER 格式的付款方式处理供应商付款。 默认情况下，从应用程序调用 ER 格式时，仅 [考虑](general-electronic-reporting.md#component-versioning)状态为 **已完成** 或 **已共享** 的版本。 此行为有助于避免使用未完成设计的 ER 格式。 但是，对于测试运行，可以强制应用程序使用状态为 **草稿** 的 ER 格式版本。 因此，如果需要进行任何修改，可以调整当前格式版本。 有关详细信息，请参阅[适用性](electronic-reporting-destinations.md#applicability)。

要使用 ER 格式的草稿版本，必须显式标记 ER 格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
4. 根据需要，选择 **编辑** 以使当前页面可供编辑。
5. 在左侧窗格的配置树中，选择 **BACS（UK 自定义）**。
6. 将 **运行草稿** 选项设置为 **是**。

    !["配置"页面上的"运行草稿"选项](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>使用自定义 ER 格式处理供应商付款

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>设置电子付款方式

必须配置电子付款方式，以便使用自定义 ER 格式处理供应商付款。

1. 转到 **应付帐款** \> **付款设置** \> **付款方式**。
2. 在 **付款方式 - 供应商** 页面中，在左侧窗格中选择 **电子** 付款方式。
3. 选择 **编辑**。
4. 在 **文件格式** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。
5. 在 **导出格式配置** 字段中，选择 **BACS（UK 自定义）** 格式配置。

    ![付款方式 - 供应商页面](./media/er-quick-start2-method-of-payment2.png)

6. 选择 **保存**。

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>处理供应商付款

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 在 **供应商付款日记帐** 页面上，选择您先前创建的付款日记帐。
3. 选择 **行**。
4. 在 **供应商付款** 页面中网格上方，选择 **付款状态** \> **无**。
5. 选择 **生成付款**。
6. 在 **生成付款** 对话框中，输入以下信息：

    - 在 **付款方式** 字段中，选择 **电子**。
    - 在 **银行帐户** 字段中，选择 **GBSI OPER**。

7. 选择 **确定**。
8. 在 **电子报表参数** 对话框中，将 **打印控制报表** 选项设置为 **是**，然后选择 **确定**。

    > [!NOTE]
    > 除了付款文件，只能生成控制报表。

9. 下载 zip 文件，然后从中提取以下文件：

    - Excel 格式的控制报表
    - TXT 格式的付款文件

        请注意，按照自定义 ER 格式的结构，生成的文件中的付款行现在以为处理了其付款的供应商的银行帐户[输入的](#DefineSWIFTCode) SWIFT 代码[开始](#PositionSWIFTCode)。

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>导入标准 ER 格式配置的新版本

对于本部分中显示的示例，您将收到有关知识库文章 [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) 的通知。 此通知通知您 Microsoft 已发布的 **BACS (UK)** ER 格式新版本。 除了控制报表，用户还可以在处理供应商付款时通过这个新版本生成付款通知报表和出席单报表。 您希望开始使用此功能。

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>导入标准 ER 配置的新版本

若要向当前 Finance 实例添加新 ER 配置版本，必须从已配置的的 ER [存储库](general-electronic-reporting.md#Repository)导入这些配置。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置提供程序** 部分中，选择 **Microsoft** 磁贴，然后选择 **存储库** 查看 Microsoft 提供程序的存储库列表。
3. 在 **配置存储库** 页，选择 **全球** 类型的存储库，然后选择 **打开**。 如果提示您进行授权以连接到 Regulatory Configuration Service，请按照授权说明进行操作。
4. 在 **配置存储库** 页面左侧窗格的配置树中，选择 **BACS (UK)** 格式配置。
5. 在 **版本** 快速选项卡上，选择所选 ER 格式配置的版本 **3.3**。
6. 选择 **导入** 将所选版本从全局存储库下载到当前 Finance 实例。

![配置存储库页面](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> 如果在访问[全球存储库](er-download-configurations-global-repo.md)时遇到问题，可改为从 LCS [下载配置](download-electronic-reporting-configuration-lcs.md)。

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>查看导入的 ER 格式配置

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS (UK)**。
4. 在 **版本** 快速选项卡中，选择版本 **3.3**。
5. 选择 **设计器**。
6. 在 **格式设计器** 页面中，展开 **BACSReportsFolder** 格式元素。
7.  请注意，版本 3.3 中包含 **PaymentAdviceReport** 格式元素，用于在处理供应商付款时生成付款通知报表。

    ![ER Operations 设计器中的 PaymentAdviceReport 格式元素](./media/er-quick-start2-imported-solution2.png)

8. 关闭设计器页面。

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>在自定义格式中采用在所导入格式的新版本中进行的更改

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>完成自定义格式的当前草稿版本

如果要保持自定义格式的当前状态，请通过将状态从 **草稿** 更改为 **已完成** 来完成草稿版本 1.1.1。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，展开 **BACS (UK)**，然后选择 **BACS（UK 自定义）**。
4. 在 **版本** 快速选项卡上，选择 **更改状态** \> **完成**，然后选择 **确定**。

版本 1.1.1 的状态将从 **草稿** 更改为 **已完成**，并且该版本变为只读。 已添加了一个新的可编辑版本 1.1.2，其状态为 **草稿**。 您可以使用此版本在自定义 ER 格式中进行进一步的更改。

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>将自定义格式重定为新基本版本

若要开始在自定义中使用 **BACS (UK)** 格式版本 3.3 的新功能，必须更改自定义配置 **BACS（UK 自定义）** 的基本基本配置版本。 此流程称为[重定基本值](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)。 使用 **BACS (UK)** 版本 3.3，而不是版本 1.1。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，然后选择 **BACS（UK 自定义）**。
3. 在 **版本** 快速选项卡上，选择版本 **1.1.2**，然后选择 **重定**。
4. 在 **重定** 对话框的 **目标** 字段中，选择基本配置的版本 **3.3** 将其作为新基础应用，并用于更新配置。

    ![“重定基本版本”对话框](./media/er-quick-start2-rebase1.png)

5. 选择 **确定**。
6. 请注意，草稿版本的版本号已经从 **1.1.2** 更改为 **3.3.2** 以体现基本版本中的更改。

    在合并自定义版本和新基本版本时，可能会发现一些冲突，因为不能自动合并格式更改。

    ![“配置”页中存在冲突的重定后配置](./media/er-quick-start2-rebase2.png)

    如果发现了冲突，必须在格式设计器中手动解决。

7. 在 **版本** 快速选项卡中，选择版本 **3.3.2**。
8. 选择 **设计器**。
9. 在 **格式设计器** 页面的 **详细信息** 快速选项卡上，选择重定冲突记录，然后选择 **应用基值**。

    ![ER Operations 设计器中的重定冲突记录](./media/er-quick-start2-rebase3.png)

10. 选择 **保存**。

    **详细信息** 快速选项卡中不应再显示重定冲突记录。

    ![ER Operations 设计器中已解决冲突](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > 您通过确认必须在此 ER 格式中使用基本模型版本 3 解决了冲突。

11. 展开 **BACSReportsFolder** \> **文件** \> **transactions** \> **transaction**。
12. 在 **映射** 选项卡上，注意自定义 ER 格式版本 3.3.2 中同时包含您的自定义（**vendBankSWIFT** 格式元素及其绑定）和 Microsoft 提供的基本 ER 格式版本 3.3 的新功能（**PaymentAdviceReport** 格式元素及其嵌套元素和配置的绑定）。 您单击了几次鼠标通过将新基本版本的修改与自定义合并，采用了这些修改。

    ![ER Operations 设计器中合并后的格式](./media/er-quick-start2-rebase5.png)

13. 关闭设计器页面。

> [!NOTE]
> 重定操作可逆。 若要取消此重定，请在 **版本** 快速选项卡上选择 **BACS（UK 自定义）** 格式版本 **1.1.1**，然后选择 **获取此版本**。 然后将把版本 3.3.2 重新编号为 1.1.2，而草稿版本 1.1.2 的内容将与版本 1.1.1 的内容匹配。

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>使用重定 ER 格式处理供应商付款

1. 转到 **应付帐款** \> **付款** \> **供应商付款日记帐**。
2. 在 **供应商付款日记帐** 页面上，选择您先前创建的付款日记帐。
3. 选择 **行**。
4. 在 **供应商付款** 页面中网格上方，选择 **付款状态** \> **无**。
5. 选择 **生成付款**。
6. 在 **生成付款** 对话框中，输入以下信息：

    - 在 **付款方式** 字段中，选择 **电子**。
    - 在 **银行帐户** 字段中，选择 **GBSI OPER**。

7. 选择 **确定**。
8. 在 **电子报表参数** 对话框中，输入以下信息：

    - 将 **打印控制报表** 选项设置为 **是**。
    - 将 **打印付款通知** 选项设置为 **是**。

    ![电子报表参数对话框](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > 除了付款文件，现在还可以生成控制报表和付款通知报表。

9. 选择 **确定**。
10. 下载 zip 文件，然后从中提取以下文件：

    - Excel 格式的控制报表
    - Excel 格式的付款通知报表

        ![Excel 格式的付款通知报表](./media/er-quick-start2-payment-advice-report.png)

    - TXT 格式的付款文件

        请注意，生成的文件中的付款行以为处理了其付款的供应商的银行帐户输入的 SWIFT 代码开始。

        ![TXT 格式的付款文件](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [从 Lifecycle Services 下载 ER 配置](download-electronic-reporting-configuration-lcs.md)
- [从 Configuration Service 的全局存储库下载 ER 配置](er-download-configurations-global-repo.md)
