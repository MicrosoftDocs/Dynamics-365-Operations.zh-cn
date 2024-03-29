---
title: 基于文件大小和内容数量拆分生成的 XML 文件
description: 本文提供有关如何基于文件大小和内容项数量拆分生成的文件的信息。
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: 5347d4e85198893dd94f14508176db93ccd47c22
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280086"
---
# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a>基于文件大小和内容数量拆分生成的 XML 文件

[!include[banner](../includes/banner.md)]

可以设计电子申报 (ER) 格式以生成 XML 格式的传出单据。 有时，仅当这些单据满足特定条件（如最大文件大小或某些 XML 节点的最大数量）时，才能被接受。 可设计 ER 格式以生成满足这些单据指定的收货要求的电子单据。

- 对于 FILE 格式元素，可以以 ER 表达式的形式定义文件大小限制。 如果在生成 ER 报表时超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。
- 对于任何 XML ELEMENT 格式，可以以 ER 表达式的形式定义元素数量限制。 如果在运行 ER 报表时生成的文件中的 XML 节点数量超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。
- 对于任何 XML SEQUENCE 格式元素，可以以 ER 表达式的形式定义子元素数量限制。 如果在运行 ER 报表时生成的文件中的格式元素的嵌套 XML 节点数量超过了定义的限制，ER 将完成当前文件的创建，然后继续创建下一个文件。
- 可将任何 XML ELEMENT 格式元素标记为不可拆分。 这样就可以将生成的 XML 节点的嵌套项保留在生成的单个文件的格式元素下。

除了使用 XML ELEMENT 和 XML SEQUENCE 格式元素向生成的文件添加 XML 节点，还可以使用原始 XML 格式元素。 但是，计算节点数量以便为元素数量限制求值时，将不考虑使用原始 RAW XML 格式元素添加的节点。

如果为已配置为只要超过了特定限制就拆分生成的输出的 FILE 格式元素配置了文件目标，则将生成的输出的每一段作为单个文件发送到配置的文件目标。 若要为通过拆分输出创建的文件唯一命名，必须为 FILE 格式元素配置 ER 表达式。 如果添加 NUMBER SEQUENCE 类型的 ER 数据源，拆分的输出的每一段的编号规则将采用递增方式。

若要了解此功能的详细信息，请播放 **ER 基于文件大小或内容项数量拆分 XML 文件** 任务指南，该任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677)** 业务流程，可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载。 此任务指南可以引导您完成配置 ER 格式以根据文件大小和内容项数量拆分生成的文件这一过程。 若要完成此任务指南，必须下载以下文件：

- [ER 模型配置 - XmlFilesSplittingModel.xml](https://download.microsoft.com/download/e/a/f/eaffe96a-22ec-4a32-898a-f4328c91c387/XmlFilesSplittingModel.xml)
- [ER 格式配置 - XmlFilesSplittingFormat.xml](https://download.microsoft.com/download/e/9/c/e9c5849b-8254-4cdf-bb00-4c2ebc72ddec/XmlFilesSplittingFormat.xml)

## <a name="additional-resources"></a>其他资源
[电子申报 (ER) 目标](electronic-reporting-destinations.md)

[电子申报中 (ER) 的配方设计器](general-electronic-reporting-formula-designer.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
