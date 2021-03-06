---
title: 设置采购订单的工作模板
description: 该过程的重点是设置物料入库时使用的简单工作模板。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558311"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a>设置采购订单的工作模板

[!include [task guide banner](../../includes/task-guide-banner.md)]

该过程的重点是设置物料入库时使用的简单工作模板。 工作模板确定了在从接受区转移物料时，向仓管人员移动设备显示的指令集。 您可以使用演示数据公司 USMF 中提及的数据运行该过程。 在您开始本指南之前，请创建工作池 ID。 在此示例中，将使用称为“进货”的工作池 ID。 该过程专门面向仓库经理。

1. 转到“仓库管理”>“设置”>“工作”>“工作模板”。
2. 在“工作订单类型”字段中，选择“采购订单”。

## <a name="create-a-work-template-header"></a>创建工作模板标题
1. 单击“新建”。
2. 在“序列号”字段中，输入一个数字。
    * 这是工作模板的评估顺序。 如果需要，可以修改此序列。  
3. 在“工作模板”字段中，键入一个值。
    * 这是此模板的唯一标识符。  
4. 在“工作模板描述”字段中，键入一个值。
    * “有效”选项在您填写完模板所需的所有信息，以及单击“保存”后才会勾选。  
    * 采购订单类型的工作订单无法自动处理，因此将“自动处理”选项设置为“否”。  
5. 在”工作池 ID“字段中，键入一个值。
    * 工作池 ID 使您可组织工作组。 您在此处设置的值将为使用此模板创建的所有工作的默认值。  
6. 在“工作优先级”字段中，输入“1”。
    * 这表明您在此处设置的工作重要性和值将会成为使用此模板创建的所有工作的默认值。  
7. 单击“保存”。
    * 您必须保存工作模板标题才能使用“编辑查询”按钮。  

## <a name="set-up-the-query-for-the-work-template"></a>设置工作模板的查询
1. 单击“编辑查询”。
    * 我们将设置模板仅在特定仓库中使用的限制。  
2. 单击“添加”。
3. 在列表中，标记所选的行。
4. 在“字段”字段中，键入“仓库”。
5. 在“标准”字段中，输入一个值。
6. 单击“确定”。
7. 单击“是”。

## <a name="set-work-template-details"></a>设置工作模板详细信息
1. 单击“新建”。
2. 在“工作类型”字段中，选择“领料”。
3. 在“工作类 ID”字段中，键入“采购”。
    * 您在此处设置的工作类将默认显示在使用此模板创建的领料类型的所有工作行上。 工作订单行上的工作类不能被覆盖。 工作类用于处理和/或限制工作订单行的类型，而仓管人员可以在移动设备上处理此类工作订单行。  
4. 单击“新建”。
5. 在“工作类型”字段中，选择“放置”。
6. 在“工作类 ID”字段中，键入一个值。
    * 已设置领料和放置指令。 每个领料/放置必须有相同的工作类。 使用与领料指令相同的工作类。  
7. 单击“保存”。
    * 请注意，“有效”复选框现在已勾选。  

