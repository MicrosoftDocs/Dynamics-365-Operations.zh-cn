---
title: 更新非制造环境中的标准成本
description: 本文提供在非制造环境中更新标准成本的指导。
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4fa545aa6903bd6f789dda20ab5755ffe9a12b88
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "323011"
---
# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a>更新非制造环境中的标准成本

[!include [banner](../includes/banner.md)]

本文提供在非制造环境中更新标准成本的指导。

以下准则假定将双版本方法用于更新标准成本。 在此方法中，一个成本计算版本包含为冻结期间最初定义的标准成本，并且第二个成本计算版本包含增量更新。 每次更新作为在第二个成本计算版本包括的成本记录输入，并且最终启用。 备选方案，一个版本方法使用最初定义的标准成本集。 双版本方法需要您定义第二个成本计算版本。 以下是定义此成本计算版本的准则：

-   分配**标准成本**的成本计算类型。
-   分配指示成本计算版本内容的有意义的标识符，例如 **2016-UPDATES**。
-   请确保内容包括成本记录。
-   允许输入所有站点的成本记录。 如果您指定某一站点，成本记录可以只为该站点输入。
-   指示回退原则为**无**。 该回退原则只应用于制造物料的成本计算。

若要纠正、调整或更新新物料的标准成本，请完成以下这些步骤。

1.  使用**成本计算版本设置**页可以使成本数据输入到第二个成本计算版本中。 可以选择阻止启用未决成本，以便在未决成本已完全和精确定义后允许启用。 您还可以选择在**开始日期**字段中输入日期。 一般而言，使用您想要启用增量更新时的日期。 或者，则将成本计算版本的**开始日期**字段留空，则在每个成本记录的**开始日期**字段中输入日期。
2.  使用**物料价格**页可以输入更新为在第二个成本计算版本报告的物料成本记录。
3.  使用**物料价格**报表验证包括在第二个成本计算版本的物料成本记录的完整性和精确性。
4.  使用**成本计算版本维护**页更改锁定标志，以便允许启用在第二个成本计算版本中的未决成本记录。
5.  使用**启用价格**页（您从**成本计算版本维护**页打开的页面）启用第二个成本计算版本中的所有未决物料成本记录。 您还可以通过单击**物料价格**页上的**启用未决价格**按钮，启用单独物料的未决成本记录。
6.  若要阻止进一步的数据维护，使用**成本计算版本设置**页更改在第二个成本计算版本内的锁定标志。 这些锁定策略将阻止输入新的未决成本和启用未决成本。




