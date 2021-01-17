---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490352"
---
# <span data-ttu-id="ef126-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="ef126-101">New-AzTag</span></span>

## <span data-ttu-id="ef126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef126-102">SYNOPSIS</span></span>
<span data-ttu-id="ef126-103">미리 정의된 Azure 태그를 만들거나 기존 태그에 값을 추가 | 리소스 또는 구독에서 전체 태그 집합을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="ef126-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef126-104">SYNTAX</span></span>

### <span data-ttu-id="ef126-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef126-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef126-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef126-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="ef126-107">설명</span><span class="sxs-lookup"><span data-stu-id="ef126-107">DESCRIPTION</span></span>

<span data-ttu-id="ef126-108">**CreatePredefinedTagSet:** **New-AzTag** cmdlet은 선택적으로 미리 정의된 값으로 미리 정의된 Azure 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="ef126-109">기존 미리 정의된 태그에 값을 추가하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="ef126-110">미리 정의된 태그를 만들 경우 고유한 태그 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="ef126-111">기존 미리 정의된 태그에 값을 추가하기 위해 기존 태그의 이름과 새 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="ef126-112">이 cmdlet은 해당 값 및 적용된 리소스 수를 사용하여 새 태그 또는 수정된 태그를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="ef126-113">**New-AzTag가** 일부인 Azure Tags 모듈은 미리 정의한 Azure 태그를 관리하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="ef126-114">Azure 태그는 부서 또는 비용 센터와 같은 Azure 리소스 및 리소스 그룹을 분류하거나 리소스 및 그룹에 대한 메모 또는 메모를 추적하는 데 사용할 수 있는 이름-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="ef126-115">한 단계에서 태그를 정의하고 적용할 수 있지만 미리 정의된 태그를 사용하면 구독의 태그에 대한 표준, 일관되고 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ef126-116">리소스 또는 리소스 그룹에 미리 정의된 태그를 적용하기 위해 New-AzTag cmdlet의 Tag 매개 변수를 사용합니다. </span><span class="sxs-lookup"><span data-stu-id="ef126-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="ef126-117">지정된 태그 이름 또는 이름 및 값을 사용하여 리소스  그룹을 검색하기 위해 Get-AzResourceGroup cmdlet의 Tag 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="ef126-118">모든 태그에는 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-118">Every tag has a name.</span></span>
<span data-ttu-id="ef126-119">값은 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-119">The values are optional.</span></span>
<span data-ttu-id="ef126-120">미리 정의한 Azure 태그에는 여러 값이 있을 수 있지만, 리소스 또는 리소스 그룹에 태그를 적용할 때 태그 이름과 해당 값 중 하나만 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="ef126-121">예를 들어 재무, 인사 관리 및 IT와 같은 각 부서에 대한 값을 사용하여 미리 정의한 부서 태그를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="ef126-122">리소스에 부서 태그를 적용하는 경우 재무와 같은 미리 정의한 값 하나만 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="ef126-123">**CreateByResourceIdParameterSet:** **ResourceId가** 있는 **New-AzTag** cmdlet은 리소스 또는 구독에 태그의 전체 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="ef126-124">이 작업을 통해 지정된 리소스 또는 구독에 태그의 전체 집합을 추가하거나 대체할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="ef126-125">지정된 엔터티에는 최대 50개 태그가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="ef126-126">예제</span><span class="sxs-lookup"><span data-stu-id="ef126-126">EXAMPLES</span></span>

### <span data-ttu-id="ef126-127">예제 1: 미리 정의된 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="ef126-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="ef126-128">이 명령은 FY2015라는 미리 정의된 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="ef126-129">이 태그에는 값이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-129">This tag has no values.</span></span>
<span data-ttu-id="ef126-130">리소스 또는 리소스 그룹에 값이 없는 태그를 적용하거나 **New-AzTag를** 사용하여 태그에 값을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="ef126-131">리소스 또는 리소스 그룹에 태그를 적용할 때 값을 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="ef126-132">예제 2: 값이 있는 미리 정의된 태그 만들기</span><span class="sxs-lookup"><span data-stu-id="ef126-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="ef126-133">이 명령은 Finance 값을 사용하여 Department라는 미리 정의된 태그를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="ef126-134">예제 3: 미리 정의한 태그에 값 추가</span><span class="sxs-lookup"><span data-stu-id="ef126-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="ef126-135">이러한 명령은 두 개의 값을 사용하여 Department라는 미리 정의된 태그를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="ef126-136">태그 이름이 있는 경우 **New-AzTag는** 새 태그를 만드는 대신 기존 태그에 값을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="ef126-137">예제 4: 미리 정의한 태그 사용</span><span class="sxs-lookup"><span data-stu-id="ef126-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="ef126-138">이 예제의 명령은 미리 정의한 태그를 만들고 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="ef126-139">예제 5: 구독에서 전체 태그 집합을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="ef126-140">이 명령은 {subId}를 사용하여 구독에 대한 태그의 전체 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="ef126-141">예제 6: 리소스에 대한 전체 태그 집합을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="ef126-142">이 명령은 {resourceId}를 사용하여 리소스에 태그의 전체 집합을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="ef126-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef126-143">PARAMETERS</span></span>

### <span data-ttu-id="ef126-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef126-144">-DefaultProfile</span></span>
<span data-ttu-id="ef126-145">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-146">-Name</span><span class="sxs-lookup"><span data-stu-id="ef126-146">-Name</span></span>
<span data-ttu-id="ef126-147">미리 정의한 태그 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="ef126-148">미리 정의한 새 태그를 만들 때 고유한 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="ef126-149">기존 태그에 값을 추가하기 위해 기존 태그의 이름을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="ef126-150">기존 미리 정의된 태그에 지정된 이름이 있는 경우 **New-AzTag는** 새 태그를 만드는 대신 해당 이름의 태그에 지정된 값(있는 경우)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-151">-Value</span><span class="sxs-lookup"><span data-stu-id="ef126-151">-Value</span></span>
<span data-ttu-id="ef126-152">미리 정의한 태그 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="ef126-153">미리 정의된 태그는 여러 값을 사용할 수 있지만 각 명령에 하나의 값만 입력할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="ef126-154">태그는 값 없이 이름을 사용할 수 있기 때문에 이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ef126-155">-ResourceId</span></span>
<span data-ttu-id="ef126-156">태그가 지정되는 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="ef126-157">리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef126-158">-Tag</span></span>
<span data-ttu-id="ef126-159">리소스에 넣을 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef126-160">-Confirm</span></span>
<span data-ttu-id="ef126-161">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef126-162">-WhatIf</span></span>
<span data-ttu-id="ef126-163">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ef126-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef126-164">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef126-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef126-165">CommonParameters</span></span>
<span data-ttu-id="ef126-166">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef126-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef126-167">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ef126-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef126-168">입력</span><span class="sxs-lookup"><span data-stu-id="ef126-168">INPUTS</span></span>

### <span data-ttu-id="ef126-169">System.String</span><span class="sxs-lookup"><span data-stu-id="ef126-169">System.String</span></span>

### <span data-ttu-id="ef126-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef126-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ef126-171">출력</span><span class="sxs-lookup"><span data-stu-id="ef126-171">OUTPUTS</span></span>

### <span data-ttu-id="ef126-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="ef126-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="ef126-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef126-173">NOTES</span></span>

## <span data-ttu-id="ef126-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef126-174">RELATED LINKS</span></span>

[<span data-ttu-id="ef126-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="ef126-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="ef126-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="ef126-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="ef126-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="ef126-177">Update-AzTag</span></span>](./Update-AzTag.md)