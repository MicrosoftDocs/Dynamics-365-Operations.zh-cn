---
title: 派生帐簿
description: 本文提供衍生帐簿功能的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176584"
---
# <a name="derived-books"></a>派生帐簿

[!include [banner](../includes/banner.md)]

本文提供衍生帐簿功能的概览。

衍生帐簿用于简化定期计划的固定资产帐簿交易记录的过帐。  选择一个帐簿作为主帐簿。 这通常是用于核算折旧的帐簿。 您随后附加到作为主要帐簿以相同的间隔设置来过帐交易记录的其他帐簿。 纳税折旧帐簿通常设置为衍生帐簿。 

设置为过帐到衍生帐簿的最常见交易记录是购置、购置价格调整和处置。 

## <a name="example"></a>示例

帐簿 B 和帐簿 C 设置为针对购置交易记录类型的帐簿 A 的衍生帐簿。 在帐簿 A 中，为资产 123 的购置交易记录输入 1,500.00。 

在过帐交易记录时，在资产 123 中为帐簿 B 生成并过帐购置交易记录，并且在资产 123 中为 1,500.00 的帐簿 C 生成并过帐购置交易记录。 在您准备该主要帐簿的交易记录以用于在固定资产日志中过帐时，还可以查看和修改衍生帐簿的交易记录。 如果您在其他日志中准备主要帐簿交易记录，则衍生价值的交易记录不显示。 然而，在您过帐主要帐簿交易记录时，它们过帐到相应的帐户和过帐层。

> [!NOTE]                                                                                                                               
> 对于设置为按并非主要帐簿间隔的其他间隔过帐交易记录的帐簿，必须将它们作为单独的帐簿附加到固定资产，而不作为衍生帐簿附加。  

有关详细信息，请参阅[使用衍生帐簿过帐](post-derived-value-models.md)。



