---
title: 采购 cXML 增强功能
description: 采购 cXML 增强功能建立在现有的外部目录功能 PunchOut 的基础上，该功能用于采购申请。
author: dasani-madipalli
manager: tfehr
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: cd0435fd89050311ecd4f24400d5830cbcf8fdfd
ms.sourcegitcommit: b281ac04157f6ccbd159fc89f58910b430a3b6a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826917"
---
# <a name="purchasing-cxml-enhancements"></a>采购 cXML 增强功能

[!include [banner](../includes/banner.md)]

_采购 cXML 增强功能_建立在[现有的外部目录功能](set-up-external-catalog-for-punchout.md)的基础上，该功能用于采购申请。 此现有功能称为 _PunchOut_。 虽然采购订单不必一定要来自采购申请，但是采购订单上的供应商与用于发送采购订单单据的参数之间必须存在联系。

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>打开“采购 cXML 增强功能”

要打开此功能，请打开**[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 页，然后搜索名为*采购 cXML 增强功能*的功能。 选择此功能，然后然后选择**立即启用**将其打开。

启用功能后，应在以下三个区域配置设置：

- **[cXML 参数](#cxml-parameters)** – 使用这些设置为发送采购订单的功能设置一些全局参数。
- **[供应商设置](#vendor-setup)** – 如果默认情况下应为为任何供应商创建的所有新采购订单使用商业可扩展标记语言 (cXML)，请将该供应商的**通过 cXML 发送采购订单**选项设置为_是_。
- **[外部目录](#external-catalog-setup)** – 使用新**订单属性**设置定义采购订单单据的格式及其发送方式。

下图总结了此配置。

![用于设置 cXML 功能的区域](media/cxml-settings-areas.png "用于设置 cXML 功能的区域")

此外，您必须设置[采购订单请求批处理作业](#po-batch)。 此批处理作业用于发送已确认的采购订单。

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>设置全局 cXML 参数

使用 **cXML 参数**页进行一些将应用于发送采购订单的功能的全局设置。

![cXML 参数页](media/cxml-parameters.png "cXML 参数页")

转到**采购 \> 设置 \> cXML 管理 \> cXML 参数**，设置以下参数：

- **cXML 测试模式** – 此全局参数影响从批处理作业实际发送采购订单的方式。 选择以下值之一：

    - **测试** – 在此模式下，批处理作业可以运行，消息的 XML 文档将生成，但不发送。 而是保存在采购订单请求中以供审核。 在最初的实现中，如果想要查看数据在 cXML 消息中是如何输入的，此模式很有用。 您可能还希望生成示例消息，然后将其发送给供应商以进行初始验证。
    - **活动** – 在此模式下，此功能使用[外部目录设置](#external-catalog-setup)将每个单据实际传输给供应商。

- **发送采购请求更新** – 将此选项设置为*是*发送采购订单的更新消息。 设置为*否*阻止发送消息。 大多数供应商都不希望接收更新消息。 在采购订单应该更改时，他们需要客户通过电话或电子邮件与他们联系。 此参数是一个全局参数，不能在每个供应商的外部目录上指定替代。 如果您在采购订单上发布第二个确认，采购订单将被标记为已更新，但是第一个确认已被供应商发送并确认。 如果有第二个确认，但尚未发送第一个确认，第二个确认将被视为新单据。 在发送一个确认前，您可以根据需要多次确认采购订单。 接下来的确认将被视为更新消息。
- **发送采购请求删除** – 将此选项设置为*是*发送采购订单的删除消息。 设置为*否*阻止发送消息。 大多数供应商都不希望接收删除消息。 如果采购订单被错误发送，他们需要客户通过电话或电子邮件与他们联系。 此参数是一个全局参数，不能在每个供应商的外部目录上指定替代。 如果您在 Supply Chain Management 中取消了采购订单，该采购订单将被标记为已删除。
- **存档文件** – 指定用于导出和保存已存档的 cXML 文档的文件路径。 从**采购订单请求**页运行清除功能时，将使用此路径。
- **街道行的最大字符数** – 输入街道字段中可用于 cXML 文档中的地址的最大字符数。 除非在外部目录属性上指定了替代，否则此全局参数会影响所有供应商。

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>设置供应商采购订单以使用 cXML

每次您确认将**通过 cXML 发送采购订单**选项设置为_是_的采购订单时，系统都会自动生成 cXML 消息并将其传递给与该采购订单关联的供应商。 有两种方法可以控制采购订单的这个选项：

- 要设置供应商以自动将 cXML 用于从申请创建的所有新采购订单，请转到**采购 \> 供应商 \> 所有供应商**，然后选择或创建供应商打开其详细信息页面。 然后，在**采购订单默认值**快速选项卡上，将**通过 cXML 发送采购订单**选项设置为_是_。 如果 cXML 还应自动用于**不**是从申请创建的新采购订单，您还必须将相关外部目录的 **ENABLEMANUALPO** 订单属性设置为 _True_，如本主题后面的[设置订单属性](#set-order-properties)一节所述。
- 对于单个采购订单，请转到**采购 \> 采购订单 \> 所有采购订单**，选择或创建一个采购订单并打开其详细信息页面。 切换到**标题**视图，然后在**设置**快速选项卡上，根据需要设置**通过 cXML 发送采购订单**选项。

![供应商采购订单的默认设置](media/cxml-order-defaults.png "供应商采购订单的默认设置")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>设置外部目录以使用 cXML

在**外部目录**页上，对于每个目录，可以设置 PunchOut 功能和用于发送采购订单的功能。 要找到相关设置，请转到**采购 \> 目录 \> 外部目录**。 首先[照常设置每个目录](set-up-external-catalog-for-punchout.md)。 此过程包括分配供应商、选择允许供应商提供的类别和激活目录。 然后配置本节中所述的其他设置。

> [!NOTE]
> 当您确认可以通过 cXML 发送的采购订单时，系统会查找与该采购订单关联的供应商，然后找到与该供应商关联的第一个活动的外部目录。 然后，系统使用该外部目录中的设置发送采购订单。 如果设置了多个外部目录，系统会根据采购订单上的供应商仅使用找到的第一个外部目录。 因此，我们建议您只为每个供应商创建一个外部目录。

![外部目录设置](media/cxml-supplier-catalog.png "外部目录设置")

### <a name="set-the-punchout-protocol-type"></a>设置 PunchOut 协议类型

在**外部目录**页的**常规**快速选项卡上，将 **Punchout 协议类型**字段设置为 _cXML_。 除非合作伙伴扩展了功能并在扩展中提供了其他选项，否则此选项将是唯一可用的选项。

如果您还将目录用于 PunchOut，则还必须[设置消息格式](set-up-external-catalog-for-punchout.md)。 消息格式用于从申请建立与 PunchOut 交易中的供应商的连接。 发送采购订单时，订单属性将用于与供应商建立连接。

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>设置订单属性

_采购 cXML 增强功能_为外部目录添加了新的**订单属性**快速选项卡。 此快速选项卡提供了一个网格，您可以在其中定义订单属性。 它还提供了一个工具栏。 此工具栏包含以下三个按钮，可用于管理订单属性：

- **默认属性** – 设置新目录时，选择此按钮可将常用属性的预定义集合添加到网格。
- **新建** – 将新属性添加到网格。
- **删除** – 从网格中删除当前选定的属性。 如果您意外删除了默认属性，请选择**默认属性**恢复所有缺少的属性。

每次将一个或多个属性添加到网格时，请使用右列为每个属性指定一个值。

通过以下方式使用默认属性：

- **BUYER\_COOKIE** – 此跟踪字段可用于指示您的公司的特定信息。 除非您与供应商就如何使用此属性达成协议，否则在发送采购订单时它没有太多意义。 因此，应将其设置为一个简单值。
- **DELIVERTO** – 在采购订单的单据中输入装运地址后，**需引起注意的信息**字段用于设置 XML 消息中的 **DeliverTo** 字段。 如果您需要将此值用作申请者名称，并且将在采购订单标题上设置申请者字段，请为此属性输入值 _REQUESTER_，以使申请者名称输入到 XML 中的 **DeliverTo** 字段中。 在这种情况下，使用的主要电子邮件地址和电话号码将来自申请者而不是订货人。
- **DEPLOYMENTMODE** – 根据供应商的要求设置此属性。 值通常是 _PRODUCTION_ 或 _TEST_。 请根据您与供应商的沟通来设置值。 通常，它必须与供应商指示为测试或生产系统的 **ORDERCHECKURL** 值后面的预期系统相匹配。
- **FIXEDBILLADDRESSID** – 设置 XML 消息中的 **addressID** 字段时，它将选择地址中指定的位置。 如果由于某些原因您传达给供应商的 ID 值与地址位置中的值不同，您可以在此处指定值来强制替代。 假定您只对供应商使用一个地址，并且该地址是在供应商的系统中设置的。 账单地址是在 Supply Chain Management 中为法人指定的主要发票地址。
- **FIXEDSHIPADDRESSID** – 设置 XML 消息中的 **addressID** 字段时，它将选择地址中指定的位置。 如果由于某些原因您传达给供应商的 ID 值与地址位置中的值不同，您可以在此处指定值来强制替代。 假定您只对供应商使用一个地址，并且该地址是在供应商的系统中设置的。 装运地址是在采购订单的标题中指定的地址。 大多数供应商仅接受标题地址，不接受行地址。 虽然 XML 中有行地址字段，但它们将被设置为标题地址。
- **FROM\_DOMAIN** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **FROM\_IDENTITY** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **ORDERCHECKURL** – 输入要将采购订单单据发送到的 URL。 此 URL 以 `https://` 开头，由您的供应商提供。
- **PAYLOAD\_ID** – 根据当前供应商所采用的业务流程的要求，输入有效负载 ID 的前缀值。
- **SENDER\_DOMAIN** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **SENDER\_IDENTITY** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **SHARED\_SECRET** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **STREETLENGTH** – 输入表示供应商接受的街道名称最大字符数的数字。 如果在此处输入一个值，它将替代在 **cXML 参数**页指定的值。 系统将删除换行符和空格，以尝试使 Supply Chain Management 中的标准地址符合此处指定的字符数。 任何其他字符将被截断。
- **TO\_DOMAIN** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **TO\_IDENTITY** – 输入用于发送采购订单单据的值。 此值由您的供应商提供。
- **USERAGENT** – 输入一个值以标识您正在使用的系统。 例如，输入 _Dynamics 365 Supply Chain Management_。
- **VERSION** – 输入 cXML 版本号（如果供应商要求此信息）。 默认版本为 *1.2.008*。 此版本是固定的，多数供应商都接受。
- **RESPONSETEXT** – 输入您希望订单发送后供应商在 cXML 响应消息中返回的任何自定义文本。 这样，系统可以将消息标记为_已确认_。 如果响应与标准文本或您在此处输入的客户文本不匹配，请求将被标记为_错误_。
- **RESPONSETEXTSUB** – 如果要在供应商响应文本中搜索 **RESPONSETEXT** 字段中指定的值，请将此属性设置为 _TRUE_。 例如，供应商可能会在响应中返回包含“OK”的长字符串。 在这种情况下，您可以在 **RESPONSETEXT** 字段中输入 _OK_，并将 **RESPONSETESTSUB** 设置为 _TRUE_，以在响应中的任何位置搜索“OK”。 然后可以将订单设置为_已确认_。
- **CONTENTTYPE** – 在典型的目录设置中，无需设置此属性。 如果在发送采购订单时收到来自供应商系统的服务器 500 错误，可以通过将此属性设置为 _FALSE_ 来进行测试。 该值将更改 Web 请求中的设置，可能让消息可以在某些平台上发送。
- **ENABLEHEADERS** – 将此属性设置为 _TRUE_ 可以将标题与采购订单一起发送。 仅在供应商需要时才必须设置此属性。 如果将此属性设置为 _TRUE_，请添加基于供应商提供的名称的其他自定义属性，并在其前面加上 _H\__ 前缀。 典型示例包括 **H\_USERID**、**H\_PASSWORD**、**H\_RECEIVERID** 和 **H\_ACTIONREQUEST**。 默认属性中包括以下自定义属性：

    - **H\_USERID** – 如果贸易伙伴需要您发送用户 ID 作为 URL 的一部分来提交采购订单，请在此处输入值。
    - **H\_PASSWORD** – 如果贸易伙伴需要您发送密码作为 URL 的一部分来提交采购订单，请在此处输入值。

- **ENABLEMANUALPO** – 如果将此属性设置为 _TRUE_，则当用户手动创建采购订单时（即当他们不是从申请开始时），这些采购订单将继承供应商的**通过 cXML 发送采购订单**选项的设置。 如果未设置此属性，或设置为 _FALSE_，将不会在手动创建的采购订单的采购订单标题上设置**通过 cXML 发送采购订单**选项。 对于从申请创建的采购订单，无论此属性如何设置，始终会继承供应商的**通过 cXML 发送采购订单**选项的设置。 有关详细信息，请参阅本主题前面的[设置供应商采购订单以使用 cXML](#vendor-setup) 一节。
- **PUNCHOUTPOONLY** – 如果将此属性设置为 _TRUE_，仅从 PunchOut 流程创建的采购申请行会在采购订单标题上设置**通过 cXML 发送采购订单**选项。 此外，采购订单上所有行的采购申请行类型必须为_外部目录项_。 否则，将无法创建 cXML 采购订单。
- **PUNCHOUTSHIPTO** – 如果此属性设置为 _TRUE_，当用户打开外部目录时，法人的默认地址将添加到 PunchOut 设置请求消息中。 此地址将添加为 **ShipTo** 地址。 供应商将使用 **ShipTo** 地址来根据公司位置显示定价。
- **TRACEPUNCHOUT** – 如果您尝试从申请浏览到外部目录时收到错误消息，请将此属性设置为 _TRUE_。 然后，将填充在 Supply Chain Management 和供应商站点之间发送的 **PunchOutSetupRequest** 和 **PunchOutResponse** 消息的跟踪信息。 您可以在 **cXML 购物车消息日志**页上查看此信息，可以从遇到问题的供应商目录的**外部目录设置**页打开此页面。 仅在进行故障排除时，才应将此属性设置为 _TRUE_，因为这会在数据库中对每个 PunchOut 造成很大的性能开销。 有关详细信息，请参阅本主题后面的[查看外部目录 PunchOut 的 cXML 购物车消息日志](#message-log)一节。
- **REPLACENEWLINE** – 如果由于供应商的系统正在发送包含换行符 (\\n) 的 **PunchOutResponse** 消息而遇到问题，请将此属性设置为 _TRUE_。 如果通过中间件或采购中心分析了供应商的消息，则可能会发生此问题。 如果您在使用新供应商设置时遇到问题，请将 **TRACEPUNCHOUT** 属性设置为 _TRUE_ 来查看 **PunchOutResponse** 消息，确定 XML 标记是否被换行符破坏。
- **POCOMMENTS** – 如果您希望 cXML 文档包括附加到 Supply Chain Management 中采购订单的注释，将此属性设置为 _TRUE_。 附件文本包含在采购订单消息的标题注释中。 有关系统如何选择和处理这些附件的详细信息，请参阅本主题后面的[将注释附加到采购订单](#attach-po-notes)一节。
- **VENDCOMMENTS** – 如果您希望 cXML 文档包括附加到 Supply Chain Management 中采购订单的注释，将此属性设置为 _TRUE_。 附件文本包含在采购订单消息的标题注释中。 有关系统如何选择和处理这些附件的详细信息，请参阅[将注释附加到采购订单](#attach-po-notes)一节。
- **CLEANAMP** – 如果在尝试对供应商执行 PunchOut 时收到错误消息，并且此供应商的返回 URL 包含错误编码的与号 (\&)，将此属性设置为 _TRUE_。
- **PUNCHOUTTZ** – 如果您正在使用的供应商使用国际标准化组织 (ISO) 8601 标准对 PunchOut 请求消息的日期/时间进行特定验证，将此属性设置为 _TRUE_。 Supply Chain Management 在 **PunchOutSetupRequest** 消息中使用协调世界时 (UTC) 日期。 因此，当您将此属性设置为 _TRUE_ 时，将会在日期/时间格式中添加 *+00:00*。
- **WMSADDRESSID** – 将此属性设置为 _TRUE_ 可以将采购订单标题上的仓库编号用作发送给供应商的采购订单请求的 **ShipTo** 地址中的 **addressID** 值。 如果为 **FIXEDSHIPADDRESSID** 属性设置了值，该值优先于此值。 因此，您应该使用一个属性或另一个属性在文档的 **ShipTo** 地址中设置 **addressID** 值。
- **PUNCHOUTSHIPTOUSER** – 此属性与 **PUNCHOUTSHIPTO** 属性一起使用。 如果 **PUNCHOUTSHIPTO** 设置为 _TRUE_，将选择法人的地址。 如果 **PUNCHOUTSHIPTOUSER** 设置为 _TRUE_，将使用 PunchOut 用户的主地址代替法人地址。

### <a name="activate-the-external-catalog"></a>激活外部目录

完成设置所有属性并为外部目录配置其他设置后，返回**外部目录**页的**常规**快速选项卡，将**活动**选项设置为*是*。

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>将注释附加到采购订单

如[设置订单属性](#set-order-properties)一节所述，如果您希望传递的 cXML 包含附加到相关采购订单和/或供应商记录的注释中的文本，您可以在外部目录设置中将 **POCOMMENTS** 和/或 **VENDCOMMENTS** 属性设置为 _TRUE_。 本节提供有关系统如何选择和处理这些附件（如果使用）的更多详细信息。

若要设置系统要查找的注释类型，请转到**采购 \> 设置 \> 窗体 \> 窗体设置**。 然后，在**采购订单**选项卡上，将**包括单据的类型**字段设置为您希望包含的注释类型。 将仅包含文本注释，不包含文档附件。

![窗体设置页面](media/cxml-form-setup.png "窗体设置页面")

仅当附件的**类型**字段设置为您在**包括单据的类型**字段中选择的值，并且附件的**限制**字段设置为_外部_时，附件才会包含在采购订单中。 要创建、查看或编辑采购订单的附件，请转到**采购 \> 所有采购订单**，选择或创建采购订单，然后选择右上角的**附件**按钮（回形针符号）。

![设置为发送给供应商的附加注释](media/cxml-note-to-vendor.png "设置为发送给供应商的附加注释")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>查看外部目录 PunchOut 的 cXML 购物车消息日志

当您将外部目录的 **Punchout 协议类型**字段设置为 _cXML_ 时，系统将捕获从供应商返回的购物车的消息日志。 此日志可用于故障排除和其他数据目的。

要打开外部目录的日志，请选择相关目录，然后在操作窗格上选择 **cXML 购物车消息日志**。 **cXML 购物车消息日志**页将显示已返回购物车的列表、与这些购物车相关的 XML，以及在相关采购申请上创建的行。

![cXML 购物车消息日志页面](media/cxml-cart-message-log.png "cXML 购物车消息日志页面")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>设置外部目录 PunchOut 的外在元素

当您将外部目录的 **Punchout 协议类型**字段设置为 *cXML* 时，可以添加自定义外在元素，这些元素将插入请求 XML 消息中的正确位置。

要将外在元素添加到外部目录，请按照下列步骤操作。

1. 转到**采购 \> 目录 \> 外部目录**。
1. 选择相关目录。
1. 在**消息格式**快速选项卡上的**外在**部分，选择**添加**，为您要包括的每个外在元素向网格添加一行。 在每一行上，设置以下字段：

    - **名称** – 为元素输入名称。 此值将成为每一行创建的**外在** XML元素的**名称**属性的值。 通常，您将与供应商一起商定每个外在元素的名称。
    - **值** – 为元素选择一个值。 此值将成为每一行创建的 XML元素的值。 提供以下值：

        - **用户名** – 使用正在执行 PunchOut 的用户的名称。 此名称是 Supply Chain Management 的登录名称。
        - **用户电子邮件** – 使用正在执行 PunchOut 的用户的电子邮件地址。 此地址是用户在**用户选项**页的**帐户**选项卡上设置的地址。
        - **随机值** – 使用唯一的随机值。
        - **用户全名** – 使用与正在访问外部目录的用户关联的联系人的全名。
        - **名字** – 使用与正在访问外部目录的用户关联的联系人的名字。
        - **姓氏** – 使用与正在访问外部目录的用户关联的联系人的姓氏。
        - **电话号码** – 使用与正在访问外部目录的用户关联的联系人的主电话号码。

![外在元素设置](media/cxml-extrinsics.png "外在元素设置")

用户或管理员看不到外在元素，因为在用户执行 PunchOut 之前不会添加它们。 它们会自动插入到 cXML 设置请求消息中的 **BuyerCookie** 和 **BrowserFromPost** 元素之间。 因此，在设置外部目录时，无需在 XML 中手动设置它们。

![添加到 XML 的外在元素](media/cxml-extrinsics-xml.png "添加到 XML 的外在元素")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>创建和处理采购订单

为供应商创建采购订单时，将继承该供应商的**通过 cXML 发送采购订单**选项的设置。 但是，此设置在采购订单的**标题**视图中的**设置**快速选项卡上仍然可用，因此您以后可以根据需要进行更改。

![设置为使用 cXML 的采购订单](media/cxml-purchase-order.png "设置为使用 cXML 的采购订单")

当您从来自 PunchOut 流的采购申请创建采购订单时，将填充所有必需的行详细信息。 然后，您可以手动添加采购订单行或从其他采购订单复制。 请确保设置所有必填字段。 这些必填字段包括外部参考编号，即将在 cXML 消息中使用的供应商编号。

![外部参考编号的示例](media/cxml-line-details.png "外部参考编号的示例")

填写采购订单的所有详细信息后，请确保进行确认。 除非采购订单已确认，否则不会发送任何消息。 要确认采购订单，在操作窗格上，在**采购**选项卡上的**操作**组中，选择**确认**。 

确认采购订单后，您可以通过**采购订单确认**日记帐查看确认状态。 在操作窗格上，在**采购**选项卡的**日记帐**组中，选择**采购订单确认**。

每个采购订单可以有很多确认。 每个确认标有递增编号。 在下图中，采购订单为 *00000275*，确认为 *00000275-1*。 此编号反映了标准 Supply Chain Management 功能，其中基于确认确定采购订单的更改，以及因此应发送给供应商的 cXML 消息的类型。 如图所示，**采购订单确认**页还包括**订单发送状态**和**订单请求供应商状态**字段。 有关您可能在此页面上看到的各种状态值的详细信息，请参阅本主题后面的[监视采购订单请求](#monitor-po-requests)一节。

![采购订单确认页面](media/cxml-po-confirmations.png "采购订单确认页面")

要查看有关文档的详细信息，请选择网格上方的**采购订单请求**。

**采购订单请求**页面包含两个网格。 在页面上部的网格中，每个采购订单有一个标记为发送的记录。 页面下部**采购订单请求历史记录**选项卡上的网格可能有所选采购订单的多个记录，指示每个确认的状态。 下图显示了上部网格中的采购订单 00000275 和**采购订单请求历史记录**选项卡上的网格中的单据 00000275-1。

![采购订单请求页面](media/cxml-po-request.png "采购订单请求页面")

如果批处理作业已设置并正在运行，将发送单据。 发送单据后，您可以查看状态更改。 在下图中，**订单发送状态**字段设置为_已发送_。 **订单请求供应商状态**字段设置为_已确认_，指示供应商已收到单据，并且能够读取该单据并将其存储在系统中。 **采购订单请求历史记录**选项卡上的网格显示发送单据的时间。 有关您可能在此页面上看到的各种状态值的详细信息，请参阅[监视采购订单请求](#monitor-po-requests)一节。

![采购订单请求页面上的状态消息](media/cxml-po-request-2.png "采购订单请求页面上的状态消息")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>计划采购订单请求批处理作业

要激活发送采购订单请求的批处理作业，请转到**采购 \> 设置 \> cXML 管理 \> 采购订单请求**，然后在操作窗格上的**采购订单请求**选项卡上，在**批处理**组中，选择**提交作业**以打开**采购请求准备与发送**对话框。 您可以像在 Supply Chain Management 中处理批处理作业那样使用此对话框设置定期。 根据您的订单量选择一个间隔。 虽然您可以每分钟运行批处理作业，但可能最好的做法是根据与供应商的计划匹配的订单接收窗口在整个工作日内发送批处理。

例如，您的供应商有一项政策规定，下午 1 点之前收到的所有订单都在同一天装运。 在这种情况下，您可能只需要在早上运行几次批处理来传达您有的全部订单。 其余订单将在第二天发送。 此决定只是一个业务决定。 您可以进行检查，然后相应地设置参数。

过程中将查找状态为*等待*的采购订单请求文档。 如果您有必须立即发送给供应商的订单，可以选择**提交作业**并将**批处理**选项设置为*否*。

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>监视采购订单请求

### <a name="view-the-status-of-a-purchase-order"></a>查看采购订单的状态

确认可以通过 cXML 发送的订单后，它们将进入_等待_状态。 如[创建和处理采购订单](#create-po)一节所述，您可以在**采购订单请求**页查看采购订单状态。 每个采购订单请求可以具有几种状态之一，具体取决于其参数和数据。 本节介绍各种状态类型及其可以具有的值。 此信息可以帮助您管理问题并了解采购订单的状态。

![采购订单请求页面上的采购订单状态](media/cxml-monitor-po-request.png "采购订单请求页面上的采购订单状态")

**采购订单请求**页上部的网格可能会显示以下状态值：

- **订单发送状态** – 此字段可以具有以下值之一：

    - **等待** – 文档正在等待发送。
    - **已发送** – 文档已发送。
    - **已停止** – 文档在发送之前被标记为_已停止_。 （要将文档标记为_已停止_，在**采购请求**页的操作窗格上选择**停止**。）
    - **存档** – 文档已清除。 （要清除文档，在**采购请求**页的操作窗格上选择**清除**。）

- **订单请求供应商状态** – 此字段可以具有以下值之一：

    - **等待** – 文档正在等待发送。
    - **已确认** – 供应商已确认文档已接收。 您可以通过选择页面下部的**响应 XML** 选项卡来查看从供应商返回的详细 XML 消息。
    - **错误** – 文档已发送给供应商，但发生错误。 您可以通过选择页面下部的**响应 XML** 选项卡查看错误消息。

**采购订单请求**页下部的**采购订单请求历史记录**选项卡上的网格可能显示以下值：

- **订单请求类型** – 此字段可以具有以下值之一：

    - **新** – 确认采购订单后，行将立即标记为新行。
    - **更新** – 如果供应商已经发送并确认了确认，下一个确认将标记为_更新_。 仅当**发送采购请求更新**选项在[全局 cXML 参数](#cxml-parameters)中设置为*是*时，才会发送更新。
    - **删除** – 如果供应商已经发送并确认了确认，但采购订单被取消，正在等待的确认将被标记为_删除_。 仅当**发送采购请求删除**选项在[全局 cXML 参数](#cxml-parameters)中设置为*是*时，才会发送删除。

- **请求时间** – 创建订单确认的时间。 您可以将请求时间与订单状态时间进行比较，来确定确认和供应商确认之间的时间。
- **订单发送状态** – 此字段与页面上部的**订单发送状态**字段相同。 在此处重复出现是为了让您更轻松地在确认级别查看状态。 如果**订单请求类型**字段设置为*新*，并且在发送确认之前重新确认了采购订单，**订单发送状态**字段将设置为*存档*。
- **订单状态时间** – 采购订单请求历史记录最后更新的时间。 （更新包括状态更改。）
- **订单请求供应商状态** – 此字段与页面上部的**订单请求供应商状态**字段相同。 在此处重复出现是为了让您更轻松地在确认级别查看状态。
- **重新提交时间** – 记录重新提交的时间。
- **重新提交计数** – 记录重新提交的次数。 大数字指示多次失败，因此可能表示您的数据设置或供应商的数据设置有问题。

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>查看采购订单请求消息的 XML

要查看采购订单请求消息的 XML，请选择**采购订单请求**页底部的**请求 XML 文本**选项卡。 此选项卡上的信息在测试或错误验证期间可能会有所帮助。 为了使信息更易于阅读，您可以将其作为格式化的消息来查看。 将选项卡的内容复制到文本文件，然后在 XML 编辑器中进行查看。

![请求 XML 文本选项卡](media/cxml-request-xml-text.png "请求 XML 文本选项卡")

### <a name="view-the-details-of-the-vendor-response"></a>查看供应商响应的详细信息

要查看供应商确认或错误响应的内容，请选择**采购订单请求**页底部的**响应 XML** 选项卡。

![响应 XML 选项卡](media/cxml-response-xml.png "响应 XML 选项卡")

## <a name="additional-resources"></a>其他资源

- [为电子采购发包设置外部目录](set-up-external-catalog-for-punchout.md)
- [针对电子采购发包使用外部目录](use-external-catalogs-for-punchout.md)