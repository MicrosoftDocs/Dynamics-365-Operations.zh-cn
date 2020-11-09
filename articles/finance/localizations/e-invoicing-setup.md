---
title: 设置电子开票附加产品
description: 本主题说明如何在 Microsoft Dynamics 365 Finance 和 Dynamics 365 Supply Chain Management 中设置电子开票附加产品。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 7e631f1bf64b47b5f3e85d4f98c6edafe67d627a
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039884"
---
# <a name="set-up-the-electronic-invoicing-add-on"></a>设置电子开票附加产品

[!include [banner](../includes/banner.md)]


电子开票附加产品功能设置是通过 Regulatory Configuration Services (RCS) 环境创建所需配置并将该配置发布到电子开票附加产品服务器的过程。 此设置使您可以创建可配置规则，以使电子开票附加产品可以通过 Internet 使用安全协议来通过 Web 服务与第三方实体进行通信和交换数据。

可配置性依赖电子报告 (ER) 格式配置作为构建通过数字文件发送和接收的内容的方法。 它还依赖于通信操作的流程来向第三方 Web 服务发送请求并接收来自这些服务的响应，您无需编写代码。

## <a name="overview"></a>概览

“电子开票附加产品功能”是配置和发布以使用电子开票附加产品服务器的资源的通用名称。 功能设置将使用 ER 配置格式来创建可配置的导出和导入文件，与使用操作和操作流来支持创建可配置规则以发送请求、导入响应和分析响应内容，以及另外一些设置相结合。

下图显示了电子开票附加产品功能的主要组件。

![电子开票附加产品功能概述](media/e-Invoicing-services-feature-setup-Overview-e-Invoicing-feature.png)

由于发票格式和操作流的变化，功能设置可能会因国家或地区或业务要求而异。

## <a name="set-up-the-electronic-invoicing-add-on-feature"></a>设置电子开票附加产品功能

设置过程必须在您的 RCS 环境中完成。 请按照以下步骤创建新的电子开票附加产品功能。

1. 登录您的 RCS 环境。
2. 在 **全球化功能** 工作区的 **功能** 部分，选择 **电子开票附加产品** 磁贴。
3. 在 **电子开票附加产品功能** 页上，选择 **导入** 从全局存储库导入 ER 数据模型配置。
4. 选择 **添加** 创建电子开票附加产品功能。 您可以从头创建此功能，也可以从现有的电子开票附加产品功能派生。

    ![添加电子开票附加产品功能](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature.png)

> [!NOTE]
> 创建新的电子开票附加产品功能时，它具有版本号，默认状态将设置为 **草稿** 。

### <a name="configurations"></a>配置

配置保留转换和创建在与第三方 Web 服务通信期间将交换的文件所需的 ER 格式配置。 基于 Web 服务提供商提供的集成技术规范，电子开票附加产品功能可以具有所需的任意数量的 ER 文件格式配置。

请按照以下步骤将 ER 格式添加到电子开票附加产品功能。

