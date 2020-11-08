---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: 1a4a2579b05c60133fa1b0f7ab057be602965eaa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204884"
---
# <span data-ttu-id="8675d-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8675d-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="8675d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8675d-102">SYNOPSIS</span></span>
<span data-ttu-id="8675d-103">정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="8675d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8675d-104">SYNTAX</span></span>

### <span data-ttu-id="8675d-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8675d-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-GroupDefinition <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8675d-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8675d-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8675d-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8675d-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-GroupDefinition <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8675d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8675d-108">DESCRIPTION</span></span>
<span data-ttu-id="8675d-109">**새 AzPolicySetDefinition** cmdlet은 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="8675d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8675d-110">EXAMPLES</span></span>

### <span data-ttu-id="8675d-111">예제 1: 정책 집합 파일을 사용 하 여 메타 데이터를 사용 하 여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="8675d-111">Example 1: Create a policy set definition with metadata by using a policy set file</span></span>
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

<span data-ttu-id="8675d-112">이 명령은 해당 범주를 나타내는 메타 데이터가 있는 VMPolicySetDefinition 이라는 정책 집합 정의를 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 "가상 컴퓨터"로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-112">This command creates a policy set definition named VMPolicySetDefinition with metadata indicating its category is "Virtual Machine" that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8675d-113">VMPolicy.js의 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="8675d-114">예제 2: 매개 변수가 있는 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="8675d-114">Example 2: Create a parameterized policy set definition</span></span>
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

<span data-ttu-id="8675d-115">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 VMPolicySetDefinition 이라는 매개 변수가 있는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-115">This command creates a parameterized policy set definition named VMPolicySetDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8675d-116">VMPolicy.js의 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-116">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="8675d-117">예제 3: 정책 정의 그룹을 사용 하 여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="8675d-117">Example 3: Create a policy set definition with policy definition groups</span></span>
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

<span data-ttu-id="8675d-118">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 그룹화 하 여 VMPolicySetDefinition 이라는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-118">This command creates a policy set definition named VMPolicySetDefinition with grouping of policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="8675d-119">VMPolicy.js의 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-119">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="8675d-120">변수</span><span class="sxs-lookup"><span data-stu-id="8675d-120">PARAMETERS</span></span>

### <span data-ttu-id="8675d-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8675d-121">-ApiVersion</span></span>
<span data-ttu-id="8675d-122">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8675d-123">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8675d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8675d-124">-DefaultProfile</span></span>
<span data-ttu-id="8675d-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8675d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8675d-126">-설명</span><span class="sxs-lookup"><span data-stu-id="8675d-126">-Description</span></span>
<span data-ttu-id="8675d-127">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-127">The description for policy set definition.</span></span>

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

### <span data-ttu-id="8675d-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8675d-128">-DisplayName</span></span>
<span data-ttu-id="8675d-129">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-129">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="8675d-130">-GroupDefinition</span><span class="sxs-lookup"><span data-stu-id="8675d-130">-GroupDefinition</span></span>
<span data-ttu-id="8675d-131">새 정책 집합 정의에 대 한 정책 정의 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-131">The policy definition groups for the new policy set definition.</span></span> <span data-ttu-id="8675d-132">그룹을 포함 하는 파일의 경로 이거나 그룹을 JSON 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-132">This can either be a path to a file containing the groups, or the groups as a JSON string.</span></span>

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

### <span data-ttu-id="8675d-133">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8675d-133">-ManagementGroupName</span></span>
<span data-ttu-id="8675d-134">새 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-134">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="8675d-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8675d-135">-Metadata</span></span>
<span data-ttu-id="8675d-136">정책 집합 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-136">The metadata for policy set definition.</span></span> <span data-ttu-id="8675d-137">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 JSON 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-137">This can either be a path to a file name containing the metadata, or the metadata as a JSON string.</span></span>

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

### <span data-ttu-id="8675d-138">-이름</span><span class="sxs-lookup"><span data-stu-id="8675d-138">-Name</span></span>
<span data-ttu-id="8675d-139">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-139">The policy set definition name.</span></span>

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

### <span data-ttu-id="8675d-140">-Parameter</span><span class="sxs-lookup"><span data-stu-id="8675d-140">-Parameter</span></span>
<span data-ttu-id="8675d-141">정책 집합 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-141">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="8675d-142">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 JSON 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-142">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as a JSON string.</span></span>

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

### <span data-ttu-id="8675d-143">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8675d-143">-PolicyDefinition</span></span>
<span data-ttu-id="8675d-144">정책 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-144">The policy definitions.</span></span> <span data-ttu-id="8675d-145">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나, JSON 문자열로 된 정책 정의 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-145">This can either be a path to a file name containing the policy definitions, or the policy definitions as a JSON string.</span></span>

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

### <span data-ttu-id="8675d-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="8675d-146">-Pre</span></span>
<span data-ttu-id="8675d-147">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-147">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8675d-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8675d-148">-SubscriptionId</span></span>
<span data-ttu-id="8675d-149">새 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-149">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="8675d-150">-확인</span><span class="sxs-lookup"><span data-stu-id="8675d-150">-Confirm</span></span>
<span data-ttu-id="8675d-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8675d-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8675d-152">-WhatIf</span></span>
<span data-ttu-id="8675d-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8675d-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8675d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8675d-155">CommonParameters</span></span>
<span data-ttu-id="8675d-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8675d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8675d-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8675d-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8675d-158">입력</span><span class="sxs-lookup"><span data-stu-id="8675d-158">INPUTS</span></span>

### <span data-ttu-id="8675d-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8675d-159">System.String</span></span>

### <span data-ttu-id="8675d-160">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8675d-160">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8675d-161">출력</span><span class="sxs-lookup"><span data-stu-id="8675d-161">OUTPUTS</span></span>

### <span data-ttu-id="8675d-162">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="8675d-162">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8675d-163">상속자</span><span class="sxs-lookup"><span data-stu-id="8675d-163">NOTES</span></span>

## <span data-ttu-id="8675d-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8675d-164">RELATED LINKS</span></span>
