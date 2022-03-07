---
title: 将燃油指数作为附属费用与承运人关联
description: 本指南显示如何创建附属分配、承运人附加费用、燃油附加费的附属主数据，以及将承运人燃油指数与承运人关联。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df75f8dc88124b3e07cc342a3e28c8049068d37
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205170"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>将燃油指数作为附属费用与承运人关联

[!include [banner](../../includes/banner.md)]

本指南显示如何创建附属分配、承运人附加费用、燃油附加费的附属主数据，以及将承运人燃油指数与承运人关联。 您需要设置承运人燃油指数才能运行此指南。 您可以使用“设置承运人燃油指数”指南来执行此操作。 这些设置任务通常由物流经理完成。 使用 USMF 演示数据创建此过程。


## <a name="create-an-accessorial-master"></a>创建附属主数据
1. 转到“运输管理”>“设置”>“评级”>“附属主数据”。
2. 单击“新建”。
3. 在“附属主数据”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 单击“保存”。

## <a name="create-a-carrier-accessorial-charge"></a>创建装运承运人附加费
1. 转到“运输管理”>“设置”>“评级”>“承运人附加费”。
2. 单击“新建”。
3. 在“承运人附属 ID”字段中，键入一个值。
4. 在“装运承运人”字段中，单击下拉按钮以打开查找。
5. 在列表中，找到并选择所需记录。
    * 在本示例中，选择卡车承运人。  
6. 在列表中，单击所选行中的链接。
7. 在“承运人服务”字段中，单击下拉按钮以打开查找。
8. 在列表中，单击所选行中的链接。
9. 在“附属主数据”字段中，单击下拉按钮以打开查找。
10. 在列表中，找到并选择所需记录。
    * 在本示例中，选择新创建的附属主数据。  
11. 单击“保存”。

## <a name="create-an-accessorial-assignment"></a>创建附属分配
1. 单击“附属分配”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
4. 切换“标准”部分的展开项。
    * 在此标准中，您可以选择始终应用燃油附加费或为此示例选择仅特定区域适用的燃油附加费。  
5. 在“发件人邮政编码”字段中，键入一个值。
6. 在“收件人邮政编码”字段中，键入一个值。
7. 切换“计算”部分的展开项。
    * 在计算部分可以指定如何计算燃油附加费。 此计算取决于您选择作为计算基数的附属单位。  
8. 在“附加费用类型”字段中，选择“燃油附加费”。
9. 在“附属单位”字段中，选择“里程”。
10. 在“区域”字段中，单击下拉按钮以打开查找。
11. 在列表中，单击所选行中的链接。
12. 单击“保存”。

## <a name="update-the-carrier-rating-profile"></a>更新承运人评级资料
1. 转到“运输管理”>“设置”>“承运人”>“装运承运人”。
2. 在列表中，找到并选择所需记录。
3. 切换“评级资料”部分的展开项。
4. 单击“编辑”。
5. 在“承运人燃油指数”字段中，单击下拉按钮以打开查找。
6. 在列表中，单击所选行中的链接。
7. 单击“保存”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]