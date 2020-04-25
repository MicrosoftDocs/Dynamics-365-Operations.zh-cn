---
title: 资产出借
description: 本主题介绍如何在资产管理中登记出借资产。
author: josaw1
manager: tfehr
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205245"
---
# <a name="asset-loans"></a>资产出借

[!include [banner](../../includes/banner.md)]

 

如果您的公司从内部位置或客户处收到用于维修作业或维护作业的资产，以及如果您暂时将资产出借给这些位置或客户，资产管理可以跟踪资产出借。

## <a name="register-asset-loans-on-a-maintenance-request"></a>登记维护请求的资产出借

1. 选择**资产管理** \> **常用** \> **维护请求** \> **所有维护请求**或**有效维护请求**。
2. 选择要为其登记资产出借的维护请求，然后选择**编辑**。
3. 在**请求**页，选择**发送出借资产**。
4. 选择资产，然后输入预期返回日期。
5. 选择**确定**。

> [!NOTE]
> - 仅当有相同资产类型的资产时，才可以发送出借资产。
> - 出借的资产必须有允许其用作出借资产的资产生命周期状态，如 **InStorage**。 登记资产出借时，将把资产的资产生命周期状态自动更新为 **OnLoan** 之类状态。

若要查看您已出借给其他位置或客户的所有资产的列表，请选择**资产管理** \> **常用** \> **资产出借** \> **所有资产出借**。 如果为资产选中了**已结束**复选框，则已将资产登记为已退给公司。

![管理维护请求](media/06-manage-maintenance-requests.png)

在**有效资产出借**页上，可查看尚未退给您的公司的所有出借资产的列表。

## <a name="register-loan-assets-as-returned"></a>将出借资产登记为已退回

1. 选择**资产管理** \> **常用** \> **资产出借** \> **有效资产出借**。
2. 选择登记为已退回的资产出借，然后选择**退回资产出借**。
3. 在**已退回**字段中，输入日期和时间。
4. 选择**确定**。
5. 刷新**有效资产出借**列表页，然后注意列表中不再显示该资产出借。
