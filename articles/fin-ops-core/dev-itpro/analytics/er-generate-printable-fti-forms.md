---
title: 生成可打印的 FTI 表单
description: 本主题说明如何使用电子申报 (ER) 框架生成 Microsoft Office 文档格式的可打印普通发票 (FTI) 表单。
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 168cef1b5f5d48cb739b08fa395c1bcd62089494
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686713"
---
# <a name="generate-printable-fti-forms"></a>生成可打印的 FTI 窗体

[!include[banner](../includes/banner.md)]

可使用电子申报 (ER) 框架生成 Microsoft Office 文档格式的可打印普通发票 (FTI) 表单。 此主题提供有关如何构建自己的配置的信息和有关可用配置模板的详细信息。

## <a name="overview"></a>概览

除了通过使用 Microsoft SQL Server Reporting Services (SSRS) 生成可打印 FTI 表单这一项现有功能，现在还可以使用 ER 框架。 可在 Microsoft Office Excel 和 Word 中管理可打印 FTI 表单。 还可以修改布局、数据流和格式设置以满足特定要求，同时无需更改代码。

> [!NOTE]
> 如果要从现有 ER 配置的概述开始了解这个可打印 FTI 表单解决方案示例，可直接转至本主题后文的 **下载示例 ER 配置以生成可打印 FTI 表单** 部分。

## <a name="create-customized-configurations-for-fti-printable-forms"></a>为 FTI 可打印表单创建自定义配置
在可打印 FTI 表单的自定义解决方案中，必须创建一组 ER 配置。

### <a name="configure-the-er-data-model"></a>配置 ER 数据模型
您的应用程序中必须包含 ER 数据模型配置，其中包含一个数据模型，用于描述客户开票业务域。 按照要求，此数据模型的名称必须为 **CustomersInvoicing**。 有关如何设计 ER 数据模型的信息，请参阅 [ER 设计域特定数据模型](tasks/er-design-domain-specific-data-model-2016-11.md)。

### <a name="configure-the-er-model-mapping"></a>配置 ER 模型映射
您的应用程序中必须包含 CustomersInvoicing 数据模型的 ER 模型映射。 此模型映射可以为 ER 数据模型配置或 ER 模型映射配置。 但是，该模型映射的根描述符的名称必须为 **FreeTextInvoice**。

该映射中必须包含以下数据源：

- 数据源类型：**表记录**

    - 该数据源的名称必须为 **CustInvoiceJour**。
    - 它必须引用 CustInvoiceJour 应用程序表。
    - 它用于在运行时将已选择打印的发票的列表从应用程序传递到 ER 模型映射。

- 数据源类型：**对象**

    - 该数据源的名称必须为 **PrintMgmtPrintSettingDetail**。
    - 它必须引用 **PrintMgmtPrintSettingDetail** 应用程序表。
    - 它用于在运行时将运行的 ER 格式的打印管理设置的详细信息从应用程序传递到 ER 模型映射。

应用程序源代码的 **ERPrintMgmtReportFormatSubscriber** 类（ER 应用程序套件集成模型）中包含有关应用程序与 ER 框架之间的集成的详细信息。

有关设计 ER 模型映射的详细信息，请参阅[定义 ER 模型映射并从中选择数据源](tasks/er-define-model-mapping-select-data-sources-2016-11.md)。

### <a name="configure-the-er-format"></a>配置 ER 格式
在您的应用程序实例中，必须设置要用于生成 FTI 表单的 ER 格式配置。 

> [!NOTE]
> 必须为 CustomersInvoicing 数据模型创建此格式配置，并且此格式配置必须使用具有 **FreeTextInvoice** 根描述符的模型映射。

有关如何配置 ER 格式的信息，请参阅 [ER 创建格式配置（2016 年 11 月）](tasks/er-format-configuration-2016-11.md)。 有关如何设计 ER 格式以生成 OpenXML 格式的报表的信息，请参阅 [ER 设计以 OPENXML 格式生成报表的配置（2016 年 11 月）](tasks/er-design-reports-openxml-2016-11.md)。

## <a name="configure-print-management"></a>配置打印管理
若要通过使用 ER 框架生成 FTI 表单，可以按照分配 SSRS 报表的相同方法分配 ER 格式。 若要将 ER 格式与所有应收帐款 FTI 关联，请转至 **应收帐款** \> **设置** \> **表单** \> **表单设置** \> **常规** \> **打印管理** \> **普通发票** \> **原件**。 若要将 ER 格式与特定客户或发票关联，请执行以下步骤。

1. 转至 **应收帐款** \> **发票** \> **所有普通发票**。
2. 选择 ER 格式要关联的 FTI，然后打开 **打印管理设置** 页面。
3. 选择文档级别以指定要处理的发票范围。
4. 为指定的文档级别选择 ER 格式。

