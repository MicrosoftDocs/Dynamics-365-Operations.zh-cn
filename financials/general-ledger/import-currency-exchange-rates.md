---
title: "导入币种汇率。"
description: "如果在接收外汇法人，转换为发票外汇本币是必需的。 这意味着需要不同币种的最新汇率。 此主题为导入外汇参考费率提供所要求的设置和流程概览发布到 Internet 汇率按提供程序，例如 Europe 和央行俄罗斯的主办银行。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>导入币种汇率。

如果在接收外汇法人，转换为发票外汇本币是必需的。 这意味着需要不同币种的最新汇率。 此主题为导入外汇参考费率提供所要求的设置和流程概览发布到 Internet 汇率按提供程序，例如 Europe 和央行俄罗斯的主办银行。

以下各节介绍为设置和处理外汇比率导入的信息流。

## <a name="configure-an-exchange-rate-provider"></a>汇率配置提供程序
在汇率可以导入之前，必须安装提供程序需要提供汇率的信息。 **使用汇率"配置提供程序**页可以选择汇率提供程序。 汇率某些程序提供随附的演示数据。工序 365 的 Microsoft Dynamics 中。 下表介绍已针对控制措施{{在此：on}}页。

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | 汇率提供方的名称。                                                                                                                                                                                     |
| ** **参数   | 提供方所需的每条配置信息的唯一标识符。 此信息。每汇率提供程序自动添加您添加您什么时候单击** **添加按钮。 |
| **Value** | 每个参数的信息。 此信息。每汇率提供商添加您添加您什么时候单击** **添加按钮。                                                                                         |

## <a name="import-currency-exchange-rates"></a>导入币种汇率。
您可以导入从汇率提供程序源的汇率，并为它们在**币种汇率**页。 **使用导入币种汇率**页面导入汇率。 下表介绍要求成功完成导入过程的字段。

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | 的汇率为类型。                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | 汇率提供程序。                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | 此参数是管理"导入截至今天日期或某日期范围。 如果要使用日期范围，请输入或选择开始日期和结束日期。                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | 此复选框可以对自动创建，管理币种，则导入的币种对不存在。 此选项可能不可用。为某些提供程序。                                                                                                                                                                                               |
| **Override existing exchange rates**   | 在汇率，特定日期已存在时，此复选框可管理现有汇率的更新一个对的币种。 如果您没有选中此复选框，则不会导入特定日期的汇率，如果有另的汇率为已存在。                                                                                       |
| **Prevent import on national holiday** | 此复选框可以管理的汇率、导入是一个日的日期。 例如，如果您选中此复选框并使用央行欧洲为汇率提供程序，系统在与当前的法人一个日、不会更新汇率。 此选项可能不可用。为某些提供程序。 |




