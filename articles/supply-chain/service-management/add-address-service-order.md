---
title: 将地址添加到服务订单
description: 此主题描述如何将客户地址添加到服务订单。
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a5b1c0e300edc45ae3f4be9eae8afa56e06cccd6
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203081"
---
# <a name="add-an-address-to-a-service-order"></a>将地址添加到服务订单    

[!include [banner](../includes/banner.md)]


此主题描述如何将客户地址添加到服务订单。 在您创建某一服务订单时，地址信息将从该服务订单附加到的项目转移。 但是，您可以从已在 Microsoft Dynamics AX 中输入的客户、供应商、站点、仓库、服务订单和项目的地址，选择备选位置。

您还可以创建新地址。 默认情况下，将新地址转移到项目。 但是，您可以指定新地址仅与该服务实例相关。 如果您执行此操作，则新地址不会转移到项目。

## <a name="create-a-customer-address-for-a-service-order"></a>为服务订单创建客户地址

若要添加地址到销售订单，请执行以下步骤：

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  打开想要为其创建地址的服务订单。

3.  在**操作窗格**上，单击**编辑**，然后单击**标头视图**。

4.  在**地址**快速选项卡，单击**添加地址**。

5.  在**新地址**窗体中，输入地址的唯一名称并完成其余的字段。 
    

    > [!WARNING]
    > <P>如果输入与现有地址相同的名称，则您在剩余字段中输入的信息将覆盖现有地址信息。</P>


6.  单击 **确定**以将新地址复制到您的服务订单中。

## <a name="specify-an-alternative-address-on-a-service-order"></a>在服务订单上指定备选地址

若要将备选地址添加到服务订单，请执行以下步骤：

1.  单击**服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  打开您想要为其输入备选地址的服务订单。

3.  在**操作窗格**上，单击**编辑**，然后单击**标头视图**。

4.  在**地址**快速选项卡，单击**其他地址**。

5.  在**地址选择**窗体**记录类型**字段中，选择**服务订单**。

6.  选择地址，然后单击**确定**以将其复制到您的服务订单中。


  


