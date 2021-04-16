---
title: NF-e 自定义证书验证
description: 本主题提供有关启用和使用 NF-e 自定义证书的信息。
author: gionoder
ms.date: 10/06/2020
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813960"
---
# <a name="nf-e-custom-certificate-validation"></a>NF-e 自定义证书验证

[!include [banner](../includes/banner.md)]

当启用 NF-e 自定义证书验证功能时，自定义验证允许与 Web 服务连接。 需要此连接才能传输 NF-e 并接收 SEFAZ 的授权。

证书 V5 的 **服务器身份验证目的** 属性由巴西根证书颁发机构颁发。 此属性默认情况下处于关闭状态，必须手动启用。 在某些情况下，自动证书更新可以将此属性切换为不再启用。 如果发生这种情况，TLS 连接将受到影响，并且不再受信任。 对于米纳斯吉拉斯 (MG) 州和巴拉那 (PR) 州，在生产环境中颁发 NF-e 的能力也将受到影响。

此更新允许用于证书验证的替代解决方案，这意味着可以建立安全通信。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]