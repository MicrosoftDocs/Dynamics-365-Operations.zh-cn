---
title: 验证 Finance and Operations 应用和 Dataverse 中的双写入配置
description: 本主题说明如何确定在 Finance and Operations 应用和 Dataverse 中是否配置了双写入。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0a1da32713f3d4d19b4d343c5b67b416a6c4ffbb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566757"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>验证 Finance and Operations 应用和 Dataverse 中的双写入配置

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



本主题提供 Finance and Operations 应用与 Dataverse 之间的双写入集成的故障排除信息。 具体来说，说明如何确定在 Finance and Operations 应用和 Dataverse 中是否配置了双写入。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>验证 Finance and Operations 应用中是否配置了双写入

若要确定您尝试保存行以进行更新时看到的错误是否来自双写入，请首先验证是否配置了双写入。

+ 如果您在 Finance and Operations 应用中有管理员权限，请转到 **工作区 \> 数据管理**，然后选择 **双写入** 磁贴。 如果显示了链接环境的详细信息以及正在运行的表映射的列表，则说明配置了双写入。

    ![验证具有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_1.png)

+ 如果您没有管理员权限，则会收到错误消息 *无法将数据写入实体 \<entity name\>*。 在下图的示例中，您无法在 Finance and Operations 应用中创建客户行，因为配置了双写入，但客户组和付款期限引用数据在 Dataverse 中不存在。

    ![验证没有管理员权限时 Finance and Operations 应用的连接](media/verify_fin_ops_2.png)

有关如何解决在 Finance and Operations 应用中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>验证 Dataverse 中是否配置了双写入

创建数据时，如果您在 Dataverse 中的页面上看到了 **公司** 列，则说明配置了双写入。

![验证 Dataverse 连接](media/verify_cds.png)

有关如何解决在 Dataverse 中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

有关在 Dataverse 中创建数据的过程中遇到错误时如何查看错误详细信息的信息，请参阅[在 Dataverse 中启用和查看插件跟踪日志来查看错误详细信息](dual-write-troubleshooting.md#enable-view-trace)。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]