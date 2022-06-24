---
title: 处理传入的电子单据
description: 本文概要介绍了如何处理传入的电子单据。
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: dec4c16c8ba9f0ba55f30f3944eff172cf9db724
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909999"
---
# <a name="processing-of-incoming-electronic-documents"></a>处理传入的电子单据

[!include [banner](../includes/banner.md)]

可以通过两种方式导入和处理传入的电子单据，如供应商电子发票：

- 文件从外部渠道检索然后直接传递到您的已连接应用程序。 在那里，它们将经过另外的转换，然后被导入数据库。
- 文件在电子开票服务中进行预处理，然后传递到您的已连接应用程序。

电子开票支持两个传入文档渠道：电子邮件和 Microsoft SharePoint 文件夹。

有两种设置类型可以指定单据是经过预处理还是直接传递到您的已连接应用程序：

- **数据渠道** – 系统会将单据直接传递到已连接的应用程序。
- **数据渠道与处理管道** – 您可以设置将在单据传递到连接的应用程序之前运行的其他操作。

有关如何为不同渠道设置处理传入电子单据的方案的信息，请参阅[配置电子邮件渠道](e-invoicing-configure-email.md)和[配置 SharePoint 渠道](e-invoicing-configure-sharepoint-channel.md)。
