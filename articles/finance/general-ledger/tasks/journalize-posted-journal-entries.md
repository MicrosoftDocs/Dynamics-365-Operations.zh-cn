---
title: 将过帐日记帐条目记入日记帐
description: 该过程显示如何将过帐的日记帐条目记入日记帐。
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad18063e0a66a4aac0ebef7f0ce45c73137abcc7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968521"
---
# <a name="journalize-posted-journal-entries"></a>将过帐日记帐条目记入日记帐

[!include [banner](../../includes/banner.md)]

该过程显示如何将过帐的日记帐条目记入日记帐。 此过程使用演示数据公司 USMF。

1. 在 **导航窗格** 中，转到 **模块 > 总帐 > 分类帐设置 > 总帐参数**。
2. 可将 **扩展分类日记帐** 字段设置为“是”或“否”。 如果设置为“是”，报表输出将不同。
3. 选择如果尚未运行日记帐分录流程时是否可关闭期间。 如果此选项设置为“是”，则完成期间的日记帐分录流程之前，不能关闭该期间。  
4. 关闭该页面。
5. 在 **导航窗格** 中，转到 **模块 > 总帐 > 定期任务 > 日记帐分录**。
6. 单击 **筛选器**。
7. 突出显示带有要定义的筛选条件的行。
8. 在 **条件** 字段中，输入或选择筛选条件。
9. 单击 **确定** 以关闭“筛选”页面。
10. 单击 **确定** 开始日记帐分录过程。 此流程完成之后将生成一个报告。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]