---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 51c5608c8212b519e6ca979e470c2ab1a5d96e6b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307937"
---
# <span data-ttu-id="d6159-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6159-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="d6159-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6159-102">SYNOPSIS</span></span>
<span data-ttu-id="d6159-103">정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-103">Creates a policy definition.</span></span>

## <span data-ttu-id="d6159-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6159-104">SYNTAX</span></span>

### <span data-ttu-id="d6159-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6159-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6159-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6159-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6159-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6159-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6159-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6159-108">DESCRIPTION</span></span>
<span data-ttu-id="d6159-109">**AzPolicyDefinition** CMDLET은 JSON (JavaScript 개체 표기) 형식의 정책 규칙을 포함 하는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="d6159-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6159-110">EXAMPLES</span></span>

### <span data-ttu-id="d6159-111">예제 1: 정책 파일을 사용 하 여 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d6159-111">Example 1: Create a policy definition by using a policy file</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": ["eastus", "westus", "centralus"]
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json
```

<span data-ttu-id="d6159-112">이 명령은 C:\LocationPolicy.js에 지정 된 정책 규칙을 포함 하는 LocationDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="d6159-113">파일의 LocationPolicy.js에 대 한 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="d6159-114">예제 2: 인라인 매개 변수를 사용 하 여 매개 변수가 있는 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d6159-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
```
{
   "if": {
      "field": "location",
      "notIn": "[parameters('listOfAllowedLocations')]"
   },
   "then": {
      "effect": "audit"
   }
}
```

```
PS C:\> New-AzPolicyDefinition -Name 'LocationDefinition' -Policy C:\LocationPolicy.json -Parameter '{ "listOfAllowedLocations": { "type": "array" } }'
```

<span data-ttu-id="d6159-115">이 명령은 C:\LocationPolicy.js에 지정 된 정책 규칙을 포함 하는 LocationDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="d6159-116">정책 규칙에 대 한 매개 변수 정의가 인라인으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="d6159-117">예제 3: 관리 그룹에서 인라인 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d6159-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="d6159-118">이 명령은 관리 그룹 Dept42에 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="d6159-119">명령은 정책을 유효한 JSON 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="d6159-120">예제 4: 메타 데이터를 사용 하 여 인라인 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d6159-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}' -Policy '{"if":{"field":"type","equals":"Microsoft.Compute/virtualMachines"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="d6159-121">이 명령은 범주가 "가상 컴퓨터" 인 메타 데이터를 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="d6159-122">명령은 정책을 유효한 JSON 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-122">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="d6159-123">예제 5: 모드를 사용 하 여 인라인 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="d6159-123">Example 5: Create a policy definition inline with mode</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'TagsPolicyDefinition' -Policy '{"if":{"value":"[less(length(field(''tags'')), 3)]","equals":true},"then":{"effect":"deny"}}' -Mode Indexed


Name               : TagsPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
ResourceName       : TagsPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=TagsPolicyDefinition; policyType=Custom; mode=Indexed; metadata=; parameters=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/TagsPolicyDefinition
```

<span data-ttu-id="d6159-124">이 명령은 태그 및 위치를 지 원하는 리소스 유형에 대해서만 정책을 평가 해야 함을 나타내는 "인덱싱된" 모드의 TagsPolicyDefinition 라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-124">This command creates a policy definition named TagsPolicyDefinition with mode "Indexed" indicating the policy should be evaluated only for resource types that support tags and location.</span></span>

## <span data-ttu-id="d6159-125">변수</span><span class="sxs-lookup"><span data-stu-id="d6159-125">PARAMETERS</span></span>

### <span data-ttu-id="d6159-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d6159-126">-ApiVersion</span></span>
<span data-ttu-id="d6159-127">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-127">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d6159-128">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-128">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d6159-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6159-129">-DefaultProfile</span></span>
<span data-ttu-id="d6159-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d6159-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6159-131">-설명</span><span class="sxs-lookup"><span data-stu-id="d6159-131">-Description</span></span>
<span data-ttu-id="d6159-132">정책 정의에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-132">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="d6159-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d6159-133">-DisplayName</span></span>
<span data-ttu-id="d6159-134">정책 정의의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-134">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="d6159-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="d6159-135">-ManagementGroupName</span></span>
<span data-ttu-id="d6159-136">새 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-136">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="d6159-137">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d6159-137">-Metadata</span></span>
<span data-ttu-id="d6159-138">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-138">The metadata for policy definition.</span></span> <span data-ttu-id="d6159-139">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터를 string으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-139">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="d6159-140">-모드</span><span class="sxs-lookup"><span data-stu-id="d6159-140">-Mode</span></span>
<span data-ttu-id="d6159-141">정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-141">The mode of the policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: All
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6159-142">-이름</span><span class="sxs-lookup"><span data-stu-id="d6159-142">-Name</span></span>
<span data-ttu-id="d6159-143">정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-143">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="d6159-144">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d6159-144">-Parameter</span></span>
<span data-ttu-id="d6159-145">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-145">The parameters declaration for policy definition.</span></span> <span data-ttu-id="d6159-146">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-146">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="d6159-147">-정책</span><span class="sxs-lookup"><span data-stu-id="d6159-147">-Policy</span></span>
<span data-ttu-id="d6159-148">정책 정의에 대 한 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-148">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="d6159-149">Json 파일의 경로 또는 정책 (JSON 형식)을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-149">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="d6159-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="d6159-150">-Pre</span></span>
<span data-ttu-id="d6159-151">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d6159-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d6159-152">-SubscriptionId</span></span>
<span data-ttu-id="d6159-153">새 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-153">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="d6159-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6159-154">CommonParameters</span></span>
<span data-ttu-id="d6159-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6159-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6159-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d6159-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6159-157">입력</span><span class="sxs-lookup"><span data-stu-id="d6159-157">INPUTS</span></span>

### <span data-ttu-id="d6159-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d6159-158">System.String</span></span>

### <span data-ttu-id="d6159-159">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6159-159">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d6159-160">출력</span><span class="sxs-lookup"><span data-stu-id="d6159-160">OUTPUTS</span></span>

### <span data-ttu-id="d6159-161">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="d6159-161">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d6159-162">상속자</span><span class="sxs-lookup"><span data-stu-id="d6159-162">NOTES</span></span>

## <span data-ttu-id="d6159-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6159-163">RELATED LINKS</span></span>

[<span data-ttu-id="d6159-164">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6159-164">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="d6159-165">제거-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6159-165">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="d6159-166">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d6159-166">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


