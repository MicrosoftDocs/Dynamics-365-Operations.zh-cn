---
title: 解决与解决方案意识相关的问题
description: 本主题提供故障排除信息，可以帮助您解决与解决方案意识有关的问题。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b53e07f69992a567d5b300ae1f2b24b74541d176
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416344"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>解决与解决方案意识相关的问题

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，提供可以帮助您解决与解决方案意识有关的问题的信息。

> [!IMPORTANT]
> 本主题解决的某些问题可能需要系统管理员角色或 Microsoft Azure Active Directory (Azure AD) 租户管理员凭据。 介绍每个问题的每一节说明了是否需要特定角色或凭据。

## <a name="error-on-the-dual-write-page"></a>双写入页面上的错误

在 **双写入** 页面上，您可能会收到类似于以下示例的错误消息：

*在 MetadataCache 中找不到名称为“msdyn\_dualwriteentitymap' with namemapping='Logical”的实体。*

要解决此问题，请确保已在 Dataverse 中安装了双写入核心解决方案。 双写入核心解决方案是处理解决方案意识问题的前提。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]