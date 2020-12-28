---
title: 记录模板概览
description: 本文介绍记录模板的概念并说明如何使用它们创建共享信息的记录。
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0b55046e6c523398b4a30e674dc9f77bb6fedf3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693200"
---
# <a name="record-templates-overview"></a>记录模板概览

[!include [banner](../includes/banner.md)]

本文介绍记录模板的概念并说明如何使用它们创建共享信息的记录。

记录模板可帮助您更快创建记录，但是您只能为某些记录类型创建记录模板。

例如，假设您为旧金山的汽车租赁业务输入租赁信息。 由于大多数客户可能来自旧金山地区，因此如果您能够在租赁窗体上的 **州**、**国家/地区** 和 **城市** 字段中自动填入值将是非常理想的。

> [!NOTE]
> 您仅能将模板应用于您有权访问的区域。 但在您创建新记录时，所有模板标题均对您可见，如果您创建的是将对所有用户可用的模板，则对其他用户也可见。 请确保在命名模板时考虑到这一点。 例如，如果公司某些员工享受与佣金挂钩的薪酬为秘密，请避免使用如“佣金”之类的词语。

当某个特定窗体存在您可以访问的一个或多个模板并且您尝试在该窗体中创建新记录时，将显示 **为以下项选择模板** 页面。 在您从列表中选择某一模板时，将创建新记录，并且该新记录包含基于您选择的模板的默认信息。 如果在您创建新纪录时不想使用模板，请在 **为…选择模板** 页中选中 **不再询问** 复选框。 若要再次显示模板选择对话框，则右键单击任意记录，单击 **记录信息**，然后单击 **显示模板选择**。
