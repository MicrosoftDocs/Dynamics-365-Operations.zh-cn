---
title: 云和本地功能的比较
description: 本文显示在云和本地支持的功能。
author: sericks007
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-29
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 4096089978032f150bf6d711711a948cf1d3232f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879766"
---
# <a name="comparison-of-cloud-and-on-premises-features"></a>云和本地功能的比较

[!include [banner](../includes/banner.md)]

本文显示以下应用程序的可用的云与本地功能的比较：

- [Dynamics 365 Finance](cloud-prem-comparison.md#dynamics-365-finance)
- [Dynamics 365 Supply Chain Management](cloud-prem-comparison.md#dynamics-365-supply-chain-management)
- [Dynamics 365 Commerce](cloud-prem-comparison.md#dynamics-365-commerce)
- [Dynamics 365 Human Resources](cloud-prem-comparison.md#dynamics-365-human-resources)

还包括有关[开发和管理功能](cloud-prem-comparison.md#development-and-administration-features)的信息。

下表列出了应用程序区域。 作为整体列出功能的云和本地支持。 特定功能与总体区域不同时，在“功能”列的单独的行中列出功能。

## <a name="dynamics-365-finance"></a>Dynamics 365 Finance

| **范围**             | **功能**                | **云** | **本地** |
|---------------------|-----------------------------|-----------|-----------------|
| 符合性和证书        |                                                                                           | 是       | 是             |
|                                      | SOC 1 类型 1 认证                                                                | 是       | 否              |
| 数据管理和集成      |                                                                                           | 是       | 是             |
|                                      | 将数据导出到您自己的数据仓库中                                                    | 是       | 是             |
|                                      | 启用将增量更新导出到数据实体                                 | 是       | 是             |
|                                      | 数据集成                                                                         | 是       | 是             |
| 文档管理                  |                                                                                           | 是       | 是             |
| 财务管理                 |                                                                                           | 是       | 是             |
| 帮助                                 |                                                                                           | 是       | 否              |
| 人力资源                      |                                                                                           | 是       | 是             |
| 智能                         |                                                                                           | 是       | 是             |
|                                      | 电子申报 (ER)                                                                 | 是       | 是             |
|                                      | ER：与 LCS 的集成                                                                  | 是       | 否              |
|                                      | ER：与 SharePoint 的集成                                                           | 是       | 否              |
|                                      | ER：与监管配置服务 (RCS) 的集成                              | 是       | 否              |
|                                      | ER：将本地文件系统用作可通过 ER 存储库访问的 ER 配置的存储 | 否        | 是             |
|                                      | 与 PowerBI.com 集成                                                              | 是       | 否              |
|                                      | 与 PowerBI Desktop 集成                                                          | 否        | 是             |
|                                      | 分析工作区                                                                     | 是       | 否              |
|                                      | 智能业务流程：建议                                             | 是       | 否              |
|                                      | 使用 Power BI 桌面或 Excel PowerQuery 工具创作具有 OData 的 Power BI 报表    | 是       | 否              |
|                                      | SQL Server Reporting Services (SSRS) 支持缩放                                 | 是       | 是             |
|                                      | 遥测转变为云                                                   | 是       | 否              |
| Lifecycle Services                   |                                                                                           | 是       | 是             |
|                                      | 可配置的业务流程                                                           | 是       | 否              |
| 本地化                        |                                                                                           | 是       | 是             |
| 移动应用、工作区和平台 |                                                                                           | 是       | 是             |
| Office 集成                   |                                                                                           | 是       | 是             |
| 组织管理          |                                                                                           | 是       | 是             |
| 工资单                              |                                                                                           | 是       | 是             |
|                                      | 直接存款                                                                            | 是       | 否              |
| 项目管理与核算    |                                                                                           | 是       | 是             |
| 安全性                             |                                                                                           | 是       | 是             |
| 服务管理                   |                                                                                           | 是       | 是             |
| Web 客户端                           |                                                                                           | 是       | 是             |
|                                      | 任务录制器 - 从 BPM 库保存或加载任务录制                         | 是       | 否              |
| 支持                              |                                                                                           | 是       | 是             |
|                                      | 通过“帮助和支持”菜单访问支持                                             | 是       | 否              |
|                                      | 业务事件                                                                           | 是       | 是（需要 Internet 连接，或必须实施自定义终结点以在 Intranet 中发送/接收业务事件）              |

## <a name="dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Management 

| **范围**                | **功能**             | **云** | **本地** |
|-------------------------|-------------------|-----------|-----------------|
| 资产管理                     |                                                                                           | 是       | 是             |
| 符合性和证书        |                                                                                           | 是       | 是             |
|                                      | SOC 1 类型 1 认证                                                                | 是       | 否              |
| 成本核算                      |                                                                                           | 是       | 是             |
|                                      | 用于 Power BI 的成本核算内容包                                                 | 是       | 否              |
|                                      | 移动应用的成本核算工作区                                                  | 是       | 否              |
| 成本管理                      |                                                                                           | 是       | 是             |
|                                      | 用于 Power BI 的成本管理内容包                                                 | 是       | 否              |
| 数据管理和集成      |                                                                                           | 是       | 是             |
|                                      | 配置主导的扩展                                                            | 是       | 否              |
|                                      | 将数据导出到您自己的数据仓库中                                                    | 是       | 是             |
|                                      | 启用将增量更新导出到数据实体                                 | 是       | 是             |
|                                      | 数据集成                                                                         | 是       | 是             |
| 文档管理                  |                                                                                           | 是       | 是             |
| 帮助                                 |                                                                                           | 是       | 否              |
| 智能                         |                                                                                           | 是       | 是             |
|                                      | 电子申报 (ER)                                                                 | 是       | 是             |
|                                      | ER：与 LCS 的集成                                                                  | 是       | 否              |
|                                      | ER：与 SharePoint 的集成                                                           | 是       | 否              |
|                                      | ER：与监管配置服务 (RCS) 的集成                              | 是       | 否              |
|                                      | ER：将本地文件系统用作可通过 ER 存储库访问的 ER 配置的存储 | 否        | 是             |
|                                      | 与 PowerBI.com 集成                                                              | 是       | 否              |
|                                      | 与 PowerBI Desktop 集成                                                          | 否        | 是             |
|                                      | 分析工作区                                                                     | 是       | 否              |
|                                      | 智能业务流程：建议                                             | 是       | 否              |
|                                      | 使用 Power BI 桌面或 Excel PowerQuery 工具创作具有 OData 的 Power BI 报表    | 是       | 否              |
|                                      | SQL Server Reporting Services (SSRS) 支持缩放                                 | 是       | 是             |
|                                      | 遥测转变为云                                                   | 是       | 否              |
| 库存管理                 |                                                                                           | 是       | 是             |
| Lifecycle Services                   |                                                                                           | 是       | 是             |
|                                      | 可配置的业务流程                                                           | 是       | 否              |
| 本地化                        |                                                                                           | 是       | 是             |
| 制造                        |                                                                                           | 是       | 是             |
| 主计划和预测      |                                                                                           | 是       | 是             |
| 计划优化                |                                                                                           | 是       | 否              |
| 移动应用、工作区和平台 |                                                                                           | 是       | 是             |
| Office 集成                   |                                                                                           | 是       | 是             |
| 组织管理          |                                                                                           | 是       | 是             |
| 采购             |                                                                                           | 是       | 是             |
|                                      | 从采购申请发包到外部目录                                   | 是       | 否              |
|                                      | 采购花费分析 Power BI 报表                                                  | 是       | 否              |
| 产品信息管理       |                                                                                           | 是       | 是             |
| 基础产品数据                  |                                                                                           | 是       | 是             |
| 生产                           |                                                                                           | 是       | 是             |
|                                      | 生产绩效 Power BI 报表                                                   | 是       | 否              |
| 项目管理与核算    |                                                                                           | 是       | 是             |
| 销售额                                |                                                                                           | 是       | 是             |
|                                      | 销售和收益率绩效 Power BI 报表                                      | 是       | 否              |
| 安全性                             |                                                                                           | 是       | 是             |
| 服务管理                   |                                                                                           | 是       | 是             |
| 供应链管理              |                                                                                           | 是       | 是             |
| 运输管理            |                                                                                           | 是       | 是             |
| 供应商协作                 |                                                                                           | 是       | 否              |
| 仓库管理                 |                                                                                           | 是       | 是             |
|                                      | 移动仓库应用                                                                      | 是       | 是             |
|                                      | 仓库 Power BI 报表                                                              | 是       | 否              |
| Web 客户端                           |                                                                                           | 是       | 是             |
|                                      | 任务录制器 - 从 BPM 库保存或加载任务录制                         | 是       | 否              |
| 支持                              |                                                                                           | 是       | 是             |
|                                      | 通过“帮助和支持”菜单访问支持                                             | 是       | 否              |

## <a name="dynamics-365-commerce"></a>Dynamics 365 Commerce 

若要查看本地部署中提供的功能的列表，请参阅[本地部署中提供的 Commerce 功能](../../../commerce/retail-onprem.md)。

## <a name="dynamics-365-human-resources"></a>Dynamics 365 Human Resources 

| **面积**         | **功能**         | **云** | **本地** |
|------------------|---------------------|-----------|-----------------|
| 所有 Human Resources 区域 | 所有 Human Resources 功能 | 是       | 否              |

## <a name="development-and-administration-features"></a>开发和管理功能

| **面积**                   | **功能**                               | **云** | **本地** |
|----------------------------|-------------------------------------------|-----------|-----------------|
| 构建和测试             |                                           | 是       | 是             |
| 可扩展性              |                                           | 是       | 是             |
| 监控和遥测   |                                           | 是       | 是             |
| 平台兼容性     |                                           | 是       | 是             |
| 服务                  |                                           | 是       | 是             |
|                            | 服务环境                    | 是       | 否              |
| 跟踪分析器               |                                           | 是       | 是             |
| PerfTimer                  |                                           | 是       | 是\*           |
| 升级                    |                                           | 是       | 是             |
|                            | 升级                                   | 是       | 否              |
|                            | 以前版本的升级和支持 | 是       | 否              |
| Visual Studio 开发  |                                           | 是       | 是             |

\*在本地环境中，PerfTimer 仅显示客户端的结果。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
