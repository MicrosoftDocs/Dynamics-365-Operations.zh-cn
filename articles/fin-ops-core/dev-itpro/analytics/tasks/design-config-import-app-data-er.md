---
title: 设计 ER 配置以分析传入单据
description: 此过程显示如何设计电子报告 (ER) 配置以分析传入电子单据。
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8068850ee143540ff9f3b6222485d3ecd2a2a82020063f34cfd7b5a69826eda3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756373"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>设计 ER 配置以分析传入单据

[!include [banner](../../includes/banner.md)]

此过程显示如何设计电子报告 (ER) 配置以分析传入电子单据。 在此过程中，将导入已为示例公司 Litware 公司创建的所需 ER 配置，并用于分析传入的电子单据。 为了完成此过程中的步骤，您必须首先完成“ER 创建配置提供商并标记为有效”这一过程。

此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。

可使用任何数据集完成这些步骤。 首先，请下载并保存“分析传入的文档以更新申请表数据”主题中列举的文件（[分析传入文档](../parse-incoming-electronic-documents.md)）。 文件为：EFSTA model.xml、EFSTA format.xml、Response1.xml、Response2.xml、Response3.xml、Response4.xml。

1. 转到“组织管理”>“工作区”>“电子申报”。
    * 确保示例公司 Litware 公司的配置提供程序可用且标记为“有效”。 如果没有看到此配置提供程序，请首先完成“创建配置提供程序并标记为有效”这一过程中的步骤。
2. 选择申报配置。
    * 以下方案将用于显示分析 XML 格式传入电子文档的功能：ERP 应用程序从 Web 服务（如 [efsta](http://efsta.org/) fiscal service）请求数据并分析传入的响应以相应地更新应用程序数据。 为实现最有效的分析方式，使用单个 ER 格式，尽管预期的 XML 格式的传入文档具有不同结构。

## <a name="import-and-review-er-configurations"></a>导入和查看 ER 配置

导入包含专门用于存储传入文件详细信息的示例数据模型的 ER 模型配置。

1. 选择交换。
2. 选择从 XML 文件加载。
    * 选择“浏览”并选择 EFSTA model.xml 文件。
3. 选择确定。
4. 在树结构中，选择“EFSTA 模型”。
5. 选择设计器。
    * 检查所导入数据模型的结构。 enumType 枚举被定义为识别以下服务响应类型：获取有关交易记录提交的确认，获取有关提交的上次交易记录的信息，以及识别不支持的响应类型。
6. 在树中，展开“Response”。
    * 定义根项目“响应”以指定必须从支持的服务响应获取哪类数据来相应地更新应用程序数据。
7. 关闭该页面。
    * 您将导入 ER 格式配置，其指定如何分析传入文档以在 ER 数据模型中存储数据。
8. 选择交换。
9. 选择从 XML 文件加载。
    * 选择“浏览”并选择 EFSTA format.xml 文件。
10. 选择确定。
11. 在树结构中，展开“EFSTA 模型”。
12. 在树结构中，选择“EFSTA 模型\EFSTA 格式”。
13. 选择设计器。
14. 选择“展开/折叠”。
    * CASE 格式元素被用作根，并包含三个嵌套的 FILE 元素，也就是说，此格式被设计为分析多个格式的传入文件。
15. 在树中，选择“Responses\Transaction completion\TraC”。
    * 有关提交的交易记录的响应从“TraC”根元素开始。
16. 在树中，选择“Responses\Last transaction request\Tra”。
    * 有关提交的最后一个交易记录的响应从“Era”根元素开始。
17. 在树中，选择“Responses\Unexpected response\Text”。
    * 具有嵌套的 TEXT 元素的第三个 FILE 元素已添加，以用于识别不同于上面提到的响应的任何其他响应类型。
18. 选择”将格式映射到模型“。
    * 此模型映射包含数据流的定义以使用数据模型的项目存储分析后的传入文档的详细信息。
19. 选择设计器。
20. 在树中，展开“格式”。
21. 在树中，展开“format\Responses: Case(Responses)”。
    * 检查“格式”数据源的结构。 所有三个响应类型均单独提供。
22. 在树中，选择“format\Responses: Case(Responses)\aType”。
    * 数据源项目“aType”已添加用以指示响应类型，并绑定到数据模型项目“类型”。
23. 选择“验证”选项卡。
24. 在树中，选择“类型 = format.Responses.aType”。
    * ER 验证已配置，用以通知用户响应结构与交易记录的提交确认或与上次提交的交易记录的信息不匹配的情况（不支持的响应案例）。
25. 关闭该页面。

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>运行为分析传入文件配置的 ER 格式的模型映射

您将为测试运行创建的模型映射，以了解配置的 ER 格式如何分析传入的服务响应。 此步骤使用不同的 XML 文件来模拟不同的 Web 服务响应类型。

1. 在 xml 阅读器（如 web 浏览器）中打开 Response1.xml 文件。 此文件包含有关已完成交易的确认详细信息（“TraC”是根元素）。
2. 选择运行。
    * 选择“浏览”并选择 Response1.xml 文件。
3. 选择确定。
    * 检查生成的输出。 已正确识别并解析响应类型（`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` 表示交易完成案例）。
    * 在 XML 阅读器中打开 Response2.xml 文件。 此文件包含有关上次提交的交易记录的信息（`Tra` 是根元素）。
4. 选择运行。
    * 选择“浏览”并选择 Response2.xml 文件。
5. 选择确定。
    * 检查生成的输出。 已正确识别并解析响应类型（`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` 表示系统重启案例）。
    * 在 XML 阅读器中打开 Response3.xml 文件。 此文件从 TraZ 根项目开始，并且此结构不使用 ER 格式配置。
6. 选择运行。
    * 选择“浏览”并选择 Response3.xml 文件。
7. 选择确定。
    * 检查生成的输出。 响应类型已正确识别为不受支持 (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`)。 相应的消息已放入信息日志（根据 ER 验证设置），而且大多数数据模型未填充。
    * 在 XML 阅读器中打开 Response4.xml 文件。 此文件的结构与成功分析的 Response1.xml 几乎是相同的，除了根元素“TraC”的嵌套元素的顺序。
8. 选择运行。
    * 选择“浏览”并选择 Response4.xml 文件。
9. 选择确定。
    * 检查生成的输出。 响应类型已正确识别为不受支持 (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`)。 相应的消息已放入信息日志，并且大多数数据模型未填充。 此行为是此 ER 格式的当前设置假定了某个传入文件根项目的嵌套元素的序列。
10. 关闭该页面。
11. 在树中，选择“Responses\Transaction completion\TraC”。
12. 在“分析嵌套元素的顺序”字段中，选择“任意”。
    * 在“分析嵌套元素的顺序”字段中选择“任意”以允许此根 XML 项目的任何嵌套元素顺序。
13. 选择保存。
14. 选择”将格式映射到模型“。
15. 选择运行。
    * 选择“浏览”并选择 Response4.xml 文件。
16. 选择确定。
    * 检查生成的输出。 响应类型现在已被正确识别为 Response1.xml 文件的同等项。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]