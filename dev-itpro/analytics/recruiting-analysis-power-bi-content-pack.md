---
title: "招聘 Power BI 内容"
description: "此主题描述 Dynamics 365 for Operations - 招聘 Power BI 内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4b12a2c8983cf7bef770417f76df324293f06fb2
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017


---

# <a name="recruiting-power-bi-content"></a>招聘 Power BI 内容

[!include[banner](../includes/banner.md)]


此主题描述 Dynamics 365 for Operations - 招聘 Power BI 内容。 它说明如何访问内容包中包括的报表，并提供有关用于构建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

Microsoft Dynamics Lifecycle Services (LCS) 中的共享资产库内包含招聘内容包。 有关如何下载该内容包并将其连接到您的 Microsoft Dynamics 365 for Operations 数据的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。

## <a name="reports-that-are-included-in-the-content-pack"></a>此内容包中包含的报表
在连接内容包到您的 Dynamics 365 for Operations 数据后，报表将显示组织的数据。 如果您之前从未使用 Microsoft Power BI，请可以通过 [Power BI 的指导学习页](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)了解更多相关信息。 此内容包中包含的报表有图表和表，其中包含更多信息。 下表对报表进行了描述。

| 报告                       | 内容                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| 申请人分析           | 按工作分类的申请人、申请人来源、按位置分类的申请人，以及申请人总数           |
| 申请人状态             | 按类型和状态分类的申请人，以及申请人状态                                                    |
| 申请人人口统计数据       | 按年龄和性别分类的申请人，以及按教育水平和状态分类的申请人                             |
| 招聘分析          | 净雇用比率、平均雇用天数、不良雇用百分百，以及招聘成本                    |
| 招聘项目分析 | 招聘项目数量、按招聘项目分类的空缺，以及按招聘项目分类的申请人 |

可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
Dynamics 365 for Operations 数据用于填充招聘内容包中的报表。 下表显示充当内容包基础的实体。

| 实体                          | 内容                                                         | 与其他实体之间的关系                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 招聘\_申请人           | 申请人、雇用的申请人、净雇用比率，以及成本          | 招聘\_申请人姓名 招聘\_公司 招聘\_日历偏差 招聘\_日期 招聘\_地理位置 招聘\_人口统计数据 招聘\_工作 招聘\_媒体 招聘\_招聘项目                                |
| 招聘\_申请人姓名       | 申请人名字、姓氏和全名                   | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_日历偏差      | 要切分的日历偏差报表                                | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_公司             | 充当报表筛选依据的公司                                   | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_日期                | 天数、周数、月数和年数                                   | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_人口统计数据        | 生日、性别、种族和婚姻状况         | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_雇用的申请人   | 申请人、表现、开始日期和申请人类型           | 招聘\_公司 招聘\_日历偏差 招聘\_日期 招聘\_地理位置 招聘\_申请人姓名 招聘\_雇用 招聘\_表现 招聘\_工作 招聘\_媒体 招聘\_招聘项目          |
| 招聘\_雇用          | 开始日期、结束日期和转换日期                        | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_地理位置  | 市，县，邮政编码和省/市/自治区                 | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_工作                 | 功能，类型和标题                                        | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_媒体               | 申请人来源                                             | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_表现         | 评级，描述和评级模型                            | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_招聘项目  | 项目描述、项目状态和空缺                | 招聘\_申请人 招聘\_雇用的申请人 招聘\_已离职的申请人                                                                                                                                                               |
| 招聘\_已离职的申请人 | 已离职的申请人、原因、表现和离职日期 | 招聘\_公司 招聘\_日历偏差 招聘\_日期 招聘\_地理位置 招聘\_表现 招聘\_人口统计数据 招聘\_雇用 招聘\_媒体 招聘\_招聘项目 招聘\_申请人姓名 |

这些实体用于创建计算度量值。 然后，这些计算的度量值用于计算在数据模型中使用的关键绩效指标 (KPI) 和报表。 如果要在报表和仪表板中包含更多计算，可以从 LCS 下载 Recruiting.pbix 文件并修改。 此文件是用于创建内容包的默认数据模型。 修改后，可以创建包含您已添加的信息的组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





