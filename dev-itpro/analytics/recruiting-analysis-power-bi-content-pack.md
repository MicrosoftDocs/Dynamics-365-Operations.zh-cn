---
title: "招聘 Power BI 的内容"
description: "此主题描述招聘-工序的 Power BI 的内容 Dynamics 365。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>招聘 Power BI 的内容

此主题描述招聘-工序的 Power BI 的内容 Dynamics 365。 该说明如何访问在内容包包括的报表，并提供有关用于创建内容包的数据模型和实体的信息。

<a name="accessing-the-content-pack"></a>访问内容包
--------------------------

您在 Microsoft Dynamics Lifecycle Services (LCS) 可以查找其进行招聘的内容包在共享资产的库中。 有关如何下载内容包和将它连接的详细信息。您的工序数据的 Microsoft Dynamics 365，请参阅在 [LCS 的 Power BI 的内容是从 Microsoft 和您的合作伙伴] (Microsoft partners.md BI 的内容。)

## <a name="reports-that-are-included-in-the-content-pack"></a>内容包包括报表。
在连接内容包到您的工序数据的 Dynamics 365 后，报表查看组织的数据。 如果您选择"从不使用 Microsoft Power BI "，您可以了解在此{{对：about}}引导了解 Power BI 的 [] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) 页。 在内容包包括的报表具有包含附加信息的两个图表和表。 下表对报表进行了描述。

| 报告                       | 内容                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| 申请人分析           | 按工作、申请人源、申请人按位置和申请人总数的申请人           |
| 申请人状态             | 按类型和状态的申请人和申请人状态                                                    |
| 申请人人口统计学       | 教育按级别和按状态的申请人和申请人的性别和年限                             |
| 招聘的分析          | 净雇用比率、平均值坏雇用的天数与雇用，百分比和其进行招聘的成本                    |
| 招聘项目分析 | 招聘项目、申请人和期初由招聘项目编号由招聘项目 |

您可以筛选平铺和图表，这些报表和单边锁定图表和平铺到仪表板。 有关如何筛选和单边锁定的更多信息的详细信息。Power BI，请参阅创建和配置 [] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards) 仪表板。

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
工序数据的 Dynamics 365:用于填充时，会在招聘的内容包的报表。 下表显示实体，内容包基础。

| 实体                          | 内容                                                         | 关系具有其他实体                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 其进行招聘的\_申请人           | 申请人、雇用的净额雇用申请人、费率和成本          | 其进行招聘的\_招聘\_公司的 ApplicantName 招聘\_CalendarOffset Recuriting 日期\_其进行招聘的\_招聘\_人口统计学的招聘 GeographicLocation 招聘\_媒体的\_作业\_招聘 RecruitmentProject                                |
| 其进行招聘的\_ApplicantName       | 申请人名、姓氏全名和                   | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_CalendarOffset      | 为希望将切片报表的偏移日历                                | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_公司             | 筛选报表的公司                                    | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_日期                | 天、周、在职个月和年                                   | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_人口统计学        | 出生日期、性别、婚姻状况血统和种族         | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_EmployedApplicant   | 申请人、性能、开始日期和申请人类型           | 招聘\_的 CalendarOffset 其进行招聘的\_公司招聘\_约会其进行招聘的\_招聘\_ApplicantName 的招聘 GeographicLocation 招聘\_性能的\_雇用招聘招聘\_媒体的\_作业\_招聘 RecruitmentProject          |
| 其进行招聘的\_雇用          | 日期、开始过渡日期和结束日期                        | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_GeographicLocation  | 城市、县、邮政编码和省/市/自治区                 | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_作业                 | 功能、类型和标题                                        | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_媒体               | 申请人源                                              | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_性能         | 等级、该代码的描述和该评级模型                            | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_RecruitmentProject  | 项目表说明、未结和项目状态                | 招聘\_的 EmployedApplicant 其进行招聘的\_申请人\_招聘 TerminatedApplicant                                                                                                                                                               |
| 其进行招聘的\_TerminatedApplicant | 终止、申请人的原因、绩效和结束日期 | 招聘\_的 CalendarOffset 其进行招聘的\_公司招聘\_约会其进行招聘的\_招聘\_性能的 GeographicLocation 招聘招聘\_雇用的\_人口统计学招聘\_招聘 RecruitmentProject 的媒体\_招聘\_ApplicantName |

这些实体用于创建计算度量值。 这些计算度量值随后将用于计算在内容包的关键绩效指标 (KPI) 和报表。 如果您需要对您包括的报表和仪表板的其他计算，可以下载并修改了 Recruiting.pbix LCS 的文件。 此文件是用于创建内容包的默认数据模型。 在您进行了修改后，可以创建包含信息您已添加的有组织内容包和仪表板。

## <a name="additional-resources"></a>其他资源
以下是与实体和构建 Power BI 内容相关的一些有用的链接：

-   [数据实体](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [创建组织内容包](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [使用 Power BI 的数据建模](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [将 Power BI 磁贴添加到工作区](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