1. 在 **电子开票附加产品功能** 页上的 **配置** 选项卡上，选择 **添加** 为电子开票附加产品功能添加 ER 文件格式配置。

    ![添加电子开票附加产品功能配置](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > 从头创建电子开票附加产品功能时，必须手动添加所有 ER 文件格式配置。 从现有功能派生电子开票附加产品功能时，将自动创建 ER 文件格式配置，因为它们是从原始电子开票附加产品功能继承而来的。

2. 选择 **编辑** 打开 **格式设计器** 页，您可以在其中编辑 ER 文件格式配置。

    ![编辑电子开票附加产品功能配置](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Configurations.png)

    > [!NOTE]
    > 在编辑格式时，配置版本的状态将设置为 **草稿** 。

3. 使用 **格式设计器** 页更改文件格式配置。 有关详细信息，请参阅[创建电子单据配置](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration)。

    ![“格式设计器”页面](media/e-Invoicing-services-feature-setup-ER-Format-designer.png)

### <a name="feature-setups"></a>功能设置

功能设置封装第三方 Web 服务的通信和安全性规则。 根据您要完成的业务规则，电子开票附加产品功能可以具有所需的任意数量的功能设置。

请按照以下步骤将功能设置添加到电子开票附加产品功能。

1. 在 **电子开票附加产品功能** 页上的 **设置** 选项卡上，选择 **添加** 向电子开票附加产品功能添加功能设置。

    ![添加电子开票附加产品功能设置](media/e-Invoicing-services-feature-setup-Select-Add-e-Invoicing-feature-Setups.png)

    > [!NOTE]
    > 从头创建电子开票附加产品功能时，必须手动添加所需的所有功能设置。 从现有功能派生电子开票附加产品功能时，将自动创建所有功能设置，因为它们是从原始电子开票附加产品功能继承而来的。

2. 选择 **编辑** 编辑功能版本设置。

    ![编辑电子开票附加产品功能设置](media/e-Invoicing-services-feature-setup-Select-Edit-e-Invoicing-feature-Setups.png)

3. 使用 **功能版本设置** 页配置操作、适用性规则和变量。

    ![操作、适用性规则和变量](media/e-Invoicing-services-feature-setup-View-Actions-Applicability-Rules-Variables.png)

### <a name="actions"></a>行动

操作是按顺序运行的预定义操作列表。 此列表代表完整执行电子开票附加产品功能所需的步骤的分解。 操作可以在同一个电子开票附加产品功能中封装双向通信：发送目标请求、接收响应和分析内容。

每个操作包含一个预定义的参数列表，这些参数是操作完成目的所必需的。 可以选择提供其他参数。

#### <a name="actions-fasttab"></a>“操作”快速选项卡

在 **功能版本设置** 页上的 **操作** 选项卡上，在 **操作** 快速选项卡上，按照以下其中一个步骤或全部两个步骤来管理操作：

- 选择 **新建** 或 **删除** 添加新操作或删除现有操作。
- 选择 **向上** 或 **向下** 在网格中向上或向下移动选定的动作，从而更改它们的运行顺序。 操作从上到下按照它们在网格中出现的顺序运行。

![管理操作](media/e-Invoicing-services-feature-setup-Manage-Actions.png)

下表说明了 **操作** 快速选项卡上可用的字段。

| 字段        | 说明 |
|--------------|-------------|
| 行动       | 有八个预定义操作：<ul><li><strong>对文档签名</strong></li><li><strong>FileStoreActionName</strong></li><li><strong>转换文档</strong></li><li><strong>处理响应</strong></li><li><strong>调用 REST Web 服务</strong></li><li><strong>调用墨西哥 PAC 服务</strong></li><li><strong>调用巴西 SEFAZ 服务</strong></li><li><strong>调用意大利 SDI 服务</strong></li></ul> |
| 操作名称  | 操作的名称及其执行顺序。 |
| 说明  | 操作的说明。 |
| 启用重试 | 选中复选框表示如果上一次尝试失败，可以重试该操作。 |
| 重试操作 | 重试时，从其开始重试的操作。 然后重试于当前操作（包括重试）结束。 对于有重试的操作， **最小退避** 和 **最大退避** 参数指定最小重试次数和最大重试次数。 |

#### <a name="parameters-fasttab"></a>“参数”快速选项卡

**参数** 快速选项卡列出在 **操作** 快速选项卡上选择的操作的参数。

![“参数”快速选项卡](media/e-Invoicing-services-feature-setup-View-Actions-Parameters.png)

下表说明了 **参数** 快速选项卡上可用的字段。

| 字段       | 说明 |
|-------------|-------------|
| 姓名        | 预定义的参数列表。 有关详细信息，请参阅[按操作排列的参数列表](#list-of-parameters-by-action)一节。 |
| 说明 | 参数的说明。 |
| 值       | 参数的值。 |

#### <a name="list-of-parameters-by-action"></a>按操作排列的参数列表

可用参数会有所不同，具体取决于在 **操作** 快速选项卡上选择的操作。

###### <a name="action-sign-document"></a>操作：对文档签名

| 参数                             | 说明 |
|---------------------------------------|-------------|
| 输入字段                            | 必须使用电子签名进行签名的输入 XML 文档文件。 |
| 证书名称                      | 存储中证书的名称。 |
| 签名类型                        | 要使用的签名类型。 |
| 签名方法名称                 | 用于生成电子签名的签名方法的名称。 |
| 摘要方法名称                    | 用于在数字签名中生成摘要字符串的摘要方法。 |
| 规范化方法名称          | 用于计算签名哈希的规范化方法。 |
| 引用属性名称              | 指示引用 ID 应该在签名元素中插入的位置的属性名称。 |
| 要进行签名的元素名称               | 必须使用电子签名进行签名的文档中的 XML 元素的名称。 如果未指定元素，将对文档的根进行签名。 |
| 插入签名的元素的名称   | 应在其中插入生成的数字签名的 XML 元素的名称。 如果未指定元素，签名将插入文档的根。 |
| 带有摘要转换的 XLST 文件       | 包含用于为电子签名生成摘要字符串的摘要转换规则的可扩展样式表语言转换 (XSLT) 文件。 |
| 插入摘要字符串的路径          | 必须在其中插入生成的摘要字符串的位置的路径，格式为 **\<elementName\>.\<Attribute.Path\>** 。 |
| 证书编号位置           | 应放置证书编号的元素和属性的名称。 |
| 证书数据的位置          | 必须在其中插入证书数据 (base64) 的元素和属性的名称。 |
| 证书编号为 ASCII 格式 | 指定证书的编号是否以 ASCII 格式编码的值。 |

###### <a name="action-filestoreactionname"></a>操作：FileStoreActionName

| 参数  | 说明 |
|------------|-------------|
| 输入字段 | 要存储的输入文件。 |

###### <a name="action-transform-document"></a>操作：转换文档

| 参数                       | 说明 |
|---------------------------------|-------------|
| 输入字段                      | 提供必须对操作运行的数据的源文件。 |
| 方向                       | 指示应使用导入格式还是导出格式的值。 |
| 配置 ID                | 应该运行的格式。 |
| 配置版本           | 如果未指定配置版本，将使用最新版本。 |
| 配置集成点 | 为报告运行时提供数据的源文件。 |

###### <a name="action-process-response"></a>操作：处理响应

| 参数                    | 说明 |
|------------------------------|-------------|
| 输入字段                   | 要分析的响应。 |
| 报告配置列表 | 用于解析响应的配置列表。 |

###### <a name="action-call-rest-web-service"></a>操作：调用 REST Web 服务

| 参数                   | 说明 |
|-----------------------------|-------------|
| Web 服务 URL             | 请求发送到的 URL。 |
| Web 请求超时         | 等待 Web 服务响应的最长时间（以毫秒为单位）。 |
| 请求操作类型      | HTTP 请求操作的类型（例如， **GET** 、 **POST** 或 **DELETE** ）。 |
| 证书名称           | 证书名称。 |
| 响应正文编码      | 预期的 HTTP 响应正文的编码，以可以正确解码。 |
| HTTP 请求内容类型   | HTTP 请求内容类型标题输入。 |
| HTTP 请求内容正文   | HTTP 请求正文。 （正文可以为空。） |
| HTTP 参数查询值 | 用于使用可变参数填充 URL 的参数查询值。 |
| 请求路由               | HTTP 请求的路由路径。 变量参数可以用 **\{paramName\}** 表示法编写。 这是一个示例： **"api/{id}/submit"** 。 |
| 路由参数列表        | 用于将变量插入路由的路由参数（采用键值表示法）。 |
| 自定义 HTTP 标题         | 要放入请求中的自定义 HTTP 标题。 |
| HTTP 请求 cookie        | 要放入 HTTP cookie 标题请求中的 cookie（采用键值表示法）的列表。 |
| 安全协议           | 用于 HTTP 请求与服务器通信的安全协议。 （默认情况下，使用传输层安全性 \[TLS\] 1.2。） |

###### <a name="action-call-mexican-pac-service"></a>操作：调用墨西哥 PAC 服务

| 参数                | 说明 |
|--------------------------|-------------|
| 输入字段               | 包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。 |
| URL 地址              | Web 服务地址（终结点）。 |
| Web 方法（操作）名称 | 必须运行的 Web 方法（操作）的名称。 |
| 证书             | Web 服务进行客户端身份验证所需的证书链。 客户端证书应该是链中的最后一个证书。 根证书和中间证书应该是第一个。 |
| Web 请求超时      | 等待 Web 服务响应的最长时间（以毫秒为单位）。 |
| 重试间隔           | 尝试从 Web 服务调用和接收响应之间的间隔。 如果未指定间隔，在第一个调用失败后将不进行其他重试。 |
| 重试计数              | 从 Web 服务调用和检索响应的最大重试尝试次数。 |
| 重试截止时间               | 重试调用可以继续的最长时间（以毫秒为单位）。 |
| 最小退避         | 重试间隔指数计算的最小退避率。 |
| 最大退避         | 重试间隔指数计算的最大退避率。 |
| 安全协议        | 用于 HTTP 请求与服务器通信的安全协议。 （默认情况下，使用 TLS 1.2。） |

###### <a name="action-call-brazilian-sefaz-service"></a>操作：调用巴西 SEFAZ 服务

| 参数                | 说明 |
|--------------------------|-------------|
| 输入字段               | 包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。 |
| URL 地址              | Web 服务地址（终结点）。 |
| Web 方法（操作）名称 | 必须运行的 Web 方法（操作）的名称。 |
| 证书             | Web 服务进行客户端身份验证所需的证书链。 客户端证书应该是链中的最后一个证书。 根证书和中间证书应该是第一个。 |
| Web 请求超时      | 等待 Web 服务响应的最长时间（以毫秒为单位）。 |
| 重试间隔           | 尝试从 Web 服务调用和接收响应之间的间隔。 如果未指定间隔，在第一个调用失败后将不进行其他重试。 |
| 重试计数              | 从 Web 服务调用和检索响应的最大重试尝试次数。 |
| 重试截止时间               | 重试调用可以继续的最长时间（以毫秒为单位）。 |
| 最小退避         | 重试间隔指数计算的最小退避率。 |
| 最大退避         | 重试间隔指数计算的最大退避率。 |
| 安全协议        | 用于 HTTP 请求与服务器通信的安全协议。 （默认情况下，使用 TLS 1.2。） |

###### <a name="action-call-italian-sdi-service"></a>操作：调用意大利 SDI 服务

| 参数                | 说明 |
|--------------------------|-------------|
| 输入字段               | 包含将作为方法输入参数发送到 Web 服务的 XML 数据的文件。 |
| URL 地址              | Web 服务地址（终结点）。 |
| Web 方法（操作）名称 | 必须运行的 Web 方法（操作）的名称。 |
| 证书             | Web 服务进行客户端身份验证所需的证书链。 客户端证书应该是链中的最后一个证书。 根证书和中间证书应该是第一个。 |
| Web 请求超时      | 等待 Web 服务响应的最长时间（以毫秒为单位）。 |
| 重试间隔           | 尝试从 Web 服务调用和接收响应之间的间隔。 如果未指定间隔，在第一个调用失败后将不进行其他重试。 |
| 重试计数              | 从 Web 服务调用和检索响应的最大重试尝试次数。 |
| 重试截止时间               | 重试调用可以继续的最长时间（以毫秒为单位）。 |
| 最小退避         | 重试间隔指数计算的最小退避率。 |
| 最大退避         | 重试间隔指数计算的最大退避率。 |
| 安全协议        | 用于 HTTP 请求与服务器通信的安全协议。 （默认情况下，使用 TLS 1.2。） |

### <a name="applicability-rules"></a>适用性规则

适用性规则使您可以创建确定功能设置用法上下文的逻辑规则。 因此，所发送的要进行处理的业务文档给定的上下文与适用性规则条件之间的匹配，确定使用哪个电子开票附加产品功能来处理该提交。

#### <a name="set-up-applicability-rules"></a>设置适用性规则

1. 在 **功能版本设置** 页，在 **适用性规则** 选项卡上，选择 **新建** 添加适用性规则。

    ![管理适用性规则](media/e-Invoicing-services-feature-setup-Manage-Actions-Applicability-rules.png)

2. 在网格中，选择应分组的子句。
3. 选择 **分组子句** 。

    ![分组子句](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-clause.png)

    将子句分组后，一个新列将添加到网格中。 此列指定分组子句的逻辑运算符。

    ![分组子句的逻辑运算符](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-Group-criterias.png)

若要取消对子句的分组，请选择要取消分组的分组子句，然后选择 **取消子句分组** 。

![取消子句分组](media/e-Invoicing-services-feature-setup-Manage-Applicability-rules-UnGroup-criterias.png)

> [!NOTE]
> 取消子句分组时，请始终从最内部的分组级别开始。

下表说明了 **适用性规则** 选项卡上可用的字段。

| 字段         | 说明 |
|---------------|-------------|
| 与/或        | 逻辑运算符。 |
| 字段         | 用于构造规则的字段。 |
| 运算符类型 | 运算符的类型：<ul><li>相等</li><li>不等于</li><li>大于/小于</li><li>大于等于/小于等于</li><li>包含</li><li>开头为</li></ul> |
| 值         | 规则的条件。 |

### <a name="variables"></a>变量

您可以创建变量，然后将它们用作特定操作的参数的输入值。 您还可以使用它们在电子开票附加产品服务与客户端之间交换作为提交流一部分执行特定操作的结果信息。

#### <a name="set-up-variables"></a>设置变量

- 在 **功能版本设置** 页上的 **变量** 选项卡上，选择 **新建** 或 **删除** 管理变量。

    ![管理变量](media/e-Invoicing-services-feature-setup-Manage-Variables.png)

下表说明了 **变量** 选项卡上可用的字段。

| 字段       | 说明 |
|-------------|-------------|
| 姓名        | 变量的名称。 |
| 说明 | 变量的简要说明。 |
| 类型        | 变量的类型：<ul><li><strong>常数</strong> – 变量的内容是固定的。</li><li><strong>从客户端</strong> – 变量的内容在执行提交流程期间从 Microsoft Dynamics 365 客户端获取。</li><li><strong>到客户端</strong> – 变量的内容在执行提交流程期间可以供 Microsoft Dynamics 365 客户端导入。</li></ul> |
| 数据类型   | 变量的数据类型：<ul><li>Boolean</li><li>日期</li><li>数值</li><li>UUID</li><li>字符串</li><li>文件</li></ul> |
| 值       | 变量的值或设置变量值的操作的名称。 |

### <a name="validate-the-feature-setup"></a>验证功能设置

- 在 **功能版本设置** 页上的操作窗格上，选择 **验证** 验证功能版本设置。

   ![选择“验证”按钮](media/e-Invoicing-services-feature-setup-Select-Validate-Button.png)

验证检查整个配置的一致性。 例如，如果某个操作的特定参数是强制性的，但其值仍为空白，验证会检测到这种不一致，您会收到警告。

## <a name="environments"></a>环境

电子开票附加产品环境必须与电子开票附加产品功能关联并启用。 必须通过在组织的 RCS 帐户中配置全球化功能预先创建和发布电子开票附加产品环境。

请按照以下步骤为电子开票附加产品功能启用电子开票附加产品环境。

1. 在 **电子开票附加产品功能** 页上的 **环境** 选项卡上，选择 **启用** 添加电子开票附加产品环境。
2. 在 **生效开始日期** 字段中，输入新环境生效的日期。

![启用电子开票附加产品环境](media/e-Invoicing-services-feature-setup-Select-Enable-e-Invoicing-feature-Environment.png)

## <a name="organizations"></a>组织

电子开票附加产品功能可以在多个组织之间共享。

- 在 **电子开票附加产品功能** 页上的 **组织** 选项卡上，选择 **共享** 添加要与之共享电子开票附加产品功能的组织。

要停止与组织共享电子开票附加产品功能，请选择 **取消共享** 。

## <a name="versions"></a>版本

版本通过管理电子开票附加产品功能的状态来帮助控制电子开票附加产品功能的生命周期。 您可以创建现有电子开票附加产品功能的新版本，或在完成电子开票附加产品功能的所有配置后，可以将功能的状态更改为 **完成** ，然后更改为 **发布** 。

### <a name="create-a-new-version-of-an-existing-electronic-invoicing-add-on-feature"></a>创建现有电子开票附加产品功能的新版本

1. 在 **电子开票附加产品功能** 页上，在左侧的网格中，选择电子开票附加产品功能。
2. 在 **版本** 选项卡上，选择 **新建** 添加电子开票附加产品功能的新版本。

### <a name="change-the-status-of-the-electronic-invoicing-add-on-feature"></a>更改电子开票附加产品功能的状态

请按照以下步骤管理电子开票附加产品功能的生命周期。

1. 在 **电子开票附加产品功能** 页上，在左侧的网格中，选择电子开票附加产品功能。
2. 在 **版本** 选项卡上，选择 **更改状态** ，然后将状态从 **草稿** 更改为 **完成** 。
3. 系统将提示您确认要完成电子开票附加产品功能及其所有组件。 选择 **是** 确认操作或选择 **否** 取消。

    > [!NOTE]
    > 当您选择 **是** 时，作为电子开票附加产品功能的组件的配置版本的状态会自动从 **草稿** 更改为 **完成** 。

4. 选择 **更改状态** ，然后将状态从 **完成** 更改为 **发布** 。
5. 系统将提示您确认要将电子开票附加产品功能及其所有组件发布到全局存储库。 选择 **是** 确认操作或选择 **否** 取消。

    > [!NOTE]
    > 当您选择 **是** 时，配置版本的状态会自动从 **已完成** 更改为 **已共享** 。
