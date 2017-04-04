---
title: "POS 应用程序和用户语言设置"
description: "此主题描述如何更改在 Retail Modern POS (MPOS) 的语言设置和覆盖 POS。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>POS 应用程序和用户语言设置

此主题描述如何更改在 Retail Modern POS (MPOS) 的语言设置和覆盖 POS。

<a name="overview"></a>概览
========

Retail Modern POS (MPOS) 和云 POS 环境和转换设置语言支持可以在不同商店和用户设置之间的位置。 例如，商店可能在有用于其客户端是最常见的区域所在，工作人员，但某些首选用于向法国转换的应用程序。

## <a name="data-language"></a>数据语言
无论用户的设置，端和云 POS 将始终使用商店的语言设置确定用于数据的转换。 这将确保所有用户和客户将存在一致的体验。  数据的示例包括：

-   产品
-   属性和值
-   类别名称
-   打印的或已发送电子邮件的交易记录收据
-   付款方式名称
-   行显示消息

商店的主要语言为 POS 登录画面，也将使用{{不：before}}，因为用户登录前向是已知的。 转换。如果商店的语言不可用，POS 将恢复公司的语言。

### <a name="configuring-the-stores-language-setting"></a>配置商店的语言设置

商店的语言设置**所有从零售店** **在 Retail Store ** ** "下的 &gt;&gt; 一般范围设置语言。 **行踪请使用下选择每个商店的语言。

## <a name="user-interface-language"></a>使用界面语言
POS 用户的语言设置决定了应用程序用户界面中的转换。 这包括没有被视为数据的所有标签、菜单和列表中。 一种例外情况是在 POS 按钮网格中显示的文本。 按钮网格不支持转换，因此，它们在按钮将始终显示文本根据中定义。 为了支持转换"按钮，您必须将复制和维护不同的按钮和网格分配给相应用户。

### <a name="configuring-the-users-language-setting"></a>配置用户的语言设置

POS 用户的语言设置设置从**所有工作人员** **对下一工作人员**页面**零售 &gt; **语言。  在"主要"选项卡上未设置模板。  POS 不使用此设置。 如果未设置用户的语言或设置为不可使用翻译的语言，POS 将恢复为商店的语言。  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | ** UI 语言** ** **      | **数据语言（产品、收据格式、行显示等）** |
| **公司** | 默认值                    | 默认值                                                           |
| **商店**   | 覆盖公司          | 覆盖公司                                                 |
| **User**    | 覆盖商店或公司 | 从不                                                             |




