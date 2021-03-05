---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 201e341ce05b22597f05601d7d269d2eb27c2358
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979424"
---
# <span data-ttu-id="15b6c-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="15b6c-101">Remove-AzTag</span></span>

## <span data-ttu-id="15b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="15b6c-103">미리 정의된 Azure 태그 또는 값을 | 리소스 또는 구독에서 태그의 전체 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="15b6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="15b6c-104">SYNTAX</span></span>

### <span data-ttu-id="15b6c-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="15b6c-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15b6c-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15b6c-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="15b6c-107">설명</span><span class="sxs-lookup"><span data-stu-id="15b6c-107">DESCRIPTION</span></span>

<span data-ttu-id="15b6c-108">**RemovePredefinedTagSet:** **Remove-AzTag** cmdlet은 구독에서 미리 정의한 Azure 태그 및 값을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="15b6c-109">미리 정의된 태그에서 특정 값을 삭제하려면 Value 매개 *변수를* 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="15b6c-110">기본적으로 **Remove-AzTag는** 지정된 태그와 해당 값을 모두 삭제합니다. 현재 리소스 또는 리소스 그룹에 적용되는 태그 또는 값을 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="15b6c-111">**Remove-AzTag를** 사용하기 전에  리소스 Set-AzResourceGroup cmdlet의 태그 매개 변수를 사용하여 리소스 또는 리소스 그룹에서 태그 또는 값을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="15b6c-112">**Remove-AzTag의** 일부인 Azure Tags 모듈은 미리 정의된 Azure 태그를 관리하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="15b6c-113">Azure 태그는 부서 또는 비용 센터별로 Azure 리소스 및 리소스 그룹을 분류하거나 리소스 및 그룹에 대한 메모 또는 메모를 추적하는 데 사용할 수 있는 이름 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="15b6c-114">한 단계에서 태그를 정의하고 적용할 수 있지만 미리 정의된 태그를 사용하면 구독의 태그에 대한 표준, 일관성, 예측 가능한 이름 및 값을 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="15b6c-115">**RemoveByResourceIdParameterSet:** **ResourceId가** 있는 **Remove-AzTag** cmdlet은 리소스 또는 구독에서 태그의 전체 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="15b6c-116">예제</span><span class="sxs-lookup"><span data-stu-id="15b6c-116">EXAMPLES</span></span>

### <span data-ttu-id="15b6c-117">예제 1: 미리 정의된 태그 삭제</span><span class="sxs-lookup"><span data-stu-id="15b6c-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="15b6c-118">이 명령은 부서라는 미리 정의된 태그와 해당 값 모두를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="15b6c-119">태그가 리소스 또는 리소스 그룹에 적용된 경우 명령이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="15b6c-120">예제 2: 미리 정의된 태그에서 값 삭제</span><span class="sxs-lookup"><span data-stu-id="15b6c-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="15b6c-121">이 명령은 미리 정의된 부서 태그에서 HumanResources 값을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="15b6c-122">태그는 삭제되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-122">It does not delete the tag.</span></span>
<span data-ttu-id="15b6c-123">값이 리소스 또는 리소스 그룹에 적용된 경우 명령이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="15b6c-124">예제 3: 구독의 태그 집합 전체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="15b6c-125">이 명령은 {subId}를 사용하여 구독의 태그 전체 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="15b6c-126">"-PassThru"를 통과하지 않을 경우 삭제된 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="15b6c-127">예제 4: 리소스의 전체 태그 집합을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="15b6c-128">이 명령은 {resourceId}를 사용하여 리소스의 태그 집합 전체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="15b6c-129">"-PassThru"를 전달할 때 삭제된 oject를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="15b6c-130">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15b6c-130">PARAMETERS</span></span>

### <span data-ttu-id="15b6c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b6c-131">-DefaultProfile</span></span>
<span data-ttu-id="15b6c-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b6c-133">-Name</span><span class="sxs-lookup"><span data-stu-id="15b6c-133">-Name</span></span>
<span data-ttu-id="15b6c-134">제거할 미리 정의된 태그의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="15b6c-135">기본적으로 **Remove-AzTag는** 지정된 태그와 해당 값을 모두 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="15b6c-136">선택한 값을 삭제하지만 태그를 삭제하지하려면 Value 매개 *변수를* 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b6c-137">-Value</span><span class="sxs-lookup"><span data-stu-id="15b6c-137">-Value</span></span>
<span data-ttu-id="15b6c-138">미리 정의된 태그에서 지정된 값을 삭제하지만 태그는 삭제하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b6c-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15b6c-139">-ResourceId</span></span>
<span data-ttu-id="15b6c-140">태그가 지정된 엔터티의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="15b6c-141">리소스, 리소스 그룹 또는 구독에 태그가 지정될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b6c-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15b6c-142">-PassThru</span></span>
<span data-ttu-id="15b6c-143">삭제된 태그 또는 삭제된 값의 결과 태그를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b6c-144">-확인</span><span class="sxs-lookup"><span data-stu-id="15b6c-144">-Confirm</span></span>
<span data-ttu-id="15b6c-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b6c-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b6c-146">-WhatIf</span></span>
<span data-ttu-id="15b6c-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15b6c-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b6c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b6c-149">CommonParameters</span></span>
<span data-ttu-id="15b6c-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15b6c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b6c-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15b6c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b6c-152">입력</span><span class="sxs-lookup"><span data-stu-id="15b6c-152">INPUTS</span></span>

### <span data-ttu-id="15b6c-153">System.String</span><span class="sxs-lookup"><span data-stu-id="15b6c-153">System.String</span></span>

### <span data-ttu-id="15b6c-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="15b6c-154">System.String[]</span></span>

### <span data-ttu-id="15b6c-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15b6c-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15b6c-156">출력</span><span class="sxs-lookup"><span data-stu-id="15b6c-156">OUTPUTS</span></span>

### <span data-ttu-id="15b6c-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="15b6c-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="15b6c-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15b6c-158">NOTES</span></span>

## <span data-ttu-id="15b6c-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15b6c-159">RELATED LINKS</span></span>

[<span data-ttu-id="15b6c-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="15b6c-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="15b6c-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="15b6c-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="15b6c-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="15b6c-162">Update-AzTag</span></span>](./Update-AzTag.md)