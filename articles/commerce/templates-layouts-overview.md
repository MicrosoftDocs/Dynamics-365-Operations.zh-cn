---
title: 模板和布局概览
description: 本文介绍 Microsoft Dynamics 365 Commerce 中的模板和布局。
author: phinneyridge
ms.date: 10/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 0664dd1ae06d09557cf8b8ec58baf6d27c1198bd
ms.sourcegitcommit: 023ae5557e1351a8329a59a41a551e8901db99a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733376"
---
# <a name="templates-and-layouts-overview"></a>模板和布局概览


[!include [banner](includes/banner.md)]

模板是 Microsoft Dynamics 365 Commerce 页面模型的基础元素。 如果您的目标是最大限度发挥站点创作工作流的效率和一致性，请务必了解如何为网站利用模板。 尽早做出有关模板结构的决策非常重要，可以显著影响每日、季节性和站点范围品牌更新的成本和敏捷性。 精心构造的模板还有别的一些优点。 例如，有助于提高网站范围的搜索引擎优化 (SEO) 分数和最大限度降低缺陷数量。

开始使用模板的一个好方法是，了解模板和布局的功能优点，两者之间的区别，以及层次结构。

下图显示呈现的网页背后的页面模型层次结构。

![页面模型图。](../commerce/media/page-model-diagram.png)

| 实体        | 基本功能 |
|---------------|----------------|
| 模板      | 模板定义一组布局和页面实例的模块选项和基本支架。 |
| 布局        | 布局定义为一个或一组页面最终选择的模块及其排列。 |
| 页面实例 | 页面实例定义特定页面的数据和内容。 |

## <a name="templates"></a>模板

模板位于 Dynamics 365 Commerce 页面模型层次结构顶端，并提供站点配置的重要早期步骤。 从概念上来说，模板通过定义下游布局创建与页面创建工作流的基础结构和创作环境，帮助控制一系列子布局和页面之间的一致性。 模块可以通过预定义的集中管理元素（如页眉和页脚）和引导式创作流（可以帮助确保模块配置选项品牌化），帮助简化内容创作流程。

### <a name="controlling-consistency"></a>控制一致性

设计模板时，必须做出的最大业务决策是，模板对页面创建流程的控制力度应该有多深。 要创建模板，最简单的方法是将一切都开发给下游作者，但是要维护基于此类模板创建的页面，可能存在长期性的后果。 精心编写携带模板可以提供指导和简化创作体验，同时可以为作者提供灵活性，使其可以完成自己的任务。 所有这些方面都取决于模板实施的控制级别。

模板可以通过以下方法帮助内容作者提高效率和保持品牌化：

- 限制页面中可以使用的模块。
- 建议默认模块和配置选择。
- 明确进行一些在模板级控制的模块和配置选择。 此过程也称为 *锁定* 设置。

以下示例演示如何配置一个基本模板（模板 X）：

- 模板 X 的所有子布局都必须有页眉容器、主体容器和页脚容器。
- 在模板 X 中，页眉容器的配置已锁定，只能在模板 X 本身中更改。 所有子布局和页面始终具有此页眉。
- 主体容器需要至少一个模块，最多十个模块。 这些模块由下游布局和页面定义。
- 对于主体容器，可以使用主图、特色、传送和横幅模块。
- 页脚容器在模板 X 中配置，但是可以被下游布局和页面替换。

此示例中的模板为下游内容作业定义一个简单结构和一组选项。 请注意，模板中定义和锁定了页面的某些部分（此示例中为页眉），下游作者不能更改这些部分。 在特定范围内（此示例中为最小数量和最大数量的特定类型模块），下游作者可以定义其他部分（此示例中为主体）。 其他部分（此示例中为页脚）在模板中定义，但是可以被下游作者替换。

站点和品牌管理员的一个重要初始步骤是，确定子布局和页面作者的约束与灵活性之间的正确平衡。 如果使用模板，此平衡完全可配置。 它影响页面元素是集中更新（在元素中锁定），还是留给页面层次结构中更下方的单个子级别。

### <a name="relationship-between-template-defaults-and-page-content"></a>模板默认值和页面内容之间的关系

模板的主要功能是在创建页面时简化模块创作体验。 除了在编辑页面时，其他情况下，即使在模板中设置甚至锁定了模块默认值，也没有从页面的模块配置到模板默认值的进一步数据连接。 模板控制页面结构的创作体验，页面创建后，模板默认值不再链接到该页面上的可本地化内容。 换言之，在模板中设置的模块默认值控制子页面的创作体验。 在创建和编辑页面后，它们不再控制这些页面上的内容。

