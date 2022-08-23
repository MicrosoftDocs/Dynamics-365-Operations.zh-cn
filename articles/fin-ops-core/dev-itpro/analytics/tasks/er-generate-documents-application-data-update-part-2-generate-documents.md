---
title: 设计配置以生成包含应用程序数据的单据
description: 本文介绍如何设计电子报告 (ER) 配置以生成电子文档。 （第 1 部分 - 导入配置）。
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8494f54c6f84e63e75469aa9d80d090c050b0f7f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290535"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a>设计配置以生成包含应用程序数据的单据

[!include [banner](../../includes/banner.md)]

若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 1 部分：导入配置）”这一过程。



此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据。 在此过程中，将运行已为示例公司 Litware 公司创建的 ER 导入格式配置，以便生成电子单据。



此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 可使用 DEMF 数据集完成这些步骤。 



首先，将 DEMF 公司的国家/地区上下文从 DEU（德国）更改为 BEL（比利时）。 单击“组织管理”>“组织”>“法人”以更新法人 DEMF 的主地址中的国家/地区代码。 重新启动应用程序。


## <a name="run-imported-er-format"></a>运行导入的 ER 格式
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“内部统计(模型)”。
3. 在树中，选择“内部统计(模型)\内部统计(格式)”。
4. 单击“运行”。
    * 运行 ER 格式映射的草稿版本以生成内部统计报表。  
5. 在“输入文件名”字段中，键入“intrastat.xml”。
    * 指定文件的名称。  
6. 单击“确定”。
    * 检查生成的 XML 文件。  
7. 关闭该页面。
8. 转到“纳税”>“申报”>“外贸”>“内部统计”。
    * 打开此窗体以查看所生成电子单据中包含的内部统计交易记录。  
9. 单击“内部统计存档”。
    * 由于执行的 ER 格式中不包含应用程序数据更新的任何设置，所以尚未归档已完成内部统计报表的详细信息。  
10. 关闭该页面。
11. 关闭该页面。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
