---
title: 证书类型
description: 本主题介绍 Dynamics 365 Human Resources 的“证书类型”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798384"
---
# <a name="certificate-type"></a>证书类型

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

本主题介绍 Dynamics 365 Human Resources 的“证书类型”实体。

物理名称：mshr_hcmcertificatetypeentity

## <a name="description"></a>说明

此实体定义在 Human Resources 中设置的专业证书类型列表。 此实体不特定于法人（公司）。

## <a name="json-representation"></a>JSON 表示

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>属性

| 属性<br>**物理名称**<br>**_类型_** | 使用 | 说明 |
| --- | --- | --- |
| **证书类型实体 ID**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | 只读<br>必填 
系统生成 | 证书类型的唯一主要标识符。 |
| **证书类型**<br>mshr_certificatetype<br>*字符串* | 读/写<br>必填 | 证书类型的唯一用户可读标识符。 |
| **说明**<br>mshr_description<br>*字符串* | 读/写<br>必填 | 证书类型的描述。 |
| **需要续订**<br>mshr_requirerenewal<br>*mshr_noyes 选项集* | 读/写<br>可选 | 指示证书是否需要续订。 |

## <a name="see-also"></a>请参阅

[申请人跟踪系统集成 API 简介](hr-admin-integration-ats-api-introduction.md)<br>
[可雇用的应聘者的查询示例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]