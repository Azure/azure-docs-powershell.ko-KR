---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 9ea6f37d21d35736116b2e9bf4fc3fcf20becf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973552"
---
# <span data-ttu-id="24fd6-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="24fd6-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="24fd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24fd6-102">SYNOPSIS</span></span>
<span data-ttu-id="24fd6-103">정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="24fd6-104">구문</span><span class="sxs-lookup"><span data-stu-id="24fd6-104">SYNTAX</span></span>

### <span data-ttu-id="24fd6-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="24fd6-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24fd6-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fd6-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24fd6-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fd6-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24fd6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fd6-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24fd6-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fd6-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24fd6-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="24fd6-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24fd6-111">설명</span><span class="sxs-lookup"><span data-stu-id="24fd6-111">DESCRIPTION</span></span>
<span data-ttu-id="24fd6-112">**Get-AzPolicySetDefinition** cmdlet은 정책 집합 정의 또는 이름 또는 ID로 식별된 특정 정책 집합 정의의 컬렉션을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="24fd6-113">예제</span><span class="sxs-lookup"><span data-stu-id="24fd6-113">EXAMPLES</span></span>

### <span data-ttu-id="24fd6-114">예제 1: 모든 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="24fd6-115">이 명령은 모든 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="24fd6-116">예제 2: 이름에 따라 현재 구독에서 정책 집합 정의를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="24fd6-117">이 명령은 현재 기본 구독에서 VMPolicySetDefinition이라는 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="24fd6-118">예제 3: 구독에서 이름에 따라 정책 집합 정의를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="24fd6-119">이 명령은 ID 3bf44b72-c631-427a-b8c8-53e2595398ca를 사용하여 구독에서 VMPolicySetDefinition이라는 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="24fd6-120">예제 4: 관리 그룹에서 모든 사용자 지정 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="24fd6-121">이 명령은 Dept42라는 관리 그룹에서 모든 사용자 지정 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="24fd6-122">예제 5: 주어진 범주에서 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="24fd6-123">이 명령은 "Virtual Machine"범주의 모든 정책 집합 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="24fd6-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="24fd6-124">PARAMETERS</span></span>

### <span data-ttu-id="24fd6-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24fd6-125">-ApiVersion</span></span>
<span data-ttu-id="24fd6-126">설정하면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="24fd6-127">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="24fd6-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="24fd6-128">-Builtin</span></span>
<span data-ttu-id="24fd6-129">결과 목록을 기본 제공 정책 집합 정의로만 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fd6-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="24fd6-130">-Custom</span></span>
<span data-ttu-id="24fd6-131">결과 목록을 사용자 지정 정책 집합 정의로만 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24fd6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24fd6-132">-DefaultProfile</span></span>
<span data-ttu-id="24fd6-133">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24fd6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24fd6-134">-Id</span><span class="sxs-lookup"><span data-stu-id="24fd6-134">-Id</span></span>
<span data-ttu-id="24fd6-135">구독을 포함하여 완전히 자격을 갖춘 정책 집합 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="24fd6-136">예: /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="24fd6-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="24fd6-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="24fd6-137">-ManagementGroupName</span></span>
<span data-ttu-id="24fd6-138">얻을 정책 집합 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fd6-139">-Name</span><span class="sxs-lookup"><span data-stu-id="24fd6-139">-Name</span></span>
<span data-ttu-id="24fd6-140">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fd6-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="24fd6-141">-Pre</span></span>
<span data-ttu-id="24fd6-142">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="24fd6-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24fd6-143">-SubscriptionId</span></span>
<span data-ttu-id="24fd6-144">얻을 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24fd6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24fd6-145">CommonParameters</span></span>
<span data-ttu-id="24fd6-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24fd6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24fd6-147">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24fd6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24fd6-148">입력</span><span class="sxs-lookup"><span data-stu-id="24fd6-148">INPUTS</span></span>

### <span data-ttu-id="24fd6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="24fd6-149">System.String</span></span>

### <span data-ttu-id="24fd6-150">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="24fd6-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="24fd6-151">출력</span><span class="sxs-lookup"><span data-stu-id="24fd6-151">OUTPUTS</span></span>

### <span data-ttu-id="24fd6-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="24fd6-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="24fd6-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24fd6-153">NOTES</span></span>

## <span data-ttu-id="24fd6-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24fd6-154">RELATED LINKS</span></span>
