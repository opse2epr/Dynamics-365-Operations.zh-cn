--- 
title: "设置承运人燃油指数"
description: "本指南介绍了如何创建燃油指数区域、燃油指数和承运人燃油指数。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: e9491e027a9a7806d5a10c8e0c3505c05f216a91
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-a-carrier-fuel-index"></a>设置承运人燃油指数

[!include[task guide banner](../../includes/task-guide-banner.md)]

本指南介绍了如何创建燃油指数区域、燃油指数和承运人燃油指数。 燃油指数区域指定燃油指数应该应用到哪个区域，燃油指数指定特定时间段的燃油价格。 若要反映燃料价格随时间的变化，可将多个燃油指数与承运人关联。  这些任务通常由运输协调员完成。 您可以使用演示数据公司 USMF，也可使用您自己的数据运行该过程。


## <a name="create-a-fuel-index-region"></a>创建燃油指数区域
1. 转到“运输管理”>“设置”>“燃油指数”>“燃油指数区域”。
    * 首先您必须创建不同的区域，这些区域供您操作和计算不同的燃油附加费。  
2. 单击“新建”。
3. 在“区域”字段中，键入一个值。
4. 在“名称”字段中，键入一个值。
5. 单击“保存”。

## <a name="create-a-fuel-index"></a>创建燃料指数
1. 转到“运输管理”>“设置”>“燃油指数”>“燃油指数”。
    * 对于您已设置的区域，您需要输入燃料的当前价格。  
2. 单击“新建”。
3. 在“区域”字段中，单击下拉按钮以打开查找。
4. 在列表中，单击所选行中的链接。
5. 在“每加仑油价”字段中，输入一个数字。
6. 在“生效开始日期和时间”字段中，输入日期和时间。
7. 单击“保存”。

## <a name="create-a-carrier-fuel-index"></a>创建承运人燃油指数
1. 转到“运输管理”>“设置”>“燃油指数”>“承运人燃油指数”。
2. 单击“新建”。
3. 在“承运人燃料指数”字段中，键入一个值。
4. 在“描述”字段中，键入一个值。
5. 单击“新建”。
6. 在“生效开始日期和时间”字段中，输入日期和时间。
7. 在“PPG 发件人”字段中，输入一个数字。
    * 在此示例中，您可以设置“PPG 发件人”字段为 1.95。  
8. 在“PPG 收件人”字段中，输入一个数字。
    * 在此示例中，您可以设置“PPG 收件人”字段为 2。  
9. 在“百分比”字段中，输入一个数字。
    * 在此示例中，您可以设置百分比为 3。  
10. 在“货币”字段中，单击下拉按钮以打开查找。
11. 在列表中，找到并选择所需记录。
12. 在列表中，单击所选行中的链接。
13. 单击“保存”。

