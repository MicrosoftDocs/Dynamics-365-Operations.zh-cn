---
title: 税务计算参数中的空白税务功能列表
description: 本主题介绍如何解决税款计算参数页面上的税务功能列表空白的问题。
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388545"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>税务计算参数中的空白税务功能列表

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>问题

您在 Regulatory Configuration Service (RCS) 中发布了一项功能，以可以在 Microsoft Dynamics 365 Finance 中使用此功能。 但是，当您打开 Finance，转到 **税务** \> **设置** \> **税务配置** \> **税款计算参数**，尝试在 **功能设置名称** 字段中选择值时，值列表为空。

## <a name="reason"></a>原因

发生此问题通常是因为您的 Finance 环境和 RCS 环境不在同一个租户下。

### <a name="rcs-tenant"></a>RCS 租户

按照以下步骤查找您的 RCS 租户的 ID。

1. 复制完整的 RCS URL。 例如，URL 可能是 `https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`。
2. 打开 InPrivate 浏览器窗口，将 RCS URL 粘贴到地址栏中，然后选择 **Enter**。 您将被定向到登录页面，您可以在其中找到 RCS 租户 ID。 例如，如果登录页面的 URL 是 `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d`，租户 ID 是出现在 `https://login.microsoftonline.com/` 或 **d335a570-a05b-4bc5-8eb3-c42c65f9560d** 之后的信息。

### <a name="finance-environment-tenant-id"></a>Finance 环境的租户 ID

要查找 Finance 环境的租户 ID，请按照查找 RCS 租户所采用的相同步骤进行操作。 但是，复制并粘贴 Finance 环境的完整 URL，而不是完整的 RCS URL。

## <a name="resolution"></a>解决方法

如果两个租户 ID 不同，您将遇到本主题中描述的问题。 如果相同，说明您遇到的是不相关的问题。 在这种情况下，我们建议您与 Microsoft 支持部门联系。

### <a name="solution-1"></a>解决方法 1

将您的 RCS 环境登录到您的 Finance 环境登录的同一租户。 然后创建并发布税务功能。

### <a name="solution-2"></a>解决方法 2

在 RCS 中与 Finance 租户共享税务功能。

1. 在 RCS 中，转到 **全球化功能** \> **税款计算**。
2. 选择要共享的功能，然后在 **组织** 选项卡上，选择 **共享**。
3. 在 **组织域名** 字段中，输入名称。 例如，输入 **contoso.onmicrosoft.com**。
4. 选择 **共享**。

![“与外部组织共享”下拉对话框。](media/ShareTaxFeature.png)
