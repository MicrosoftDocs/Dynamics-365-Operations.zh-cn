---
title: Finance Insights 的配置
description: 本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。
author: ShivamPandey-msft
ms.date: 11/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6183e8a7500e9deff0ebf6b5dec8842ad4ca94cb
ms.sourcegitcommit: 6a9f068b59b62c95a507d1cc18b23f9fd80a859b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2021
ms.locfileid: "7827020"
---
# <a name="configuration-for-finance-insights"></a>Finance Insights 的配置

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights 组合了 Microsoft Dynamics 365 Finance 的功能和 Dataverse、Azure 和 AI Builder，以便为贵组织提供强大的预测功能。 本主题介绍的配置步骤用于让系统使用 Finance Insights 中的可用功能。 要成功完成本主题中的过程，您必须在 [Power Portal 管理中心](https://admin.powerplatform.microsoft.com/)具有系统管理员和系统定制员访问权限，在 Dynamics 365 Finance 中具有系统管理员访问权限，并在 Microsoft Dynamics Lifecycle Services (LCS) 中具有创建环境的访问权限。

> [!NOTE]
> 以下设置 Finance Insights 的过程适用于 Dynamics 365 Finance 版本 10.0.21 及更高版本。

## <a name="deploy-dynamics-365-finance"></a>部署 Dynamics 365 Finance

按照以下步骤部署环境。

1. 在 LCS 中，创建或更新 Dynamics 365 Finance 环境。 此环境需要应用版本 10.0.21 或更高版本。

    > [!NOTE]
    > 此环境必须是高可用性 (HA) 环境。 （这种类型的环境也称为二级环境。）有关详细信息，请参阅[环境规划](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)。

2. 如果您要在沙盒环境中配置 Finance Insights，可能必须将生产数据复制到该环境，预测才能够工作。 预测模型使用多年的数据来生成预测。 Contoso 演示数据包含的历史数据不足以充分定型预测模型。 

## <a name="configure-your-azure-ad-tenant"></a>配置您的 Azure AD 租户

必须配置 Azure Active Directory (Azure AD)，以便它可以与 Dataverse 和 Microsoft Power Platform 应用程序一起使用。 此配置要求将 **项目负责人** 角色或 **环境管理员** 角色分配给 LCS 内 **项目安全角色** 字段中的用户。

验证以下设置是否已完成：

- 您在 Power Portal 管理中心具有 **系统管理员** 和 **系统定制员** 访问权限。
- Dynamics 365 Finance 许可证或等效许可证适用于正在安装 Finance Insights 加载项的用户。

已在 Azure AD 中注册以下 Azure AD 应用。

|  申请                             | 应用程序 ID                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>配置 Dataverse

按照以下步骤为 Finance Insights 配置 Dataverse。

- 在 LCS 中，打开环境页面，验证是否已设置 **Power Platform 集成** 部分。

    - 如果已经设置 Dataverse，则应该列出链接到 Finance 环境的 Dataverse 环境名称。
    - 如果尚未设置 Dataverse，请选择 **设置**。 设置 Dataverse 环境最多可能需要一个小时。 设置成功完成后，应该会列出 Finance 环境中链接到的 Dataverse 环境名称。
    - 如果已用现有 Microsoft Power Platform 环境设置了此集成，请与您的管理员联系以确保链接的环境未处于禁用状态。

        有关详细信息，请参阅[启用 Power Platform 集成](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)。 

        要访问 Microsoft Power Platform 管理员站点，请转到 <https://admin.powerplatform.microsoft.com/environments>。

## <a name="configure-the-finance-insights-add-in"></a>配置 Finance Insights 加载项

如果之前安装了 Finance insights 加载项，请先卸载，然后再完成以下过程。

> [!NOTE]
> 如果您已经在 LCS 中安装了 Data Lake 加载项，Finance insights 将使用它来保存预测所需的数据。 如果您尚未在 LCS 中安装 Data Lake 加载项，Finance insights 加载项将为您创建一个托管 Data Lake。

按照以下步骤安装 Finance Insights 加载项。

1. 登录到 LCS，然后在页面右侧的环境名称下，选择 **完整详细信息**。
2. 在 **环境加载项** 部分中，选择 **安装新加载项**。
3. 选择 **Finance Insights** 加载项。
4. 同意条款和条件，然后选择 **安装**。

安装加载项可能需要几分钟时间。

## <a name="one-last-thing"></a>最后一件事...

加载项成功安装后，您最多可能需要在一个小时后可以在 Dynamics 365 Finance 中的 **功能管理** 工作区中启用 Finance insights 功能。 如果您不想等待这段时间，可以手动运行 **见解预配状态检查** 流程。 

1. 在 Dynamics 365 Finance 中，转到 **系统管理 \> 设置 \> 流程自动化**。
2. 在 **后台流程** 选项卡上，找到 **见解预配状态检查**，选择 **编辑**。
3. 将 **下一次执行** 字段设置为当前时间前 30 分钟。

   此更改应会强制 **见解预配状态检查** 流程立即运行。

   **见解预配状态检查** 流程成功运行后，您可以在 **功能管理** 工作区中启用 Finance insights 功能。

## <a name="feedback-and-support"></a>反馈和支持

如果您对提供反馈感兴趣，或者如果您需要支持，请向 [Finance Insights（预览）](mailto:fiap@microsoft.com)发送电子邮件。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
