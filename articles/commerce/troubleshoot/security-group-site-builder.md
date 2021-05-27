---
title: 初始部署期间无法为 Commerce 站点构建器配置安全组
description: 本主题提供了故障排除指南，初始部署新电子商务租户期间，在 Microsoft Dynamics Lifecycle Services (LCS) 中创建电子商务组件时，如果 Commerce 站点构建器的 Microsoft Azure Active Directory (Azure AD) 安全组未显示为选项，此指南可提供帮助。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d29e560d0f7b2bbc2415d7a0f6fe18f2ca17dc7c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020724"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a>初始部署期间无法为 Commerce 站点构建器配置安全组

[!include [banner](../../includes/banner.md)]

本主题提供了故障排除指南，初始部署新电子商务租户期间，在 Microsoft Dynamics Lifecycle Services (LCS) 中创建电子商务组件时，如果 Commerce 站点构建器的 Microsoft Azure Active Directory (Azure AD) 安全组未显示为选项，此指南可提供帮助。

## <a name="description"></a>说明

在部署包括 Commerce 站点构建器组件的新电子商务租户的过程中创建电子商务组件时，Azure AD 安全组不会在对话框中显示为选项。

## <a name="resolution"></a>解决方法

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a>在正确的租户中为用户预配电子商务站点

1. 转到 [Azure 门户](https://portal.azure.com/)。
1. 在预配电子商务站点 LCS 项目所针对的租户下，请按照[使用 Azure Active Directory 创建一个基本组并添加成员](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)中的说明进行操作。
1. 转到 [LCS](https://lcs.dynamics.com/)，然后使用帐户登录，此帐户与您刚创建的 Azure AD 安全组共享相同租户。 该帐户必须有权查看 Azure AD 安全组。
1. 完成设置步骤以配置电子商务站点。 在预配电子商务组件时，安全组现在应作为一个选项出现在对话框中。

> [!NOTE]
> 为确保对话框中的字段填充了安全组列表，您必须在输入您创建的 Azure AD 安全组的名称后选择 **输入**。 搜索结果将列出所有以搜索文本开头且用户有权访问的 Azure AD 安全组。 您可以使用较短的搜索词来获得更广泛的搜索结果。

## <a name="additional-resources"></a>其他资源

[使用 Azure Active Directory 创建一个基本组并添加成员](/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[部署新的电子商务租户](../deploy-ecommerce-site.md)