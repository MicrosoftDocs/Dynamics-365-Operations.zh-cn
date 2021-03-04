---
title: 将固定资产与租赁关联
description: 本主题说明如何将现有固定资产与新租赁相关联。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
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
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d627633e43c2e6f5cad90dfe4100ff95a71541f7
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440959"
---
# <a name="associate-fixed-assets-with-leases"></a>将固定资产与租赁关联

[!include [banner](../includes/banner.md)]

本主题说明如何将现有固定资产与新租赁相关联。 将固定资产与租赁相关联时，初始确认时的使用权 (ROU) 资产价值将是固定资产的购置成本。

在将固定资产与租赁关联之前，必须在“固定资产”中为该固定资产创建一条记录。 然后，在 **租赁摘要** 页面上，您必须创建租赁并将资产链接到该租赁。

1. 按照[添加或复制租赁](add-lease.md)中的步骤添加租赁。 在 **添加租赁** 页面的 **固定资产编号** 字段中，选择尚未购置的资产。
2. 选择 **帐簿**，然后确认付款计划。
3. 选择 **初始确认**。
4. 选择 **资产租赁日记帐**。

    租赁的初始确认日记帐条目从固定资产中扣除通常从使用权资产科目中扣除的金额。

    现在，您可以查看固定资产的交易类型和帐簿。

5. 选择 **日记帐详细信息**。
6. 选择 **行** 查看日记帐条目的各行。
7. 选择包含资产的日记帐行，然后选择 **固定资产** 选项卡。

    **固定资产** 选项卡显示交易类型和帐簿。 默认情况下，**交易类型** 字段设置为 **购置**，**帐簿** 字段设置为固定资产的当前帐簿。

过帐初始确认日记帐条目后，该交易显示为固定资产的购置交易。 要查看交易表，请转到 **固定资产 \> 固定资产 \> 固定资产**，选择相应资产，然后选择 **估价**。 您应该会看到初始确认日记帐条目已经为指定的固定资产创建了一笔购置交易。

现在可以使用固定资产中的标准折旧功能对固定资产进行折旧。 有关折旧的详细信息，请参阅[折旧法和惯例](../fixed-assets/depreciation-methods-conventions.md)。

> [!NOTE]
> 如果您将固定资产与租赁关联，“资产租赁”中将禁用 **资产折旧** 和 **租赁减损** 按钮。 您可以从“固定资产”查看资产折旧和租赁减损交易。 还将禁用 **资产交易** 按钮，该按钮用于打开一个查询窗体。 您也可以在“固定资产”中打开 **资产交易** 查询窗体。  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]