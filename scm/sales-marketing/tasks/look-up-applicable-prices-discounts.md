--- 
title: "查找适用的价格和折扣"
description: "该过程会显示如何查找当前对于特定客户有效的产品价格和折扣，无需创建销售订单。"
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: ecfe2ad4dbba74cb067628b63abaf780bcf0680e
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="look-up-applicable-prices-and-discounts"></a>查找适用的价格和折扣

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程会显示如何查找当前对于特定客户有效的产品价格和折扣，无需创建销售订单。 该过程用一个具体示例进行示范，您需要遵循该示例，使用 USMF 演示公司，以选择所需的值。


## <a name="find-the-applicable-price"></a>查找适用的价格
1. 转至“销售和营销”>“价格和折扣”>“查找价格”。
2. 在“客户帐户”字段中，单击下拉按钮以打开查找。
3. 在列表中，找到并选择客户 US-001。
4. 在列表中，单击所选行中的链接。
5. 在“物料编号”字段中，键入“T0004”。
    * 默认情况下，“数量”字段设置为 1。 但是，如果您知道客户打算订购所讨论的物料的订货量，则输入该数值。 如果与客户签订的贸易协议有数量分段，即该产品的价格取决于采购的最小数量，此信息是相关的。  
6. 在“日期”字段中，输入客户预计下单的日期。 
    * 日期可以是今天或未来的任何日期。  
    * 当选定客户在选定日期购买规定数量的选定产品时，系统会立即返回对于该选定产品有效的价格。 在此示例中，如果客户 US-001 今天购买 1 个单位的产品 T0004，每个单位被收取 350 加拿大元。 此价格源自与该客户签订的现行有效的贸易协议。      该页面的其他字段提供了关于产品价格和产品成本（如果在基础产品上设置）以及计算得出的利润率的更多详情。  
    * 如果选中“显示相关产品变型”选项，这意味着产品变量还有额外的贸易协议。  
7. 单击“显示相关产品变型”复选框。
    * 产品变型列表及其维度信息会显示。  
8. 在列表中，标记行中的代表颜色“白色”
    * 注意，未根据维度指定时，产品价格现在不同于以前显示的价格。  
9. 单击“查看销售价格”。
    * 价格（售价）页会显示适用于产品的所有贸易协议，包括其变型。  
10. 关闭该页面。

## <a name="find-the-applicable-discount"></a>查找适用的折扣
    * 确保“客户帐户”字段包含客户编号 US-001   
1. 在“物料编号”字段中，键入“T0012”。
    * 请确保“数量”字段被设置为 1。  
    * 产品 T0012 所显示的以下定价详情源自一个或多个贸易协议：单价为 1,000 加拿大元，并且折扣百分比是 5。  
2. 将“数量”设置为“20”。
    * 增加的订单数量导致提供给客户的行折扣从 5 更改为 7。  
    * “净额”是基于单价、折扣和总数量计算得出的。  
3. 单击“查看行折扣”。
    * 产品 T0012 有 2 个单行折扣协议，规定订单行数量为 1-10 的折扣百分比是 5，订单行数量为 10 以上的折扣百分比是 7。 请注意，该折扣适用于产品组，在本示例中，组代码为 01，产品 T0012 包括在其中。  
4. 关闭该页面。

