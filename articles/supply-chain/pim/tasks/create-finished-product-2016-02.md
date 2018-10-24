--- 
title: "创建成品（2016 年 2 月）"
description: "此任务的重点是创建成品。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 44b3bf17c69f37e7a96c75345a3e4f27ba9eab50
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="d7cfa-103">创建成品（2016 年 2 月）</span><span class="sxs-lookup"><span data-stu-id="d7cfa-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7cfa-104">此任务的重点是创建成品。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="d7cfa-105">这是 BOM 计算系列中的第一个任务。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="d7cfa-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="d7cfa-107">转到“产品信息管理”>“产品”>“已发布产品”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d7cfa-108">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-108">Click New.</span></span>
3. <span data-ttu-id="d7cfa-109">在“产品编号”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="d7cfa-110">对于此演示，输入“BOM_1”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="d7cfa-111">在“物料模型组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-112">选择“标准”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-112">Select STD.</span></span> <span data-ttu-id="d7cfa-113">“标准”指的是标准成本，是计算成本时最常用的模型。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="d7cfa-114">在“物料组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-115">例如，选择“音频”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-115">For example, select Audio.</span></span> <span data-ttu-id="d7cfa-116">这不影响成本计算。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="d7cfa-117">在“存储维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-118">选择“SiteWH”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-118">Select SiteWH.</span></span> <span data-ttu-id="d7cfa-119">将对此演示仅使用站点和仓库。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="d7cfa-120">在“跟踪维度组”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-121">将不对此示例使用跟踪维度。请选择"无"。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="d7cfa-122">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-122">Click OK.</span></span>
9. <span data-ttu-id="d7cfa-123">在“操作窗格”上，单击“库存管理”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="d7cfa-124">点击默认订单设置。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-124">Click Default order settings.</span></span>
11. <span data-ttu-id="d7cfa-125">在“默认订单类型”字段中，选择“生产”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="d7cfa-126">因为这是将生产的成品，所以请选择“生产”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="d7cfa-127">在“采购站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-128">对于此演示，请选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="d7cfa-129">在“库存站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-130">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="d7cfa-131">在“销售站点”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="d7cfa-132">在这个例子中选择“站点 1”。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="d7cfa-133">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d7cfa-133">Close the page.</span></span>

