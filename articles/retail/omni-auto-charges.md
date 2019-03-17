---
title: 全渠道高级自动费用
description: 此主题描述使用高级自动费用功能管理零售渠道订单的额外订单费用的功能。
author: hhaines
manager: annbe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10
ms.openlocfilehash: a980ae9571fb47522d3966dc172b2343641b827e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "345551"
---
# <a name="omni-channel-advanced-auto-charges"></a>全渠道高级自动费用

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

此主题提供有关 Dynamics 365 for Retail 版本 10.0 中提供的高级自动费用功能的配置与部署的信息。

在高级自动费用功能启用时，在任何支持的零售渠道（销售点 (POS)、呼叫中心和在线）中创建的订单均可以利用在 ERP 应用程序中为标题和行级别相关费用中定义的[自动费用](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)配置。  

在 Dynamics 365 for Retail 版本 10.0 之前的版本中，[自动费用](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/configure-call-center-delivery#define-charges-for-delivery-services)配只能由在电子商务和呼叫中心渠道创建的订单访问。 在版本 10.0 及以后版本中，POS 创建的订单可以利用自动费用配置。 这样，额外的杂项费用可以系统化地添加到销售交易记录中。

在使用版本 10.0 以前的版本时，将提示 POS 用户在创建“全部装运”或“装运所选产品”POS 交易记录期间手动输入装运费用。 当应用程序的杂项费用功能用于与费用如何写入到订单的相关情况时，将不提供系统计算--计算依赖于用户的输入来确定费用值。 费用只能添加为一个“装运”相关费用代码，且不能在创建后在 POS 中轻松编辑或更改。 

使用手动提示添加装运费用在版本 10.0 及以后版本中仍然可用。 如果组织不启用**高级自动费用**参数，手动输入费用的 POS 提示将保持相同。

使用高级自动费用功能，POS 用户可以根据自动费用设置表系统化地计算所有定义的杂项费用。 而且，用户将能够在标题或行级别的任何 POS 销售交易记录中添加或编辑无限制的额外费用金额（对于现金和结转或客户订单）。

## <a name="enabling-advanced-auto-charges"></a>启用高级自动费用

在**零售 \> 总部设置 \> 参数 \> 零售参数**页，转到**客户订单**选项卡。在**费用**快速选项卡上，将**使用高级自动费用**设置为**是**。

![高级自动费用参数](media/advancedchargesparameter.png)

在高级自动费用启用时，用户在创建全部装运或装运所选产品客户订单时将被更长时间地提示在 POS 终端手动输入费用。 POS 订单费用被系统化地计算并添加到 POS 交易记录（如果找到与正在创建的订单的条件匹配的对应的自动费用表）。 用户还可以通过可以添加到 POS 屏幕布局的新添加的 POS 操作手动添加或维护标题或行级别费用。  

在高级自动费用启用时，不再使用**装运费用代码**和**退回装运费用**的现有**零售参数**。 仅当**使用高级自动费用**参数设置为**否**时这些参数才适用。

在启用此功能前，请确保您已测试并对员工进行了培训，因为这将更改装运或其他费用如何计算并添加到 POS 销售订单的业务流程。 确保您了解此流程对从 POS 创建交易记录的影响。 对于呼叫中心和电子商务订单，启用高级自动费用的影响是最小的。 在与计算额外订单费用的自动费用表相关的行为方面，呼叫中心和电子商务应用程序将继续具有以前所有的相同行为。 呼叫中心渠道用户将继续能够手动编辑标题或行级别的所有系统计算出的自动费用，或者在标题或行级别手动添加额外杂项费用。

## <a name="additional-pos-operations"></a>其他 POS 操作

为使高级自动费用能够在您的 POS 应用程序环境中正常工作，新 POS 操作已添加。 在部署高级自动费用时，这些操作必须添加到 [POS 屏幕布局](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts)并部署到 POS 设备。 如果这些操作未添加，用户将无法在 POS 交易记录中管理或维护杂项费用，且没有办法调整或更改基于自动费用配置系统化计算的费用值。 至少，建议您将**管理费用**操作部署到您的 POS 布局。

新操作如下所示。

- **142 - 管理费用** - 使用此操作允许 POS 用户查看和编辑通过自动费用计算手动或系统添加的 POS 交易记录的杂项费用。
- **141 - 添加标题费用** - 使用此操作为用户提供将标题级别杂项费用手动添加到任何 POS 销售交易记录的能力（以及选择要使用的费用代码）。
- **140 - 添加行费用** - 使用此操作为用户提供将行级别杂项费用手动添加到任何 POS 销售交易记录行的能力（以及选择要使用的费用代码）。
- **143 - 重新计算费用** - 使用此操作执行销售交易记录费用的完全重新计算。 先前用户覆盖的任何自动费用都将根据当前的配置重新计算。  

与 POS 操作一样，可以进行安全配置来需要经理审批才能执行操作。

## <a name="use-case-examples"></a>用例示例
在此部分，将呈现示例用例以帮助您了解零售渠道订单上下文内自动费用和杂项费用的配置和使用。 这些示例说明在启用了**使用高级自动费用**参数时应用程序的行为。

### <a name="auto-charges-header-charges-example"></a>自动费用标题费用示例
#### <a name="use-case-scenario"></a>用例场景  

零售商要在需要向客户装运产品的任何零售渠道中创建交易记录时自动添加运费。  零售商提供 2 种交货方式：陆运和空运。 如果客户选择陆运，并且订单值少于 100 美元，零售商希望向客户收取 10.00 美元运费。 如果订单值超过 100 美元，并且客户选择陆运，客户将不会被收取任何额外的运费。  如果客户为所有订单选择空运交货方式，不论订单总值是多少，其将被收取运费 20.00 美元。

#### <a name="setup-and-configuration"></a>设置和配置

此场景需要配置两个自动费用表。   

转到**应收帐款 \> 费用设置 \> 自动费用**。  

配置两个不同的标题级别自动费用。 一个为“陆运模式”交货配置，一个为“空运模式”交货配置。 对于此场景，请配置它们以用于“所有客户”。  

对于陆运费用，在**自动费用**页的行部分，将 0.01 美元到 100 美元之间的订单要应用的费用定义为 10.00 美元。 创建另一个费用行来指示超过 100.01 美元的订单没有费用。

![自动费用示例](media/headerchargesexample.png)

对于空运费用，在自动费用窗体的行部分，定义将应用于所有订单（值为 0.01 美元到 9,999,999 美元）的 20.00 美元费用。

将更改发送到 Retail Server/通道 DB，以便 POS 可以通过运行 **1040 配送计划**作业使用它们。

#### <a name="sales-processing-for-this-scenario"></a>此场景的销售处理

在上述配置步骤已完成，并且更改已应用到通道数据库后，在标题级别设置了陆运或空运方式的在 POS、呼叫中心或电子商务渠道创建的任何客户订单或销售交易记录都将使用这些费用并自动将它们应用到销售中。   

此时，费用将应用于在利用这些交货方式的法人内创建的所有销售交易记录，因为没有指定自动费用配置将只应用于特定销售渠道的功能。

对于 POS 和电子商务场景，因为未在这些订单中明晰定义“标题”，仅当交易记录中的所有销售行均被设置为使用完全相同的交货方式装运时才应用标题级别费用。 如果 POS 或电子商务创建的交易记录中存在“混合模式”履行，将仅考虑并应用行级别自动费用。

在呼叫中心场景中，用户控制订单标题的交货方式的设置，因此标题级别费用将为这些订单应用，即使某些销售订已配置为使用不同的交货方式。 呼叫中心订单的标题级别费用将始终基于在销售订单的订单标题级别定义的交货方式。

### <a name="auto-charges-line-charges-example"></a>自动费用行费用示例
#### <a name="use-case-scenario"></a>用例场景 
零售商想要在客户购买特定计算机型号时将额外费用添加到客户以收取设置费用。 此计算机需要零售商将为客户执行的额外的非可选设置操作。 零售商已通知客户将存在此设置的额外费用。 出于财务申报目的，零售商希望将与此费用相关的费用与产品销售价分开单独管理。 当此特定计算机在任何零售渠道购买时，客户将被收取 19.99 美元的设置费用。

#### <a name="setup-and-configuration"></a>设置和配置

此场景需要配置一个行级别自动费用表。

转到**应收帐款 \> 费用设置 \> 自动费用**。  

将**级别**下拉菜单设置为**行**，然后为要收取设置费用的特定产品或产品组的所有客户创建新的自动费用记录。

![自动费用示例](media/linechargesexample.png)

将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 **1040 配送计划**作业使用它们。

#### <a name="sales-processing-for-this-scenario"></a>此场景的销售处理

在上述配置步骤已完成，并且更改已应用到通道数据库后，在订单中有此项目的在 POS、呼叫中心或电子商务渠道创建的任何客户订单或销售交易记录都将触发将系统地添加到订单合计的行级别费用。   

此时，费用将应用于与法人内的行级别自动费用配置匹配的任何销售行，因为没有将行级别自动费用配置为只应用于特定销售渠道的功能。

### <a name="manual-header-charges-example"></a>手动标题费用示例
#### <a name="use-case-scenario-description"></a>用例场景描述
零售商通过向在商店内订购产品的客户提供特殊的产品家庭交货方式，为典型流程设置了例外。 零售商和客户已同意客户将为此服务支付额外 25 美元的手续费。 订单接受者需要将此额外费用添加到交易记录中。 由于此费用是总费用且与订单上的任何一个产品都无关，将使用标题费用。

#### <a name="setup-and-configuration"></a>设置和配置

确保将此场景中使用的费用代码已正确配置，方法是转到**应收帐款 \> 费用设置 \> 费用**为此场景定义适当的费用代码。

![费用示例](media/chargesexample.png)

如果由于装运相关的折扣或促销目的，费用应被视作“装运”相关费用，应将费用代码中的**装运费用**设置为**是**。 如果在处理 POS 应用程序中的退货交易期间，此费用也被允许系统地退还，应将**可退还**设置为**是**。 **可退还**标志仅在**使用高级自动费用**参数设置为**是**时适用。   

将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 **1040 配送计划**作业使用它们。

**添加标题费用**操作必须在您的 [POS 屏幕布局](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts)中配置，以使用户可从 POS 访问的按钮可以调用此操作（操作 141）。  屏幕布局的更改也必须通过分配计划功能分配到零售渠道。 

#### <a name="sales-processing-of-manual-header-charges"></a>手动标题费用的销售处理

若要在 POS 应用程序中执行此方案，POS 用户将照常创建销售交易记录，并将产品和所有其他配置添加到销售中。 在收取付款前，用户应执行**添加标题费用**操作，这将提示用户选择费用代码并输入费用值。 在用户完成流程后，此费用将作为标题级别费用添加到销售订单。  

此流程可以通过使用工具栏上的**销售**选项卡中的现有**费用**功能在呼叫中心应用。 在**维护费用**页，用户可以将新费用行添加到订单头中。

### <a name="manual-line-charges-example"></a>手动行费用示例
#### <a name="use-case-scenario"></a>用例场景
客户请求将其销售订单中的 2 件商品（共 5 件）包装成礼品。 零售商提供此可选服务的费用为每件商品 2.00 美元。 订单接受者需要将这些费用添加到需要礼品包装的特定商品。

#### <a name="setup-and-configuration"></a>设置和配置

确保将此场景中使用的费用代码已正确配置，方法是转到**应收帐款 \> 费用设置 \> 费用**为此场景定义适当的费用代码。

如果由于装运相关的折扣或促销目的，费用应被视作“装运”相关费用，应将费用代码中的**装运费用**设置为**是**。 如果在处理 POS 应用程序中的退货交易期间，该费用也被允许系统地退还，应将**可退还**设置为**是**。 **可退还**标志仅在**使用高级自动费用**参数设置为**是**时适用。  

将费用发送到 Retail Server/通道 DB，以便 POS 可以通过运行 **1040 配送计划**作业使用它们。

**添加行费用**操作必须在您的 [POS 屏幕布局](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts)中配置，以使用户可从 POS 访问的按钮可以调用此操作（操作 140）。  屏幕布局的更改也必须通过分配计划功能分配到零售渠道。 

#### <a name="sales-processing-of-the-manual-line-charge"></a>手动行费用的销售处理

若要在 POS 应用程序中执行此方案，POS 用户将照常创建销售交易记录，并将产品和所有其他配置添加到销售中。 在收取付款前，用户应选择将从 POS 物料列表显示应用费用的特定行，并执行**添加行费用**操作。 系统将提示用户选择费用代码并输入费用值。 在用户完成流程后，此费用将被链接到行并作为行级别费用添加到订单合计。 如果需要，用户可以重复此流程，将其他行费用添加到交易记录中的其他物料行。

同一流程可以通过使用**销售订单**页上**销售订单行**部分的**财务**下拉菜单下的“维护费用”功能在呼叫中心应用。  这将打开**维护费用**页，用户在其中可以将新行的特定费用添加到交易记录中。

## <a name="additional-features"></a>附加功能

### <a name="editing-charges-on-a-pos-sales-transaction"></a>编辑 POS 销售交易记录中的费用

**管理费用**操作 (142) 应该添加到 [POS 屏幕布局](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-screen-layouts)，以便用户可以查看和编辑或覆盖任何系统计算或手动计算的标题或行级别费用。 如果未添加此操作，用户将无法调整 POS 交易记录中的费用值，也不能查看费用的详细信息，如与费用关联的费用代码的类型。  

在 POS 中的**管理费用**页，用户可以查看标题和行级别费用详细信息。 用户可以使用此页提供的**编辑**功能对计费到特定费用行的金额进行更改。 在费用行被手动覆盖后，它将不会被系统地重新计算，除非用户发起**重新计算费用**操作。

如果已在**零售参数**设置页面配置了**费用覆盖原因代码**，当费用已在 POS 应用程序中修改时，用户将被提示提供原因代码。

如果已为覆盖的费用捕获了原因代码，还将提供新报表来查看和审核这些覆盖。 此报表可以在**零售 \> 查询和报表 \> 费用覆盖历史记录**中找到。

### <a name="refunding-charges-on-a-pos-return-transaction"></a>退还 POS 退货交易记录中的费用

如果**使用高级自动费用**参数设置为**是**，**退回装运费用**的现有零售参数不再适用。 若要指示哪些费用应在使用高级自动费用时系统地退还给客户，请确保相关费用代码已在**费用代码**设置页面配置为**可退还**。 请确保设置已通过分配计划处理同步到您的零售渠道数据库。

### <a name="refunding-charges-on-a-return-order-transaction"></a>退还退货单交易记录中的费用

费用不会系统地退还到在 Retail 中创建的**退货单**。 在创建**退货单**时，用户需要选择**复制费用**选项。 如果没有选择**复制费用**，原始销售交易记录中的费用将不自动退还。 如果选择**复制费用**，所有费用将被复制到退货单，并且用户可以手动编辑或删除他们不希望退还的任何费用。 呼叫中心退货单流程目前不认可**费用代码**设置中的**可退还**标志。

### <a name="configuring-pos-receipts-to-show-charges"></a>配置 POS 收据以显示费用

以下收据元素已添加到收据行和页脚以支持高级自动费用功能。

- **订单行装运费用** - 此行级别元素可用于概括已应用到销售订单行的特定费用代码。 仅在**费用代码**页标记为**装运**费用的费用代码将在此处显示。

- **订单行其他费用** - 此行级别元素可用于概括已应用到销售订单行的任何非装运特定费用代码。 这些是**费用代码**页上的**装运**标志未启用的费用代码。

- **订单装运费用详细信息** - 此页脚级别元素显示应用到在**费用代码**设置页面上标记为**装运**费用的订单的费用代码的描述。

- **订单装运费用** - 此页脚级别元素显示装运相关费用的美元金额。

- **订单其他费用详细信息** - 此页脚级别元素显示应用到未标记为装运相关费用的订单的费用代码的描述。

- **订单其他费用** - 此页脚级别元素显示与装运无关的其他费用的美元金额。

建议组织也将自由文本字段添加到收据页脚，以便定义将概括费用的区域。 

### <a name="preventing-charges-from-being-calculated-until-the-pos-order-is-completed"></a>防止费用在完成 POS 订单前计算

某些组织可能更愿意等待用户将所有销售订单行都添加到 POS 交易记录后再计算费用。 若要防止在物料添加到 POS 交易记录时计算费用，在商店使用的**功能配置文件**中打开**手动费用计算**参数。 启用此参数将需要 POS 用户在完成向 POS 交易记录添加产品时使用**计算合计**操作。 **计算合计**操作然后将触发计算订单头或行的任何自动费用（如果适用）。