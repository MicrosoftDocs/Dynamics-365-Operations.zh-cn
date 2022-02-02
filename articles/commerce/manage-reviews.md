---
title: 管理评分和评价
description: 本主题介绍了如何在 Microsoft Dynamics 365 Commerce 站点构建器中选择管理评分和评价。
author: gvrmohanreddy
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1aefa6eb93ef251778a48ba972d87e0cd5930bf0
ms.sourcegitcommit: 7adf9ad53b4e6d1c4d5d612ce0977b76c61ec173
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/13/2022
ms.locfileid: "7968219"
---
# <a name="manage-ratings-and-reviews"></a>管理评分和评价

[!include [banner](includes/banner.md)]

本主题介绍了如何在 Microsoft Dynamics 365 Commerce 站点构建器中选择管理评分和评价。

Dynamics 365 Commerce 使用 Microsoft Azure Cognitive Service 通过修正猥亵词自动审查评价文本。 此外，审查者可以使用 Dynamics 365 Commerce 站点构建器实现以下手动任务：

- 通过响应或删除评级来审查评级
- 在客户的请求下删除客户的评价。
- 将所有产品的评分和评价数据批量导入 Microsoft Power BI 模板中，以便分析评分和评价的趋势。

## <a name="read-a-review"></a>阅读评价 

若要在 Commerce 站点构建器中阅读评价，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 审查**。
1. 可使用页面右上角的搜索字段按产品 ID、产品名或评价文本筛选评价。

可使用更多筛选器按期间、评分、渠道或关注状态（已撤下、已响应或已报告）限制评价。

![审查主页。](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>响应评价 

有时，购买了产品的客户会表示自己满意或不满意，或者不知道如何使用产品。 作为审查者，您可以发布对评价的响应。 此响应和评价一起在站点中显示。 

若要在 Commerce 站点构建器中响应评价，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 审查**。
1. 找到并选择需要响应的评价。
1. 在右侧的属性窗格中，选择 **添加响应**。
1. 输入响应文本和应该对响应者显示的名称。 默认响应者名称为 **审查者**。
1. 当您完成时，选择 **发布响应**。

![响应评价。](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>撤下评价 

有时设立了业务仲裁供审查者撤下客户评价。 

若要在 Commerce 站点构建器中撤下评价，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 审查**。
1. 找到并选择必须撤下的评价。
1. 在右侧的属性窗格中，在 **撤下评价** 下方选择撤下原因，然后选择 **撤下**。
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>在客户的请求下删除客户的评价 

有时，客户希望从电子商务网站中永久删除自己的评分和评价数据。 收到客户的删除请求的注册者可以使用评价删除功能删除客户的数据。 若要找到并删除客户的数据，审查者需要客户用于登录和提供评价的电子邮件地址。 

若要在 Commerce 站点构建器中查找和删除客户数据，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 删除**。
1. 在 **按电子邮件地址搜索用户** 框中，输入客户的电子邮件地址，然后选择 **搜索**。
1. 如果客户进行了任何评价活动（例如，提交评价，对另一位客户的评价是否有帮助投票，或评论了另一位客户的评价），将显示结果。 每项有一个 **删除** 按钮。
1. 为必须删除的每项选择 **删除**。 提示确认时，选择 **是**。 
    
![删除客户数据。](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - 最多可能需要七天，才会从系统中完全删除数据。 审查者应该通知客户存在此延迟。
> - 如果改变了其帐户设置中自己的姓名，搜索结果中可能会显示多项。 在此情况下，要完全删除此客户的数据，审查者必须为各项选择 **删除**。 

## <a name="download-ratings-and-reviews-data"></a>下载评分和评价数据

通过 Commerce 站点构建器，审查者可以批量导入评分和评价数据，以便分析趋势。 提供其中包含基本度量的 Power BI 模板。 审查者可使用此模板连接批量导入的数据和查看仪表板。 不必创建自定义仪表板。 审查者也可以自定义 Power BI 模板满足其具体需求。 

若要在 Commerce 站点构建器中下载评分和评价，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 报告**。
1. 选择 **下载评价数据** 使用逗号分隔的值 (CSV) 格式批量下载评分和评价数据。

## <a name="view-ratings-and-reviews-trends"></a>查看评分和评价趋势

审查者可下载 Power BI 模板，以便在仪表板中查看趋势。

若要在 Commerce 站点构建器中查看评分和评价趋势，请执行以下步骤。

1. 转到 **主页 \> 评价 \> 报告**。
1. 选择 **PowerBI 模板** 下载模板。

    ![下载 Power BI 模板。](media/rnr-moderation-reports.png) 

1. 使用 Power BI 应用打开下载的模板。 关闭显示的 **访问 Web 内容** 对话框，然后关闭显示的“刷新”错误消息。
1. 转到 **主页**，选择 **编辑查询**，然后选择 **数据源设置**。
1. 在 **数据源设置** 对话框中，选择 **更改源**。
1. 在 **URL** 字段中，输入上一过程中下载的评价数据的路径（例如，**c:\\reviews\\ReviewsData.csv**）。

    ![“逗号分隔值”对话框中的 URL 字段。](media/rnr-powerbi-datasource-settings.png) 

1. 选择 **确定**，然后选择 **应用更改**。 需要一到两分钟才能应用对数据源的更改。
1. 选择 **趋势表** 显示评分和评价趋势。

    ![评分和评价趋势。](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>其他资源

[评分和评价概览](ratings-reviews-overview.md)

[选择使用评分和评价](opt-in-ratings-reviews.md)

[配置评分和评价](configure-ratings-reviews.md)

[在 Dynamics 365 Retail 中同步产品评分](sync-product-ratings.md)

[启用审查者手动发布评分和评价](manual-publish-rating-reviews.md)

[导入和导出评分和评价](import-export-reviews.md)

[配置服务对服务身份验证](service-to-service-auth.md)

[评分和评价常见问题解答](ratings-reviews-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
