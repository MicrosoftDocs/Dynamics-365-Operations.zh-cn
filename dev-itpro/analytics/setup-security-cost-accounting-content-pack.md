---
title: "成本核算分析 Power BI 的内容设置安全"
description: "本主题说明了如何在成本核算具有行级别的安全访问级别安全性。Microsoft Power BI。 此功能有助于保障用户仅看到 Power BI 数据授予它们访问权限。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>成本核算分析 Power BI 的内容设置安全

本主题说明了如何在成本核算具有行级别的安全访问级别安全性。Microsoft Power BI。 此功能有助于保障用户仅看到 Power BI 数据授予它们访问权限。

<a name="overview"></a>概览
--------

**成本核算分析** Microsoft Power BI 内容使用 Power BI 行级安全性限制用户访问。 安全基于成本核算参数设置的访问级别。组织层次结构 **有关成本核算分析** Power BI 的详细信息，请参阅、成本核算分析 Power BI [] (项成本核算 pack.md -分析内容)。

## <a name="setup"></a>设置
若要具有安全访问级别为 Power BI，Power BI 的内容必须将所有者执行以下步骤。 **注释：**发布的用户**成本核算分析** Power BI 内容自动成为所有者。 只有所有者可以设置。Power BI 的安全。 此外，在所有者，添加的其他用户 PowerBI.com，没有人员，只不过所有者可以查看在成本核算分析** ** Power BI 内容的数据。

1.  发布定义文件为 Power BI。
2.  登录到 PowerBI.com。
3.  **查找成本核算分析** Power BI 内容的数据集。
4.  安全打开页面。 

    [] (安全打开页面 https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png) 的![

5.  **的成本对象控制器**角色已创建。 添加件是成本核算访问级别将组织层次结构中的其他部分的成员。 

    [] (添加成员 https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)] (https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png) 的![

**的用户添加到该成本对象控制器**根据角色在成本核算中访问组织结构的层次级别定义要看到他们，只允许查看的数据。 **注释：**行级别安全性。从 Power BI 嵌入的工序的 Microsoft Dynamics 365 中应用于平铺和报告。

## <a name="updating-security"></a>安全更新
如果更新对在成本核算的访问级别，安全，并且您想要 Power BI 反映这些更新，必须更新**成本核算分析** Power BI 的内容实体商店。 在您完成从 Dynamics 365 的实体商店更新的工序后，必须在 PowerBI.com 更新的项目。 有关如何执行实体商店更新的详细信息，请参阅更新实体商店 [] (高级 BI 集成实体 store.md#update 实体商店)。 **成本核算分析**所有者 Power BI 的内容必须还执行实体商店更新，如果授予新用户到该组织层次结构的输入。 此外，必须将所有者将新的用户添加到 PowerBI.com **的成本的对象控制器**角色，因此，行级安全性。这些记录会应用。

## <a name="disabling-security"></a>禁用安全
我们假定您的组织若要限制数据访问。 如果包括，因为某些原因，禁用安全参数，当您在中运行成本核算时，必须将所有者将用户添加到。Power BI 的成本会计员** **角色。 如果您从一个更改启用状态的安全。禁用状态，无论业务是哪一个环节。从**的成本对象控制器**角色中删除用户。 反之亦然，则重新授权允许安全。 用户可以属于两个角色。 要访问角色是两行上移。 **对于成本核算分析** Power BI 请首先，有权访问要具有未限制数据的访问的用户。 如果您的目标是应用有限的访问，用户必须仅分配给**请成本对象控制器**角色。 这些行级安全性更新程序立即生效。 影响用户都刷新其查看器。

## <a name="additional-resources"></a>其他资源
若要了解有关 Power BI 行级别安全性，请参阅管理 [请在您的模型的安全性。Power BI] (https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model)。


