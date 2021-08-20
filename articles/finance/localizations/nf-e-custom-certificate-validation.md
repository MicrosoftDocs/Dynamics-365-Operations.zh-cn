---
title: NF-e 自定义证书验证
description: 本主题提供有关启用和使用 NF-e 自定义证书的信息。
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755583"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e 自定义证书验证

[!include [banner](../includes/banner.md)]

巴西根证书颁发机构颁发的证书中的 **服务器身份验证用途** 属性默认情况下已关闭，必须手动启用。 在某些情况下，自动证书更新可以将此属性切换为不再启用。 如果发生这种情况，TLS 连接将受到影响，并且无法再受信任。 对于米纳斯吉拉斯 (MG) 州和巴拉那 (PR) 州，在生产环境中发布巴西电子财政文件模型 55 (NF-e) 的能力也将受到影响。

若要启用 **NF-e 自定义证书验证** 修复，请转到 **功能管理**。 此功能允许使用 V5 和 V10 证书验证的替代解决方案，并允许与 Web 服务建立可信连接，这对于安全传输 NF-e 以及从 SEFAZ 接收授权是必需的。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
