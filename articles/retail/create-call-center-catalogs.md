---
title: "创建呼叫中心目录"
description: "文本提供创建呼叫中心目录的流程的概览。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, RetailCatalogDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29d005655856fd1eb0f1490c45e07649465539f2
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="create-a-call-center-catalog"></a>创建呼叫中心目录

[!INCLUDE [banner](includes/banner.md)]

文本提供创建呼叫中心目录的流程的概览。 

在呼叫中心，可以使用产品目录来标识您要为客户提供的产品。 呼叫中心常使用打印目录。 打印目录的设计和生产在 Microsoft Dynamics 365 for Retail 外部处理。 但是，您可以使用您用来设置联机零售目录的相同窗体创建和存储目录的数字窗体。 在您可以创建目录之前，必须设置产品分类和将此分类分配给呼叫中心。 然后，您可以通过从这些分类中选择产品，从而将产品添加到目录中。 在将产品添加到目录，并且目录就完成好之后，您必须验证该目录来对数据进行验证。 然后，必须提交目录以供复查和审核。 审核目录后，即可发布。 当创建呼叫中心目录时，您可以在发布该目录时，对该目录数据采用快照。 此快照功能允许您访问该目录的某一特定版本，即使以后对该目录做出更改和更新。 还可以对呼叫中心目录进行设置以包括以下可选功能。

-   **源代码** – 用于跟踪客户对特定目录邮件的响应的代码。
-   **免费产品** – 在不另行收费的情况下包含在客户订单中的产品。 当把该目录的源代码输入订单时，这些产品会被自动添加到该订单。
-   **脚本** – 在创建销售订单时，呼叫中心工作人员给客户朗读的文本。 脚本可以包括问候语或采购方案。
-   **向上销售或交叉销售物料** - 在特定产品添加到订单时显示为建议的物料。

在审核和发布目录之前，必须设置这些选项。

## <a name="prerequisites"></a>必备项
在您开始之前，必须完成以下任务：

-   设置产品和产品分类。
-   设置零售产品。
-   设置分类。
-   创建呼叫中心。
-   设置呼叫中心。
-   将呼叫中心添加到组织层次结构。
-   创建或修改组织层次结构。

## <a name="create-a-catalog"></a>创建目录
您必须首先创建一个目录，再将产品添加到该目录中，然后审查并更新产品的属性。

## <a name="validate-the-catalog"></a>验证目录
在您完成设置该目录后，必须验证它。 此验证流程验证渠道属性和产品属性所需的数据是否完整有效，并验证是否可以发布此目录。

## <a name="submit-the-catalog-for-review-and-approval"></a>提交目录以供审核和批准
验证目录后，您可以提交目录以供审查和审核。 必须先审核目录，然后才可发布。 您可以配置工作流，以便自动审核目录或需要人工审核。

## <a name="optional-add-source-codes-free-products-and-scripts"></a>可选：添加源代码、免费产品和脚本
您还可以将以下各项添加到呼叫中心目录。 这些项是可选的。

-   **“源代码”**可以由提供印刷目录的公司使用，用来跟踪客户对特定目录的响应。 源代码通常被印刷在目录的背面，在客户购买时也会输入到销售订单中。 若要将源代码添加给目录，您必须首先创建目标市场。 目标市场通常映射到所拥有的或租赁的邮寄列表。
-   **免费产品**是促销物料，在引用该目录时会免费包括在客户的订单中。
-   **脚本**可以用于在目录上下文或目录内的产品中引导工作人员与客户的交互。

## <a name="publish-the-catalog"></a>发布目录
通过发布呼叫中心的目录，就完成了该目录中的产品信息。 发布还指示该目录可供您要执行的任何其他操作使用。 例如，您可以创建打印目录。 您可以手动发布目录，也可以按照计划使用批处理发布。 必须先验证和审核目录，然后才能发布目录。 发布目录后，若要更改该目录，可以撤销该目录，然后重新发布它。




