---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicySetDefinition.md
ms.openlocfilehash: cf1f1993c58e9c87c36538199555e5ebd7c2175a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699381"
---
# <span data-ttu-id="f67dc-101">New-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="f67dc-101">New-AzPolicySetDefinition</span></span>

## <span data-ttu-id="f67dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f67dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f67dc-103">정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-103">Creates a policy set definition.</span></span>

## <span data-ttu-id="f67dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f67dc-104">SYNTAX</span></span>

### <span data-ttu-id="f67dc-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f67dc-105">NameParameterSet (Default)</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f67dc-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f67dc-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f67dc-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f67dc-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Metadata <String>]
 -PolicyDefinition <String> [-Parameter <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f67dc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f67dc-108">DESCRIPTION</span></span>
<span data-ttu-id="f67dc-109">**새 AzPolicySetDefinition** cmdlet은 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-109">The **New-AzPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="f67dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f67dc-110">EXAMPLES</span></span>

### <span data-ttu-id="f67dc-111">예제 1: 정책 집합 파일을 사용 하 여 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="f67dc-111">Example 1: Create a policy set definition by using a policy set file</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="f67dc-112">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 VMPolicyDefinition 이라는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-112">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f67dc-113">VMPolicy.js의 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-113">Example content of the VMPolicy.json is provided above.</span></span>

### <span data-ttu-id="f67dc-114">예제 2: 매개 변수가 있는 정책 집합 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="f67dc-114">Example 2: Create a parameterized policy set definition</span></span>
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
PS C:\> New-AzPolicySetDefinition -Name 'VMPolicyDefinition' -PolicyDefinition C:\VMPolicySet.json -Parameter '{ "buTagValue": { "type": "string" } }'
```

<span data-ttu-id="f67dc-115">이 명령은 C:\VMPolicy.js에 지정 된 정책 정의를 포함 하는 VMPolicyDefinition 이라는 매개 변수가 있는 정책 집합 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-115">This command creates a parameterized policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span> <span data-ttu-id="f67dc-116">VMPolicy.js의 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-116">Example content of the VMPolicy.json is provided above.</span></span>

## <span data-ttu-id="f67dc-117">변수</span><span class="sxs-lookup"><span data-stu-id="f67dc-117">PARAMETERS</span></span>

### <span data-ttu-id="f67dc-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f67dc-118">-ApiVersion</span></span>
<span data-ttu-id="f67dc-119">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f67dc-120">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-120">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f67dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f67dc-121">-DefaultProfile</span></span>
<span data-ttu-id="f67dc-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f67dc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f67dc-123">-설명</span><span class="sxs-lookup"><span data-stu-id="f67dc-123">-Description</span></span>
<span data-ttu-id="f67dc-124">정책 집합 정의에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-124">The description for policy set definition.</span></span>

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

### <span data-ttu-id="f67dc-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f67dc-125">-DisplayName</span></span>
<span data-ttu-id="f67dc-126">정책 집합 정의의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-126">The display name for policy set definition.</span></span>

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

### <span data-ttu-id="f67dc-127">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f67dc-127">-ManagementGroupName</span></span>
<span data-ttu-id="f67dc-128">새 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-128">The name of the management group of the new policy set definition.</span></span>

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

### <span data-ttu-id="f67dc-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f67dc-129">-Metadata</span></span>
<span data-ttu-id="f67dc-130">정책 집합 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-130">The metadata for policy set definition.</span></span> <span data-ttu-id="f67dc-131">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터를 string으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-131">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="f67dc-132">-이름</span><span class="sxs-lookup"><span data-stu-id="f67dc-132">-Name</span></span>
<span data-ttu-id="f67dc-133">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-133">The policy set definition name.</span></span>

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

### <span data-ttu-id="f67dc-134">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f67dc-134">-Parameter</span></span>
<span data-ttu-id="f67dc-135">정책 집합 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-135">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="f67dc-136">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-136">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="f67dc-137">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f67dc-137">-PolicyDefinition</span></span>
<span data-ttu-id="f67dc-138">정책 집합 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-138">The policy set definition.</span></span> <span data-ttu-id="f67dc-139">이는 정책 정의를 포함 하는 파일 이름에 대 한 경로 이거나 정책 집합 정의를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-139">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

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

### <span data-ttu-id="f67dc-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="f67dc-140">-Pre</span></span>
<span data-ttu-id="f67dc-141">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-141">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f67dc-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f67dc-142">-SubscriptionId</span></span>
<span data-ttu-id="f67dc-143">새 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-143">The subscription ID of the new policy set definition.</span></span>

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

### <span data-ttu-id="f67dc-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f67dc-144">-Confirm</span></span>
<span data-ttu-id="f67dc-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f67dc-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f67dc-146">-WhatIf</span></span>
<span data-ttu-id="f67dc-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f67dc-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f67dc-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f67dc-149">CommonParameters</span></span>
<span data-ttu-id="f67dc-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f67dc-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f67dc-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f67dc-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f67dc-152">입력</span><span class="sxs-lookup"><span data-stu-id="f67dc-152">INPUTS</span></span>

### <span data-ttu-id="f67dc-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f67dc-153">System.String</span></span>

### <span data-ttu-id="f67dc-154">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f67dc-154">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f67dc-155">출력</span><span class="sxs-lookup"><span data-stu-id="f67dc-155">OUTPUTS</span></span>

### <span data-ttu-id="f67dc-156">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="f67dc-156">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f67dc-157">상속자</span><span class="sxs-lookup"><span data-stu-id="f67dc-157">NOTES</span></span>

## <span data-ttu-id="f67dc-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f67dc-158">RELATED LINKS</span></span>
