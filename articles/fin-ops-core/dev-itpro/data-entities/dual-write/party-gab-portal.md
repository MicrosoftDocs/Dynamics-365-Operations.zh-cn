---
title: 将 Microsoft Power Apps 门户与当事方数据模型配合使用
description: 本文介绍由于双重写入中的当事方数据模型对 Microsoft Power Apps 门户的 Web 角色的更改。
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: 8d7a6ae48834ddd5f06f73bfe3129e44d14d86b8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288977"
---
# <a name="using-microsoft-power-apps-portals-with-the-party-data-model"></a>将 Microsoft Power Apps 门户与当事方数据模型配合使用

[!INCLUDE[banner](../../includes/banner.md)]



双重写入应用程序业务流程解决方案版本 2.0.999.0 及更高版本包括对帐户和联系人表的当事方和全球通讯簿的数据模型更改。 这些更改允许支持高级业务方案的多对多关系。 这些更改不受门户 Web 角色支持，包括客户门户，在安装双重写入之前，这些角色是现成的或存在于您的环境中。 为了使 Web 角色按预期工作，您需要使用新的数据模型创建新 Web 角色。 

总而言之，表交互的方式已更改，但是客户门户中的表权限未更改。 本文说明如何创建与新的高级数据模型一起使用的新 Web 角色。

该图显示了 **没有** 当事方和全球通讯簿数据模型的表关系：

   ![没有当事方模型。](media/without-party-model.PNG)

该图显示了 **具有** 当事方和全球通讯簿数据模型的表关系：

   ![具有当事方模型。](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>创建新的表权限

若要创建这些新的表权限，请按照下列步骤操作：

1. 登录到 [Power Apps](https://make.powerapps.com)，然后转到您的应用。
2. 选择您的门户管理应用。
3. 在侧边栏中，选择 **安全性 > 表权限**。

    您必须创建三个新权限：

    + **联系人** 与 **当事方** 表的连接
    + **当事方** 与 **客户** 表的连接
    + **客户** 与 **订单** 表的连接

4. 创建并保存联系人与当事方的连接的新权限，设置以下参数：

    + **名称**：**当事方** 与 **客户** 表的连接（或您的选择）
    + **表名称**：msdyn_contactforparty
    + **网站**：客户门户
    + **范围**：联系人
    + **特权**：全选
    + **Web 角色**：经过身份验证的用户、客户代表（或您的选择）

5. 创建并保存当事方与帐户的连接的新权限，设置以下参数：

    + **名称**：当事方与帐户的连接（或您的选择）
    + **表名称**：帐户
    + **网站**：客户门户
    + **范围**：父级
    + **特权**：全选
    + **父表权限**：联系人与当事方的连接

6. 创建并保存帐户与订单的连接的新权限，设置以下参数：

    + **名称**：帐户与订单的连接（或您的选择）
    + **标名称**：销售订单
    + **网站**：客户门户
    + **范围**：父级
    + **特权**：全选
    + **父表权限**：当事方与帐户的连接

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
