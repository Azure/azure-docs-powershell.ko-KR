---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicySetDefinition.md
ms.openlocfilehash: cd8bc24a0cedac91ef18e19a80e1662fdcbac297
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492382"
---
# <span data-ttu-id="3a359-101">Set-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3a359-101">Set-AzPolicySetDefinition</span></span>

## <span data-ttu-id="3a359-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a359-102">SYNOPSIS</span></span>
<span data-ttu-id="3a359-103">정책 집합 정의 수정</span><span class="sxs-lookup"><span data-stu-id="3a359-103">Modifies a policy set definition</span></span>

## <span data-ttu-id="3a359-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a359-104">SYNTAX</span></span>

### <span data-ttu-id="3a359-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a359-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a359-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a359-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a359-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a359-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a359-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a359-108">IdParameterSet</span></span>
```
Set-AzPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a359-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a359-109">InputObjectParameterSet</span></span>
```
Set-AzPolicySetDefinition [-DisplayName <String>] [-Description <String>] [-PolicyDefinition <String>]
 [-Metadata <String>] [-Parameter <String>] -InputObject <PsPolicySetDefinition> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a359-110">설명</span><span class="sxs-lookup"><span data-stu-id="3a359-110">DESCRIPTION</span></span>
<span data-ttu-id="3a359-111">**Set-AzPolicySetDefinition** cmdlet은 정책 정의를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-111">The **Set-AzPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="3a359-112">예제</span><span class="sxs-lookup"><span data-stu-id="3a359-112">EXAMPLES</span></span>

### <span data-ttu-id="3a359-113">예제 1: 정책 집합 정의에 대한 설명 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a359-113">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="3a359-114">첫 번째 명령은 Get-AzPolicySetDefinition cmdlet을 사용하여 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-114">The first command gets a policy set definition by using the Get-AzPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="3a359-115">이 명령은 해당 개체를 $PolicySetDefinition 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-115">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="3a359-116">두 번째 명령은 리소스의 **ResourceId** 속성으로 식별되는 정책 집합 정의에 대한 설명을 $PolicySetDefinition.</span><span class="sxs-lookup"><span data-stu-id="3a359-116">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

### <span data-ttu-id="3a359-117">예제 2: 정책 집합 정의의 메타데이터 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a359-117">Example 2: Update the metadata of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}'


