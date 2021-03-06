---
title: 设置费率主数据
description: 此过程显示如何设置费率主数据。
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 462bfce89fa77c8830a93a22b0dd6c8c8fb2cde6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555298"
---
# <a name="set-up-rate-masters"></a>设置费率主数据

[!include [task guide banner](../../includes/task-guide-banner.md)]

此过程显示如何设置费率主数据。 物流经理通常根据与承运人签订的合同设置费率主数据。 在此场景中，您将设置航空承运人的费率主数据。 创建此程序的演示数据公司是 USMF。


## <a name="set-up-rate-master"></a>设置费率主数据
1. 转到“运输管理”>“设置”>“评级”>“费率主数据”。
2. 单击“新建”。
3. 在“费率主数据”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“评级元数据 ID”字段中，单击下拉按钮以打开查找。
    * 评级元数据 ID 将确定费率主数据所需的数据，因为其定义使用此费率主数据的 TMS 引擎预期的主数据。  
6. 在本示例中，选择 P2P 选项
7. 在列表中，单击所选行中的链接。
8. 单击“保存”。

## <a name="set-up-rate-base"></a>设置基本费率
1. 单击“基本费率”。
    * 基本费率确定承运人的费率，并且可用于设置关税结构，因为其构成分解主数据中定义的中断点的费率。  
2. 单击“新建”。
3. 在“基本费率”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 在“分解主数据”字段中，单击下拉按钮以打开查找。
    * 分解主数据用于定义价格结构及其中断点。 价格结构使用基于物理维度的分层定价方式。  
6. 在本示例中，使用重量
7. 在列表中，单击所选行中的链接。
8. 切换“详细信息”部分的展开项。
9. 单击“新建”。
10. 在“卸货地邮政编码起始编号”字段中，键入“30301”。
11. 在“卸货地邮政编码结束编号”字段中，键入“30318”。
12. 在“卸货国家/地区”字段中，键入“美国”。
13. 在“<1.00 磅”字段中，键入 '100'。
    * 如果负荷的总重量少于 1 磅，插入每磅费率。  
14. 在“< 5.00 磅”字段中，键入“300”。
    * 如果负荷的总重量少于 5 磅，插入每磅费率。  
15. 在“< 20.00 磅”字段中，键入“500”。
    * 如果负荷的总重量少于 20 磅，插入每磅费率。  
16. 在“< 100.00 磅”字段中，键入“1000”。
    * 如果负荷的总重量少于 100 磅，插入每磅费率。  
17. 在“< 1,000.00 磅”字段中，键入“3000”。
    * 如果负荷的总重量少于 1000 磅，插入每磅费率。  
18. 单击“保存”。
19. 关闭该页面。

## <a name="assign-rate-base"></a>分配基本费率
1. 切换“基本费率分配”部分的展开项。
2. 单击“新建”。
    * 对于每个费率主数据，您可以有几个基本费率分配。 这使得可能根据目的地、服务或不同的基本费率，为每个承运人创建多个不同的价格点。 在此过程将只创建基本费率分配。  
3. 在“名称”字段中，键入一个值。
4. 在“基本费率”字段中，单击下拉按钮以打开查找。
5. 在列表中，单击所选行中的链接。
6. 在“服务”字段中，单击下拉按钮以打开查找。
7. 在列表中，找到并选择所需记录。
8. 在列表中，单击所选行中的链接。
9. 在“提货邮政编码”字段中，键入“98052”。
    * 指定哪些邮政编码对于此基本费率分配是有效的。    
10. 在“提货国家/地区”字段中，键入“美国”。
11. 单击“保存”。

