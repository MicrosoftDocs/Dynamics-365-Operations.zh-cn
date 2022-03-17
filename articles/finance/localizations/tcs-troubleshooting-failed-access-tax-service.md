---
title: 无法访问税务服务
description: 本主题说明如何解决无法访问税款计算服务的问题。
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388544"
---
# <a name="failed-to-access-tax-service"></a>无法访问税务服务

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

本主题介绍如何修复税款计算服务的“无法访问税务服务”错误。

## <a name="symptoms"></a>故障特征

在 Microsoft Dynamics 365 Finance 中，您转到 **税务** \> **设置** \> **税务配置** \> **税务服务参数**。 在 **常规** 选项卡上，您启用 **启用税款计算** 选项。 如果您随后尝试在 **功能设置名称** 字段中选择一个值，发生错误。 错误消息显示“无法访问税务服务”。

## <a name="cause"></a>原因

出现此错误的原因是 Finance 无法访问税款计算服务。

## <a name="resolution"></a>解决方法 

1. 登录 Microsoft Dynamics Lifecycle Services (LCS)。
2. 在 **环境** 页面上，在 **环境加载项** 选项卡上，找到 **税款计算** 项，查看其状态。 状态应为 **正在安装** 或 **已安装**。 如果税款计算服务加载项未安装，您将收到错误。

## <a name="mitigation"></a>减轻

1. 在 LCS 中，在 **Finance** 页面上，在 **Power Platform 集成** 部分，选择 **安装新加载项**。
2. 滚动到页面底部，然后选择 **税款计算** 加载项进行安装。
3. 返回您的 Finance 环境，尝试访问税款计算服务。

> [!NOTE]
> 安装税款计算服务之前，请查看[税款计算服务先决条件](global-get-started-with-tax-calculation-service.md#prerequisites)。
> 
> 如果由于 **Power Platform 集成** 部分不可用而无法安装加载项，请参阅[加载项概述](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)。 如果您在安装加载项后仍然遇到错误，请联系您的系统管理员。
