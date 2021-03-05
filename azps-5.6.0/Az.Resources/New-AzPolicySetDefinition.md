---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: ae1cc96cd617ec74a69fc2c95ec50973e688ebe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995227"
---
# <span data-ttu-id="11258-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="11258-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="11258-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11258-102">SYNOPSIS</span></span>
<span data-ttu-id="11258-103">정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11258-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="11258-104">구문</span><span class="sxs-lookup"><span data-stu-id="11258-104">SYNTAX</span></span>

### <span data-ttu-id="11258-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="11258-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11258-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11258-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11258-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11258-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11258-108">설명</span><span class="sxs-lookup"><span data-stu-id="11258-108">DESCRIPTION</span></span>
<span data-ttu-id="11258-109">**New-AzPolicySetDefinition** cmdlet은 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11258-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="11258-110">예제</span><span class="sxs-lookup"><span data-stu-id="11258-110">EXAMPLES</span></span>

### <span data-ttu-id="11258-111">예제 1: 정책 집합 파일을 사용하여 메타데이터를 사용하여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="11258-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "Finance"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -Metadata '{"category":"Virtual Machine"}' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="11258-112">이 명령은 해당 범주가 "Virtual Machine"임을 나타내는 메타데이터가 있는 VMPolicySetDefinition이라는 정책 집합 정의를 C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="11258-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="11258-113">위의 VMPolicy.js예제 콘텐츠가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="11258-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="11258-114">예제 2: 매개 변수화된 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="11258-114">Example 2: Create a parameterized policy set definition</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "parameters": {
         "tagName": {
            "value": "Business Unit"
         },
         "tagValue": {
            "value": "[parameters('buTagValue')]"
         }
      }
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf"
   }
]
```

```
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="11258-115">이 명령은 VMPolicySetDefin C:\VMPolicy.jsition이라는 매개 변수화된 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="11258-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="11258-116">위의 VMPolicy.js예제 콘텐츠가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="11258-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="11258-117">예제 3: 정책 정의 그룹을 사용하여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="11258-117">Example 3: Create a policy set definition with policy definition groups</span></span>
```
[
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/2a0e14a6-b0a6-4fab-991a-187a4f81c498",
      "groupNames": [ "group1" ]
   },
   {
      "policyDefinitionId": "/providers/Microsoft.Authorization/policyDefinitions/464dbb85-3d5f-4a1d-bb09-95a9b5dd19cf",
      "groupNames": [ "group2" ]
   }
]
```

```
$groupsJson = ConvertTo-Json @{ name = "group1" }, @{ name = "group2" }
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -GroupDefinition $groupsJson -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="11258-118">이 명령은 VMPolicySetDefinition이라는 정책 집합 정의를 만들고, 설정에 지정된 정책 정의의 그룹화가 C:\VMPolicy.js.</span><span class="sxs-lookup"><span data-stu-id="11258-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="11258-119">위의 VMPolicy.js예제 콘텐츠가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="11258-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="11258-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="11258-120">PARAMETERS</span></span>

### <span data-ttu-id="11258-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="11258-121">-ApiVersion</span></span>
<span data-ttu-id="11258-122">설정하면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11258-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="11258-123">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="11258-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="11258-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11258-124">-DefaultProfile</span></span>
<span data-ttu-id="11258-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="11258-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11258-126">-Description</span><span class="sxs-lookup"><span data-stu-id="11258-126">-Description</span></span>
<span data-ttu-id="11258-127">정책 집합 정의에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="11258-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="11258-128">-DisplayName</span></span>
<span data-ttu-id="11258-129">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="11258-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="11258-130">-GroupDefinition</span></span>
<span data-ttu-id="11258-131">새 정책 집합 정의에 대한 정책 정의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="11258-132">그룹이 포함된 파일에 대한 경로 또는 JSON 문자열로 그룹을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11258-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="11258-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="11258-133">-ManagementGroupName</span></span>
<span data-ttu-id="11258-134">새 정책 집합 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="11258-135">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="11258-135">-Metadata</span></span>
<span data-ttu-id="11258-136">정책 집합 정의에 대한 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-136">The metadata for policy set definition.</span></span> <span data-ttu-id="11258-137">메타데이터를 포함하는 파일 이름에 대한 경로 또는 JSON 문자열로 메타데이터가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11258-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="11258-138">-Name</span><span class="sxs-lookup"><span data-stu-id="11258-138">-Name</span></span>
<span data-ttu-id="11258-139">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-139">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11258-140">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="11258-140">-Parameter</span></span>
<span data-ttu-id="11258-141">정책 집합 정의에 대한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="11258-142">매개 변수 선언을 포함하는 파일 이름의 경로 또는 매개 변수 선언을 JSON 문자열로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11258-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="11258-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="11258-143">-PolicyDefinition</span></span>
<span data-ttu-id="11258-144">정책 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-144">The policy definitions.</span></span> <span data-ttu-id="11258-145">정책 정의를 포함하는 파일 이름에 대한 경로 또는 JSON 문자열로 정책 정의일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11258-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11258-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="11258-146">-Pre</span></span>
<span data-ttu-id="11258-147">설정하면 cmdlet이 사용할 버전을 자동으로 결정할 때 미리 릴리스 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11258-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="11258-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11258-148">-SubscriptionId</span></span>
<span data-ttu-id="11258-149">새 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11258-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="11258-150">-확인</span><span class="sxs-lookup"><span data-stu-id="11258-150">-Confirm</span></span>
<span data-ttu-id="11258-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="11258-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11258-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11258-152">-WhatIf</span></span>
<span data-ttu-id="11258-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="11258-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11258-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11258-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11258-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11258-155">CommonParameters</span></span>
<span data-ttu-id="11258-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="11258-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11258-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11258-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11258-158">입력</span><span class="sxs-lookup"><span data-stu-id="11258-158">INPUTS</span></span>

### <span data-ttu-id="11258-159">System.String</span><span class="sxs-lookup"><span data-stu-id="11258-159">System.String</span></span>

### <span data-ttu-id="11258-160">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11258-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="11258-161">출력</span><span class="sxs-lookup"><span data-stu-id="11258-161">OUTPUTS</span></span>

### <span data-ttu-id="11258-162">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="11258-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="11258-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="11258-163">NOTES</span></span>

## <span data-ttu-id="11258-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11258-164">RELATED LINKS</span></span>
