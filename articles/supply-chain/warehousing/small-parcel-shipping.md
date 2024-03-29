---
title: 小型包裹装运
description: 本文提供有关小型包裹装运 (SPS) 功能的信息。 此功能让 Microsoft Dynamics 365 Supply Chain Management 可以将有关已装箱集装箱的详细信息提交给承运人，然后从该承运人处接收发货标签、装运费用和跟踪号。
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b2adde2b81ed881a3c81193a2220fbe569069c7c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336146"
---
# <a name="small-parcel-shipping"></a>小型包裹装运

[!include [banner](../../includes/banner.md)]

小型包裹装运 (SPS) 功能提供通过承运人 API 进行通信的框架，以此让 Microsoft Dynamics 365 Supply Chain Management 可以直接与装运承运人交互。 当您通过商业装运承运人装运各个销售订单，而不是使用集装箱装运或零担 (LTL) 装运时，此功能很有用。

SPS 功能通过专用的 *费率引擎* 与您的装运承运人交互。 您的组织必须与您的承运人或承运人中心服务合作开发此费率引擎。 费率引擎让 Supply Chain Management 可以将有关已装箱集装箱的详细信息提交给您的承运人，然后从该承运人处接收发货标签、装运费用和跟踪号。

返回的装运费用作为杂项费用添加到关联的销售订单中。 然后，可以使用 Zebra 编程语言 (ZPL) 打印机自动打印返回的发货标签，在装运时使用。 承运人在您的仓库领取包裹时会扫描此发货标签。

## <a name="prepare-your-system-to-support-sps"></a>准备系统以支持 SPS

您必须先在“功能管理”中打开 SPS 功能，添加费率引擎，并设置 **运输管理** 和 **仓库管理** 模块以支持它，然后才能够开始使用 SPS 功能。

### <a name="turn-the-sps-feature-on-or-off"></a>打开或关闭 SPS 功能

要使用此功能，必须为您的系统打开它。 从 Supply Chain Management 版本 10.0.29 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.29，管理员可以通过在 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *小型包裹装运* 功能来打开或关闭此功能。

### <a name="deploy-and-set-up-rate-engines"></a>部署和设置费率引擎

Supply Chain Management 不包括任何费率引擎。 您必须获取或创建所需的任何费率引擎，然后将它们添加到系统中。 不过，Microsoft 提供了可用于测试的演示费率引擎。

#### <a name="download-and-deploy-the-demo-rate-engine"></a>下载和部署演示费率引擎

请按照以下步骤获取演示费率引擎。

