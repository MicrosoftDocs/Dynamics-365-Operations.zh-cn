---
title: Base64StringToContainer ER 函数
description: 本主题提供有关 Base64StringToContainer 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739059"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER 函数

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [函数](er-formula-language.md#functions)将 *字符串* 类型的指定输入转换为 *[容器](er-functions-category-container.md)* 类型的数据项。

## <a name="syntax"></a>语法

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>参数

`input`：*字符串*

*字符串* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*集装箱*

二进制大型对象 (BLOB) 格式的结果二进制值。

## <a name="usage-notes"></a>使用说明

如果输入字符串未提供正确的二进制到文本编码方案的 Base64 组，则会引发“参数无效”异常。

## <a name="example"></a>示例

在模型映射中定义以下数据源：

- 引用 **DocuTypeGroup** 应用程序枚举的 *Dynamics 365 for Operations/枚举* 类型的根 **DocuTypeGroupEnum** 数据源
- 引用 **CustTable** 应用程序表的 *Dynamics 365 for Operations/表记录* 类型的根 **Customer** 数据源
- 如下配置的 *计算字段* 类型的 **\#Media** 数据源：

    - 被添加为 **Customer** 数据源的子数据源。
    - 包含 `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` 表达式。

- 如下配置的 *计算字段* 类型的 **\#MediaAsBase64String** 数据源：

    - 被添加为 **Customer.'\#Media'** 数据源的子数据源。
    - 包含 `Customer.'#Media'.'getFileContentAsBase64String()'` 表达式。

- 如下配置的 *计算字段* 类型的 **\#BlobFomBase64** 数据源：

    - 被添加为 **Customer.'\#Media'** 数据源的子数据源。
    - 包含 `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` 表达式。

在此示例中，**\#MediaAsBase64String** 数据源将当前媒体附件的二进制内容编码为表示二进制到文本编码方案的 Base64 组的文本。 **\#BlobFomBase64** 数据源对 Base64 字符串进行解码，以 BLOB 格式返回二进制值。

![ER 模型映射设计器页上的示例数据源](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>其他资源

[容器函数](er-functions-category-container.md)
