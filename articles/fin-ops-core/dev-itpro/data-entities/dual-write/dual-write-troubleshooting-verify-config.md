---
title: 验证 Finance and Operations 应用和 Common Data Service 中是否配置了双写入
description: 本主题说明如何确定在 Finance and Operations 应用和 Common Data Service 中是否配置了双写入。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997222"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a>验证 Finance and Operations 应用和 Common Data Service 中是否配置了双写入

[!include [banner](../../includes/banner.md)]



本主题提供 Finance and Operations 应用与 Common Data Service 之间的双写入集成的故障排除信息。 具体来说，说明如何确定在 Finance and Operations 应用和 Common Data Service 中是否配置了双写入。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>验证 Finance and Operations 应用中是否配置了双写入

若要确定您尝试保存记录以进行更新时看到的错误是否来自双写入，请首先验证是否配置了双写入。

+ 如果您在 Finance and Operations 应用中有管理员权限，请转到 **工作区 \> 数据管理** ，然后选择 **双写入** 磁贴。 如果显示了链接环境的详细信息以及正在运行的实体映射的列表，则说明配置了双写入。

    ![验证具有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_1.png)

+ 如果您没有管理员权限，则会收到错误消息 *无法将数据写入实体 \<entity name\>* 。 在下图的示例中，您无法在 Finance and Operations 应用中创建客户记录，因为配置了双写入，但客户组和付款期限引用数据在 Common Data Service 中不存在。

    ![验证没有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_2.png)

有关如何解决在 Finance and Operations 应用中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a>验证 Common Data Service 中是否配置了双写入

创建数据时，如果您在 Common Data Service 中的页面上看到了 **公司** 字段，则说明配置了双写入。

![验证 Common Data Service 连接](media/verify_cds.png)

有关如何解决在 Common Data Service 中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

有关在 Common Data Service 中创建数据的过程中遇到错误时如何查看错误详细信息的信息，请参阅[在 Common Data Service 中启用和查看插件跟踪日志来查看错误详细信息](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details)。
