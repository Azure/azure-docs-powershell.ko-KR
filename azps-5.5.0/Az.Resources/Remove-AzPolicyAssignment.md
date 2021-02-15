---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201849"
---
# <span data-ttu-id="7d387-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7d387-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="7d387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d387-102">SYNOPSIS</span></span>
<span data-ttu-id="7d387-103">정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="7d387-104">구문</span><span class="sxs-lookup"><span data-stu-id="7d387-104">SYNTAX</span></span>

### <span data-ttu-id="7d387-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7d387-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d387-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d387-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d387-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d387-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d387-108">설명</span><span class="sxs-lookup"><span data-stu-id="7d387-108">DESCRIPTION</span></span>
<span data-ttu-id="7d387-109">**Remove-AzPolicyAssignment** cmdlet은 지정된 정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="7d387-110">예제</span><span class="sxs-lookup"><span data-stu-id="7d387-110">EXAMPLES</span></span>

### <span data-ttu-id="7d387-111">예제 1: 이름 및 범위에 따라 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="7d387-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="7d387-112">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="7d387-113">이 명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7d387-114">두 번째 명령은 리소스 그룹 수준에서 할당된 PolicyAssignment07이라는 정책 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="7d387-115">리소스 **그룹의 ResourceId** 속성은 $ResourceGroup 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="7d387-116">예제 2: ID로 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="7d387-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="7d387-117">첫 번째 명령은 ResourceGroup11이라는 리소스 그룹을 구한 다음 해당 개체를 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="7d387-118">두 번째 명령은 리소스 그룹 수준에서 정책 할당을 구한 다음, 리소스 $PolicyAssignment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="7d387-119">리소스 **그룹의 ResourceId** 속성은 $ResourceGroup 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="7d387-120">마지막 명령은 리소스의 **ResourceId** 속성이 식별하는 $PolicyAssignment 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="7d387-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d387-121">PARAMETERS</span></span>

### <span data-ttu-id="7d387-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7d387-122">-ApiVersion</span></span>
<span data-ttu-id="7d387-123">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="7d387-124">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="7d387-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d387-125">-DefaultProfile</span></span>
<span data-ttu-id="7d387-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d387-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d387-127">-Id</span><span class="sxs-lookup"><span data-stu-id="7d387-127">-Id</span></span>
<span data-ttu-id="7d387-128">이 cmdlet에서 제거하는 정책 할당에 대한 자격이 있는 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d387-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d387-129">-InputObject</span></span>
<span data-ttu-id="7d387-130">다른 cmdlet에서 출력된 정책을 제거할 정책 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="7d387-131">-Name</span><span class="sxs-lookup"><span data-stu-id="7d387-131">-Name</span></span>
<span data-ttu-id="7d387-132">이 cmdlet이 제거하는 정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7d387-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="7d387-133">-Pre</span></span>
<span data-ttu-id="7d387-134">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7d387-135">-Scope</span><span class="sxs-lookup"><span data-stu-id="7d387-135">-Scope</span></span>
<span data-ttu-id="7d387-136">정책이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-136">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="7d387-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d387-137">-Confirm</span></span>
<span data-ttu-id="7d387-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d387-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d387-139">-WhatIf</span></span>
<span data-ttu-id="7d387-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7d387-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d387-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d387-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d387-142">CommonParameters</span></span>
<span data-ttu-id="7d387-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7d387-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d387-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d387-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d387-145">입력</span><span class="sxs-lookup"><span data-stu-id="7d387-145">INPUTS</span></span>

### <span data-ttu-id="7d387-146">System.String</span><span class="sxs-lookup"><span data-stu-id="7d387-146">System.String</span></span>

## <span data-ttu-id="7d387-147">출력</span><span class="sxs-lookup"><span data-stu-id="7d387-147">OUTPUTS</span></span>

### <span data-ttu-id="7d387-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7d387-148">System.Boolean</span></span>

## <span data-ttu-id="7d387-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7d387-149">NOTES</span></span>

## <span data-ttu-id="7d387-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d387-150">RELATED LINKS</span></span>

[<span data-ttu-id="7d387-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7d387-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="7d387-152">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7d387-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="7d387-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="7d387-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


