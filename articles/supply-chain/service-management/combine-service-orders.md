---
title: "合并服务订单"
description: "可以合并服务订单。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8bc28d03d36d184e4bf41de2c50dac15e6d7813c
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="abe1c-103">合并服务订单</span><span class="sxs-lookup"><span data-stu-id="abe1c-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="abe1c-104">当您在**服务协议**窗体中自动创建服务订单行时，您可以选择以下选项之一以指定您如何对它们进行分组：</span><span class="sxs-lookup"><span data-stu-id="abe1c-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="abe1c-105">**按服务协议**</span><span class="sxs-lookup"><span data-stu-id="abe1c-105">**By service agreement**</span></span>

  - <span data-ttu-id="abe1c-106">**按服务任务**</span><span class="sxs-lookup"><span data-stu-id="abe1c-106">**By service task**</span></span>

  - <span data-ttu-id="abe1c-107">**按员工**</span><span class="sxs-lookup"><span data-stu-id="abe1c-107">**By employee**</span></span>

  - <span data-ttu-id="abe1c-108">**按服务对象**</span><span class="sxs-lookup"><span data-stu-id="abe1c-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="abe1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="abe1c-109">Example</span></span>

<span data-ttu-id="abe1c-110">您创建了开始日期为 2007 年 3 月 31 日的服务协议。</span><span class="sxs-lookup"><span data-stu-id="abe1c-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="abe1c-111">在**合并服务订单**字段中，指定**按服务对象**。</span><span class="sxs-lookup"><span data-stu-id="abe1c-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="abe1c-112">然后您创建了以下服务协议行：</span><span class="sxs-lookup"><span data-stu-id="abe1c-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="abe1c-113">协议行号</span><span class="sxs-lookup"><span data-stu-id="abe1c-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="abe1c-114">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="abe1c-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="abe1c-115">说明</span><span class="sxs-lookup"><span data-stu-id="abe1c-115">Description</span></span></p></th>
<th><p><span data-ttu-id="abe1c-116">间期</span><span class="sxs-lookup"><span data-stu-id="abe1c-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="abe1c-117">服务对象</span><span class="sxs-lookup"><span data-stu-id="abe1c-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="abe1c-118">入职日期</span><span class="sxs-lookup"><span data-stu-id="abe1c-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="abe1c-119">1</span><span class="sxs-lookup"><span data-stu-id="abe1c-119">1</span></span></p></td>
<td><p><span data-ttu-id="abe1c-120"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="abe1c-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="abe1c-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="abe1c-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="abe1c-122">每周</span><span class="sxs-lookup"><span data-stu-id="abe1c-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="abe1c-123">X-1</span><span class="sxs-lookup"><span data-stu-id="abe1c-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="abe1c-124">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="abe1c-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="abe1c-125">2</span><span class="sxs-lookup"><span data-stu-id="abe1c-125">2</span></span></p></td>
<td><p><span data-ttu-id="abe1c-126"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="abe1c-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="abe1c-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="abe1c-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="abe1c-128">每两周</span><span class="sxs-lookup"><span data-stu-id="abe1c-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="abe1c-129">X-2</span><span class="sxs-lookup"><span data-stu-id="abe1c-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="abe1c-130">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="abe1c-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="abe1c-131">3</span><span class="sxs-lookup"><span data-stu-id="abe1c-131">3</span></span></p></td>
<td><p><span data-ttu-id="abe1c-132"><strong>工时</strong></span><span class="sxs-lookup"><span data-stu-id="abe1c-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="abe1c-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="abe1c-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="abe1c-134">每周</span><span class="sxs-lookup"><span data-stu-id="abe1c-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="abe1c-135">X-2</span><span class="sxs-lookup"><span data-stu-id="abe1c-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="abe1c-136">2007 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="abe1c-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="abe1c-137">您未指定任何服务协议行的时间范围。</span><span class="sxs-lookup"><span data-stu-id="abe1c-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="abe1c-138">因此，服务订单行将不从它们所在的计算日移动。</span><span class="sxs-lookup"><span data-stu-id="abe1c-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="abe1c-139">接着，您从**创建服务订单**窗体生成了从 2007 年 4 月 1 日到 2007 年 4 月 30 日的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="abe1c-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="abe1c-140">总共创建了 10 个服务订单。</span><span class="sxs-lookup"><span data-stu-id="abe1c-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="abe1c-141">因为您选择的组合设置为**按服务对象**，创建的所有服务订单将只包含具有一个特定服务对象的服务订单行。</span><span class="sxs-lookup"><span data-stu-id="abe1c-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="abe1c-142">从该服务协议生成并具有相同服务日期和对象的服务订单行被组合为同一个服务订单。</span><span class="sxs-lookup"><span data-stu-id="abe1c-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="abe1c-143">在此示例中，在<STRONG>服务管理参数</STRONG>窗体中指定的日历没有休息日。</span><span class="sxs-lookup"><span data-stu-id="abe1c-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="abe1c-144">可以根据您在服务协议行上指定的任意时间范围将服务订单行的附加组合为服务订单。</span><span class="sxs-lookup"><span data-stu-id="abe1c-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="abe1c-145">请参阅</span><span class="sxs-lookup"><span data-stu-id="abe1c-145">See also</span></span>

[<span data-ttu-id="abe1c-146">自动创建服务订单</span><span class="sxs-lookup"><span data-stu-id="abe1c-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  