将[片段](work-with-fragments.md)添加到模板时，会出现上述行为的唯一例外情况。 片段可用于随时在模板或布局的所有子页面上动态添加或编辑可本地化内容，即使是在从给定模板创建了很多页面之后。 每当应在所有子页面上动态添加、删除或编辑可本地化内容时，最佳做法是在模板和布局中使用片段。 例如，片段应用于页眉、页脚、通用元数据/脚本或任何其他必须可集中编辑且在所有子页面中相同的内容。 片段提供了一种使用模板和布局来控制所有子页面内容的方法。

要开始使用模板，请参阅[使用模板](work-with-templates.md)。

## <a name="layouts"></a>布局

模板是页面模型层次结构中低于模板的下一个级别。 模板定义允许页面采用的所有模块，而布局这是对模块的明确选择和排列。 页面是页面模型层次结构中低于布局的下一个级别。 它们定义布局中所选模块的本地化内容。

以下示例建立在上一部分中的模板示例基础上，并显示可如何配置基本布局：

- 布局的父模板要求主体容器中有一到十个模块。 这些模块只能是主图、特色、传送和横幅模块。 因此，布局可以定义对模块的以下选择和排列：

    - 主体容器中的第一个模块为横幅模块，然后是一个主图模块和两个特色模块。
    - 第一个特色模块左对齐，第二个特色模块右对齐。

- 即使默认页脚是从父模板继承的，模板作者仍然未锁定页脚。 因此，布局可以通过定义其他页脚片段来替换它。

此示例中的布局定义子页面的最终模块排列。 和模板一样，布局可以定义子页面始终继承的默认或锁定模块属性（例如，特色模块的对齐方式）。 然后在每个子页面实例中层次结构内继续向下定义布局中每个模块的实际内容或数据。 此处的一个重要区别是，布局不直接包含可本地化内容，而是子页面包含。 布局的主要功能是定义其子页面的模块的最终排列和默认配置。

此层次结构非常强大，原因有两个。 第一，对于布局切换方案来说，共享同一个父模板的布局被视为兼容。 因此，无需创作页面级内容，即可从同一个模板层次结构将任何页面的布局更改为另一个布局。 可以利用此功能执行季节性设计更新、试验或永久站点重新设计。 其次，还可以通过布局集中修改一组页面的共享元素，无需对单个页面进行更新。 例如，如果一个产品类别有 1,000 页共享同一个布局，并在该布局中对模块重新排序，将在所有 1,000 个子页面中立即体现此更改。

可通过理解此层次结构交付敏捷、高效的站点结构来帮助节约成本，实现灵活性和随着站点的进化产生更好的结果。

### <a name="preset-and-custom-layouts"></a>预设布局和自定义布局

站点中的布局可以是 *预设的* 或 *自定义的*：

- **预设布局** 可用于执行下面的页面创建工作流：已选择和排列了所有模块，只需要输入数据。 如果必须制作具有相同布局要求的大量页面，这种方法可以帮助节约时间。 预设布局与其子页面之间存在一对多关系。 因此，可以使用一个预设布局集中控制成百上千个子页面的模块排列。
- **自定义布局** 本质上是一个页面中嵌入的单一用途布局。 创建其他新页面时或在布局切换方案中时，它们不会显示为选项。 这种方法的优点是，作者可以通过制作使用自定义布局的页面进行试验。 然后，如果作者要将布局用于其他页面，可以将其轻松转换为预设布局。 然后，新的预设布局在页面创建工作流中和布局切换方案中显示为同一个模板层次结构内的页面的一个选项。 相反，预设布局可以拆分为自定义布局。 这样，作者就可以从预设布局中分解页面，并创建新的单一用途自定义布局。 （这些新的自定义布局仍然需要遵守父模板中的所有约束。）

预设布局和自定义布局在创作工具集中的不同部分进行编辑。 因为自定义布局不依赖其他任何页面，所以直接在页面编辑器中编辑。 因此，布局的存在对用户来说最透明，并仅在页面级属性中和布局选项的操作中显示。 但是，因为对预设布局的更改可能影响大量子页面，所以必须在布局编辑器中编辑，在布局编辑器中，发布操作会考虑整个下游对子页面的影响。

下图显示预设布局和自定义布局的方案。

![预设布局方案和自定义布局方案。](../commerce/media/template-figure1.png)

若要开始使用预设布局，请参阅[使用预设布局](work-with-layouts.md)。

## <a name="additional-resources"></a>其他资源

[使用模板](work-with-templates.md)

[使用预设布局](work-with-layouts.md)

[使用发布组](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
