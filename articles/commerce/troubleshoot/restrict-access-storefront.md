---
title: 在测试或开发过程中限制访问店面
description: 本文说明在进行内部测试或开发时如何限制访问 Microsoft Dynamics 365 Commerce 店面。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: e382f01f82b368ad89f7abf122bf806dca4f0340
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292019"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>在测试或开发过程中限制访问店面

[!include [banner](../../includes/banner.md)]

本文说明在进行内部测试或开发时如何限制访问 Microsoft Dynamics 365 Commerce 店面。

## <a name="description"></a>说明

在内部测试或主动开发期间，您可能希望限制对站点的访问，以防止外部用户访问已发布的店面页面。

## <a name="resolution"></a>解决方法

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>使用标准用户流设置 Azure AD B2C

有关如何为电子商务站点配置 Azure Active Directory B2C (Azure AD B2C) 的信息，请参见[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)。

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>限制用户访问店面页面并阻止创建新用户

要限制用户访问 Commerce 站点构建器中的店面页面，请按照下列步骤操作。

1. 转到您的站点。
1. 选择 **页面**，然后选择限制用户访问的页面。
1. 选择模块或片段插槽，然后选择 **编辑**。
1. 在属性窗格中，选择 **需要登录？**，然后选择 **完成编辑**。
1. 选择 **发布**。

若要阻止在 Azure AD 中创建新用户，请按照以下步骤操作。

1. 转到 [Azure 门户](https://portal.azure.com/)。
1. 选择您为站点访问而创建的 Azure AD B2C 应用程序。
1. 在左侧导航中，选择 **用户流**。
1. 在 **用户流** 页面顶部，选择 **新建用户流**。
1. 在 **选择用户流类型** 页面上，选择 **预览**。
1. 在页面中间，选择 **登录 v2**。 然后，在测试或开发过程中，按照[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)中的步骤，将流配置为站点的 Azure AD B2C 标准用户流。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)

[设置用户登录自定义页面](../custom-pages-user-logins.md)
