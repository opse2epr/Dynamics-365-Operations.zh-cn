---
title: 使用物料到达日记帐登记启用的基础仓库物料
description: 此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3e8ffa6cee7742de1cd98c9c83d134b6d5e4a89
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1528790"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a>使用物料到达日记帐登记启用的基础仓库物料

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程说明了在库存管理模块中使用“基本仓库”时如何使用物料到达日记帐登记物料。 这将通常由一个收料员完成。 您可以使用所示的示例值运行 USMF 公司演示数据的过程。  如果您没有使用 USMF，则在开始本指南前，您需要使用未结采购订单行以确认采购订单。 必须贮存行中的物料。 而且物料需与存储维度组进行关联，其站点和仓库是有效的。


## <a name="create-item-arrival-journal-header"></a>创建物料到达日记帐标题
1. 转到“库存管理”>“日记帐条目”>“物料到达”>“物料到达”。
2. 单击“新建”。
3. 在“名称”字段中，键入一个值。
    * 如果您正在使用 USMF，可以键入 WHS。 如果您正在使用其他数据，您选择的日记帐名称必须具有以下属性：“检查领料库位”必须设置为“否”，以及“检验管理”必须设置为“否”。  
4. 在“装箱单”字段中，键入一个值。
    * 它是来自供应商签发的装箱单的 ID。 添加唯一编号。  
5. 在“数字”字段中，在“数字”字段中，选择采购订单..
6. 单击“确定”。

## <a name="add-lines-to-item-arrival-journal"></a>添加行至物料到达日记帐
1. 单击“功能”。
2. 单击“创建行”。
    * 行可以手动输入到此日记帐中或自动创建。 它将显示您如何自动创建此字段。  
3. 选中或取消选中“初始化数量”复选框。
    * 这将用采购订单行未登记的数量初始化日记帐行上的数量。  
4. 单击“确定”。

## <a name="post-the-journal"></a>过帐日记帐
1. 单击“过帐”。
2. 单击“确定”。

## <a name="generate-the-product-receipt"></a>生成产品收据
1. 单击“功能”。
2. 单击“产品收据”。
3. 单击“确定”。

