---
title: "Project Service Automation 集成参数"
description: "本主题介绍在将 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 集成时，如何配置默认数据的输入方式。"
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 33960a97f69d6bcc70a3035d4d68095ca6993a10
ms.contentlocale: zh-cn
ms.lasthandoff: 08/08/2018

---

# <a name="project-service-automation-integration-parameters"></a><span data-ttu-id="b8b53-103">Project Service Automation 集成参数</span><span class="sxs-lookup"><span data-stu-id="b8b53-103">Project Service Automation integration parameters</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b8b53-104">在将 Microsoft Dynamics 365 for Project Service Automation 与 Microsoft Dynamics 365 for Finance and Operations 集成时，可在 **Project Service Automation 集成参数**页面配置默认数据的输入方式。</span><span class="sxs-lookup"><span data-stu-id="b8b53-104">On the **Project Service Automation integration parameters** page, you can configure how default data is entered when you integrate Microsoft Dynamics 365 for Project Service Automation with Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b8b53-105">必须设置以下字段，才能将项目从 Project Service Automation 成功同步到 Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="b8b53-105">For projects to be successfully synchronized from Project Service Automation to Finance and Operations, you must set up the following fields.</span></span>

> [!NOTE]
> - <span data-ttu-id="b8b53-106">Microsoft Dynamics 365 for Finance and Operations 版本 8.0 中提供项目任务集成、费用交易记录类别、工时估计值、费用估计值和功能锁定。</span><span class="sxs-lookup"><span data-stu-id="b8b53-106">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="b8b53-107">Microsoft Dynamics 365 for Finance and Operations 版本 8.0.1 或更高版本中支持实际值集成。</span><span class="sxs-lookup"><span data-stu-id="b8b53-107">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b8b53-108">如果您正在使用 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3.0，则安装 KB 4132657 和 KB 4132660 之后，可以使用模板集成项目任务、费用交易记录类别、工时估计值、费用估计值和实际值和配置功能锁定。</span><span class="sxs-lookup"><span data-stu-id="b8b53-108">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b8b53-109">如果必须重置会计分配，建议也安装 KB 4131710。</span><span class="sxs-lookup"><span data-stu-id="b8b53-109">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>

