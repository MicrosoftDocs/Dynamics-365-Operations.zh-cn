---
title: 审核特定采购类别的供应商
description: 本主题说明如何在 Dynamics 365 Supply Chain Management 中审核特定采购类别的供应商。
author: kamaybac
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, DirPartyEcoResCategory, EcoResCategorySingleLookup, ProcCategoryHierarchyManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 887905c35c684f2f60c3ce17eb652532831193cc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812438"
---
# <a name="approve-vendors-for-specific-procurement-categories"></a>审核特定采购类别的供应商

[!include [banner](../../includes/banner.md)]

本主题说明如何在 Dynamics 365 Supply Chain Management 中审核特定采购类别的供应商。 创建采购申请时，可能需要选择核准供应商或首选供应商，具体取决于制订的采购政策。 此过程演示如何指定供应商是特定采购类别的核准供应商或首选供应商。 此任务通常由采购专业人员完成。 您可以在演示数据公司 USMF 中使用此过程。

1. 在导航窗格中，转到 **模块 > 采购 > 供应商 > 所有供应商**。
2. 选择要设置为类别的核准供应商或首选供应商的供应商。
3. 在操作窗格上，选择 **常规**。
4. 选择 **类别**。
5. 选择 **添加类别**。
6. 在 **类别** 字段中，选择 **办公和桌面附件(办公和桌面附件)**。
7. 在 **供应商类别状态** 字段中，选择 **首选**。 可以为一个类别指定多家首选供应商。  
8. 选择 **保存**。
9. 在导航窗格中，转到 **模块 > 采购 > 采购目录**。
10. 在树中，选择 **企业采购类别\办公和桌面附件**。
11. 展开 **供应商** 部分。 检查所选供应商是否显示为办公室和桌面附件类别的首选供应商。 如果您要将此过程作为任务指南运行，可能必须选择 **解锁** 按钮才能向下滚动到供应商列表。  还可以在此页中添加首选供应商和核准供应商。  
12. 在树中，展开 **办公和桌面附件**，然后选择 **剪刀**。
13. 在 **从父类别继承供应商:** 字段中选择 **否**。
14. 在 **从父类别继承供应商:** 字段中选择 **是**。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]