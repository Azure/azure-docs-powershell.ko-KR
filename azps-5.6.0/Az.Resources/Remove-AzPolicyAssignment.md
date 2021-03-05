---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 83c6cc2ba8103b95aed6d6d365c700e656ac16a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005808"
---
# <span data-ttu-id="43232-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43232-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="43232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43232-102">SYNOPSIS</span></span>
<span data-ttu-id="43232-103">정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="43232-104">구문</span><span class="sxs-lookup"><span data-stu-id="43232-104">SYNTAX</span></span>

### <span data-ttu-id="43232-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="43232-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43232-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43232-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43232-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43232-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43232-108">설명</span><span class="sxs-lookup"><span data-stu-id="43232-108">DESCRIPTION</span></span>
<span data-ttu-id="43232-109">**Remove-AzPolicyAssignment** cmdlet은 지정된 정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="43232-110">예제</span><span class="sxs-lookup"><span data-stu-id="43232-110">EXAMPLES</span></span>

### <span data-ttu-id="43232-111">예제 1: 이름 및 범위에 따라 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="43232-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="43232-112">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43232-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="43232-113">명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="43232-114">두 번째 명령은 리소스 그룹 수준에서 할당된 PolicyAssignment07이라는 정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="43232-115">$ResourceGroup **ResourceId** 속성은 리소스 그룹을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="43232-116">예제 2: ID로 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="43232-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="43232-117">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹을 구한 다음 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="43232-118">두 번째 명령은 리소스 그룹 수준에서 정책 할당을 수행한 다음, 정책 할당을 $PolicyAssignment 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="43232-119">$ResourceGroup **ResourceId** 속성은 리소스 그룹을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="43232-120">마지막 명령은 해당 리소스의 **ResourceId** 속성이 식별하는 정책 $PolicyAssignment 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="43232-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="43232-121">PARAMETERS</span></span>

### <span data-ttu-id="43232-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="43232-122">-ApiVersion</span></span>
<span data-ttu-id="43232-123">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="43232-124">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43232-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43232-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43232-125">-DefaultProfile</span></span>
<span data-ttu-id="43232-126">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43232-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43232-127">-Id</span><span class="sxs-lookup"><span data-stu-id="43232-127">-Id</span></span>
<span data-ttu-id="43232-128">이 cmdlet이 제거한 정책 할당에 대해 완전히 자격을 갖춘 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43232-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43232-129">-InputObject</span></span>
<span data-ttu-id="43232-130">다른 cmdlet에서 출력된 정책을 제거할 정책 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="43232-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43232-131">-Name</span><span class="sxs-lookup"><span data-stu-id="43232-131">-Name</span></span>
<span data-ttu-id="43232-132">이 cmdlet이 제거하는 정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43232-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="43232-133">-Pre</span></span>
<span data-ttu-id="43232-134">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43232-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43232-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="43232-135">-Scope</span></span>
<span data-ttu-id="43232-136">정책이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43232-137">-확인</span><span class="sxs-lookup"><span data-stu-id="43232-137">-Confirm</span></span>
<span data-ttu-id="43232-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43232-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43232-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43232-139">-WhatIf</span></span>
<span data-ttu-id="43232-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="43232-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43232-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43232-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43232-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43232-142">CommonParameters</span></span>
<span data-ttu-id="43232-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43232-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43232-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43232-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43232-145">입력</span><span class="sxs-lookup"><span data-stu-id="43232-145">INPUTS</span></span>

### <span data-ttu-id="43232-146">System.String</span><span class="sxs-lookup"><span data-stu-id="43232-146">System.String</span></span>

## <span data-ttu-id="43232-147">출력</span><span class="sxs-lookup"><span data-stu-id="43232-147">OUTPUTS</span></span>

### <span data-ttu-id="43232-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="43232-148">System.Boolean</span></span>

## <span data-ttu-id="43232-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43232-149">NOTES</span></span>

## <span data-ttu-id="43232-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43232-150">RELATED LINKS</span></span>

[<span data-ttu-id="43232-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43232-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="43232-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43232-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="43232-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43232-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


