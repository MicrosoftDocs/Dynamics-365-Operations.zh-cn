---
title: "与产品相关的翻译常见问题"
description: "此主题描述了如何管理产品、产品维度值和产品属性的转换。"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 87dfdf7085e185b3e0467088118838eb832546d7
ms.contentlocale: zh-cn
ms.lasthandoff: 02/07/2018

---

# <a name="product-related-translations-faq"></a>与产品相关的翻译常见问题

[!include[banner](../includes/banner.md)]


此主题描述了如何管理产品、产品维度值和产品属性的转换。 

<a name="what-product-related-data-can-be-translated"></a>如何转换与产品相关的数据？
--------------------------------------------

您可以创建以下与产品信息相关的转换：
-   产品的名称和描述。
-   描述、友好名称和产品属性值的帮助文本。
-   产品维度值的名称和描述。

您可以将产品相关信息翻译成“**文本翻译**”页面提供的任何语言。 有关详细信息，请参阅下一节的“**如何创建产品相关信息的翻译**”。

## <a name="where-can-i-view-the-translated-information"></a>在哪儿可以查看已转换的信息？
您可以查看所有使用可转换语言的外部源文档中的与产品相关的信息的转换，比如发票。

## <a name="how-do-i-create-translations-for-product-related-information"></a>如何创建转换与产品相关的信息的转换？
按照以下步骤创产品转换：
1.  单击**产品信息管理** &gt; **通用** &gt; **已发布产品**。
2.  选择产品，在“操作窗格”的**语言**组，单击**翻译**。
3.  在“**文本翻译**”页面的“**语言**”字段选择语言。 若要添加更多的语言，请展开**语言**字段，然后单击**确定**。
4.  在“**翻译文本**”组中的“**描述**”和“**产品名称**”字段中输入翻译。

按照以下步骤创产品属性的转换：
1.  单击**产品信息管理** &gt; **通用** &gt; **已发布产品**。
2.  在“**设置**”下单击“**属性**”，然后再单击“**属性**”。
3.  在“**属性**”页面，单击“**翻译**”。
4.  在“**文本翻译**”页面的“**语言**”字段选择语言。 若要添加更多的语言，请展开**语言**字段，然后单击**确定**。
5.  在“**翻译文本**”组中的“**描述**”、“**友好名称**”和“**帮助文本**”字段中输入翻译。

按照以下步骤创产品维度值的转换：
1.  单击**产品信息管理** &gt; **通用** &gt; **已发布产品**。
2.  选择产品，然后单击“**产品维度**”。
3.  选择产品维度的一个链接：**配置**，**尺寸**，**颜色**或**样式**。
4.  选择一个维度值，然后单击“**翻译**”。
5.  在“**文本翻译**”页面的“**语言**”字段选择语言。 若要添加更多的语言，请展开**语言**字段，然后单击**确定**。
6.  在**翻译文本**组中的**名称**和**描述**字段中输入翻译。

## <a name="can-the-names-of-product-variants-be-translated"></a>可以转换产品变量的名称吗？
产品变量基于已发布产品的维度。 产品变量名称基于维度值的组合。 在转换与产品变量关联的维度值时，产品变量的名称会在已转换的版本中出现。  

**示例**  

您的产品是到大小和颜色不同的 T 恤，并且变量名称基于以下详细信息：
-   产品编号：\#3
-   维度：尺寸和颜色
-   尺寸维度值：小、中、大
-   颜色维度值：红色、绿色、黑色

基于维度值“小码”和“红色”的产品变型的名称为 **\#3:Small:Red**。  

客户需要购买一些小号的红色 T 恤，并且 T 恤的名称必须在发票上用法语显示。 您将维度值“小码”和“红色”翻译成法语，产品变型的名称为 **\#3:Petit:Rouge**。
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>提示</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>若要设置客户的首选语言，请执行以下步骤：
<ol>  
<li>单击<strong>销售和市场营销</strong> &gt; <strong>通用</strong> &gt; <strong>客户</strong> &gt; <strong>所有</strong> <strong>客户</strong>。</li>
<li>双击客户以打开“<strong>客户</strong>”页面。 在“<strong>常规</strong>”选项卡中的“<strong>语言</strong>”字段中选择“<strong>语言</strong>”。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>如果客户的首选语言是不可转换的呢？
如果客户的首选语言不可转换，则名称和描述将用您公司的全球语言显示。

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>我可以同时管理一系列维度值的转换吗？
维度值针对具体产品而有所不同，您可以管理每个产品的维度值的转换。 但是，如果您在值组中创建了维度值组和值的转换，则很容易管理转换。   

**示例**  

您的公司生产不同款式的 T 恤，每种款式都分为小码、中码和大码。 将所有尺寸收集至一个维度值组。 在添加新 T 恤款式时，可以将其与用于尺寸的维度值组关联，这样产品可拥有所有尺寸。 您还可以随时添加或更改维度值组中的所有尺寸。  

通过维度变量组与产品关联的维度值必须在产品变量组中得到维护。   
要创建一个维度值组，请执行这些步骤：
1.  单击**产品信息管理** &gt; **设置** &gt; **变型组**。
2.  选择**尺寸组**、**颜色组**或**样式组**。
3.  单击**新建**，然后在**尺寸组**、**颜色组**或**样式组**字段中输入组的名称。 单击“**尺寸**”、“**颜色**”或“**样式**”为组创建行。
4.  在**尺寸组**行、**颜色组行**或**样式组行**页面上，单击**新建**，然后为组创建尺寸、颜色和样式。

若要在维度值组中管理值的转换，请执行以下步骤：
1.  按照前面所述的创建维度值组的步骤打开“**尺寸组行**”、“**颜色组行**”或“**样式组行**”页面。
2.  单击“**文本翻译**”。 在**文本翻译**页面的**翻译文本**组的**名称**和**描述**字段中输入翻译。

## <a name="when-can-translations-of-product-related-information-be-managed"></a>何时管理与产品相关信息的转换？
可以随时管理与产品相关的信息的转换。 在为与产品相关的维度值更新转换时，无论产品是否已转换，产品信息都会更新。






