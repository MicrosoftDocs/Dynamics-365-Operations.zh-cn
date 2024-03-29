---
title: 生成包含应用程序数据的单据
description: 若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 4 部分 - 修改格式）”这一过程。
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
ms.openlocfilehash: e0f4fe5c948d1d6ea7c306a37d629c6e381dbd00
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290445"
---
# <a name="generate-documents-that-have-application-data"></a>生成包含应用程序数据的单据

[!include [banner](../../includes/banner.md)]

若要完成此过程中的步骤，首先必须完成“ER 使用应用程序数据更新生成单据（第 4 部分：修改格式）”这一过程。



此过程中的步骤介绍如何设计电子申报 (ER) 配置以生成电子单据和更新应用程序数据。 在此过程中，将执行 ER 格式配置以生成内部统计报表，并更新应用程序数据以存档报告流程的详细信息。



此过程是为向其分配了系统管理员角色或电子申报开发人员角色的用户创建的。 可使用 DEMF 数据集完成这些步骤。 首先，确保 DEMF 公司的国家/地区上下文为 BEL（比利时）。


## <a name="set-up-foreign-trade-parameters"></a>设置外贸参数
1. 转到缴税>设置 >外贸>外贸参数。
2. 单击“数序”选项卡。

    存档内部统计报告流程的详细信息时，需要标识所创建各存档的记录。 必须为其配置特殊编号规则。  

3. 选择“内部统计存档标识”参考。
4. 在“编号规则代码”字段中，键入一个值。

    在“编号规则代码”字段中，输入或选择值“Fore_2”。  

5. 对编号规则代码执行 ResolveChanges。
6. 单击“保存”。
7. 关闭该页面。

## <a name="run-modified-er-format"></a>运行修改后的 ER 格式
1. 转到“组织管理”>“电子申报”>“配置”。
2. 在树中，展开“内部统计(模型)”。
3. 在树中，选择“内部统计(模型)\内部统计(格式)”。
4. 单击“运行”。
5. 在“输入文件名”字段中，键入“intrastat2.xml”。
6. 单击“确定”。

## <a name="review-er-format-executions-results"></a>检查 ER 格式执行结果
检查生成的 XML 文件。  
1. 关闭该页面。
2. 转到“纳税”>“申报”>“外贸”>“内部统计”。

    打开此窗体（其中包含已包括的内部统计交易记录）以查看所生成电子单据。  

3. 单击“内部统计存档”。

    由于执行的 ER 格式中现在包含应用程序数据更新的任何设置，所以已归档已完成内部统计报告的详细信息。 在此窗体中，可以查看创建的存档的标题记录。  

4. 单击“详细信息”。

    在此窗体中，可以查看创建的存档的详细信息。  

5. 关闭该页面。
6. 关闭该页面。
7. 关闭该页面。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
