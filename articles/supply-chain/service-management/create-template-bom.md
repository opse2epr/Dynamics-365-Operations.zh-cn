---
title: "创建物料清单模板"
description: "您可以使用多种方法创建物料清单模板。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
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
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="0c8e9-103">创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0c8e9-104">您可以使用以下任一方法创建物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="0c8e9-105">对于所有方法，**开始日期**字段和**结束日期**字段都是可选的，仅供参考。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="0c8e9-106">手动创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="0c8e9-107">单击**服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0c8e9-108">按 CTRL+N 打开**创建物料清单模板**窗体。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0c8e9-109">在**从引用复制物料清单行**下，选择**手动**选项。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="0c8e9-110">在**物料编号**字段中，键入类型为**物料清单**的项。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="0c8e9-111">在**名称**字段中，为模板输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0c8e9-112">在**开始日期**字段和**结束日期**字段中，输入物料清单模板处于活动状态的日期间隔。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0c8e9-113">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-113">Click **OK**.</span></span>

<span data-ttu-id="0c8e9-114">将创建新的空物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="0c8e9-115">基于其他物料清单模板创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="0c8e9-116">单击**服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0c8e9-117">按 CTRL+N 打开**创建物料清单模板**窗体。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0c8e9-118">在**从引用复制物料清单行**下，选择**物料清单模板**选项。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="0c8e9-119">在**参考编号**字段中，选择要复制到您的新物料清单模板的现有物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="0c8e9-120">在**名称**字段中，为模板输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0c8e9-121">在**开始日期**字段和**结束日期**字段中，输入物料清单模板处于活动状态的日期间隔。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0c8e9-122">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-122">Click **OK**.</span></span>

<span data-ttu-id="0c8e9-123">将创建一个新的物料清单模板，该模板中的行与原始物料清单模板中的行相对应。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="0c8e9-124">基于某一物料的物料清单创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="0c8e9-125">单击**服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0c8e9-126">按 CTRL+N 打开**创建物料清单模板**窗体。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0c8e9-127">在**从引用复制物料清单行**中，选择**物料清单**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="0c8e9-128">在**参考编号**字段中，选择一个物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="0c8e9-129">该类型的物料清单的物料将复制到**物料编号**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="0c8e9-130">在**名称**字段中，为模板输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0c8e9-131">在**开始日期**字段和**结束日期**字段中，输入物料清单模板处于活动状态的日期间隔。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0c8e9-132">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-132">Click **OK**.</span></span>

<span data-ttu-id="0c8e9-133">通过使用与在**物料清单**中列出的物料清单行相对应的行，创建新的物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="0c8e9-134">基于某一生产物料清单创建物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="0c8e9-135">单击**服务管理** \> **设置** \> **服务对象** \> **物料清单模板**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="0c8e9-136">按 CTRL+N 打开**创建物料清单模板**窗体。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="0c8e9-137">在**从引用复制物料清单行**中，选择**生产**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="0c8e9-138">在**参考编号**字段中，选择一个生产物料清单。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="0c8e9-139">在**名称**字段中，为模板输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="0c8e9-140">在**开始日期**字段和**结束日期**字段中，输入物料清单模板处于活动状态的日期间隔。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="0c8e9-141">单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-141">Click **OK**.</span></span>

<span data-ttu-id="0c8e9-142">通过使用与在**物料清单**中列出的物料清单行相对应的行，创建新的物料清单模板。</span><span class="sxs-lookup"><span data-stu-id="0c8e9-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c8e9-143">请参阅</span><span class="sxs-lookup"><span data-stu-id="0c8e9-143">See also</span></span>

[<span data-ttu-id="0c8e9-144">物料清单模板</span><span class="sxs-lookup"><span data-stu-id="0c8e9-144">Template BOMs</span></span>](template-boms.md)

  


