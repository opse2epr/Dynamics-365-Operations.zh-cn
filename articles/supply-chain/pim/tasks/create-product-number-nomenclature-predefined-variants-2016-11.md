--- 
title: "为预定义的产品变型创建产品编号"
description: "此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。"
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: f14ee57564ad70bb7f28cd9274fc97d07974ec32
ms.contentlocale: zh-cn
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a>为预定义的产品变型创建产品编号

[!include[task guide banner](../../includes/task-guide-banner.md)]

此指南显示如何为预定义的产品变型设置产品编号命名法，以及如何将其分配给适当的产品维度组。 创建此程序的演示数据公司是 USMF。 将为“颜色和大小”产品维度组分配新产品编号命名法。 此任务通常由产品设计师完成。


## <a name="create-a-product-number-nomenclature"></a>创建产品编号命名法
1. 单击“产品变型模型定义”。
2. 单击“产品命名法”。
3. 单击“新建”。
4. 在"名称"字段中，输入可帮助识别目标产品维度组的命名法名称，如 ColorSize。
5. 在“描述”字段中，键入一个值。
6. 单击“添加”。
7. 单击“基础产品编号”。
8. 单击“添加”。
9. 单击“文本常量”。
10. 在“文本”字段中，键入一个值。
11. 单击“添加”。
12. 单击“颜色”。
13. 单击“添加”。
14. 单击“文本常量”。
15. 在“文本”字段中，键入一个值。
16. 单击“添加”。
17. 单击"大小"。
18. 关闭该页面。

## <a name="assign-the-nomenclature-to-a-product-master"></a>为基础产品分配命名法
1. 单击“产品维度组”。
2. 选择“SizeCol”产品维度组。
3. 单击“编辑”。
4. 在“使用命名法”字段中选择“是”。
5. 在“产品变型编号命名法”字段中，输入或选择一个值。
6. 关闭该页面。

