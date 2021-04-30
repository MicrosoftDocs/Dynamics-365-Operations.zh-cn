---
title: Regulatory Configuration Service
description: 本主题提供 Regulatory Configuration Service (RCS) 功能的概述并说明如何访问服务。
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890792"
---
# <a name="regulatory-configuration-service"></a>Regulatory Configuration Service

[!include [banner](../includes/banner.md)]

Regulatory Configuration Service (RCS) 是用于无代码/低代码全球化功能的独立设计器和生命周期管理服务。 通过 RCS，全球化利益相关者可以扩展和自定义税务、电子开票、监管报告、银行和业务文档的关键全球化区域，而无需开发人员的参与。 此无代码/低代码全球化方法支持更简单、更快且更具成本效益地创建或扩展全球化。

RCS 提供以下功能：

- 支持电子报告 (ER) 提供的所有功能。
- 配置新全球化微服务的先决条件。
- 支持电子开票。 有关详细信息，请参阅[电子开票](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga)。
- 支持税务计算。 有关详细信息，请参阅[税务服务](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview)。
- 支持新全球化功能，用于简化多组件功能的生命周期管理，并提供额外的功能来配置操作和设置功能参数。 有关详细信息，请参阅 [Regulatory Configuration Service – 全球化服务的简化全球化功能管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)。
- 支持在全局存储库中集中发布、存储和共享自定义配置以简化配置管理，而无需使用 Microsoft Dynamics Lifecycle Services (LCS)。

## <a name="access-rcs"></a>访问 RCS

您可以从 [Regulatory Configuration Service 页面](https://marketing.configure.global.dynamics.com/)注册或登录到 RCS。

![RCS 注册/登录](media/202103_RCS%20Marketing%20page_updated_1.jpg)

在 **Regulatory Configuration Service** 页面上，查看并接受使用服务的补充条款和条件，然后选择以下按钮之一：

- **注册**，如果您是首次使用服务的用户，并且您要使用公司电子邮件地址为您的组织预配服务环境
- **登录**，如果您之前已经注册了服务，并且想要访问您的组织环境

## <a name="regional-availability"></a>区域可用性

RCS 在以下地区正式发布：

- 美国
- 印度
- 法国
- 欧洲

有关地区的完整列表，请参阅 [Dynamics 365 和 Power Platform：可用性、数据位置、语言和本地化](https://aka.ms/dynamics_365_international_availability_deck)。

## <a name="related-rcs-documentation"></a>相关的 RCS 文档

有关相关组件的详细信息，请参阅以下文档：

- **全局存储库：**

    - [创建 ER 配置并上传到全局存储库](rcs-global-repo-upload.md)
    - [全局存储库中的共享配置](rcs-global-repo-share-configuration.md)
    - [全局存储库中的增强筛选](enhanced-filtering-global-repo.md)
    - [从全局存储库中下载 ER 配置](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [终止全局存储库中的配置](discontinuing-configurations-rcs-global-repo.md)

- **全球化功能：**

    - [Regulatory Configuration Service (RCS) - 全球化功能](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)