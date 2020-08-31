---
title: 调整基于 AI-ML 的产品建议结果
description: 此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: bc6a793061a3e644599f0882ff163f5f57b2162d
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664946"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a>调整基于 AI-ML 的产品建议结果


[!include [banner](includes/banner.md)]

此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。 

启用产品建议之后，默认设置将生效；这些参数适用于许多需要的许多工作。 最好计划花一些时间评估结果是否符合产品的销售动态。 建议在更改参数前根据需要评估一些天的结果，之后再次测试。 

## <a name="understanding-recommendation-list-parameters"></a>了解建议列表参数

更改参数之前，在下面了解对结果的影响。

### <a name="trending-product-list"></a>“热门”产品列表

“热门”产品列表有两个可更改的参数：

![示例“热门”列表默认参数](./media/exampletrendingparameters.png)

1. **包括过去 X 天的新产品** - 可使用当天前指定天数内已添加的产品选择候选产品。 图片中的默认值表明旧产品已有 180 天，可在热门产品列表中使用。
1. **包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。 上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在热门产品列表中的位置。 

### <a name="best-selling-product-list"></a>“最畅销”产品列表

“最畅销”列表可根据您的业务提供不同于热门的结果，即使两者都使用交易记录数据订购产品。 因为最畅销没有基于分类日期的截止，所以最畅销仍然可以突出显示非常受欢迎，并且可能已从热门列表撤下的较早产品。 

“最畅销”产品列表有一个可更改的参数：

![示例最畅销列表默认参数](./media/examplebestsellingparameters.PNG)

1. **包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。 上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在最畅销产品列表中的位置。 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a>在建议列表中手动添加或删除产品

### <a name="for-new-trending-or-best-selling-lists"></a>对于“新品”、“热门”或“最畅销”列表

1.  转到 **Retail 和 Commerce** > **产品建议** > **建议参数**。
1.  在共享参数列表中，选择**建议列表**。
1.  选择要在其中添加或删除产品的列表。
1.  若要向表添加产品，请选择**添加行**。 
1.  在“产品”列下，按**名称**或**产品编号**搜索产品。

    ![在“新品”产品列表中搜索产品的示例](./media/examplenewlistconfiguration1.png)

1.  在“行类型”列下，选择两个选项之一：
    -   **包含** – 强制产品位于列表前部
    -   **排除** – 在列表中隐藏某个产品。
    
    ![在“新品”产品列表中包含或排除某个产品的示例](./media/examplenewlistconfiguration2.png)

1.  更改**显示顺序**将更改标记为**包含**的产品在列表中的显示顺序。
    - 如果两个产品的**显示顺序**值相同，则这两个结果的最终顺序可能与后端不同。
1.  若要从表中删除产品：选择要删除的行，然后选择**删除**。


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a>对于“用户也喜欢”或“人气组合”列表

在“人气组合”或“用户也喜欢”列表的上下文中，使用机器学习分析消费者购买模式为唯一种子产品推荐通常一起购买的相关产品。 
 
*种子产品*是要生成其结果的产品。 在手动调整建议列表的上下文中，添加或删除此产品的结果。 

执行以下步骤手动添加或删除种子产品的结果：
1.  选择**种子产品**。 
1.  在**产品**列下，按**名称**或**产品编号**搜索产品。
![搜索“人气组合”列表中的产品的示例](./media/exampleFBTlistconfiguration1.png)
1. 在**行类型**列下，选择两个选项之一：
    - **包含** – 强制产品位于列表前部
    - **排除** – 在列表中隐藏某个产品。     
![在“人气组合”列表中包含或排除产品的示例](./media/exampleFBTlistconfiguration2.png)
1.  若要从表中删除产品：选择要删除的行，然后选择删除。


## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用产品建议](enable-product-recommendations.md)

[启用个性化建议](personalized-recommendations.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[在 POS 上添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)
