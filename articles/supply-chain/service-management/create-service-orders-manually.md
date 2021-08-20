---
title: 手动创建服务订单
description: 您可以通过使用服务协议或通过使用 **服务订单** 窗体，手动创建服务订单。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05c03cd07599c5ee2e739a785896888c8cfe8822e57529f7603783a2f011c97c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740639"
---
# <a name="create-service-orders-manually"></a>手动创建服务订单    

[!include [banner](../includes/banner.md)]


您可以通过使用服务协议或通过使用 **服务订单** 窗体，手动创建服务订单。 您还可以从项目创建服务订单。

> [!TIP]
> <P>您可以使用自动执行流程创建服务订单。 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>手动从服务协议创建服务订单

1.  选择 **服务管理** \> **常用** \> **服务协议** \> **服务协议**。

2.  选择某一服务协议，或者创建新的服务协议。

3.  选择 **交货** 选项卡，然后在 **创建** 组中选择 **计划服务订单** 打开 **创建服务订单** 窗体。

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>在服务订单窗体中手动创建服务订单

1.  选择 **服务管理** \> **通用** \> **服务订单** \> **服务订单**。

2.  选择 **新建** 创建新服务订单。

3.  为服务订单创建服务订单行。

> [!NOTE]
> <P>如果在<STRONG>服务管理参数</STRONG>窗体中选中了<STRONG>允许，但没有服务协议</STRONG>复选框，则您可以从服务订单行过帐交易记录，而无需将服务订单附加到服务协议。 如果取消选中该复选框，则您必须将手动创建的服务订单附加到项目，然后才能过帐服务订单行。</P>

## <a name="create-a-service-order-from-a-project"></a>从一个项目创建服务订单

1.  转到 **项目管理与会计** \> **通用** \> **项目** \> **所有项目**。

2.  在 **项目** 窗体中的 **操作窗格** 上，选择 **管理** 选项卡 \> **服务** \> **服务订单**。

3.  按照前面的过程执行，以便在 **服务订单** 窗体中手动创建某一服务订单。 **项目 ID** 字段显示项目参考。

> [!NOTE]
> <P>如果在<STRONG>服务管理参数</STRONG>窗体中选中了<STRONG>允许，但没有服务协议</STRONG>复选框，则您可以从服务订单行过帐交易记录，而无需将服务订单附加到服务协议。 如果取消选中该复选框，则您必须将手动创建的服务订单附加到项目，然后才能过帐服务订单行。</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>从销售订单窗体创建一个服务订单

可使用 **基于销售订单创建新的服务订单** 向导从 **服务订单** 窗体创建服务订单。

1.  转到 **销售和市场营销** \> **通用** \> **销售订单** \> **所有销售订单**。

2.  打开相关销售订单。

3.  在 **销售订单** 选项卡上，选择 **服务订单** 启动 **基于销售订单创建新的服务订单** 向导。

4.  选择 **下一步 \>**，然后在 **选择服务订单关联的协议** 页上完成以下步骤：
    
      - 使用 **服务协议** 字段可以选择新的服务订单应与之关联的服务协议。
    
      - 可选：使用 **项目 ID** 字段可以将此服务订单与特定项目相关联。

5.  选择 **下一步 \>**，然后在 **创建服务订单** 页上完成以下步骤：
    
      - 在 **首选服务时间** 字段中输入服务电话要开始的日期和时间。
    
      - 可选：修改 **说明** 字段中的文本。 默认情况下，此字段包含您在前一页上选择的服务协议的描述。
    
      - 在 **负责人** 字段中，选择负责该协议的员工的 ID；并且如果您知道，输入该服务电话的客户首选技术人员的 ID。
    
      - 在 **联系人 ID** 字段，选择客户公司中应针对此服务订单与之联系的人员。

6.  选择 **下一步 \>**，然后选择 **完成**。


## <a name="see-also"></a>请参阅

[服务订单](service-orders.md)

[自动创建服务订单](create-service-orders-automatically.md)

[创建服务订单（类窗体）](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]