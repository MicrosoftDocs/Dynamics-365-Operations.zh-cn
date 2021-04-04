---
title: NF-e 自定义证书验证
description: 本主题提供有关启用和使用 NF-e 自定义证书的信息。
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3efa05f49748f6bbff680f322a77cec24da46c0c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240571"
---
# <a name="nf-e-custom-certificate-validation"></a><span data-ttu-id="931c8-103">NF-e 自定义证书验证</span><span class="sxs-lookup"><span data-stu-id="931c8-103">NF-e custom certificate validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="931c8-104">当启用 NF-e 自定义证书验证功能时，自定义验证允许与 Web 服务连接。</span><span class="sxs-lookup"><span data-stu-id="931c8-104">When you turn the NF-e custom certificate verification feature, custom validation allows a connection with the web services.</span></span> <span data-ttu-id="931c8-105">需要此连接才能传输 NF-e 并接收 SEFAZ 的授权。</span><span class="sxs-lookup"><span data-stu-id="931c8-105">This connection is required to transmit NF-e and receive authorization from SEFAZ.</span></span>

<span data-ttu-id="931c8-106">证书 V5 的 **服务器身份验证目的** 属性由巴西根证书颁发机构颁发。</span><span class="sxs-lookup"><span data-stu-id="931c8-106">The **Server authentication purpose** property from the certificate V5 is issued by the Brazilian Root Certificate Authority.</span></span> <span data-ttu-id="931c8-107">此属性默认情况下处于关闭状态，必须手动启用。</span><span class="sxs-lookup"><span data-stu-id="931c8-107">This property is turned off by default and must be manually enabled.</span></span> <span data-ttu-id="931c8-108">在某些情况下，自动证书更新可以将此属性切换为不再启用。</span><span class="sxs-lookup"><span data-stu-id="931c8-108">In some circumstances, the automatic certificate update can switch this property to no longer be enabled.</span></span> <span data-ttu-id="931c8-109">如果发生这种情况，TLS 连接将受到影响，并且不再受信任。</span><span class="sxs-lookup"><span data-stu-id="931c8-109">If this happens, the TLS connection is affected and is no longer trusted.</span></span> <span data-ttu-id="931c8-110">对于米纳斯吉拉斯 (MG) 州和巴拉那 (PR) 州，在生产环境中颁发 NF-e 的能力也将受到影响。</span><span class="sxs-lookup"><span data-stu-id="931c8-110">The ability to issue NF-e on production environments for states of Minas Gerais (MG) and Paraná (PR) states is also impacted.</span></span>

<span data-ttu-id="931c8-111">此更新允许用于证书验证的替代解决方案，这意味着可以建立安全通信。</span><span class="sxs-lookup"><span data-stu-id="931c8-111">This update allows for an alternative solution for certificate validation, which means that it’s possible to establish a secure communication.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]