---
title: 开始使用适用于法国的电子开票加载项
description: 本文提供的信息将帮助您开始使用适用于法国的电子开票附加产品。
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220640"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>开始使用适用于法国的电子开票加载项

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

本文提供的信息将帮助您开始使用适用于法国的电子开票。 指导您完成 Regulatory Configuration Service (RCS) 中与国家/地区相关的配置步骤。 这些步骤补充了[开始使用电子开票附加产品](e-invoicing-get-started.md)中描述的步骤。

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>法国 Chorus Pro 提交 (FR) 电子开票功能的国家/地区特定配置

配置 **法国 Chorus Pro 提交 (FR)** 电子开票功能需要执行某些步骤。 配置中的一些参数使用默认值发布。 必须查看和更新这些值，以便它们能够更好地反映您的业务运营。

### <a name="prerequisites"></a>先决条件

在开始本文中的过程之前，请完成以下先决条件：

- 熟悉电子开票。 有关详细信息，请参阅[电子开票概览](e-invoicing-service-overview.md)。
- 注册 RCS，并设置电子开票。 有关详细信息，请参阅以下文章：

    - [注册并安装电子开票服务](e-invoicing-sign-up-install.md)
    - [设置电子开票的 Azure 资源](e-invoicing-set-up-azure-resources.md)
    - [在 Lifecycle Services 中安装微服务的加载项](e-invoicing-install-add-in-microservices-lcs.md)
    - [激活和设置与电子开票的集成](e-invoicing-activate-setup-integration.md) – 使用本文中的信息激活 Microsoft Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 应用与电子发票服务之间的集成。
    - [NAF 代码和 Siret 号码](emea-fra-naf-codes-siret-numbers.md)和[设置 NAF 代码和 Siret 号码](tasks/fr-00003-naf-codes-siret-numbers.md) - 使用这些文章中的信息在您的法人中设置 NAF 代码和 Siret 号码。 

- 必须注册您的组织才能使用 Chorus Pro 运营。 Microsoft 通过应用编程接口 (API) 在 OAuth2 模式下提供与 Chorus Pro 的集成。 有关 Chorus Pro 注册和应用程序激活的详细信息，请参阅[正式文档](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/)。

    按照以下步骤注册 Chorus Pro。

    1. 转到 [PISTE 门户](https://piste.gouv.fr/en/component/apiportal/registration)以开始注册。 
    2. 注册应用程序并激活 Open Authorization (OAuth) 凭据。
    3. 复制并保存 OAuth 凭据和密钥的客户端 ID。 您将在以后的步骤中使用此信息。
    4. 转到 [Chorus Pro 门户](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment)以进行注册。 
    5. 创建 API 访问技术帐户。 有关详细信息，请参阅[在生产中创建 API 访问技术帐户](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/)。
    6. 复制技术帐户的用户 ID 和密码。 您将在以后的步骤中使用此信息。

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>法国 Chorus Pro 提交 (FR) 电子开票功能的应用程序设置的国家/地区特定配置

**法国 Chorus Pro 提交 (FR)** 电子开票功能的一些参数使用默认值发布。 在将电子开票功能部署到服务环境之前，请查看和更新默认值并根据需要进行更新，以便它们更好地反映您的业务操作。

1. 在 Azure 密钥保管库中，创建机密和对它们的相应引用。 有关详细信息，请参阅[客户证书和机密](e-invoicing-customer-certificates-secrets.md)。
2. 导入最新版本的 **法国 Chorus Pro 提交 (FR)** 全球化功能，如[从全局存储库导入功能](e-invoicing-import-feature-global-repository.md)中所述。
3. 创建导入的全球化功能的副本，并选择您的配置提供程序。 有关详细信息，请参阅[创建全球化功能](e-invoicing-create-new-globalization-feature.md)。
4. 在 **版本** 选项卡上，验证是否已选择 **草稿** 版本。
5. 在 **设置** 选项卡上的网格中，选择 **派生的 UBL 销售发票** 功能设置。
6. 选择 **编辑**，然后在 **处理管道** 选项卡上的 **处理管道** 部分中，选择操作名称为 **法国 Chorus Pro 提交** 的 **（预览版）与法国 Chorus Pro 集成**。
7. 在 **参数** 部分中的 **客户端 ID 密码名称** 字段中，选择您在密钥保管库中为客户端 ID 创建的密码名称。
8. 在 **客户端密码名称** 字段中，选择您在密钥保管库中为客户端密码创建的密码名称。
9. 在 **技术登录密码名称** 字段中，选择您在密钥保管库中为技术帐户登录创建的密码名称。
10. 在 **技术密码名称** 字段中，选择您在密钥保管库中为技术帐户密码创建的密码名称。
11. 在 **处理管道** 选项卡上的 **处理管道** 部分中，选择操作名称为 **法国 Chorus Pro 请求状态** 的 **与法国 Chorus Pro 集成**。
12. 在 **参数** 部分中的 **客户端 ID 密码名称** 字段中，选择您在密钥保管库中为客户端 ID 创建的密码名称。
13. 在 **客户端密码名称** 字段中，选择您在密钥保管库中为客户端密码创建的密码名称。
14. 在 **技术登录密码名称** 字段中，选择您在密钥保管库中为技术帐户登录创建的密码名称。
15. 在 **技术密码名称** 字段中，选择您在密钥保管库中为技术帐户密码创建的密码名称。
16. 选择 **保存**，然后关闭页面。
17. 重复步骤 6 到 16，以进行 **派生的 UBL 项目发票** 功能设置、**派生的 UBL 销售贷方通知单** 功能设置和 **派生的 UBL 项目贷方通知单** 功能设置。

## <a name="additional-resources"></a>其他资源

- [电子开票加载项概览](e-invoicing-service-overview.md)
- [开始使用电子开票加载项服务管理](e-invoicing-get-started-service-administration.md)
- [开始使用电子开票加载项](e-invoicing-get-started.md)
