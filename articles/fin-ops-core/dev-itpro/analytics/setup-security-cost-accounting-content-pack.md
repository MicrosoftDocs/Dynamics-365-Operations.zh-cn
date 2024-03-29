---
title: 设置成本核算分析 Power BI 内容的安全性
description: 本文介绍在 Microsoft Power BI 中如何将成本核算中的访问级别安全性传播到行级别安全性。
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.openlocfilehash: 9f019bec9c28602e31b43a8b3ab820f4a3a31ee8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267923"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>设置成本核算分析 Power BI 内容的安全性

[!include [banner](../includes/banner.md)]

本文介绍在 Microsoft Power BI 中如何将成本核算中的访问级别安全性传播到行级别安全性。 此功能有助于确保用户仅查看有权访问的 Power BI 数据。

## <a name="overview"></a>概览

**成本核算分析** Microsoft Power BI 内容使用 Power BI 低级别安全性限制用户的访问权限。 安全性基于“成本核算”参数中设置的访问级别组织层次结构。 有关 **成本核算分析** Power BI 内容的详细信息，请参阅[成本核算分析 Power BI 内容](cost-accounting-analysis-content-pack.md)。

## <a name="setup"></a>设置
若要将访问级别的安全性传播到 Power BI，Power BI 内容的所有者必须执行以下步骤。

> [!NOTE]
> 发布 **成本核算分析** Power BI 内容的用户将自动成为所有者。 只有所有者才能在 Power BI 中设置安全性。 此外，所有者在 PowerBI.com 中添加其他用户之前，只有所有者才能查看 **成本核算分析** Power BI 内容中的数据。

1. 将定义文件发布到 Power BI。
2. 登录 PowerBI.com，
3. 找到 **成本核算分析** Power BI 内容的数据集。
4. 打开安全性页面。

    ![打开安全性页面。](./media/CA-picture-1.png)

5. 已创建了 **成本对象控制员** 角色。 添加属于成本核算访问级别组织层次结构的其他成员。

    ![添加成员。](./media/CA-picture-2.png)

添加到 **成本对象控制员** 角色的用户只能查看根据成本核算访问级别组织层次结构中的定义允许其查看的数据。

> [!NOTE]
> 行级别安全性适用于从 Power BI 嵌入的磁贴和报表。

## <a name="updating-security"></a>更新安全性
如果对成本核算中的访问级别安全性进行更新，并且希望 Power BI 体现这些更新，则必须更新 **成本核算分析** Power BI 内容的实体商店。 完成了实体商店更新之后，必须更新 PowerBI.com 中的项目。 有关如何执行实体商店更新的详细信息，请参阅 [Power BI 与实体商店的集成](power-bi-integration-entity-store.md#update-entity-store)。 如果为新用户授予了组织层次结构的访问权限，**成本核算分析** Power BI 内容的所有者还必须执行实体商店更新。 此外，该所有者还必须在 PowerBI.com 上将新用户添加到 **成本对象控制员** 角色，以便为其应用行级别的安全性。

## <a name="disabling-security"></a>禁用安全性
假设您的组织希望限制数据访问权限。 如果出于某种原因，当您运行成本核算时禁用了安全性参数，则所有者必须改为在 Power BI 中将用户添加到 **成本会计师** 角色。 如果您将安全性从已启用状态更改为已禁用状态，建议从 **成本对象控制员** 角色删除用户。 如果重新启用安全性，则执行相反操作。 用户可以同时属于两种角色。 联合访问权限是两种角色的结合。 在 **成本核算分析** Power BI 内容中，具有联合访问权限的用户的数据访问权限不受限制。 如果您的目标是应用受限访问权限，则必须仅为用户分配 **成本对象控制员** 角色。 这些行级别的安全性更新立即生效。 受影响的用户应刷新自己的浏览器。

## <a name="additional-resources"></a>其他资源
若要了解有关 Power BI 行级别安全性的详细信息，请参阅[在 Power BI 中管理模型的安全性](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model)。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
