---
title: 创建租赁组
description: 本主题说明如何设置租赁组。 需要租赁组才能创建建新租赁。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8ad226e87776615d9c19a239e0fb90b648d9c49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210449"
---
# <a name="create-a-lease-group"></a>创建租赁组

[!include [banner](../includes/banner.md)]

本主题说明如何设置租赁组。 需要租赁组才能创建建新租赁。 租赁帐簿与每个租赁组关联。 租赁帐簿确定必须为每个租赁创建的默认帐簿。 您可以在 **租赁过帐参数** 页上将特定科目分配给租赁组。

## <a name="create-a-lease-book-and-add-a-lease-group"></a>创建租赁帐簿和添加租赁组

1. 转到 **资产租赁 \> 设置 \> 租赁组**。
2. 在操作窗格中，选择 **新建** 添加租赁组。 将向网格添加一行。
3. 在新行的 **租赁组** 字段中，输入一个值。
4. 在 **描述** 字段中，输入一个值。

将把您刚才输入的信息添加到 **添加租赁** 页上的 **租赁组** 字段中。

## <a name="associate-a-book-with-a-lease-group"></a>将帐簿与租赁组关联

创建租赁组后，可以为每个组分配帐簿。 创建租赁并将其分配给租赁组时，系统会为与该租赁组关联的每本帐簿创建一组计划。

> [!NOTE]
> 必须先设置帐簿，然后才能将它们分配给租赁组。

1. 转到 **资产租赁 \> 设置 \> 租赁组**。
2. 选择一个租赁组，然后选择 **帐簿**。
3. 选择 **新建**，然后在 **帐簿类型** 字段中，选择要分配给租赁组的帐簿。 如果必须以不同的方式核算租赁，则可以为一个租赁组分配多个帐簿。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]