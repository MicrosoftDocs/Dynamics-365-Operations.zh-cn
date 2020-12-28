---
title: 在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage
description: 本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage，这是启用产品推荐的先决条件。
author: bebeale
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: 27e4f1c751ee865b0df536f3c1912cb1d8946032
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410397"
---
# <a name="enable-azure-data-lake-storage-in-a-dynamics-365-commerce-environment"></a>在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage

[!include [banner](includes/banner.md)]

本主题说明如何针对 Dynamics 365 Commerce 环境启用和测试 Azure Data Lake Storage，这是启用产品推荐的先决条件。

## <a name="overview"></a>概览

在 Dynamics 365 Commerce 解决方案中，所有产品和交易信息都在环境的实体商店中进行跟踪。 为了使此数据可供其他 Dynamics 365 服务（例如数据分析、商业智能和个性化建议）访问，必须将环境连接到客户拥有的 Azure Data Lake Storage 第 2 代解决方案。

由于在环境中配置了 Azure Data Lake Storage，因此从实体商店中镜像了所有必需的数据，同时仍受到保护并在客户的控制之下。

如果在环境中也启用了产品推荐或个性化推荐，则将向产品推荐堆栈授予 Azure Data Lake Storage 中专用文件夹的访问权限，以检索客户的数据并基于该数据计算推荐。

## <a name="prerequisites"></a>先决条件

客户需要在其拥有的 Azure 订阅中配置 Azure Data Lake Storage。 本主题不涉及购买 Azure 订阅或设置启用 Azure Data Lake Storage 的存储帐户。

有关 Azure Data Lake Storage 的详细信息，请参阅 [Azure Data Lake Storage Gen2 官方文档](https://azure.microsoft.com/pricing/details/storage/data-lake)。
  
## <a name="configuration-steps"></a>配置步骤

此部分介绍在环境中启用 Azure Data Lake Storage（当其与产品建议有关时）需要执行的配置步骤。
有关启用 Azure Data Lake Storage 需要执行的步骤的更深度概述，请参阅[将实体商店用作 Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)。

### <a name="enable-azure-data-lake-storage-in-the-environment"></a>在环境中启用 Azure Data Lake Storage

1. 登录到环境的后台办公室门户。
1. 搜索 **系统参数** 并导航到 **数据连接** 选项卡。 
1. 将 **启用 Data Lake 集成** 设置为 **是**。
1. 将 **缓慢更新 Data Lake** 设置为 **是**。
1. 然后，输入以下必需信息：
    1. **应用程序 ID** // **应用程序密钥** // **DNS 名称** - 需要连接到存储 ADLS 密钥的 Azure Data Lake Storage。
    1. **密钥名称** - 密钥名称存储在 KeyVault 中，用于通过 Azure Data Lake Storage 进行身份验证。
1. 将更改保存在页面的左上角。

下图显示了一个 Azure Data Lake Storage 配置示例。

![Azure Data Lake Storage 配置示例](./media/exampleADLSConfig1.png)

### <a name="test-the-azure-data-lake-storage-connection"></a>测试 Azure Data Lake Storage 连接

1. 使用 **测试 Azure 密钥保管库** 链接测试与 KeyVault 的连接。
1. 使用 **测试 Azure 存储** 链接测试与 Azure Data Lake Storage 的连接。

> [!NOTE]
> 如果测试失败，请仔细检查上面添加的所有 KeyVault 信息是否正确，然后重试。

连接测试成功后，必须为实体商店启用自动刷新。

要为实体商店启用自动刷新，请按照下列步骤操作。

1. 搜索 **实体商店**。
1. 在左侧列表中，导航到 **RetailSales** 条目，然后选择 **编辑**。
1. 确保 **启用自动刷新** 设定为 **是**，选择 **刷新**，然后选择 **保存**。

下图显示了启用了自动刷新的实体商店的示例。

![启用了自动刷新的实体商店示例](./media/exampleADLSConfig2.png)

现在为环境配置了 Azure Data Lake Storage。 

如果尚未完成，请按照以下步骤为环境[配置产品推荐和个性化设置](enable-product-recommendations.md)。

## <a name="additional-resources"></a>其他资源

[将实体商店用作 Data Lake](../fin-ops-core/dev-itpro/data-entities/entity-store-data-lake.md)

[产品建议概览](product-recommendations.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)
