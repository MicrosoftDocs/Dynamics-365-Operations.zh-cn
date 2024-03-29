---
title: 配置跨公司财务数据共享
description: 此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2caaa971790c31ed4c88bd0b2365179fb22b644e3d4512f4f06bb33bd29f8d1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736270"
---
# <a name="configure-financial-cross-company-data-sharing"></a>配置跨公司财务数据共享

[!include [banner](../../includes/banner.md)]

此过程显示在公司间共享数据时，如何配置、启用、验证和解决冲突。 它使用 USMF 公司和共享模板的财务数据。

此任务指南需要 Dynamics AX 平台 7.1 或更高版本。

1. 转到 **导航窗格 > 模块 > 系统管理 > 工作区 > 数据管理**。
2. 单击 **导入**。
3. 在 **名称** 字段中，键入一个值。
4. 在 **源数据格式** 字段中，选择“包装”类型。 单击 **上载**。 导航到共享模板包装文件的财务数据的位置并选择该文档。
5. 单击 **保存**。
6. 在列表中，标记所选的行。 选择共享刚才创建的策略的数据。  
7. 单击 **导入**。
8. 单击 **关闭**。
9. 刷新该页面。
10. 关闭该页面。
11. 关闭该页面。
12. 关闭该页面。
13. 转到 **导航窗格 > 模块 > 系统管理 > 设置 > 配置跨公司数据共享**。
14. 在列表中，找到并选择 **付款日**。
15. 单击 **添加**。
16. 在列表中，标记所选的行。
17. 在 **公司** 字段中，键入 'USSI'。
18. 单击 **添加**。
19. 在 **公司** 字段中，键入 'USMF'。
20. 单击 **保存**。
21. 单击 **启用**。
22. 单击 **是**。
23. 单击 **查找共享问题**。
24. 单击 **是**。
25. 单击 **更新字段值**。
26. 单击 **使用公司 1 的值**。
27. 刷新该页面。
28. 关闭该页面。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]