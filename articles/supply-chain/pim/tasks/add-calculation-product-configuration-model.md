---
title: 将计算添加到产品配置模型
description: 该过程显示如何添加新计算到产品配置模型。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d201061ff47203f09f96dc08ff6fc8ac437a6f9e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570649"
---
# <a name="add-a-calculation-to-a-product-configuration-model"></a>将计算添加到产品配置模型

[!include [banner](../../includes/banner.md)]

该过程显示如何添加新计算到产品配置模型。 它显示如何通过使用“If”运算符将白色扬声器高度设置为 10，将所有其他完工机柜设置为 15 来创建逻辑表达式。 该过程使用演示公司 USMF 的高端扬声器组件。


## <a name="add-a-calculation"></a>添加一个计算

## <a name="create-calculation-expression"></a>创建计算表达式
1. 单击“编辑表达式”。
2. 在“约束体”字段中，输入“如果[完工机柜==“白色”，10, 15]”。
3. 单击“验证”。
4. 单击“关闭”。
5. 单击“确定”。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]