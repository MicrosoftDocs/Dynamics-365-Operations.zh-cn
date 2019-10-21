---
title: (RCS) 导入包含可选属性的 XML 格式文件
description: 本主题介绍用户如何设计 ER 格式配置以导入 XML 格式且包含可选属性的文件。
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182178"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a>(RCS) 导入包含可选属性的 XML 格式文件

[!include [task guide banner](../../includes/task-guide-banner.md)]

以下步骤说明系统管理员或电子报表开发人员角色的用户如何设计 ER 格式配置，以便导入包含可选属性的 XML 格式文件。 为了完成这些步骤，您必须首先完成“创建配置提供商并标记为有效”这一过程中的步骤。 开始之前，从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载 IncomingDocumentToLearnHowToHandleOptionalAttributes.xml 文件并保存到本地。

1.  转到**所有工作区** > **电子申报**。
2.  确保示例公司 Litware 公司的配置提供程序可用且标记为**有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](er-configuration-provider-mark-it-active-2016-11.md)这一过程中的步骤。
3.  单击**申报配置**。

## <a name="create-a-new-data-model-configuration"></a>创建新的数据模型配置
1.  单击**创建配置**，以打开下拉对话框。
2.  在**名称**字段中，键入“用于导入 xml 文件的模型”。
3.  单击**创建配置**。
4.  单击**设计器**。
5.  单击**新建**，以打开对话框。
6.  在**名称**字段中，键入“根”。
7.  单击**添加**。
8.  单击**新建**，以打开对话框。
9.  在**名称**字段中，键入“列表”。
10. 在**物料类型**字段中，选择**记录列表**。
11. 单击**添加**。
12. 单击**新建**，以打开对话框。
13. 在**名称**字段中，键入“代码”。
14. 在**物料类型**字段中，选择**字符串**。
15. 单击**添加**。
16. 单击**保存**。
17. 关闭该页面。
18. 单击**更改状态**。
19. 单击**完成**。
20. 单击 **确定**。

## <a name="create-a-format-for-data-import"></a>创建格式以导入数据
1.  单击**创建配置**，以打开下拉对话框。
2.  在**新建**字段中，输入“格式基于‘用于导入 xml 文件的模型’数据模型”。
3.  在**名称**字段中，键入“用于导入 xml 文件的格式”。
4.  在**支持数据导入**字段中选择**是**。
5.  单击**创建配置**。

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>设计格式以分析 xml 格式的传入文件
1.  单击**设计器**。
2.  单击**添加根**以打开下拉对话框。
3.  在树结构中，选择 **XML\元素**。
4.  在**名称**字段中，键入“根”。
5.  单击 **确定**。
6.  单击**添加**以打开下拉对话框。
7.  在树结构中，选择 **XML\元素**。
8.  在**名称**字段中，键入“单据”。
9.  在**多样性**字段中，选择**一个 多个**。
10. 单击 **确定**。
11. 在树中，选择**根\文档**。
12. 单击**添加**以打开下拉对话框。
13. 在树结构中，选择 **XML\属性**。
14. 在**名称**字段中，键入“ID”。
15. 单击 **确定**。
16. 单击**保存**。

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>设计格式映射以将分析的信息保存到数据模型
1. 单击**将格式映射到模型**。
2. 单击**新建**。
3. 在**定义**字段中，输入或选择一个值。
4. 在列表中，单击所选行中的链接。
5. 在**名称**字段中，键入“映射”。
6. 单击**保存**。
7. 单击**设计器**。
8. 在树中，展开**格式**。
9. 在树中，展开**格式\根: XML 元素(根)**。
10. 在树中，选择 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)**。
11. 单击**绑定**。
12. 在树中，展开 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)**。
13. 在树中，选择 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)\id**。
14. 在树中，展开**列表 = format.root.document**。
15. 在树中，选择**列表 = format.root.document\代码**。
16. 单击**绑定**。
17. 单击**保存**。
18. 关闭该页面。
 
## <a name="run-format-mapping"></a>运行格式映射
1. 单击**运行**。
2. 单击**浏览**，然后选择 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。
3. 单击 **确定**。

> [!NOTE]
> 尚未导入所选文件，因为格式设计认为“文档”元素有“id”属性，但是导入的文件中不包含此类属性。

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>修改格式结构以将 xml 属性作为可选属性处理。
1. 关闭该页面。
2. 在树中，展开**根\文档**。
3. 在树中，选择**根\文档\id**。
4. 在**清空所缺少属性的字符串**字段中选择**是**。
5. 单击**保存**。
 
## <a name="run-format-mapping-to-test-changes"></a>运行格式映射以测试更改
1. 单击**将格式映射到模型**。
2. 单击**运行**。
3. 单击**浏览**，然后选择 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** 文件。
4. 单击 **确定**。
5. 检查生成的文件。 

> [!NOTE]
> 已导入同一个文件，因为格式设计现在将“document”元素的“id”属性视为可选。
