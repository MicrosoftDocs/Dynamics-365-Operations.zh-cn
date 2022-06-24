---
title: 验证财务和运营应用和 Dataverse 中的双重写入配置
description: 本文说明如何确定在财务和运营应用和 Dataverse 中是否配置了双写入。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 7131e6c2c4ca4d9c6bb84ad74bf425faf28bd92c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884450"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>验证财务和运营应用和 Dataverse 中的双重写入配置

[!include [banner](../../includes/banner.md)]





本文提供财务和运营应用与 Dataverse 之间的双写入集成的疑难解答信息。 具体来说，说明如何确定在财务和运营应用和 Dataverse 中是否配置了双写入。

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>验证是否在财务和运营应用中配置了双写入

若要确定您尝试保存行以进行更新时看到的错误是否来自双写入，请首先验证是否配置了双写入。

+ 如果您在财务和运营应用中有管理员权限，请转到 **工作区 \> 数据管理**，然后选择 **双写入** 磁贴。 如果显示了链接环境的详细信息以及正在运行的表映射的列表，则说明配置了双写入。

    ![验证具有管理员权限时财务和运营应用的连接。](media/verify_fin_ops_1.png)

+ 如果您没有管理员权限，则会收到错误消息 *无法将数据写入实体 \<entity name\>*。 在下图的示例中，您无法在财务和运营应用中创建客户行，因为配置了双写入，但客户组和付款期限引用数据在 Dataverse 中不存在。

    ![验证没有管理员权限时财务和运营应用的连接。](media/verify_fin_ops_2.png)

有关如何解决在财务和运营应用中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>验证 Dataverse 中是否配置了双写入

创建数据时，如果您在 Dataverse 中的页面上看到了 **公司** 列，则说明配置了双写入。

![验证 Dataverse 连接。](media/verify_cds.png)

有关如何解决在 Dataverse 中创建数据时出现的问题的信息，请参阅[解决实时同步问题](dual-write-troubleshooting-live-sync.md)。

有关在 Dataverse 中创建数据的过程中遇到错误时如何查看错误详细信息的信息，请参阅[在 Dataverse 中启用和查看插件跟踪日志来查看错误详细信息](dual-write-troubleshooting.md#enable-view-trace)。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]