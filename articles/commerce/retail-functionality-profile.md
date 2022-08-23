---
title: 创建零售功能配置文件
description: 本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建功能配置文件。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f006aaf594f1df097f80c77794e34f9b831e9949
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280233"
---
# <a name="create-a-retail-functionality-profile"></a>创建零售功能配置文件

[!include [banner](includes/banner.md)]

本文介绍如何在 Microsoft Dynamics 365 Commerce 中创建功能配置文件。

Commerce 功能配置文件提供了用于在线渠道的各种设置。 每个渠道必须指定一个功能配置文件。

## <a name="create-a-functionality-profile"></a>创建功能配置文件

若要创建功能配置文件，请执行以下步骤。

1. 在导航窗格中，转到 **模块 \> 渠道设置 \> POS 配置文件 \> 功能配置文件**。
1. 在操作窗格上，选择 **新建**。
1. 在 **配置文件** 字段中，输入配置文件的 ID（下面示例图像中的“FN006”）。
1. 在 **描述** 字段中，输入一个值（下面示例图像中的“冒险工作配置文件”）。
1. 在 **常规** 部分中，为 **ISO** 区域设置选择国家/地区。
1. 在 **常规** 部分中，根据需要修改其他设置。
1. 在 **常规** 部分中，为电子邮件收据选择 **收据配置文件 ID**。
1. 在 **功能** 部分中，根据需要修改设置。
1. 在 **金额** 部分中，根据需要修改设置。
1. 在 **信息代码** 部分中，根据需要修改设置。
1. 在 **收据编号** 部分中，根据需要修改设置。 
  
下图显示了一个功能配置文件示例。
  
![功能配置文件示例。](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>其他资源

[信息代码和信息代码组](info-codes-retail.md)           

[新建通讯簿](new-address-book.md) 

[屏幕布局概览](pos-screen-layouts.md)       

[配置并安装 Retail Hardware Station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
