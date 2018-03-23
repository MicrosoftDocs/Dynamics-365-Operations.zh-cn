---
title: "在 Dynamics 365 for Finance and Operations – Warehousing 中使用摄像头扫描条码"
description: "本主题介绍如何设置 Dynamics 365 for Finance and Operations – Warehousing 以在移动设备上使用摄像头扫描条码。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: zh-cn
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>在 Dynamics 365 for Finance and Operations – Warehousing 中使用摄像头扫描条码

[!include[banner](../includes/banner.md)]

本主题介绍如何设置 Dynamics 365 for Finance and Operations – Warehousing 以在移动设备上使用摄像头扫描条码。 

## <a name="prerequisites"></a>必备项
若要使用此功能，需要安装 Warehousing 版本 1.2.0.0，并且设备必须有摄像头。 更新后打开该应用程序时，系统将提示您允许 Dynamics 365 for Finance and Operations – Warehousing 应用程序使用摄像头。 如果设备没有摄像头，将不显示此提示，而您则不能将摄像头用作扫描仪。 

## <a name="setup"></a>设置
在 Warehousing 应用程序的“显示”设置中，可选择是否应将摄像头用于执行条码扫描。 如果启用**将摄像头用作扫描仪**，则可在将首选输入模式设置为**扫描**的每个输入字段中使用摄像头。 

若要控制输入字段是否应可扫描，请将 Dynamics 365 for Finance and Operations 中的**仓库应用程序字段名**页面上的**首选输入模式**设置为**扫描**。 选择此选项之后，可在 Warehousing 应用程序中将摄像头用于扫描。 有关如何配置 Warehousing 中的应用程序字段名的信息，请参阅[配置 Warehousing 应用程序中的应用程序字段名](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse)。

## <a name="supported-bar-code-formats"></a>支持的条码格式
支持最常见的条码格式，包括 Code 128、Code 39、Code 93、EAN-8、EAN-13、UPC-E、UPC-A 和 QR 码。 

## <a name="navigation"></a>导航
在输入字段的首选输入模式设置为“扫描”的每个页面上，将启动摄像头页面。进入“摄像头”页面后，请使用以下选项进行导航：
- 单击后退按钮将返回到“任务和详细信息”页面。 
- 单击“任务和详细信息”页面上的铅笔将转到可手动键入输入的页面。
- 单击“任务和详细信息”页面上的摄像头将返回到“摄像头”页面。 

| “任务和详细信息”页 | “摄像头”页 | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

在摄像头页面中，如果单击“摄像头”按钮，尝试识别条码时页面将变暗。 如果条码在 5 秒钟内无法识别，此过程将超时，而“摄像头”按钮将再次变为可用。 然后就可以再次尝试扫描条码。

将摄像头对准条码时，请让条码在括号内对齐，以达到最佳效果。 条码扫描成功后，将处理结果，并转到下一步。 如果下一步中又包含一个将首选输入模式设置为“扫描”的输入字段，将再次启动摄像头页面。 如果下一步不是扫描字段，则不会启动摄像头页面。


