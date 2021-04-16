---
title: 为 Dynamics 365 Commerce 评估环境配置可选功能
description: 本主题说明如何为 Microsoft Dynamics 365 Commerce 评估环境配置可选功能。
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6bc968c2659380bb8c92292ee19e3a7ec8a20a2b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795899"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a>为 Dynamics 365 Commerce 评估环境配置可选功能

[!include [banner](includes/banner.md)]

本主题说明如何为 Microsoft Dynamics 365 Commerce 评估环境配置可选功能。

## <a name="prerequisites"></a>先决条件

如果要评估交易电子邮件功能，必须满足以下先决条件：

- 您有可用的电子邮件服务器（简单邮件传输协议 \[SMTP\] 服务器），可从 Microsoft Azure 订阅（在其中预配了评估环境）使用该服务器。
- 您有该服务器的完全限定域名 (FQDN)/IP 地址、SMTP 端口号和身份验证详细信息。

## <a name="configure-the-image-back-end"></a>配置图像后端

### <a name="find-your-media-base-url"></a>查找您的媒体基 URL

> [!NOTE]
> 您必须先完成[在 Commerce 中设置您的站点](cpe-post-provisioning.md#set-up-your-site-in-commerce)中的步骤，然后才能完成此过程。

1. 使用您在预配期间初始化电子商务时记下的 URL 登录 Commerce 站点构建器（请参阅[初始化电子商务](provisioning-guide.md#initialize-e-commerce)）。
1. 打开 **Fabrikam** 站点。
1. 在左侧菜单中，选择 **媒体库**。
1. 选择任何单个图像资产。
1. 在右侧的属性检查器中，找到 **公共 URL** 属性。 此值是一个 URL。 下面是一个示例：

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`。

1. 将 URL 中的最后一个标识符（前面示例中为 **MA1nQC**）替换为字符串 **search?fileName=**。 进行此更改后，示例 URL 如下所示：

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    此 URL 是您的媒体基 URL。 请记下它。

### <a name="update-the-media-base-url"></a>更新媒体基 URL

1. 登录 Commerce Headquarters。
1. 使用左侧菜单转到 **模块 \> Retail 和 Commerce \> 渠道设置 \> 渠道配置文件**。
1. 选择 **编辑**。
1. 在 **配置文件属性** 下，将 **媒体服务器基 URL** 属性的值替换为您前面创建的媒体基 URL。
1. 选择名为 **scXXXXXXXXX** 的渠道。
1. 在 **配置文件属性** 下，选择 **添加**。
1. 对于添加的属性，选择 **媒体服务器基 URL** 作为属性键。 作为属性值，输入您先前创建的媒体基 URL。
1. 选择 **保存**。

## <a name="configure-and-test-the-email-server"></a>配置和测试电子邮件服务器

> [!NOTE]
> 必须可从您用于环境的 Azure 订阅访问您在此处输入的 SMTP 服务器或电子邮件服务。

1. 登录 Commerce Headquarters。
1. 使用左侧菜单转到 **模块 \> Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 电子邮件参数**。
1. 在 **SMTP 设置** 选项卡上，在 **出站邮件服务器** 字段中，输入您的 SMTP 服务器或电子邮件服务的 FQDN 或 IP 地址。
1. 在 **SMTP 端口号** 字段中，输入端口号。 （如果您使用的不是安全套接字层 \[SSL\]，默认端口号是 **25**。）
1. 如果需要验证，请在 **用户名** 和 **密码** 字段中输入值。
1. 选择 **保存**。
1. 选择 **刷新**。
1. 在 **测试电子邮件** 选项卡上，在 **电子邮件提供程序** 字段中，选择 **SMTP**。
1. 在 **发送到** 字段中，输入要测试电子邮件应发送到的电子邮件地址。
1. 选择 **发送测试电子邮件**。

## <a name="configure-email-templates"></a>配置电子邮件模板

对于要为其发送电子邮件的每个交易事件，必须使用有效的发件人电子邮件地址更新电子邮件模板。

1. 登录 Commerce Headquarters。
1. 使用左侧菜单转到 **模块 \> Retail 和 Commerce \> Headquarters 设置 \> 参数 \> 组织电子邮件模板**。
1. 选择 **显示列表**。
1. 对于列表中的每个模板，请执行这些步骤：

    1. 在 **发件人电子邮件** 字段中，输入发件人电子邮件地址。
    1. 可选：在 **发件人名称** 字段中，输入应用作发件人名称的名称。

1. 选择 **保存**。

## <a name="customize-email-templates"></a>自定义电子邮件模板

您可能希望自定义电子邮件模板，让它们使用不同的图像。 或者，您可能想要更新模板中的链接，使其转到您的评估环境。 此过程说明如何下载默认模板，自定义默认模板和更新系统中的模板。

1. 在 Web 浏览器中，将 [Microsoft Dynamics 365 Commerce 评估默认电子邮件模板 zip 文件](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip)下载到本地计算机。 此文件包含以下 HTML 文档：

    - 订单确认模板
    - 颁发礼品卡模板
    - 新订单模板
    - 打包订单模板
    - 选择订单模板

1. 使用文本编辑器或 HTML 编辑器自定义模板。 请参阅本主题后面的[支持的标志](#supported-tokens-in-the-email-template)列表。
1. 登录 Commerce。
1. 使用左侧菜单转到 **模块 \> 组织管理 \> 设置 \> 组织电子邮件模板**。
1. 展开左侧列表查看所有模板。
1. 对于您要自定义的每个模板，请按照下列步骤操作：

    1. 在列表中选择模板。
    1. 在 **电子邮件内容** 下，在列表中选择相应语言版本。 （默认语言为 **en-us**。）
    1. 在 **电子邮件内容** 下，选择 **编辑**。 **上载电子邮件模板** 窗格将出现。
    1. 选择 **浏览**，找到具有自定义内容的 HTML 文件。
    1. 选择 **上载**。 您的模板将上载到系统，并显示预览。
    1. 选择 **确定**。
    1. 可选：自定义模板的 **主题** 属性。
    1. 选择 **保存**。

### <a name="supported-tokens-in-the-email-template"></a>电子邮件模板中支持的令牌

呈现电子邮件时，这些标志将替换为应用于客户和客户订单的实际值。

#### <a name="sales-order"></a>销售订单

以下标志应用于整个销售订单。

| 令牌的名称 | 标志 |
|-------------------|-------|
| 转移单编号      | %salesid% |
| 客户名称   | %customername% |
| 交货地址  | %deliveryaddress% |
| 帐单地址   | %customeraddress% |
| 订单日期        | %shipdate% |
| 交货模式     | %modeofdelivery% |
| 折扣          | %discount% |
| 增值税         | %tax% |
| 订单合计       | %total% |

#### <a name="sales-line"></a>销售行

以下标志由订单中每个产品的值替换。

> [!NOTE]
> 将 **产品列表 - 开始** 标志放在对每个产品重复的 HTML 块的开头，并将 **产品列表 - 结束** 标志放在块的末尾。

| 令牌的名称      | 标志 |
|------------------------|-------|
| 产品列表 - 开始   | \<!--%tablebegin.salesline% --\> |
| 产品列表 - 结束     | \<!--%tableend.salesline%--\> |
| 产品名称           | %lineproductname% |
| 说明            | %lineproductdescription% |
| 数量               | %linequantity% |
| 行单价        | %lineprice%（验证） |
| 行项总数        | %linenetamount% |
| 行折扣          | %linediscount% |
| 装运日期              | %lineshipdate% |
| 采购方法     | %linedeliverymode% |
| delivery address / 交货地址       | %linedeliveryaddress% |
| 行的销售单位 | %lineunit% |

## <a name="additional-resources"></a>其他资源

[Dynamics 365 Commerce 评估环境概览](cpe-overview.md)

[预配 Dynamics 365 Commerce 评估环境](provisioning-guide.md)

[配置 Dynamics 365 Commerce 评估环境](cpe-post-provisioning.md)

[在 Dynamics 365 Commerce 评估环境中配置 BOPIS](cpe-bopis.md)

[Dynamics 365 Commerce 评估环境常见问题](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure 门户](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce 网站](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]