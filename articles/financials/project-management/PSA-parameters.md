---
title: "Project Service Automation 集成参数"
description: "可在将 Project Service Automation 与 Dynamics 365 for Finance and Operations 集成时，配置应如何设置数据的默认值。"
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 32f7f70c5b1071cef5a3360ccc09fa2d95fbf9a9
ms.contentlocale: zh-cn
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation-integration-parameters"></a>Project Service Automation 集成参数

将 Project Service Automation 与 Finance and Operations 集成时，可在 **Project Service Automation 集成参数**页中配置应如何设置数据的默认值。 必须设置以下选项，才能在 Finance and Operations 中成功地从 Project Service Automation 同步项目。

> [!NOTE]
> Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。




| **选项卡**                      | **字段**                          | **说明**                    |
|------------------------------|------------------------------------|--------------------------------|
| **常规**                  | **默认项目类型**               | 选择**项目类型**的默认值，这是如果在集成模板中尚未提供默认值的情况下从 Project Service Automation 同步项目时的默认值。 同步期间，从 Project Service Automation 同步时，将把新项目的**项目类型**设置为该值。               |
| **常规**                  | **时间类别**                      | 选择**时间类别**的默认值，这是从 Project Service Automation 同步工时估计值时的情况。 同步期间，从 Project Service Automation 同步工时估计值和工时实际值时，Finance and Operations 中的新项目工时预测的**类别**将设置为该值。   |
| **常规**                  | **费用类别**                       | 选择**费用类别**的默认值，这是从 Project Service Automation 同步费用实际值时的情况。 同步期间，从 Project Service Automation 同步费用实际值时，Finance and Operations 中的新费用交易记录的**类别**将设置为该值。          |
| **项目组的默认值**   | **项目类型** | 单击**新建**添加一行，可在该行中选择要为默认项目组设置的项目类型。 在配置中，特定项目类型只能选择一次。              
|                              | **项目组**          | 为指定项目类型选择默认项目组。 从 Project Service Automation 同步新项目时，如果尚未在集成模板中提供默认值，该**项目组**将根据项目类型充当默认值。  |
| **计费类型默认值**    | **计费类型** | 单击**新建**添加一行，可在该行中选择要为默认行属性设置的计费类型。 在配置中，特定计费类型只能选择一次。          |
|                              | **记录属性**| 为指定计费类型选择默认行属性。 从 Project Service Automation 同步新工时估计值、新费用估计值或新实际值时，该**行属性**将根据计费类型充当默认值。          |
| **功能锁定**    |                   | 为源自 Project Service Automation 的项目和合同选择要在 Finance and Operations 中禁用的功能。 例如，可选择关闭 Finance and Operations 中的编辑合同和项目，创建工作分解结构以及输入工时单功能。 将继续启用与核算有关的字段，即使根据参数设置这些字段不可用也不例外。 默认情况下，将启用所有功能。           |

