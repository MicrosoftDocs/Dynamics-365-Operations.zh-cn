---
title: 在仓库管理移动应用中使用相机扫描条码
description: 本主题介绍如何设置仓库管理移动应用以在移动设备上使用相机扫描条码。
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831210"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>在仓库管理移动应用中使用相机扫描条码

[!include [banner](../includes/banner.md)]

本主题介绍如何设置仓库管理移动应用以在移动设备上使用相机扫描条码。

## <a name="setup"></a>设置

在仓库管理移动应用的显示设置中，可选择是否应将相机用于条码扫描。 如果启用 **将摄像头用作扫描仪**，则可在将首选输入模式设置为 **扫描** 的每个输入字段中使用摄像头。

若要控制输入字段是否应可扫描，请将 **仓库应用字段名** 页面上的 **首选输入模式** 设置为 **扫描**。 选择此选项后，可在仓库管理移动应用中将相机用于扫描。 有关详细信息，请参阅[为仓库管理移动应用配置字段](configure-app-field-names-priorities-warehouse.md)。

## <a name="supported-bar-code-formats"></a>支持的条码格式

支持最常见的条码格式，包括 Code 128、Code 39、Code 93、EAN-8、EAN-13、UPC-E、UPC-A 和 QR 码。

## <a name="navigation"></a>导航

在输入字段的 **首选输入模式** 设置为 *扫描* 的每个页面上，将启动相机页面。进入相机页面后，请使用以下选项进行导航：

- 选择后退按钮以返回到 **任务和详细信息** 页面。
- 选择 **任务和详细信息** 页面上的铅笔以转到可手动键入输入的页面。
- 选择 **任务和详细信息** 页面上的相机以返回到相机页面。

在相机页面上，如果选择相机按钮，在尝试识别条码时页面将变暗。 如果条码在 5 秒钟内无法识别，此流程将超时，而相机按钮将再次变为可用。 然后就可以再次尝试扫描条码。

将摄像头对准条码时，请让条码在括号内对齐，以达到最佳效果。 条码扫描成功后，将处理结果，并转到下一步。 如果下一步中又包含一个将首选输入模式设置为“扫描”的输入字段，将再次启动摄像头页面。 如果下一步不是扫描字段，则不会启动摄像头页面。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]