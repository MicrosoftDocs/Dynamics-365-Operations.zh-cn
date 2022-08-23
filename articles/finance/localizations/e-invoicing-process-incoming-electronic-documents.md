---
title: 处理传入的电子单据
description: 本文概要介绍了如何处理传入的电子单据。
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277292"
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