Name                  : VMPolicySetDefinition
ResourceId            : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
ResourceName          : VMPolicySetDefinition
ResourceType          : Microsoft.Authorization/policySetDefinitions
SubscriptionId        : 11111111-1111-1111-1111-111111111111
Properties            : @{displayName=VMPolicySetDefinition; policyType=Custom; metadata=; parameters=; policyDefinitions=System.Object[]}
PolicySetDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policySetDefinitions/VMPolicySetDefinition
```

<span data-ttu-id="3a359-118">이 명령은 해당 범주가 "Virtual Machine"이라는 것을 나타내기 위해 VMPolicySetDefinition이라는 정책 집합 정의의 메타데이터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-118">This command updates the metadata of a policy set definition named VMPolicySetDefinition to indicate its category is "Virtual Machine".</span></span>

### <span data-ttu-id="3a359-119">예제 3: 정책 집합 정의의 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a359-119">Example 3: Update the groups of a policy set definition</span></span>
```
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition '[{ "name": "group1", "displayName": "Virtual Machine Security" }, { "name": "group2" }]'
```

<span data-ttu-id="3a359-120">이 명령은 VMPolicySetDefinition이라는 정책 집합 정의 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-120">This command updates the groups of a policy set definition named VMPolicySetDefinition.</span></span>

### <span data-ttu-id="3a359-121">예제 4: 해시 테이블을 사용하여 정책 집합 정의 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="3a359-121">Example 4: Update the groups of a policy set definition using a hash table</span></span>
```
$groupsJson = ConvertTo-Json @{ name = "group1", displayName = "Virtual Machine Security" }, @{ name = "group2" }
PS C:\> Set-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson
```

<span data-ttu-id="3a359-122">이 명령은 해시 테이블을 사용하여 VMPolicySetDefinition이라는 정책 집합 정의 그룹을 업데이트하여 그룹을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-122">This command updates the groups of a policy set definition named VMPolicySetDefinition using a hash table to construct the groups.</span></span>

## <span data-ttu-id="3a359-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a359-123">PARAMETERS</span></span>

### <span data-ttu-id="3a359-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3a359-124">-ApiVersion</span></span>
<span data-ttu-id="3a359-125">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-125">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3a359-126">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-126">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3a359-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a359-127">-DefaultProfile</span></span>
<span data-ttu-id="3a359-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a359-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a359-129">-Description</span><span class="sxs-lookup"><span data-stu-id="3a359-129">-Description</span></span>
<span data-ttu-id="3a359-130">정책 집합 정의에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-130">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3a359-131">-DisplayName</span></span>
<span data-ttu-id="3a359-132">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-132">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-133">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="3a359-133">-GroupDefinition</span></span>
<span data-ttu-id="3a359-134">업데이트된 정책 집합 정의의 정책 정의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-134">The policy definition groups of the updated policy set definition.</span></span> <span data-ttu-id="3a359-135">그룹이 포함된 파일의 경로 또는 JSON 문자열로 그룹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-135">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-136">-Id</span><span class="sxs-lookup"><span data-stu-id="3a359-136">-Id</span></span>
<span data-ttu-id="3a359-137">구독을 포함한 정식 정책 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-137">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="3a359-138">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3a359-138">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="3a359-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a359-139">-InputObject</span></span>
<span data-ttu-id="3a359-140">다른 cmdlet에서 출력된 정의 개체를 업데이트할 정책 설정 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-140">The policy set definition object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="3a359-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3a359-141">-ManagementGroupName</span></span>
<span data-ttu-id="3a359-142">업데이트할 정책 집합 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-142">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="3a359-143">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3a359-143">-Metadata</span></span>
<span data-ttu-id="3a359-144">업데이트된 정책 집합 정의의 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-144">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="3a359-145">메타데이터를 포함하는 파일 이름의 경로 또는 메타데이터를 JSON 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-145">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-146">-Name</span><span class="sxs-lookup"><span data-stu-id="3a359-146">-Name</span></span>
<span data-ttu-id="3a359-147">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-147">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-148">-Parameter</span><span class="sxs-lookup"><span data-stu-id="3a359-148">-Parameter</span></span>
<span data-ttu-id="3a359-149">업데이트된 정책 집합 정의의 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-149">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="3a359-150">매개 변수 선언을 포함하는 파일 이름 또는 URI에 대한 경로 또는 매개 변수 선언을 JSON 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-150">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-151">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3a359-151">-PolicyDefinition</span></span>
<span data-ttu-id="3a359-152">정책 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-152">The policy definitions.</span></span> <span data-ttu-id="3a359-153">정책 정의를 포함하는 파일 이름에 대한 경로 또는 JSON 문자열로 정책 정의가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-153">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a359-154">-Pre</span><span class="sxs-lookup"><span data-stu-id="3a359-154">-Pre</span></span>
<span data-ttu-id="3a359-155">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-155">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3a359-156">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a359-156">-SubscriptionId</span></span>
<span data-ttu-id="3a359-157">업데이트할 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-157">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="3a359-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a359-158">-Confirm</span></span>
<span data-ttu-id="3a359-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a359-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a359-160">-WhatIf</span></span>
<span data-ttu-id="3a359-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3a359-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a359-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a359-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a359-163">CommonParameters</span></span>
<span data-ttu-id="3a359-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a359-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a359-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a359-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a359-166">입력</span><span class="sxs-lookup"><span data-stu-id="3a359-166">INPUTS</span></span>

### <span data-ttu-id="3a359-167">System.String</span><span class="sxs-lookup"><span data-stu-id="3a359-167">System.String</span></span>

### <span data-ttu-id="3a359-168">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3a359-168">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3a359-169">출력</span><span class="sxs-lookup"><span data-stu-id="3a359-169">OUTPUTS</span></span>

### <span data-ttu-id="3a359-170">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="3a359-170">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3a359-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a359-171">NOTES</span></span>

## <span data-ttu-id="3a359-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a359-172">RELATED LINKS</span></span>