1. 在 GitHub 上，下载[演示费率引擎的动态链接库 (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS)。
1. 在您的 Supply Chain Management 服务器上，将 DLL 保存在 **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** 文件夹中。

#### <a name="create-and-deploy-functional-rate-engines"></a>创建和部署功能费率引擎

有关如何创建和部署功能费率引擎以可以在生产或测试环境中使用的信息，请参阅以下文章：

- [创建新的运输管理引擎](../transportation/create-new-transportation-management-engine.md)
- [设置运输管理引擎](/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

有关如何创建 SPS 费率引擎的详细信息，请参阅以下博客文章：[小型包裹装运：如何利用 Microsoft Dynamics 365 中的小型包裹装运功能](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5)。

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a>在 Supply Chain Management 中设置费率引擎

为 SPS 创建和部署费率引擎后，请按照以下步骤进行设置。

1. 转到 **运输管理 \> 设置 \> 引擎 \> 费率引擎**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。
1. 在新行中，设置以下字段：

    - **费率引擎** – 为费率引擎输入唯一名称。 如果您使用的是演示费率引擎，请输入 *演示费率引擎*。
    - **名称** – 输入费率引擎的简短描述。 如果您使用的是演示费率引擎，请输入 *演示费率引擎*。
    - **评级元数据 ID** – 选择应该用于计算费率的依据。 例如，您的费率可能根据距离来计算。 如果您使用的是演示费率引擎，可以将此字段留空。
    - **引擎程序集** – 输入您部署的 DLL 包的文件名。 如果您使用的是演示费率引擎，请输入 *TMSSmallParcelShippingEngine.dll*。
    - **引擎类** – 输入为您的费率引擎确定的类名称。 如果您使用的是演示费率引擎，请输入 *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*。

## <a name="example-scenario"></a>示例场景

此示例场景演示了在准备好系统后如何设置和使用 SPS，如本文前面所述。 此场景使用前面提到的演示费率引擎。

### <a name="make-demo-data-available"></a>提供演示数据

若要使用此处指定的演示记录和值完成此场景，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/fin-ops/get-started/demo-data.md)。 此外，开始前，还必须选择 **USMF** 法人。

### <a name="set-up-the-scenario"></a>设置场景

对于此示例场景，您必须有演示承运人、承运人组、装箱策略和装箱模板。 以下小节说明如何准备场景所需的记录。 在生产场景中，设置流程通常类似于此处描述的流程。 但是，您将设置不同的值。

#### <a name="set-up-carriers"></a>设置承运人

请按照以下步骤设置承运人。

1. 转到 **运输管理 \> 设置 \> 承运人 \> 装运承运人**。
1. 在操作窗格中，选择 **新建** 添加承运人。
1. 在标题中，设置以下值：

    - **装运承运人**：*演示承运人*
    - **名称**：*演示承运人*
    - **模式**：*陆运*

1. 在 **概览** 快速选项卡上，设置以下值：

    - **启用装运承运人**：*是*
    - **启用承运人评级**：*是*

1. 在 **服务** 快速选项卡上，选择 **新建** 向网格添加服务。
1. 为新服务设置以下值：

    - **承运人服务**：*演示承运人服务*
    - **名称**：*演示承运人服务*
    - **运输方式**：*陆运*

    根据需要为所有其他字段输入任意值。 （当您保存新的装运承运人记录时，将创建新的交货模式，**交货方式** 字段将自动设置。）

1. 在 **评级模板** 快速选项卡上，选择 **新建** 将评级模板添加到网格。
1. 为新模板设置以下值：

    - **评级模板**：*演示承运人服务*
    - **名称**：*演示承运人服务*
    - **费率引擎**：*演示费率引擎*

    根据需要为所有其他字段输入任意值。

1. 在操作窗格上，选择 **保存**。

有关如何设置承运人的详细信息，请参阅[设置装运承运人](../transportation/tasks/set-up-shipping-carriers.md)。

#### <a name="set-up-carrier-service-accounts"></a>设置承运人服务帐户

请按照以下步骤设置承运人服务帐户。

1. 转到 **运输管理 \> 设置 \> 评级 \> 承运人服务帐户**。
1. 在操作窗格上，选择 **新建** 添加承运人服务帐户。
1. 为新帐户设置以下值：

    - **装运承运人**：*演示承运人*
    - **承运人服务**：*演示承运人服务*
    - **承运人客户帐号：** 用于对与装运承运人的连接进行验证和身份验证的承运人客户帐号。 您的承运人会提供此值。 如果您使用的是演示服务，可以输入任意值。
    - **站点**：*6*
    - **仓库**：*62*

    > [!NOTE]
    > 通常，**承运人客户帐号** 值是对连接进行身份验证所需的唯一值。 但是，如果承运人需要其他身份验证参数，您的组织应自定义此页面来适当添加其他字段。

#### <a name="set-up-a-container-packing-policy"></a>设置集装箱装箱策略

请按照以下步骤设置集装箱装箱策略。

1. 如果尚未设置 ZPL 打印机定义，请使用文档路线选择代理应用程序进行设置。 有关详细信息，请参阅[文档打印概述](../../fin-ops-core/dev-itpro/analytics/print-documents.md)及相关文章。
1. 转到 **仓库管理 \> 设置 \> 集装箱 \> 集装箱装箱策略**。
1. 在操作窗格上，选择 **新建** 添加集装箱装箱策略。
1. 在新策略的标题中，设置以下值：

    - **集装箱装箱策略**：*演示装箱策略*
    - **描述：** 策略的描述

1. 在 **概览** 快速选项卡上，设置以下值：

    - **仓库**：*62*
    - **最终装运的默认位置**：*货架门*
    - **重量单位**：*千克*
    - **集装箱封闭策略**：*自动发放*
    - **集装箱发放策略**：*发往最终装运位置*

1. 在 **集装箱清单** 快速选项卡上，设置以下值：

    - **容器关闭时自动显示清单**：*是*
    - **集装箱的清单要求**：*运输管理*
    - **打印集装箱内容**：*否*

1. 在 **承运人标签打印** 快速选项卡上，设置以下值：

    - **打印集装箱发货标签**：*始终*
    - **打印机名称：** 应打印发货标签的 ZPL 打印机的名称

#### <a name="set-up-a-packing-profile"></a>设置装箱模板

请按照以下步骤设置装箱模板。

1. 转到 **仓库管理 \> 设置 \> 装箱 \> 装箱模板**。
1. 在操作窗格上，选择 **新建** 向网格添加装箱模板。
1. 为新模板设置以下值：

    - **装箱模板 ID**：*演示装箱模板*
    - **描述：** 模板的描述
    - **集装箱装箱策略**：*演示装箱策略*
    - **集装箱 ID 模式**：*自动*
    - **集装箱类型**：*小箱*

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a>将客户设置为使用 SPS 承运人

请按照以下步骤设置客户，让客户可以使用您创建的承运人。

1. 转到 **应收帐款 \> 客户 \> 所有客户**。
1. 在网格中，找到并选择客户 *US-027*。
1. 在操作窗格的 **常规** 选项卡上，在 **设置** 组中，选择 **承运人客户帐户**。
1. 在 **承运人客户帐户** 页上的操作窗格上，选择 **新建** 向网格添加帐户。
1. 为新帐户设置以下值：

    - **装运承运人**：*演示承运人*
    - **承运人客户帐号**：*12345*（此值对于此场景不重要，但将在下一节中引用。）

### <a name="go-through-the-example-scenario"></a>完成示例场景

如上一节所述设置了所有示例数据之后，您就可以开始完成示例场景了。

#### <a name="create-a-sales-order-and-process-the-work"></a>创建销售订单与处理工作

请按照以下步骤创建销售订单。

1. 转到 **销售和营销 \> 销售订单 \> 所有销售订单**。
1. 选择 **新建** 以创建新的销售订单。
1. 在 **创建销售订单** 对话框中，将 **客户帐户** 字段设置为 *US-027*。
1. 选择 **确定** 创建销售订单，然后关闭对话框。
1. 将打开新销售订单。 在 **销售订单头** 快速选项卡上，将 **承运人客户帐号** 字段设置为您先前为此客户选择的值 (*12345*)。
1. 在 **销售订单行** 部分，添加一行，并为其设置以下值：

    - **物料编号：***A0002*
    - **数量：** *1*
    - **站点**：*6*
    - **仓库**：*62*

1. 切换到 **标题** 视图。
1. 在 **交货** 快速选项卡上，设置以下值：

    - **装运承运人**：*演示承运人*
    - **承运人服务**：*演示承运人服务*

1. 切换回 **行** 视图。 如果系统提示您更新销售行的交货方式，请选择 **是**。
1. 在 **销售订单行** 部分，选择您之前设置的订单行，然后选择 **库存 \> 预留**。
1. 在 **预留** 页中，选择 **预留批次** 在仓库中预留所选行的全部数量。
1. 关闭 **预留** 页回到销售订单。
1. 在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。

    将创建将物料从领料位置移到装箱工作站的工作。

1. 在 **销售订单行** 部分，选择 **仓库 \> 装运详细信息**。
1. 在 **装运详细信息** 页上，记下装运 ID。 在装箱工作站为装运装箱时，您将需要它。
1. 关闭 **装运详细信息** 页回到销售订单。
1. 记下销售订单编号，然后转到 **仓库管理 \> 工作 \> 所有工作**。
1. 使用销售订单编号查找并选择为订单创建的工作。
1. 在操作窗格上的 **工作** 选项卡中，选择 **完成工作**。
1. 在 **工作完成** 页上，在 **用户 ID** 字段中，选择一个用户 ID。 然后，在操作窗格中，选择 **验证工作**。
1. 如果工作通过验证，在操作窗格上选择 **完成工作**。

    工作将被标记为已完成，以模拟将物料移到装箱工作站。

#### <a name="pack-the-shipment"></a>装运装箱

请按照以下步骤为装运装箱。

1. 转到 **仓库管理 \> 设置 \> 工作人员**，确保您的用户帐户与用于仓库管理的工作人员帐户相关联。
1. 转到 **仓库管理 \> 领料和集装化 \> 装箱**。
1. 在 **选择装箱工作站** 对话框中，设置以下值：

    - **站点**：*6*
    - **仓库**：*62*
    - **位置**：*装箱*
    - **装箱模板 ID**：*演示装箱模板*

1. 选择 **确定**。
1. **装箱** 页将显示。 在生产场景中，工作人员将扫描牌照或装运 ID。 但是，对于此场景，请打开 **所有装运** 页，查找您刚才创建的装运的装运编号。 然后，在 **装箱** 页上的 **牌照或装运** 字段中输入此值。 或者，输入您之前记下的装运 ID。
1. 在“操作窗格”上，选择 **新建集装箱**。
1. 出现的对话框将显示有关新集装箱的详细信息。 保留默认值，然后选择 **确定**。
1. 在 **装箱** 页上的 **物料装箱** 快速选项卡上，在 **标识符** 字段中，选择 *A0002* 将该物料装箱。 物料将添加到集装箱中。
1. 在操作窗格上，选择 **装运集装箱**。

    出现的 **装运集装箱** 页上将有您刚才创建的集装箱的行。 但是，该行中的 **集装箱清单 ID** 字段当前为空白，因为您还未从承运人那里收到发货标签和跟踪号。

1. 在“操作窗格”上，选择 **封闭集装箱**。
1. 在 **封闭集装箱** 对话框中，将 **毛重** 字段设置为 *1 千克*，然后选择 **确定**。

    发货标签现在应该已经在您先前选择的 ZPL 打印机上打印。 标签应类似于以下示例。

    ![示例发货标签。](media/sps-label-example.png "示例发货标签")

1. 注意 **集装箱清单 ID** 和 **总运费** 值已添加从承运人处收到的值。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]