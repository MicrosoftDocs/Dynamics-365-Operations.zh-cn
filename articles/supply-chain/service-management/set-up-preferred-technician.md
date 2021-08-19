---
title: 设置首选技术人员
description: 您可以选择任何工作人员作为某一服务协议或服务订单的首选技术人员。
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37986d6d939ad368e5be6a4696f0122ae8781065b61dc2178f817366ce993a64
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734059"
---
# <a name="set-up-a-preferred-technician"></a>设置首选技术人员 

[!include [banner](../includes/banner.md)]


您可以选择任何工作人员作为某一服务协议或服务订单的首选技术人员。 然而，最好添加工作者到相应派遣团队，以便工作者包括在 **派遣板**。

## <a name="assign-employee-to-a-dispatch-team"></a>将员工分配到派遣团队

1.  单击 **人力资源** \> **通用** \> **工作人员** \> **工作人员**。 双击工人打开工作人员详细信息页。 在 **操作窗格** 上，单击 **设置** \> **派遣团队** 以打开 **派遣工作人员** 窗体。

2.  在 **派遣团队** 字段中，选择为其分配工作人员的团队。

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>将首选技术人员分配给某一服务协议

1.  单击 **服务管理** \> **常用** \> **服务协议** \> **服务协议**。 双击服务协议打开详细信息窗体。

2.  在 **常规** 选项卡上，选择 **首选技术人员** 字段，然后选择相应派遣团队的编号作为服务协议的首选技术人员。

## <a name="assign-a-preferred-technician-to-a-service-order"></a>将首选技术人员分配给某一服务订单

1.  单击 **服务管理** \> **定期** \> **派遣板**。
    

    > [!NOTE]
    > <P>在<STRONG>派遣板</STRONG>窗体中，指定要查看的派遣活动的日期范围。 此外，指定是否显示已关闭的活动，以及是否将派遣活动列表限制为您属于或授权监视的团队。 单击<STRONG>确定</STRONG>以打开<STRONG>派遣板</STRONG>窗体。</P>



2.  选择要修改的服务活动行。

3.  在 **相关** 选项卡上，使用 **工作人员** 列表可以将相应派遣团队的编号分配作为服务电话的首选技术人员。

## <a name="see-also"></a>请参阅

[形成和确定服务协议概览](service-agreements.md)

[手动创建服务订单](create-service-orders-manually.md)

[服务协议（窗体）](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]