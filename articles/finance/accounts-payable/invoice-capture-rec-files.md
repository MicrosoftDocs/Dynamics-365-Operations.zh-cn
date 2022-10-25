---
title: Invoice capture 已接收文件
description: 本文介绍如何在 Invoice capture 中从不同来源收集发票文件。
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690110"
---
# <a name="invoice-capture-received-files"></a>Invoice capture 已接收文件

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

在 Invoice capture 中，**已接收文件** 页面是从不同来源接收发票文件的中心位置。

## <a name="upload-invoice-files"></a>上载发票文件

应付帐款 (AP) 职员可以通过选择 **上载文件** 打开 **上载** 对话框来上载发票图像。 AP 职员选择文件后，**上载** 按钮将可用。

## <a name="include-or-obsolete-invoice-files"></a>包括或废弃发票文件

用户可以选择有错误或警告的发票，然后通过选择操作窗格上的相应按钮来包括或废弃发票。 标记为废弃的发票不会出现在 **已接收文件（废弃）** 视图中。

## <a name="view-captured-invoices"></a>查看捕获的发票

成功识别收到的文件后，AI 模型将返回捕获的发票的信息，信息将被输入 Microsoft Dataverse。 然后，AP 职员可以通过选择 **查看捕获的发票** 验证发票详细信息。 用户可根据需要下载原始发票文件。
