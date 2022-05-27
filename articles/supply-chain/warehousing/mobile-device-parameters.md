---
title: 全局移动设备参数
description: 本主题说明如何在仓库管理参数页面上设置移动设备设置。
author: Mirzaab
ms.date: 08/13/2021
ms.topic: article
ms.search.form: WHS
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-13
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0ae04c86ff1eafb649fcef7c34ace66bdc3e5cb8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679156"
---
# <a name="global-mobile-device-parameters"></a>全局移动设备参数

[!include [banner](../includes/banner.md)]

本主题说明如何设置影响系统与移动设备交互方式的全局仓库管理参数。

有关如何设置仓库工作人员的详细信息，请参阅[管理仓库工作人员](manage-warehouse-workers.md)。 有关在移动设备上处理的牌照的详细信息，请参阅[通过 Warehouse Management 移动应用的牌照接收](warehousing-mobile-device-app-license-plate-receiving.md)。 有关周期盘点流程的详细信息，请参阅[周期盘点](cycle-counting.md)和[周期盘点示例场景](cycle-counting-scenarios.md)。

## <a name="open-the-warehouse-management-parameters-page"></a>打开仓库管理参数页面

要打开 **仓库管理参数** 页面，转到 **仓库管理 \> 设置 \> 仓库管理参数**。 然后，您可以设置与移动设备工作相关的字段，如本主题下一节所述。

## <a name="mobile-device-fasttab-on-the-general-tab"></a>“常规”选项卡上的“移动设备”快速选项卡

全局移动设备设置位于 **仓库管理参数** 页面 **常规** 选项卡上的 **移动设备** 快速选项卡。 提供以下字段。

| 字段 | 说明 |
|---|---|
| 移动设备注释类型 | 选择挑选销售订单时显示给工作人员的信息类型。 |
| 已扫描的数量限制 | 使用 **工作创建流程** 值为 *调入* 的移动设备菜单项输入工作人员在每个会话期间可以扫描的最大物料数量。 此字段不影响使用任何其他类型的菜单项完成的扫描。 |
| 使用移动设备会话日志记录 | 将此选项设置为 *是* 可以保留工作人员登录历史记录。 要查看日志，转到 **工作用户会话 \> 查询和报表 \> 移动设备日志 \> 工作用户会话**。 |
| 存储的错误数 | 输入系统应存储的最大错误记录数。 要查看错误日志，转到 **工作用户会话 \> 查询和报表 \> 移动设备日志 \> 工作用户会话**。 |
| 默认仓库转移日记帐 | 选择当工作人员使用移动设备将产品从一个仓库移到另一个仓库时使用的日记帐。 |
| 外部审查时，允许登记采购订单行 | 如果工作人员应该能够使用移动设备为 **审批状态** 值为 *正在进行外部审查* 的采购订单登记订单行，将此选项设置为 *是*。 将此选项设置为 *否* 将阻止工作人员为正在进行外部审查的采购订单登记行。 |
| 启用 RSAT 支持 | 此字段启用 Warehouse Management 移动应用任务验证器，其记录和验证应用执行的每个步骤。 由于此过程会显著降低系统性能，因此您应该仅在测试期间启用验证器。 而不应该在生产环境中启用。 |
