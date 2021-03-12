---
title: 每个日记帐的帐簿数
description: 本主题描述通过批处理作业创建固定资产购置或折旧建议时，日记帐与资产帐簿之间的关系。 您可以定义各项购置和折旧所包括的最大帐簿数。
author: moaamer
manager: Ann Beebe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d4ba98cefdc0b555eedfaa56b6a3ca4870b5de93
ms.sourcegitcommit: 65f9e2584c0530b1a71655aae09101691726b47f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/01/2020
ms.locfileid: "4650648"
---
# <a name="number-of-books-per-journal"></a>每个日记帐的帐簿数

[!include [banner](../includes/banner.md)]

本主题描述通过批处理作业创建固定资产购置或折旧建议时，日记帐与资产帐簿之间的关系。 您可以使用 **固定资产参数** 页面（**固定资产 \> 设置 \> 固定资产参数**）中 **常规** 选项卡上的 **每个日记帐的帐簿数** 部分中的字段定义各项购置和折旧要包含的帐簿的数量。 这些字段使您可以分配每本购置日记帐和折旧日记帐的资产帐簿的数量。

对于购置方案，默认值为至少 10,000 本帐簿。 对于折旧方案，默认值为至少 2,000 本帐簿。

例如，如果有 4,000 项固定资产，并且每项资产与两本帐簿关联，则一本帐簿将过帐到当前层，另一本帐簿则过帐到税层。 如果通过批处理购置 4,000 项固定资产，则创建一项固定资产购置日记帐的批处理作业将包含 4,000 个资产帐簿。

> [!NOTE]
> 将继续使用创建的日记帐，直到完成批处理作业。
>
> 每个日记帐的最大帐簿数量中不包含衍生帐簿。

您可以使用批处理对同一组所购置资产运行折旧。 例如，批处理作业创建两个折旧日记帐，每个折旧日记帐由 2,000 本资产帐簿组成。 第一个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 1 到 2,000。 然后，第二个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 2,001 到 4,000。

批处理作业不包括已结帐簿。 例如，在一个折旧批处理作业中，前 2,000 本帐簿中有 10 本已结。 在此示例中，第一个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 1 到 2,011。 然后，第二个日记帐将包含与固定资产关联的帐簿，这些帐簿的编号为 2,012 到 4,000。

如果同一日记帐中不存在重复的资产 ID，则将限制帐簿的数量。 但是，如果资产 ID 与帐簿 ID 相同，则可以超出每个日记帐的帐簿数，以将资产 ID 保留在同一日记帐中。

例如，有 5,001 个固定资产 ID，每个固定资产 ID 与三本帐簿关联，而每本资产帐簿过帐到同一个过帐层。 您连续三个月运行折旧，但不汇总。 折旧日记帐将通过批处理作业创建，并且系统将创建七个日记帐，这些日记帐具有 667 个固定资产 ID，每个固定资产 ID 包含三本帐簿。 结果将为 2,001 本帐簿。 因此，在三个月内，将有 6003 个日记帐行在同一日记帐中维护相同的资产 ID。 系统还将创建一个日记帐，其中有 332 个固定资产 ID，每个固定资产 ID 三本帐簿。 在三个月内，将有 2988 行。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]