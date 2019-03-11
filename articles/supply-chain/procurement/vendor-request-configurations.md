---
title: 供应商请求配置
description: 此主题介绍在新供应商请求中必须填充的字段。
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d238e0dbb754e88dcffa171456aa0a2336238cab
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "332510"
---
# <a name="vendor-request-configurations"></a>供应商请求配置
[!include [banner](../includes/banner.md)]

为了完成供应商请求，供应商联系人必须完成潜在供应商注册向导。

在**供应商请求配置**窗体中可以创建配置文件，以指定潜在供应商注册向导中的必填字段和显示字段。

供应商注册向导将首先询问潜在供应商用户供应商开展经营所在的国家/地区。 此信息决定适用的配置。 如果没有定义某个国家/地区的具体配置，将使用默认配置。

### <a name="set-up-a-vendor-request-configuration"></a>设置供应商请求配置

默认情况下，在供应商请求配置窗体中提供了一个供应商配置。

不能选择默认配置的国家/地区，因此无法更改**国家/地区**部分。

1. 单击**采购** > **设置** > **供应商**，然后单击**供应商请求配置**。
2. 单击**字段**选项卡可以设置所列字段的状态。
3. 隐藏（不可见）
4. 显示（可见但非必填）
5. 必填（可见且必填）
6. 单击**内容**选项卡可指定文本是否要显示在向导上，以及是否应该确认潜在供应商用户必须接受后才能进入向导的下一步。 将针对用户必须接受后才能继续的任何条款和条件请求确认。

您还可以输入在完成向导时将要显示的确认消息，并且可以添加一个或多个调查表。

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>为特定国家/地区创建供应商配置
1.  单击**采购** > **设置** > **供应商**，然后单击**供应商请求配置**。
2.  单击**新建**以创建新的配置，然后为该配置提供一个名称。
3.  单击**保存**。
4.  打开**国家/地区**选项卡以选择使用配置的国家/地区。
5.  按照以下默认配置指南完成配置。