| <span data-ttu-id="b8b53-110">选项卡</span><span class="sxs-lookup"><span data-stu-id="b8b53-110">Tab</span></span>                    | <span data-ttu-id="b8b53-111">字段</span><span class="sxs-lookup"><span data-stu-id="b8b53-111">Field</span></span>                | <span data-ttu-id="b8b53-112">说明</span><span class="sxs-lookup"><span data-stu-id="b8b53-112">Description</span></span> |
|------------------------|----------------------|-------------|
| <span data-ttu-id="b8b53-113">常规</span><span class="sxs-lookup"><span data-stu-id="b8b53-113">General</span></span>                | <span data-ttu-id="b8b53-114">默认项目类型</span><span class="sxs-lookup"><span data-stu-id="b8b53-114">Default project type</span></span> | <span data-ttu-id="b8b53-115">选择默认项目类型。</span><span class="sxs-lookup"><span data-stu-id="b8b53-115">Select the default project type.</span></span> <span data-ttu-id="b8b53-116">从 Project Service Automation 同步项目时，如果在集成模板中不提供默认值，将使用该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-116">When projects are synchronized from Project Service Automation, this value is used if you didn't provide a default value in the integration template.</span></span> <span data-ttu-id="b8b53-117">同步期间，将把新项目的**项目类型**字段设置为该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-117">During synchronization, the **Project type** field of new projects is set to this value.</span></span> <span data-ttu-id="b8b53-118">但是，从 Project Service Automation 同步项目联系人行时，可能更新该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-118">However, the value might be updated when the project contract lines are synchronized from Project Service Automation.</span></span> |
|                        | <span data-ttu-id="b8b53-119">时间类别</span><span class="sxs-lookup"><span data-stu-id="b8b53-119">Time category</span></span>        | <span data-ttu-id="b8b53-120">选择默认时间类别。</span><span class="sxs-lookup"><span data-stu-id="b8b53-120">Select the default time category.</span></span> <span data-ttu-id="b8b53-121">从 Project Service Automation 同步工时估计值时使用该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-121">This value is used when hour estimates are synchronized from Project Service Automation.</span></span> <span data-ttu-id="b8b53-122">从 Project Service Automation 同步工时估计值和工时实际值时，Finance and Operations 中的新项目工时预测的**类别**字段将设置为该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-122">When the hour estimates and hour actuals are synchronized from Project Service Automation, the **Category** field of new project hour forecasts in Finance and Operations is set to this value.</span></span> |
|                        | <span data-ttu-id="b8b53-123">费用类别</span><span class="sxs-lookup"><span data-stu-id="b8b53-123">Fee category</span></span>         | <span data-ttu-id="b8b53-124">选择默认费用类别。</span><span class="sxs-lookup"><span data-stu-id="b8b53-124">Select the default fee category.</span></span> <span data-ttu-id="b8b53-125">从 Project Service Automation 同步费用实际值时使用该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-125">This value is used when fee actuals are synchronized from Project Service Automation.</span></span> <span data-ttu-id="b8b53-126">从 Project Service Automation 同步费用实际值时，Finance and Operations 中的新费用交易记录的**类别**字段将设置为该值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-126">When the fee actuals are synchronized from Project Service Automation, the **Category** field of new fee transactions in Finance and Operations is set to this value.</span></span> |
| <span data-ttu-id="b8b53-127">项目组的默认值</span><span class="sxs-lookup"><span data-stu-id="b8b53-127">Project group defaults</span></span> | <span data-ttu-id="b8b53-128">项目类型</span><span class="sxs-lookup"><span data-stu-id="b8b53-128">Project type</span></span>         | <span data-ttu-id="b8b53-129">单击**新建**添加一行，可在该行中选择要为默认项目组设置的项目类型。</span><span class="sxs-lookup"><span data-stu-id="b8b53-129">Click **New** to add a row where you can select the project type to set the default project group for.</span></span> <span data-ttu-id="b8b53-130">在配置中，特定项目类型只能选择一次。</span><span class="sxs-lookup"><span data-stu-id="b8b53-130">A specific project type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="b8b53-131">项目组</span><span class="sxs-lookup"><span data-stu-id="b8b53-131">Project group</span></span>        | <span data-ttu-id="b8b53-132">为所选项目类型选择默认项目组。</span><span class="sxs-lookup"><span data-stu-id="b8b53-132">Select the default project group for the selected project type.</span></span> <span data-ttu-id="b8b53-133">从 Project Service Automation 同步新项目时，如果尚未在集成模板中提供默认值，**项目组**字段将设置为项目类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-133">When new projects are synchronized from Project Service Automation, the **Project group** field is set to the default value for the project type if you didn't provide a default value in the integration template.</span></span> |
| <span data-ttu-id="b8b53-134">计费类型默认值</span><span class="sxs-lookup"><span data-stu-id="b8b53-134">Billing type defaults</span></span>  | <span data-ttu-id="b8b53-135">计费类型</span><span class="sxs-lookup"><span data-stu-id="b8b53-135">Billing type</span></span>         | <span data-ttu-id="b8b53-136">单击**新建**添加一行，可在该行中选择要为默认行属性设置的计费类型。</span><span class="sxs-lookup"><span data-stu-id="b8b53-136">Click **New** to add a row where you can select the billing type to set the default line property for.</span></span> <span data-ttu-id="b8b53-137">在配置中，特定计费类型只能选择一次。</span><span class="sxs-lookup"><span data-stu-id="b8b53-137">A specific billing type can be selected only one time in the configuration.</span></span> |
|                        | <span data-ttu-id="b8b53-138">行属性</span><span class="sxs-lookup"><span data-stu-id="b8b53-138">Line property</span></span>        | <span data-ttu-id="b8b53-139">为所选计费类型选择默认行属性。</span><span class="sxs-lookup"><span data-stu-id="b8b53-139">Select the default line property for the selected billing type.</span></span> <span data-ttu-id="b8b53-140">从 Project Service Automation 同步新工时估计值、新费用估计值或新实际值时，**行属性**字段将设置为计费类型的默认值。</span><span class="sxs-lookup"><span data-stu-id="b8b53-140">When new hour estimates, new expense estimates, or new actuals are synchronized from Project Service Automation, the **Line property** field is set to the default value for the billing type.</span></span> |
| <span data-ttu-id="b8b53-141">功能锁定</span><span class="sxs-lookup"><span data-stu-id="b8b53-141">Functionality locking</span></span>  | <span data-ttu-id="b8b53-142">不适用</span><span class="sxs-lookup"><span data-stu-id="b8b53-142">Not applicable</span></span>       | <span data-ttu-id="b8b53-143">为源自 Project Service Automation 的项目和合同选择要在 Finance and Operations 中禁用的功能。</span><span class="sxs-lookup"><span data-stu-id="b8b53-143">Select the functionality to disable in Finance and Operations for projects and contracts that originated from Project Service Automation.</span></span> <span data-ttu-id="b8b53-144">例如，可关闭 Finance and Operations 中的编辑合同和项目，创建工作分解结构以及输入工时单功能。</span><span class="sxs-lookup"><span data-stu-id="b8b53-144">For example, you can turn off the ability to edit contracts and projects, create work breakdown structures, and enter timesheets in Finance and Operations.</span></span> <span data-ttu-id="b8b53-145">将继续启用与核算有关的字段，即使根据参数设置这些字段不可用也不例外。</span><span class="sxs-lookup"><span data-stu-id="b8b53-145">Accounting-related fields will continue to be enabled, even if they are made unavailable by the parameter setting.</span></span> <span data-ttu-id="b8b53-146">默认情况下，将启用所有功能。</span><span class="sxs-lookup"><span data-stu-id="b8b53-146">By default, all functionality is enabled.</span></span> |
