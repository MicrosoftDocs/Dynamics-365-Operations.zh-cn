---
title: 客户记录未出现在 Commerce Headquarters 中
description: 本文提供了当客户记录没有立即出现在 Commerce Headquarters 中时可能会有所帮助的故障排除指南。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: f1ad1f45abbc95cbf6d41b3c8681db781c6c9d23
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268830"
---
# <a name="customer-records-dont-appear-in-commerce-headquarters"></a>客户记录未出现在 Commerce Headquarters 中

[!include [banner](../../includes/banner.md)]

本文提供了当客户记录没有立即出现在 Commerce Headquarters 中时可能会有所帮助的故障排除指南。

## <a name="description"></a>说明

当您使用电子商务店面中的注册流程创建新客户记录时，相应的客户记录没有立即出现在 Commerce Headquarters 中。

## <a name="resolution"></a>解决方法

### <a name="disable-customer-creation-in-async-mode"></a>禁止在异步模式下创建客户

> [!IMPORTANT]
> 如果禁用异步客户创建，则系统性能可能会受到影响，因为创建每条记录时都会向 Commerce Headquarters 发出实时请求。 此外，如果 Commerce Headquarters 已关闭（例如，在维修流中），则任何新的客户创建流都将产生错误。

要禁止在 Commerce Headquarters 中以异步模式创建客户，请按照下列步骤操作。

1. 转至 **Retail 和 Commerce \> 渠道设置 \> 在线商店设置 \> 功能配置文件**。
1. 如果您尚未对在线渠道使用功能配置文件，请创建一个。
1. 确保 **在异步模式下创建客户** 选项设置为 **否**。
1. 转至 **Retail 和 Commerce \> 渠道 \> 在线商店**。
1. 选择在线商店以对其禁用异步客户创建。
1. 在 **常规** 选项卡上，确保 **功能配置文件** 字段设置为您要用于在线渠道的功能配置文件。

## <a name="additional-resources"></a>其他资源

[在 Commerce 中设置 B2C 租户](../set-up-b2c-tenant.md)
