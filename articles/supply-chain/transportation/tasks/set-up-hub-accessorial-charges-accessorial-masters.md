---
title: 设置中心附属费用和附属主数据
description: 此过程显示如何为中心创建附属主数据，并使用主数据来创建中心附加费。
author: Weijiesa
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ae7580e0c2a2f776512a7cf4c378266f1a878e9
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672617"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a>设置中心附属费用和附属主数据

[!include [banner](../../includes/banner.md)]

此过程显示如何为中心创建附属主数据，并使用主数据来创建中心附加费。 此过程使用 USMF 数据集。 此设置通常由运输协调员完成。


## <a name="set-up-a-hub-master"></a>设置汇集点主
1. 转到“运输管理”>“设置”>“评级”>“附属主数据”。
2. 单击“新建”。
3. 在“附属主数据”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“附属类型”字段中，选择“中心”。
6. 单击“保存”。
7. 关闭该页面。

## <a name="set-up-a-hub-accessorial-charge"></a>设置中心附加费
1. 转到“运输管理”>“设置”>“评级”>“中心附加费”。
2. 单击“新建”。
3. 在“中心附属 ID”字段中，键入一个值。
4. 在“中心”字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
6. 在“中心位置”字段中，选择一个选项。
    * 您可以创建装货或卸货费用。 根据您的选择，费用将适用于您的路线中相应的运输细分市场。  
7. 在“附属主数据”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
    * 选择您刚创建的主数据。  
9. 单击“保存”。
10. 关闭该页面。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]