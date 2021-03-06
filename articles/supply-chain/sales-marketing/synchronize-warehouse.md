---
title: 将仓库从 Finance and Operations 同步到 Field Service
description: 此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的仓库的模板和基础任务。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 7e6d7626c00b9d7d98ce872652653c36ce7bc975
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535667"
---
# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a>将仓库从 Finance and Operations 同步到 Field Service

[!include[banner](../includes/banner.md)]

此主题介绍用于同步 Microsoft Dynamics 365 for Finance and Operations 与 Microsoft Dynamics 365 for Field Service 的仓库的模板和基础任务。

[![Finance and Operations 与 Field Service 之间的业务流程同步](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)

## <a name="templates-and-tasks"></a>模板和任务
以下模板和基础任务用于运行 Microsoft Dynamics 365 for Finance and Operations 到 Microsoft Dynamics 365 for Field Service 的仓库的同步。

**数据集成中的模板**
- 仓库（Fin and Ops 到 Field Service）

**数据集成项目中的任务**
- 存放地点

## <a name="entity-set"></a>实体集
| Field Service    | Finance and Operations                 |
|------------------|----------------------------------------|
| msdyn_warehouses | 仓库                             |

## <a name="entity-flow"></a>实体流
可通过 Common Data Service (CDS) 数据集成项目将在 Finance and Operations 中创建和维护的仓库同步到 Field Service。 您要同步到 Field Service 的仓库将通过项目上的“高级查询和筛选”进行控制。 从 Finance and Operations 同步的仓库在 Field Service 中创建，**外部维护**字段设置为**是**，记录为只读。

## <a name="field-service-crm-solution"></a>Field Service CRM 解决方案
若要为 Field Service 与 Finance and Operations 之间的同步提供支持，需要 Field Service CRM 解决方案的更多功能。 在此解决方案中，**外部维护**字段已添加到**仓库 (msdyn_warehouses)** 实体。 此字段帮助确定仓库是否是从 Finance and Operations 处理或是否只存在于 Field Service 中。 此字段的设置包括：
- **是** – 仓库来自 Finance and Operations，且不可在 Sales 中编辑。
- **否** – 仓库在 Field Service 中直接输入并在这里维护。

**外部维护**字段帮助控制工作订单上库存水平、调整、转移和使用的同步。 只有**外部维护**设置为**是**的仓库可以用于直接同步到其他系统中的同一仓库。 

> [!NOTE]
> 可以在 Field Service（**外部维护** = 否）中创建多个仓库，然后使用高级查询和筛选功能将它们映射到 Finance and Operations 中的单个仓库。 这用于您希望 Field Service 掌握详细的库存水平并向 Finance and Operations 发送更新的情况。 在这种情况下，Field Service 不会收到来自 Finance and Operations 的库存水平更新。 更多信息，请参阅[将库存调整从 Field Service 同步到 Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) 和[将 Field Service 的工作订单同步到链接到 Finance and Operations 中的项目的销售订单](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order)。

## <a name="prerequisites-and-mapping-setup"></a>先决条件和映射设置
### <a name="data-integration-project"></a>数据集成项目
在同步仓库前，请确保更新项目上的“高级查询和筛选”以仅包括您要从 Finance and Operations 带入 Field Service 的仓库。 请注意，您需要 Field Service 中的仓库来将其应用到工作订单、调整和转移。  

确保有 **msdyn_warehouses** 的**集成键**：
1. 转至“数据集成”。
2. 选择**连接集** 选项卡。
3. 选择用于工作订单同步的连接集。
4. 选择**集成键**选项卡。
5. 找到 msdyn_warehouses 并确认是否添加了 **msdyn_name (name)** 键。 如果不显示，请通过单击页面顶部的**添加键**，然后单击**保存**添加。

## <a name="template-mapping-in-data-integration"></a>数据集成中的模板映射

下图显示了数据集成中的模板映射。

### <a name="warehouses-fin-and-ops-to-field-service-warehouse"></a>仓库（Fin and Ops 到 Field Service）：仓库

[![数据集成中的模板映射](./media/Warehouse1.png)](./media/Warehouse1.png)
