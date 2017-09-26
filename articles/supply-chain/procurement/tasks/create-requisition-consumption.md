--- 
title: "创建消耗量申请"
description: "该过程向您介绍创建申请的流程。"
author: mkirknel
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
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb4cd47104e2df1c973e5e508c1da02617b9a1d
ms.contentlocale: zh-cn
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-requisition-for-consumption"></a>创建消耗量申请

[!include[task guide banner](../../includes/task-guide-banner.md)]

该过程向您介绍创建申请的流程。 它显示了在您的采购目录中搜索产品以及添加不在您目录中的产品的各种方法。 在启动此过程前，必须将采购策略设置为申请默认类型为“消耗量”。 您可以使用演示数据公司 USMF 或您自己的数据浏览此程序。 此过程只能由设置为工作人员的用户配置文件执行。  此任务通常由员工完成。 员工雇用安全角色可以使您执行任务，或者，如果您使用 USMF，您可以以Alicia身份登录。


## <a name="create-a-new-requisition"></a>新建申请
1. 转到“采购”>“采购申请”>“由我起草的采购申请”。
2. 单击“新建”。
3. 在“名称”字段中，为申请命名。
4. 在“请求日期”字段中，输入一个日期。
    * 在默认情况下，请求的日期和会计结算日期会被复制到采购申请行。 可以在行级别更改它们。 请求日期是请求的交货日期。  
5. 在“会计结算日期”字段中，输入一个日期。
    * 该核算日期用于在总帐中记录会计分录并验证预算资金是否可用。  
6. 单击“确定”。
7. 在“原因”字段中，单击下拉按钮以打开查找。
    * 默认情况下，您选择的业务理由原因会出现在采购申请行，但您可以在行级别更改它。    
8. 在列表中，找到并选择所需记录。
9. 选择原因
10. 在详细信息字段中，输入更具描述性的申请理由

## <a name="add-a-line-to-the-requisition"></a>添加行到申请。
1. 单击“添加行”。
    * 有两种方式可以将行添加到采购申请中。 如果您已经知道产品编号或已经知道您申请的产品不在产品目录中，则您可以直接使用“添加行”来添加行。 另一种方法是使用“添加产品”，在此处您可以使用搜索和筛选查找产品目录中的物料。    
2. 单击您刚创建的行。
    * 申请者是已提交申请的工作人员。   
    * 默认情况下，准备申请的人员是已提交申请的工作人员。 您必须获得权限，以代表其他工作人员准备申请行。 如果您拥有此类权限，则其他工作人员将会在本查找中显示。  
3. 在“项目编号”字段中，输入一个值。
    * 可供您选择的物料受到采购法人实体的类别访问策略和采购目录的限制。   
4. 在“数量”字段中，输入一个数字。

## <a name="add-more-products-to-the-requisition"></a>添加更多产品到申请
1. 单击 添加产品。
    * 此选项可供您在其中检索产品目录中的产品。    
2. 在“查找采购类别节点”字段中，键入您正在查找的类别的名称的第一部分，然后单击 "Enter" 键。
    * 例如，键入计算。  
3. 使用“InvokeDefaultButton”快捷方式。
4. 使用“筛选器”筛选选定类别中的产品列表。
5. 选择您想要添加到申请的产品卡。
6. 单击“添加到行”。
7. 在“数量”字段中，输入一个数字。
8. 在“查找采购类别节点”字段中，键入您正在查找的类别的名称的第一部分，然后单击 "Enter" 键。
    * 例如，键入高（萤光笔）。  
9. 使用“InvokeDefaultButton”快捷方式。
10. 单击“添加未列示产品到行”以添加到未列示在采购目录中的产品。
11. 在“产品名称”字段中，键入一个值。
12. 在“单位”字段中，键入一个值。
13. 单击“确定”。
14. 在“物料说明”字段中，添加产品说明。
15. 在“数量”字段中，输入一个数字。
16. 在“单位价格”字段中，输入一个数字。
    * 如果您知道特定供应商的价格（您在供应商帐户字段中选择的），则可以输入该价格   
17. 在“供应商帐户”字段中，单击下拉按钮以打开查找。
    * 可用在此字段使用的供应商取决于采购政策和供应商当前采购类别的状态。 除了在此处选择供应商的备选方法，可以单击“建议供应商”按钮。    
18. 在列表中，选择您想要使用的供应商。
19. 在“外部物料编号”字段中，键入一个值。
    * 这是供应商已知的产品的参考编号。 例如，这可能是供应商自己的产品目录中的产品的物料编号。  
20. 单击“确定”。

## <a name="distribute-amounts"></a>分摊金额
1. 单击“财务”。
2. 单击“分配金额”。
    * 该过程会显示如何在 2 个帐户之间分配第一行的成本。 在申请接受审查时，这也可能稍后执行。  
3. 单击“拆分”以新建分配行。
4. 在“分类帐户”字段中，选择第一个应负担成本的成本中心。
5. 选择其他分配行。
6. 在“分类帐户”字段中，指定其他成本中心。
7. 单击“平均分配”。
8. 关闭该页面。

## <a name="view-line-details"></a>查看行明细
1. 切换“行详细信息”部分的扩展。

## <a name="submit-the-requisition"></a>提交申请
1. 单击“工作流程”以打开下拉对话框。
2. 单击“提交”。
3. 关闭该页面。
4. 在“注解”字段中，键入申请批准人的附注。
5. 单击“提交”。
6. 关闭该页面。
7. 刷新该页面。

