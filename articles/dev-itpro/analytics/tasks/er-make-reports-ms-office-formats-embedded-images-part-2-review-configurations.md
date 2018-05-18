--- 
title: "检查配置以创建包含嵌入图像的 Microsoft Office 格式报表"
description: "若要完成这些步骤，必须首先完成“ER 创建包含嵌入图像的 MS Office 格式报表（第 1 部分 - 设置参数）”任务指南中的步骤。"
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fe58809c60fa27a605d84a61893ff569ded058ef
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---
# <a name="review-configurations-to-make-reports-in-microsoft-office-formats-with-embedded-images"></a>检查配置以创建包含嵌入图像的 Microsoft Office 格式报表

[!include [task guide banner](../../includes/task-guide-banner.md)]

若要完成这些步骤，必须首先完成“ER 创建包含嵌入图像的 MS Office 格式报表（第 1 部分：设置参数）”任务指南中的步骤。

此过程显示如何设计电子申报 (ER) 配置，以便在 Microsoft Excel 和 Microsoft Word 中生成包含嵌入图像的电子单据。 在此示例中，您将查看示例公司 Litware 公司 的 ER 配置。 

此过程针对向其分配了系统管理员角色或电子申报开发人员角色的用户。 可使用 USMF 数据集完成这些步骤。


## <a name="review-the-imported-data-model"></a>查看导入的数据模型
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，选择“支票的模型”。
3. 单击“设计器”。
    * 此模型设计为从业务角度表示付款支票和将此模型映射到应用程序的数据源。 按 ER Operations 设计器检查此模型。 注意显示的模型元素属性：结构、名称、描述、数据类型等。   
4. 在树中，展开“根”。
5. 在树中，选择“根\支票”。
6. 在树中，展开“根\支票”。
7. 在树中，展开“根\支票\属性”。
8. 在树中，展开“根\付款人”。
9. 在树中，选择“根\istestrun“.
10. 在树中，选择”根\布局“。
    * 此模型的布局元素表示所选银行帐户的打印支票表布局的详细信息。 还包括“容器”数据类型的两个节点，用于存储图像。   
11. 在树中，展开”根\布局“。
12. 在树中，选择”根\布局\公司徽标“。
13. 在树中，展开”根\布局\公司徽标“。
14. 在树中，选择”根\布局\公司徽标\图像“。
15. 在树中，选择”根\布局\公司徽标\isprinted“。
16. 在树中，选择”根\布局\签名“。
17. 在树中，展开“根\布局\签名”。
18. 在树中，选择”根\布局\签名\图像“。
19. 在树中，选择”根\布局\签名\isprinted“。
    * 请注意，已将两个图像数据模型元素绑定到其中包含二进制格式的公司徽标图像和授权人员签名图像的表的字段。  
20. 在树中，展开“根\布局\水印”。
21. 单击“映射模型到数据源”。
22. 单击“设计器”。
23. 在树中，展开“chequesselected”。
24. 在树中，展开“布局”。
25. 在树中，展开”布局\公司徽标“。
26. 在树中，展开“布局\签名”。
27. 在树中，展开“布局\水印”。
28. 打开”显示详细信息“。
    * 请注意，已将支票数据模型元素绑定到 TmpChequePrintout 表，该表在运行时将包含用户已收集来打印的支票的记录。   
29. 关闭该页面。
30. 关闭该页面。
31. 关闭该页面。

## <a name="review-the-imported-format"></a>查看导入的格式
1. 在树中，展开“支票的模型”。
2. 在树中，展开“支票的模型\支票打印格式“。
3. 单击“设计器”。
4. 单击“附加”。
5. 单击“打开”。
    * 在 Excel 中打开附加报表的模板。  
    * 查看附加的报表的将用于打印支票的 Excel 模板。 此模板中每页包含两张支票，并设计为将支票打印到预打印的表。 请注意嵌入了两个空白图像。 这些空白图像用于公司徽标和为付款授权的人员的签名。 在 Excel 中分别验证名称为 CompLogo 和 SignatureImage 的图像。   
6. 关闭该页面。
7. 在树中，展开“报表”。
8. 在树中，展开“报表\ChequeLines”。
9. 在树中，选择”报表\ChequeLines\CompLogo“。
10. 打开”显示详细信息“。
    * 请注意，“CompLogo”格式的单元格元素表示用于在报表中填充公司徽标图像的 Excel 项。 此格式元素绑定到在运行时包含二进制格式的公司徽标图像的图像数据模型元素。   
11. 单击“映射”选项卡。
12. 单击“已启用编辑”。
    * 请注意，可以创建“CompLogo”格式的单元格元素，以便不再启用该格式。 在此示例中，关联的 Excel 图像元素将隐藏所生成报表中的公司徽标。 如果启用的表达式返回 TRUE，并且定义的绑定不提供图像，关联的 Excel 图像元素将显示已在 Excel 模板中保存的图像。   
13. 关闭该页面。
14. 在树中，展开“标签: 容器”。
    * 出于测试目的创建报表时，其中将包含预打印支票表中的一些标签。 但是实际打印时将不打印这些标签，因为预打印的表已包含这些标签。  
15. 关闭该页面。


