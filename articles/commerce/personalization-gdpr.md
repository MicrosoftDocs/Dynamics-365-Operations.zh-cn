---
title: 选择退出个性化产品建议
description: 本主题说明如何在 Microsoft Dynamics 365 Commerce 中让客户选择不接收个性化建议。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a51c8c0e2743b67df9d66a8c45ab7a69597f4002
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664922"
---
# <a name="opt-out-of-personalized-recommendations"></a>选择退出个性化产品建议

[!include [banner](includes/banner.md)]

本主题说明如何在 Microsoft Dynamics 365 Commerce 中让客户选择不接收个性化建议。

## <a name="overview"></a>概览

在创建帐户期间，会自动将新客户设置为接收个性化建议。 但是，Dynamics 365 Commerce 为零售商提供了各种方式，可以让用户可以选择不接收这些建议并限制其对个人数据的处理。 选择不接收个性化建议的经过身份验证的用户会立即无法查看个性化列表。 而且，将从个性化建议模型中删除为个性化收集的所有个人数据。

有关个性化产品建议的详细信息，请参阅[启用个性化建议](personalized-recommendations.md)。

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>零售商实现退出体验的方法

零售商可以通过三种方法实现退出体验。

### <a name="opting-out-on-behalf-of-users"></a>代表用户退出

在 Commerce 后端的“帐户管理”中，零售商可以代表用户选择退出。

1. 在后端主页上搜索**所有客户**。
1. 搜索并选择一个客户，然后选择**零售**快速选项卡。

    ![“零售”快速选项卡](./media/Disablepersonalizationpart1.png)

1. 在**隐私**下，将**禁用个性化设置**选项设置为**是**。

    ![隐私设置](./media/Disablepersonalizationpart2.png)

1. 选择**保存**，然后关闭页面。

### <a name="module-based-opt-out-experience"></a>基于模块的退出体验

零售商可以让经过身份验证的用户自己选择退出个性化建议。 要提供这种退出体验，请将用户退出模块添加到客户帐户的个人资料页面。

### <a name="custom-extensions"></a>自定义扩展

零售商可以创建自己的扩展来管理用户的退出体验。 有关详细信息，请参阅[调用 Retail Server API](e-commerce-extensibility/call-retail-server-apis.md) 和[在线渠道可扩展性](e-commerce-extensibility/overview.md)。

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>代表经过身份验证的用户获取个性化建议数据的数字副本

客户可能希望获取其个人数据的数字副本，并且还希望查看其建议结果的导出视图。 如果客户请求此信息，零售商必须创建一个自定义的扩展，来调用 Retail Server 应用程序编程接口 (API)，以基于客户的客户 ID 从**为您推荐**列表中查询完整结果。 然后可以将结果以逗号分隔值 (CSV) 格式导出并与客户共享。

以下示例显示零售商如何完成此任务。

1. 零售商创建自定义扩展来代表用户提取个人建议数据。 有关如何创建模块、克隆现有模块，调用 Retail Server API 和调用数据操作的信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。
2. 自定义扩展对 **get-recommendations** 核心数据操作进行调用，然后根据列表的要求将所需信息传递给它。 如果是**为您推荐**列表，扩展必须将正确的列表名称和客户 ID 传递给此数据操作。

    创建自定义扩展的一种方法是克隆现有的用于返回建议结果的产品集合模块。 通过克隆此现有模块，零售商可以修改现有代码并添加新按钮，以将建议结果导出到 CSV 文件。 有关详细信息，请参阅[克隆入门套件模块](e-commerce-extensibility/clone-starter-module.md)和[产品集合模块](product-collection-module-overview.md)。

    有关 Retail Server API 库的完整视图，请参见 [Retail Server 客户和用户 API](dev-itpro/retail-server-customer-consumer-api.md)。

3. 创建自定义扩展后，零售商可以根据经过身份验证的用户的唯一客户 ID 导出所有建议结果的 CSV 文件。
4. 零售商可以与经过身份验证的用户共享导出的包含建议产品完整的个性化列表的 CSV 文件。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)
