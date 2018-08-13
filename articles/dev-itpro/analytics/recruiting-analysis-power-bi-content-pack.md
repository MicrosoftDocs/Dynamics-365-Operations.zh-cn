---
title: "招聘 Power BI 内容"
description: "此主题介绍招聘 Power BI 内容。 它说明如何访问报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 0d6bc8584d202810ed14367d36d113d9b109ea7a
ms.contentlocale: zh-cn
ms.lasthandoff: 12/19/2017

---

# <a name="recruiting-power-bi-content"></a>招聘 Power BI 内容

[!include [banner](../includes/banner.md)]

此主题介绍**招聘** Microsoft Power BI 内容。 它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。

## <a name="accessing-the-power-bi-content"></a>访问 Power BI 内容
**招聘** Power BI 内容显示在**招聘管理**工作区。

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>招聘管理工作区的报表和视觉对象
**招聘管理**工作区包含一个**分析**选项卡。此选项卡包含用于招聘的嵌入的 Power BI 内容。 此内容包括一个概览选项卡和包含详细信息的附加选项卡。 下表对每个选项卡上的报表进行介绍。

| 报告               | 内容 |
|----------------------|----------|
| 招聘概览 | 汇总其他报表 |
| 申请人分析   | 申请人总数、按作业分类的申请人、申请人来源、女性与男性申请人，以及按位置分类的申请人 |
| 申请人状态     | 按类型和状态分类的申请人，以及申请人状态 |
| 招聘分析  | 净雇用比率、平均雇用天数、不良雇用百分百、招聘成本、招聘项目数量、雇用人与申请人的比例，以及各招聘项目的申请人与空缺职位 |

## <a name="understanding-the-data-model-and-entities"></a>了解数据模型和实体
可以筛选这些报表中的图表和磁贴，并将图表和磁贴固定到仪表板。 有关如何在 Power BI 中筛选和固定的更多信息，请参阅[创建和配置仪表板](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)。

下表显示**招聘** Power BI 内容所基于的实体。

| 实体               | 内容                                                         | 与其他实体之间的关系 |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| 申请人            | 申请人、雇用的申请人、净雇用比率，以及成本          | 申请人姓名、公司、日历偏差、日期、地理位置、人口统计学、作业、媒体、招聘项目 |
| 申请人姓名       | 申请人名字、姓氏和全名                   | 申请人、已雇用的申请人、已离职的申请人 |
| 日历偏差      | 要切分的日历偏差报表                                | 申请人、已雇用的申请人、已离职的申请人 |
| 公司              | 充当报表筛选依据的公司                                   | 申请人、已雇用的申请人、已离职的申请人 |
| 日期                 | 天数、周数、月数和年数                                   | 申请人、已雇用的申请人、已离职的申请人 |
| 人口统计数据         | 生日、性别、种族和婚姻状况         | 申请人、已雇用的申请人、已离职的申请人 |
| 已雇用的申请人   | 申请人、表现、开始日期和申请人类型           | 公司、日历偏差、日期、地理位置、申请人姓名、雇用、绩效、作业、媒体、招聘项目 |
| 雇用           | 开始日期、结束日期和转换日期                        | 申请人、已雇用的申请人、已离职的申请人 |
| 地理位置  | 市，县，邮政编码和省/市/自治区                 | 申请人、已雇用的申请人、已离职的申请人 |
| 作业                  | 功能，类型和标题                                        | 申请人、已雇用的申请人、已离职的申请人 |
| 媒体                | 申请人来源                                             | 申请人、已雇用的申请人、已离职的申请人 |
| 绩效          | 评级，描述和评级模型                            | 申请人、已雇用的申请人、已离职的申请人 |
| 招聘项目  | 项目描述、项目状态和空缺                | 申请人、已雇用的申请人、已离职的申请人 |
| 已离职的申请人 | 已离职的申请人、原因、表现和离职日期 | 公司、日历偏差、日期、地理位置、绩效、人口统计数据、雇用、媒体、招聘项目、申请人姓名 |

