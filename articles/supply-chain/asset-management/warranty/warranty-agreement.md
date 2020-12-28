---
title: 保修协议
description: 本主题介绍资产管理中的保修协议。
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423138"
---
# <a name="warranty-agreements"></a>保修协议

[!include [banner](../../includes/banner.md)]

 


在资产管理中，可以设置应用于资产或资产类型的保修条款。 保修条款是为特定期间创建的。 设置的保修可以提供完全覆盖，也可以提供部分覆盖，您可以设置与工时、费用和物料关联的条款。

第一步是创建适用于您的设备的任何供应商保修协议。 然后将保修协议与资产或资产类型关联。 供应商保修协议仅用于参考。 如果为资产设置了供应商保修，则可查看该资产的保修覆盖期间。

## <a name="create-a-warranty-agreement"></a>创建保修协议

一个保修协议中包含多个协议行，以便覆盖工作时间、费用和物料的保修。

1. 选择 **资产管理** \> **设置** \> **资产** \> **保修**。
2. 选择 **新建** 创建产品。
3. 在 **保修** 字段中，输入保修 ID。 
4. 在 **名称** 字段中，输入描述。

    **详细信息** 快速选项卡上的 **资产** 字段显示使用保修协议的有效资产的数量。

5. 在 **保修行** 快速选项卡上，按照以下步骤添加应包含在保修协议中的行：

    1. 选择 **添加行**，向保修添加新条件。 将在 **行** 字段中输入连续的行号。
    2. 在 **期间** 字段中，选择保修期的类型。
    3. 在 **间隔** 字段中，输入一个数字。 此字段定义保修的有效期间数量。
    4. 在 **百分比** 字段中，输入保修行的覆盖百分比。 此百分比指示公司涵盖的量。

![保修页面](media/01-warranty.png)
