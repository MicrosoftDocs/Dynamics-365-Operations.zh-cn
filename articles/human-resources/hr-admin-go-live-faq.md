---
title: 实施常见问题
description: 本主题列出了有关如何实行 Dynamics 365 Human Resources 实施项目的常见问题。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c449ae6eb84fb4150072c386d02b100ca3cca219
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067218"
---
# <a name="go-live-faq"></a>实施常见问题 


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



本主题列出了有关如何实行 Dynamics 365 Human Resources 实施项目的常见问题。 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>何时可以配置和请求生产环境？ 

通常，在满足以下条件后才部署生产环境：

- 所有自定义都是代码完成的。
- 用户验收测试 (UAT) 已完成。
- 客户已签核解决方案。
- 实行没有任何锁定问题。 

当符合条件的客户处于此阶段时，Microsoft FastTrack 团队将与项目团队一起进行实行评估。 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>部署生产环境的先决条件是什么？ 

有关先决条件的列表，请参阅 [准备实行](hr-admin-go-live-prepare.md)。 

## <a name="what-is-a-go-live-assessment"></a>什么是实行评估？  

实行评估是 [Microsoft FastTrack 计划](/dynamics365/fasttrack/)的一部分。 在此审查中，解决方案架构师会评估实施项目是否已准备就绪，可以成功地进行直接转换和实行。 必须对每个实施项目执行此审查，才能请求在生产环境中实行。 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>我们的沙盒环境已在美国中部数据中心中部署。 我们希望在美国西部数据中心中部署生产环境。 我可以在生产配置中选择美国西部作为数据中心吗？ 

在部署 Human Resources 环境时，LCS 不会限制您选择其他数据中心，但是我们强烈建议您不要选择其他数据中心。  

如果您希望生产环境位于美国西部数据中心，则应首先将沙盒环境重新部署到美国西部数据中心，对其进行测试，然后签核。 

有关选择正确的数据中心的信息，请参阅[网络要求](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements)。 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>我对 Human Resources 环境的 Azure 资源具有什么级别的访问权限？  

对 Human Resources 环境的访问受到限制。 您无法访问虚拟机 (VM) 或 Microsoft Internet Information Services (IIS)。 您也无法通过 Microsoft SQL Server Management Studio 访问数据库。 

尽管您无法直接访问 Azure 资源或 Dynamics 365 Human Resources 环境，但您可以使用其他功能来访问数据：

- 您可以在自己的 Azure 租户中部署 Azure SQL 数据库，并使用提供您自己的数据库 (BYOD) 功能来同步数据。 有关详细信息，请参阅[提供您自己的数据库 (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)。

- 您可以使用 Dataverse 集成以将选定的实体同步到 Dataverse 数据库。 有关详细信息，请参阅 [Dataverse 表](hr-developer-entities.md)。 

## <a name="how-often-is-my-production-database-backed-up"></a>生产数据库多久备份一次？ 

通过以下频率的自动备份保护数据库：

| 备份类型 | 频率 |
| --- | --- |
| 完整数据库备份 | 每周 |
| 差异数据库备份 | 每 12-24 小时 |
| 交易日志备份 | 每 5 至 10 分钟 |

Microsoft 保留足够的备份，以允许过去 14 天内的时间点还原 (PITR)。 

有关详细信息，请参阅 [了解自动 SQL 数据库备份](/azure/azure-sql/database/automated-backups-overview?tabs=single-database)。 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>我可以请求生产数据库备份的副本吗？ 

编号 但是，您可以提交数据库刷新服务请求，以将生产环境复制到沙盒环境。 您可以在自己的 Azure 租户中部署 Azure SQL 数据库，并使用 BYOD 功能来同步生产环境中的数据。 有关详细信息，请参阅[提供您自己的数据库 (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)。 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>如何将沙盒环境移动到生产环境以供实行？ 

由于无法使用复制功能将环境从沙盒移动到生产环境，因此必须使用数据包将数据移动到生产环境中。  

我们建议在整个项目中维护在您的沙箱中配置的实体的清除列表。 然后，测试实行所需的所有数据包的直接转换和迁移流程。 在准备实行时，必须手动将所有数据包移动到生产环境中。 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>如果生产环境出现故障，该怎么办？ 

若要报告生产中断，请按照 [报告生产中断](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md)中介绍的流程操作。 

 ## <a name="see-also"></a>请参阅

 [准备实施](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
