---
title: 解决初始设置过程中的问题
description: 本主题提供可以帮助您解决在双写入集成的初始设置期间所发生问题的信息。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 9ffb1378eccf175fbb9bd84228f91ba606125a63
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753982"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>解决初始设置过程中的问题

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决在双写入集成的初始设置期间可能发生的问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>您无法将 Finance and Operations 应用链接到 Dataverse

**设置双写入所需的角色：** Finance and Operations 应用和 Dataverse 中的系统管理员。

**设置到 Dataverse 的链接** 页面上的错误通常是由不完整的设置或权限问题引起的。 请在 **设置到 Dataverse 的链接** 页面上通过了整个运行状况检查，如下图所示。 除非整个运行状况检查通过，否则您无法链接双写入。

![成功的运行状况检查](media/health_check.png)

您必须具有 Azure AD 租户管理员凭据才能链接 Finance and Operations 和 Dataverse 环境。 链接环境后，用户可以使用其帐户凭据登录并更新现有表映射。

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>当您打开“链接到 Dataverse”页面时出错

**解决此问题所需的凭据：** Azure AD 租户管理员

当您在 Finance and Operations 应用中打开 **链接到 Dataverse** 页面时，您可能会收到以下错误消息：

*响应状态代码未指示成功：404（未找到）。*

当同意步骤尚未完成时，将发生此错误。 若要验证同意步骤是否已完成，请使用 Azure AD 租户管理员帐户登录 portal.Azure.com，然后查看具有 ID **33976c19-1db5-4c02-810e-c243db79efde** 的第三方应用是否出现在 Azure AD **企业应用程序** 列表中。 如果未出现，您必须向应用提供同意表示。

要向应用提供同意表示，请按照以下步骤操作。

1. 使用您的管理员凭据打开以下 URL。 应会提示您同意。

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. 选择 **接受** 指示您同意在您的租户中安装具有 ID **33976c19-1db5-4c02-810e-c243db79efde** 的应用。

    > [!TIP]
    > 需要此应用才能链接 Dataverse 和 Finance and Operations 应用。 如果您在执行此步骤时遇到问题，请以匿名模式（在 Google Chrome 中）或隐私模式（在 Microsoft Edge 中）打开浏览器。

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>验证链接期间是否正确设置了公司数据和双写入团队

为确保双写入正常工作，将在 Dataverse 环境中创建您在配置过程中选择的公司。 默认情况下，这些公司是只读的，**IsDualWriteEnable** 属性设置为 **True**。 此外，还将创建默认的负责业务单位负责人和团队，并包括公司名称。 在启用映射之前，请验证是否已指定默认团队负责人。 要查找 **公司(CDM\_公司)** 表，请按照以下步骤操作。

1. 在 Dynamics 365 中的模型驱动应用中，选择右上角的筛选器。
2. 在下拉列表中，选择 **公司**。
3. 选择 **运行** 查看结果。
4. 选择配置双写入时链接的公司。
5. 验证 **默认负责团队** 列是否具有值。 在下图中，**默认负责团队** 列设置为 **USMF 双写入**。

    ![验证默认负责团队](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>查找可以为双写入链接的法人或公司的数量限制

当您尝试启用映射时，您可能会收到以下错误消息：

*双写入失败 - 插件注册失败：\[（无法获取项目的分区映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea。错误超出了映射 DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea 允许的最大分区）\]，发生一个或多个错误。*

链接环境时的当前限制约为 40 个法人。 如果您尝试启用映射，并且在环境之间链接了超过 40 个法人，将发生此错误。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]