![打印管理设置](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> 所选格式的 **报表格式查找** 字段中仅显示 **CustomersInvoicing** 数据模型的 **FreeTextInvoice** 根描述符。

## <a name="generate-fti-forms"></a>生成 FTI 表单
FTI 表单在 ER 框架中按照生成 SSRS 报表的相同方法生成。

若要生成 FTI 表单，可以根据范围或根据选择来选择发票。 

![发票选择](media/FTIbyGER-InvoiceSelection.png)

![发票预览](media/FTIbyGER-InvoiceExcelPreview.png)

按照这种方式使用 ER 格式打印 FTI 表单时，将使用默认 ER 文件目标。 不能更改该目标。 有关如何为 ER 格式配置 ER 目标的详细信息，请参阅[电子申报 (ER) 目标](electronic-reporting-destinations.md)。

也可以在发布 FTI 时生成 FTI 表单，方法是开启 **打印发票** 并关闭 **使用打印管理目标**。

> [!NOTE]
> 按照这种方式使用 ER 格式打印 FTI 表单时，将使用默认 ER 文件目标。 如果已经配置了默认目标，则可在运行时更改该目标。 若要更改目标，必须具有以下安全权限：
>
> - **名称：** ERFormatDestinationRuntimeMaintain
> - **标签：** 在运行时维护电子报告格式目标

![电子报告目标](media/FTIbyGER-ERFileDestinationSetting.png)

![电子申报格式目标](media/FTIbyGER-ERFileDestinationUsage.png)

ER 框架当前支持生成的文档采用以下目标：

- **下载的文件** – 生成的表单以可通过使用浏览器保存的下载的形式提供。
- **屏幕** – Microsoft 365 Excel 用于预览生成的 Excel 格式的 FTI 表单。
- **SharePoint 文件夹** – 生成的表单基于文档管理框架的设置存储。
- **应用程序存档** – 生成的表单作为执行日志记录的附件存储在 Microsoft Azure 存储中。
- **电子邮件** – 生成的表单作为电子邮件附件发送。

> [!NOTE]
> 不能将生成的 FTI 表单直接发送到打印机，因为现在不支持直接打印使用动态打印机路由代理。

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>下载示例 ER 配置以生成可打印 FTI 表单
可下载示例 ER 配置以用作 FTI 解决方案的模板。 配置存储在 Microsoft Dynamics Lifecycle Services (LCS) 中的共用资产库内。 配置包含：

- **客户开票模型** 配置中包含所需数据模型和模型映射。
- **客户 FTI 报表 (GER)** 配置中包含示例格式。

> [!NOTE]
> 已将这些配置创建为示例来帮助阐明可能的方案。 这些配置的未来取决于此项评估的结果和收到的反馈。

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>以示例 ER 格式实施的功能
在示例 ER 格式配置中，Excel 文件用作模板来生成 FTI 表单。

![格式设计器](media/FTIbyGER-ERFormat.png)

现在，此示例 ER 格式支持以下功能以生成 FTI 表单：

- FTI 表单同时针对已过帐的原始发票和尚未过帐的原始发票生成。 不支持经过更正的发票和贷方通知单。
- FTI 表单以发票语言生成。 生成的表单中的值和日期的格式基于用户的客户端区域设置。
- 如果处理的发票中没有行，则生成的发票显示数据不可用通知。
- 生成的发票头基于 **应收帐款参数** 页面上为 FTI 表单选择的纸张格式。 仅当纸张格式为空白时，生成的发票表单的标题中才显示公司详细信息。
- 在 **应收帐款参数** 页中为 FTI 表单选择了相应选项之后，生成的发票表单显示公司和客户免税编号。
- 生成的发票行和发票总计部分以发票登记币种显示默认发票的货币详细信息。
- 如果在 **应收帐款参数** 页面中启用了 **打印用欧元币种表示的金额** 选项，生成的发票总计部分可以以欧元币种和发票登记币种显示货币详细信息。
- 生成的发票表单基于 **应收帐款参数** 页面中的设置显示任何可用处理发票通知注释。 整个发票和每个发票行都包含注释。
- 如果已在 AR 表单注释列表中配置了客户 FTI 表单和处理发票语言，则生成的发票表单中将包含这两项的注释。
- 如果针对发票语言、ER 格式和 FTI 文档范围配置了自定义页脚文本，则生成的发票表单中将包含这些文本，具体取决于打印管理设置。
- 生成的发票表单的总计部分中包含所有可用现金折扣信息。
- 生成的发票表单的付款计划部分中包含所有可用付款计划详细信息。
- 生成的发票表单的加价部分中包含所有可用费用交易记录。
- 生成的发票表单中包含基于 **应收帐款参数** 页面上的 **销售税说明** 设置的销售税详细信息。 此部分只能以发票登记币种或同时以发票登记币种和公司记帐币种显示税务详细信息。
- 生成的发票表单显示直接借记通知详细信息。 例如，显示具有直接借记授权单 ID 的付款方式是何时为发票选择的，处理发票何时以欧元币种登记的，以及直接借记授权单 ID 是何时为发票定义的。
- 生成的发票显示已过帐发票的所有可用预付款详细信息。
- 可将生成的发票表单作为电子邮件附件发送给发票客户。 应该为所用 ER 格式配置相应 ER 文件目标。

### <a name="countryregion-specific-features"></a>国家/地区特定的功能 
示例 ER 格式中包含以下国家/地区特定的功能，用于显示可以在 ER 配置中如何处理特定要求。

#### <a name="norway"></a>挪威
为以下面的方式配置的法人处理发票时，将在生成的发票表单的标题中放入企业登记条款：

- 将使用挪威的国家/地区上下文。
- **打印 Foretaksregisteret** 参数在销售单据上处于活动状态。

#### <a name="spain"></a>西班牙
为以下面的方式配置的法人处理发票时，将在生成的发票表单的标题中放入 **现金会计方法的特别体制** 条款：

- 将使用西班牙的国家/地区上下文。
- 已在发票处理日期上启用了现金会计方法的特别体制。

如果有现金折扣详细信息（如现金折扣金额和发票行净额）,在为以下面的方式配置的法人处理这些详细信息时，生成的发票表单的发票总计部分中将包含这些详细信息：

- 将使用西班牙的国家/地区上下文。
- 发票选项（**总帐参数** \> **销售税** 部分）中已开启了 **发票中含现金折扣**。

#### <a name="italy"></a>意大利
为使用意大利的国家/地区上下文配置的法人处理生成的发票时，该发票的发票行中将包含货物折扣标记。

#### <a name="finland"></a>芬兰
除了生成的发票表单，还可以生成银行转帐单，如下所示：

- 为使用芬兰的国家/地区上下文，并且至少有一个银行帐户标记为 **转帐帐户** 和 **银行条码** 的法人。 
- 为标记为 **芬兰的** 关联付款附件所需的发票。

![转帐单](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> 示例 ER 格式已配置为可选择在单独的工作表中生成银行转帐单。

> [!NOTE]
> 必须首先在将用于预览 Excel 格式的所生成发票表单的本地机器上安装用于生成条形码的字体。

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>使用示例 ER 格式配置电子邮件目标
可使用示例 ER 格式的以下元素配置电子邮件目标：

- 可通过以下 ER 表达式访问客户联系人的电子邮件地址：**model.InvoiceBase.Contact.ElectronicMail**。
- 可通过以下 ER 表达式访问电子邮件主题文本：**Emailing.TxtToUse.Subject**。
- 可通过以下 ER 表达式访问电子邮件正文文本：**Emailing.TxtToUse.Body**。

![目标设置](media/FTIbyGER-ERFileDestinationSettingEmail.png)

电子邮件的主题和正文的默认文本以示例 ER 格式定义。 语言取决于格式的标签。 如果尚未添加已预定义了 **ERFTITMP** ID 的自定义组织电子邮件模板，将把这些默认文本用于电子邮件。

> [!NOTE]
> 已在示例 ER 格式中定义了 **ERFTITMP** 电子邮件模板 ID。 可在从该示例格式创建的新 ER 格式中根据需要更改该 ID。

如果已为您要处理其发票的法人添加了具有预定义的 **ERFTITMP** ID 的组织电子邮件模板，将把电子邮件主题和正文的模板用于生成电子邮件。 

![组织电子邮件模板](media/FTIbyGER-EmailTemplate.png)

![上载电子邮件模板](media/FTIbyGER-EmailTemplateBody.png)

将配置示例 ER 格式的 **Emailing.TxtToUse.Subject** ER 表达式，以便通过处理发票 ID 替换出现的所有占位符 %1。

将为占位符的以下替代项配置示例格式的 **Emailing.TxtToUse.Body** 表达式：

- 将把“%1”替换为客户的联系人的姓名。
- 将把“%2”替换为公司名称。
- 将把“%3”替换为客户名称。
- 将把“%4”替换为公司的联系人的姓名。
- 将把“%5”替换为公司的联系人的职称。
- 将把“%6”替换为公司的联系人的电子邮件地址。

![电子邮件地址](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>其他资源
[电子申报 (ER) 概览](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]