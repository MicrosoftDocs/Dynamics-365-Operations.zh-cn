---
title: 带有多个工作表的数据模板
description: 此主题介绍如何使用 Excel 数据实体模板将数据导入 Finance and Operations。
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 343767d056eb164a7da70fb983fe37569a12986c
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2021
ms.locfileid: "7403992"
---
# <a name="data-templates-with-multiple-worksheets"></a>带有多个工作表的数据模板

[!include [banner](../includes/banner.md)]

应用程序中的数据管理支持基于 Microsoft Excel 的数据实体模板。 这些模板可能包含一个或多个工作表。 使用包含多个工作表的模板通常是为了方便在一个文件中管理数据并将其导入到多个数据实体中。 例如站点和仓库。

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>一次性上传文件，并将其映射到所有实体
举个例子，有一个 Excel 文件包含名称为 **站点** 和 **仓库** 的工作表。 若要设置数据导入项目，则添加第一个数据实体 **站点**，然后上传文件。 您可以选择 **站点** 作为要对该实体使用的工作表。

如果您在不离开 **添加文件** 窗体的情况下添加第二个实体 **仓库**，您可以通过工作表查找功能选择 **仓库** 工作表，无需再一次上传文件。 若要上传新文件，唯一的原因是 **仓库** 数据位于不同的文件中。

![多个工作表。](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>将工作表固定到实体映射

可以从网格固定在导入作业中将工作表映射到数据实体。 网格中的 **工作表** 列显示进行映射的文件的工作表。 您可以从下拉菜单中选择不同的工作表。 如果选中的工作表已经映射到数据项目中的实体，系统将要求您确认更改。 我们建议您固定网格中的所有映射。

![更新工作表映射。](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>重新映射到新文件

如果必须为数据项目中的现有实体上传相同文件的新版本或全新文件，必须使用 **添加文件** 体验再次添加实体，如同是第一次添加这些实体一样。 在继续执行下一步操作之前，系统将询问您是否确定要覆盖数据项目中的现有实体。 未再次添加（或覆盖）的实体将继续保留之前来自上一个文件的映射。

## <a name="upload-a-file-using-run-project"></a>使用“运行项目”上传文件

您可以在使用 **运行项目** 选项执行导入项目时上传 Excel 文件。 您必须注意，上传的文件仅包含与数据项目中的数据实体的现有映射相同的工作表。 如果在新上传的文件中找不到某个工作表，系统将显示错误，并停止导入。 如果必须对某个实体更改到工作表的映射，必须先从数据项目内部更新数据项目中的映射，然后在 **运行项目** 体验中使用文件。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
