---
title: 入站资产和出站资产
description: 本文介绍如何在资产管理中登记入站资产和出站资产。
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016527"
---
# <a name="inbound-and-outbound-assets"></a>入站资产和出站资产

[!include [banner](../../includes/banner.md)]

 

如果公司对从其他位置或客户收到的资产执行维修作业或维护作业，资产管理同时可跟踪正在前往公司的入站资产和正在退回的出站资产。

> [!NOTE]
> 如果要使用入站生命周期状态和出站生命周期状态管理正在前来的资产和正在退回的资产，则必须设置维护请求生命周期状态和生命周期模型来支持这些操作。 有关详细信息，请参阅[维护请求](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview)。

资产管理的设置决定是否可以使用入站资产和出站资产。

## <a name="register-assets-as-inbound"></a>将资产登记为入站资产

1. 选择 **资产管理** \> **维护请求** \> **有效维护请求**。
2. 选择维护请求。
3. 选择 **更新维护请求状态**。
4. 选择 **入站**（或已为入站资产创建的其他生命周期状态），然后选择 **确定**。

![将资产登记为入站资产。](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>将入站资产登记为接收的资产

1. 选择 **资产管理** \> **入站/出站** \> **入站资产**。
2. 选择资产或维护请求。
3. 选择 **接收资产**。
4. 在 **接收时间** 字段中，输入日期和时间。 然后选择 **确定**。 将从 **入站资产** 列表页删除记录。

![将入站资产登记为接收的资产。](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>将资产登记为出站资产

完成维护作业或修复作业之后，可将资产登记为已返回。

1. 选择 **资产管理** \> **维护请求** \> **有效维护请求**。
2. 选择维护请求。
3. 选择 **更新维护请求状态**。
4. 选择 **出站**（或已为出站资产创建的其他生命周期状态），然后选择 **确定**。

## <a name="register-outbound-assets-as-delivered"></a>将出站资产登记为已交付

1. 选择 **资产管理** \> **入站/出站** \> **出站资产**。
2. 选择资产或维护请求。
3. 选择 **交付资产**。
4. 在 **交付时间** 字段中，输入日期和时间。 然后选择 **确定**。 将从 **出站资产** 列表页删除记录。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]