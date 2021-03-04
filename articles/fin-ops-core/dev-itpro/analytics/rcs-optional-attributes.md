---
title: 导入包含可选属性的 XML 格式文件
description: 本主题提供有关设计 ER 格式以指定 XML 属性来分析 XML 格式的传入电子单据的信息。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14b14dd609805a7cf9331427012b991791698cfd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686653"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a>导入包含可选属性的 XML 格式文件

[!include [banner](../includes/banner.md)]

可以设计电子申报 (ER) 格式以分析 XML 格式的传入电子单据。 可以将所设计 ER 格式中 XML 元素的某些属性指定为可选。 这样就可以正确处理拥有此类 XML 元素和没有此类元素的传入文件。 然后可以使用这些文件中的内容更新申请表数据。

若要了解有关此功能的详细信息，请完成 [(RCS) 导入包含可选属性的 XML 格式文件](tasks/import-files-xml-format-optional-attributes.md)主题中的步骤，该主题是 7.5.4.3 获取/开发 IT 服务/解决方案组件 (10677) 业务流程的一部分。 可从 [Microsoft 下载中心](https://go.microsoft.com/fwlink/?linkid=874684)下载此任务指南和关联的示例文件。


| 内容描述       | 文件                                                         |
|---------------------------|--------------------------------------------------------------|
| XML 格式的示例文件 | IncomingDocumentToLearnHowToHandleOptionalAttributes.xml     |
| 任务指南                | RCS 使用可选的 attributes.axtr 导入 XML 格式的文件 |


以下步骤说明系统管理员或电子报表开发人员角色的用户如何设计 ER 格式配置，以便导入包含可选属性的 XML 格式文件。 为了完成这些步骤，您必须首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)过程中的步骤。 开始之前，从 Microsoft 下载中心 (https://go.microsoft.com/fwlink/?linkid=874684) 下载 IncomingDocumentToLearnHowToHandleOptionalAttributes.xml 文件并保存到本地。

1. 转到 **组织管理** > **工作区** > **电子申报**。
2. 确保示例公司 Litware 公司的配置提供程序可用且标记为 **有效**。 如果没有看到此配置提供程序，请首先完成[创建配置提供程序并标记为当前运行的](tasks/er-configuration-provider-mark-it-active-2016-11.md)这一主题中的步骤。
3. 单击 **申报配置**。

## <a name="create-a-new-data-model-configuration"></a>创建新的数据模型配置
1. 单击 **创建配置**，以打开下拉对话框。
2. 在 **名称** 字段中，键入“用于导入 xml 文件的模型”。
3. 单击 **创建配置**。
4. 单击 **设计器**。
5. 单击 **新建**，以打开对话框。
6. 在 **名称** 字段中，键入“根”。
7. 单击 **添加**。
8. 单击 **新建**，以打开对话框。
9. 在 **名称** 字段中，键入“列表”。
10.    在 **物料类型** 字段中，选择 **记录列表**。
11.    单击 **添加**。
12.    单击 **新建**，以打开对话框。
13.    在 **名称** 字段中，键入“代码”。
14.    在 **物料类型** 字段中，选择 **字符串**。
15.    单击 **添加**。
16.    单击 **保存**。
17.    关闭该页面。
18.    单击 **更改状态**。
19.    单击 **完成**。
20.    单击 **确定**。

## <a name="create-a-format-for-data-import"></a>创建格式以导入数据
1. 单击 **创建配置**，以打开下拉对话框。
2. 在 **新建** 字段中，输入“格式基于‘用于导入 xml 文件的模型’数据模型”。
3. 在 **名称** 字段中，键入“用于导入 xml 文件的格式”。 
4. 在 **支持数据导入** 字段中选择 **是**。
5. 单击 **创建配置**。

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a>设计格式以分析 xml 格式的传入文件
1. 单击 **设计器**。
2. 单击 **添加根** 以打开下拉对话框。
3. 在树结构中，选择 **XML\元素**。
4. 在 **名称** 字段中，键入“根”。
5. 单击 **确定**。
6. 单击 **添加** 以打开下拉对话框。
7. 在树结构中，选择 **XML\元素**。
8. 在 **名称** 字段中，键入“单据”。
9. 在 **多样性** 字段中，选择 **一个 多个**。
10.    单击 **确定**。
11.    在树中，选择 **根\文档**。
12.    单击 **添加** 以打开下拉对话框。
13.    在树结构中，选择 **XML\属性**。
14.    在 **名称** 字段中，键入“Id”。
15.    单击 **确定**。
16.    单击 **保存**。

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a>设计格式映射以将分析的信息保存到数据模型
1.    单击 **将格式映射到模型**。
2.    单击 **新建**。
3.    在 **定义** 字段中，输入或选择一个值。
4.    在 **名称** 字段中，键入“映射”。
5.    单击 **保存**。
6.    单击 **设计器**。
7.    在树中，展开 **格式**。
8.    在树中，展开 **格式\根: XML 元素(根)**。
9.    在树中，选择 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)**。
10.    单击 **绑定**。
11.    在树中，展开 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)**。
12.    在树中，选择 **格式\根: XML 元素(根)\文档: XML 元素 1*。 (文档)\id**。
13.    在树中，展开 **列表 = format.root.document**。
14.    在树中，选择 **列表 = format.root.document\代码**。
15.    单击 **绑定**。
16.    单击 **保存**。
17.    关闭该页面。

## <a name="run-format-mapping"></a>运行格式映射
1. 单击 **运行**。
2. 单击 **浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。
3. 单击 **确定**。

> [!NOTE]
> 尚未导入所选文件，因为格式设计认为“文档”元素有“id”属性，但是导入的文件中不包含此类属性。

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a>修改格式结构以将 xml 属性作为可选属性处理。
1. 关闭该页面。
2. 在树中，展开 **根\文档**。
3. 在树中，选择 **根\文档\id**。
4. 在 **清空所缺少属性的字符串** 字段中，选择 **是**。
5. 单击 **保存**。

## <a name="run-format-mapping-to-test-changes"></a>运行格式映射以测试更改
1. 单击 **将格式映射到模型**。
2. 单击 **运行**。
3. 单击 **浏览**，然后选择文件 **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**。
4. 单击 **确定**。
5. 检查生成的文件。 请注意，已导入同一个文件，因为格式设计现在将“document”元素的“id”属性视为可选。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]