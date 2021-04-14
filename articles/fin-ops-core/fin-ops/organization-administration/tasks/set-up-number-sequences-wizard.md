---
title: 使用向导设置编号规则
description: 此主题说明如何同时使用向导设置所有必需的数序。
author: sericks007
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d91a619423d00509ceca2ae18cb2f0371b44ead1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747289"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>使用向导设置编号规则

[!include [banner](../../includes/banner.md)]

“数序”被用于为需要它们的主数据记录和交易记录记录生成可读的唯一的标识符。 需要标识符的主数据或交易记录称为“参考”。 在您能为一个参考创建新记录之前，您必须设置编号规则并将其与参考相关联。 此主题说明如何同时使用向导设置所有必需的数序。 创建此程序的演示数据公司是 USMF。

1. 转到 **导航 > 模块 > 组织管理 > 标号规则 > 编号规则**。
2. 选择 **生成**。
3. 选择 **下一步**。

   - 在此页上您可以修改标识代码、最低值和最高值。 此外，您可以指示该编号规则是否必须是连续的。   
   - 如果您必须为该编号规则分配编号，请不要选择 **连续** 选项。 为了将范围段落添加到编号规则的格式，请在列表中选择该格式，然后选择 **将范围包括在格式中**。 为了将范围段落从编号规则的格式中删除，请在列表中选择该格式，然后选择 **从格式中删除范围**。 为了将编号规则从自动生成中排除，请在列表中选择该编号规则，然后选择 **删除**。  

4. 选择 **下一步**。
5. 选择 **完成**。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]