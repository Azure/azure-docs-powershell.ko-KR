---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicySetDefinition.md
ms.openlocfilehash: 551e30077fe1ce836f98c18d3c00976adc779f64
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492395"
---
# <span data-ttu-id="e6bb4-101">Remove-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e6bb4-101">Remove-AzPolicySetDefinition</span></span>

## <span data-ttu-id="e6bb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="e6bb4-103">정책 집합 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-103">Removes a policy set definition.</span></span>

## <span data-ttu-id="e6bb4-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6bb4-104">SYNTAX</span></span>

### <span data-ttu-id="e6bb4-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6bb4-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicySetDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bb4-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bb4-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -ManagementGroupName <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bb4-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bb4-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Name <String>] [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bb4-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bb4-108">IdParameterSet</span></span>
```
Remove-AzPolicySetDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6bb4-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6bb4-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicySetDefinition [-Force] -InputObject <PsPolicySetDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6bb4-110">설명</span><span class="sxs-lookup"><span data-stu-id="e6bb4-110">DESCRIPTION</span></span>
<span data-ttu-id="e6bb4-111">**Remove-AzPolicySetDefinition** cmdlet은 정책 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-111">The **Remove-AzPolicySetDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="e6bb4-112">예제</span><span class="sxs-lookup"><span data-stu-id="e6bb4-112">EXAMPLES</span></span>

### <span data-ttu-id="e6bb4-113">예제 1: 리소스 ID로 정책 집합 정의 제거</span><span class="sxs-lookup"><span data-stu-id="e6bb4-113">Example 1: Remove policy set definition by resource ID</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Remove-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Force
```

<span data-ttu-id="e6bb4-114">첫 번째 명령은 Get-AzPolicySetDefinition cmdlet을 사용하여 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="e6bb4-115">이 명령은 $PolicySetDefinition 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-115">The command stores it in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="e6bb4-116">두 번째 명령은 리소스의 **ResourceId** 속성으로 식별되는 정책 집합 정의를 $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-116">The second command removes the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="e6bb4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6bb4-117">PARAMETERS</span></span>

### <span data-ttu-id="e6bb4-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e6bb4-118">-ApiVersion</span></span>
<span data-ttu-id="e6bb4-119">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e6bb4-120">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e6bb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6bb4-121">-DefaultProfile</span></span>
<span data-ttu-id="e6bb4-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e6bb4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6bb4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e6bb4-123">-Force</span></span>
<span data-ttu-id="e6bb4-124">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e6bb4-125">-Id</span><span class="sxs-lookup"><span data-stu-id="e6bb4-125">-Id</span></span>
<span data-ttu-id="e6bb4-126">구독을 포함하여 정식 정책 집합 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-126">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="e6bb4-127">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="e6bb4-127">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="e6bb4-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6bb4-128">-InputObject</span></span>
<span data-ttu-id="e6bb4-129">다른 cmdlet에서 출력된 정의 개체를 제거할 정책 설정 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-129">The policy set definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-130">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e6bb4-130">-ManagementGroupName</span></span>
<span data-ttu-id="e6bb4-131">삭제할 정책 집합 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-131">The name of the management group of the policy set definition to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-132">-Name</span><span class="sxs-lookup"><span data-stu-id="e6bb4-132">-Name</span></span>
<span data-ttu-id="e6bb4-133">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-133">The policy set definition name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="e6bb4-134">-Pre</span></span>
<span data-ttu-id="e6bb4-135">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e6bb4-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6bb4-136">-SubscriptionId</span></span>
<span data-ttu-id="e6bb4-137">삭제할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-137">The subscription ID of the policy set definition to delete.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6bb4-138">-Confirm</span></span>
<span data-ttu-id="e6bb4-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6bb4-140">-WhatIf</span></span>
<span data-ttu-id="e6bb4-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e6bb4-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6bb4-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6bb4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6bb4-143">CommonParameters</span></span>
<span data-ttu-id="e6bb4-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6bb4-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6bb4-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6bb4-146">입력</span><span class="sxs-lookup"><span data-stu-id="e6bb4-146">INPUTS</span></span>

### <span data-ttu-id="e6bb4-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e6bb4-147">System.String</span></span>

### <span data-ttu-id="e6bb4-148">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e6bb4-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e6bb4-149">출력</span><span class="sxs-lookup"><span data-stu-id="e6bb4-149">OUTPUTS</span></span>

### <span data-ttu-id="e6bb4-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6bb4-150">System.Boolean</span></span>

## <span data-ttu-id="e6bb4-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6bb4-151">NOTES</span></span>

## <span data-ttu-id="e6bb4-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6bb4-152">RELATED LINKS</span></span>
