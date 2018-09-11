--- 
title: "输入对固定资产的添加件"
description: "本流程展示如何对现有固定资产表添加新的成员。"
author: saraschi2
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3579148033023f648e1a78a3dd009018f153fdad
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="enter-an-addition-to-a-fixed-asset"></a>输入对固定资产的添加件

[!include [task guide banner](../../includes/task-guide-banner.md)]

本流程展示如何对现有固定资产表添加新的成员。 固定资产添加功能的目的就是追踪添加的资产项目，对固定资产进行维护和改进，也只是以提供信息为目的。 任何对固定资产价值或服务年限的改变要单独进行。   



本流程需要用到会计角色，使用来自法定实体 USMF 的演示数据。

1. 转到“固定资产”>“固定资产”>“固定资产”。
2. 在列表中，查找并选择要添加的固定资产。
3. 在列表中，单击所选行中的链接。
4. 在“操作”窗格上，单击“固定资产”。
5. 单击“固定资产物料添加”。
6. 单击“新建”。
7. 在“名称”字段中，键入一个值。
8. 设置添加物料采购或使用日期。
9. 输入资产物料、维护或其他改善成本。
10. 在“数量”字段中，输入一个数字。
    * 总成本对固定资产的值没有影响，仅用于跟踪和提供信息。 如果要将成本资本化，则必须单独过帐调高交易。  
11. 单击“常规”选项卡。
    * 如果增加物提供了资产的服务年限，设置增加服务年限  
    * 该字段仅用于提供信息。 要提高使用年限，请修改资产价值模型和折旧帐簿中的使用年限。  


