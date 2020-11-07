---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyDefinition.md
ms.openlocfilehash: 8879f013983888ff0400c0f43ec4e570c495760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876432"
---
# <span data-ttu-id="0d56e-101">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56e-101">New-AzPolicyDefinition</span></span>

## <span data-ttu-id="0d56e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d56e-102">SYNOPSIS</span></span>
<span data-ttu-id="0d56e-103">정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-103">Creates a policy definition.</span></span>

## <span data-ttu-id="0d56e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d56e-104">SYNTAX</span></span>

### <span data-ttu-id="0d56e-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d56e-105">NameParameterSet (Default)</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d56e-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56e-106">ManagementGroupNameParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="0d56e-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d56e-107">SubscriptionIdParameterSet</span></span>
```
New-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0d56e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0d56e-108">DESCRIPTION</span></span>
<span data-ttu-id="0d56e-109">**AzPolicyDefinition** CMDLET은 JSON (JavaScript 개체 표기) 형식의 정책 규칙을 포함 하는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-109">The **New-AzPolicyDefinition** cmdlet creates a policy definition that includes a policy rule in JavaScript Object Notation (JSON) format.</span></span>

## <span data-ttu-id="0d56e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d56e-110">EXAMPLES</span></span>

### <span data-ttu-id="0d56e-111">예제 1: 정책 파일을 사용 하 여 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="0d56e-111">Example 1: Create a policy definition by using a policy file</span></span>
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

<span data-ttu-id="0d56e-112">이 명령은 C:\LocationPolicy.js에 지정 된 정책 규칙을 포함 하는 LocationDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-112">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0d56e-113">파일의 LocationPolicy.js에 대 한 예제 콘텐츠는 위에 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-113">Example content for the LocationPolicy.json file is provided above.</span></span>

### <span data-ttu-id="0d56e-114">예제 2: 인라인 매개 변수를 사용 하 여 매개 변수가 있는 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="0d56e-114">Example 2: Create a parameterized policy definition using inline parameters</span></span>
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

<span data-ttu-id="0d56e-115">이 명령은 C:\LocationPolicy.js에 지정 된 정책 규칙을 포함 하는 LocationDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-115">This command creates a policy definition named LocationDefinition that contains the policy rule specified in C:\LocationPolicy.json.</span></span> <span data-ttu-id="0d56e-116">정책 규칙에 대 한 매개 변수 정의가 인라인으로 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-116">The parameter definition for the policy rule is provided inline.</span></span>

### <span data-ttu-id="0d56e-117">예제 3: 관리 그룹에서 인라인 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="0d56e-117">Example 3: Create a policy definition inline in a management group</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName Dept42 -DisplayName 'Virtual Machine policy definition' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'
```

<span data-ttu-id="0d56e-118">이 명령은 관리 그룹 Dept42에 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-118">This command creates a policy definition named VMPolicyDefinition in management group Dept42.</span></span>
<span data-ttu-id="0d56e-119">명령은 정책을 유효한 JSON 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-119">The command specifies the policy as a string in valid JSON format.</span></span>

### <span data-ttu-id="0d56e-120">예제 4: 메타 데이터를 사용 하 여 인라인 정책 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="0d56e-120">Example 4: Create a policy definition inline with metadata</span></span>
```
PS C:\> New-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"Category":"Virtual Machine"}' -Policy '{"if":{"source":"action","equals":"Microsoft.Compute/virtualMachines/write"},"then":{"effect":"deny"}}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="0d56e-121">이 명령은 범주가 "가상 컴퓨터" 인 메타 데이터를 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-121">This command creates a policy definition named VMPolicyDefinition with metadata indicating its category is "Virtual Machine".</span></span>
<span data-ttu-id="0d56e-122">명령은 정책을 유효한 JSON 형식의 문자열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-122">The command specifies the policy as a string in valid JSON format.</span></span>

## <span data-ttu-id="0d56e-123">변수</span><span class="sxs-lookup"><span data-stu-id="0d56e-123">PARAMETERS</span></span>

### <span data-ttu-id="0d56e-124">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d56e-124">-ApiVersion</span></span>
<span data-ttu-id="0d56e-125">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-125">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0d56e-126">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-126">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d56e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d56e-127">-DefaultProfile</span></span>
<span data-ttu-id="0d56e-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0d56e-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d56e-129">-설명</span><span class="sxs-lookup"><span data-stu-id="0d56e-129">-Description</span></span>
<span data-ttu-id="0d56e-130">정책 정의에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-130">Specifies a description for the policy definition.</span></span>

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

### <span data-ttu-id="0d56e-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0d56e-131">-DisplayName</span></span>
<span data-ttu-id="0d56e-132">정책 정의의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-132">Specifies a display name for the policy definition.</span></span>

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

### <span data-ttu-id="0d56e-133">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0d56e-133">-InformationAction</span></span>
<span data-ttu-id="0d56e-134">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-134">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="0d56e-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d56e-136">하기로</span><span class="sxs-lookup"><span data-stu-id="0d56e-136">Continue</span></span>
- <span data-ttu-id="0d56e-137">숨기기</span><span class="sxs-lookup"><span data-stu-id="0d56e-137">Ignore</span></span>
- <span data-ttu-id="0d56e-138">Inquire</span><span class="sxs-lookup"><span data-stu-id="0d56e-138">Inquire</span></span>
- <span data-ttu-id="0d56e-139">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0d56e-139">SilentlyContinue</span></span>
- <span data-ttu-id="0d56e-140">중지가</span><span class="sxs-lookup"><span data-stu-id="0d56e-140">Stop</span></span>
- <span data-ttu-id="0d56e-141">대기</span><span class="sxs-lookup"><span data-stu-id="0d56e-141">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d56e-142">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0d56e-142">-InformationVariable</span></span>
<span data-ttu-id="0d56e-143">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-143">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d56e-144">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="0d56e-144">-ManagementGroupName</span></span>
<span data-ttu-id="0d56e-145">새 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-145">The name of the management group of the new policy definition.</span></span>

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

### <span data-ttu-id="0d56e-146">-Metadata</span><span class="sxs-lookup"><span data-stu-id="0d56e-146">-Metadata</span></span>
<span data-ttu-id="0d56e-147">정책 정의에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-147">The metadata for policy definition.</span></span> <span data-ttu-id="0d56e-148">메타 데이터를 포함 하는 파일 이름에 대 한 경로 이거나 메타 데이터를 string으로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-148">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

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

### <span data-ttu-id="0d56e-149">-모드</span><span class="sxs-lookup"><span data-stu-id="0d56e-149">-Mode</span></span>
<span data-ttu-id="0d56e-150">정책 정의의 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-150">The mode of the policy definition</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d56e-151">-이름</span><span class="sxs-lookup"><span data-stu-id="0d56e-151">-Name</span></span>
<span data-ttu-id="0d56e-152">정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-152">Specifies a name for the policy definition.</span></span>

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

### <span data-ttu-id="0d56e-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0d56e-153">-Parameter</span></span>
<span data-ttu-id="0d56e-154">정책 정의에 대 한 매개 변수 선언입니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-154">The parameters declaration for policy definition.</span></span> <span data-ttu-id="0d56e-155">매개 변수 선언이 포함 된 파일 이름의 경로 이거나 매개 변수 선언이 string 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-155">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="0d56e-156">-정책</span><span class="sxs-lookup"><span data-stu-id="0d56e-156">-Policy</span></span>
<span data-ttu-id="0d56e-157">정책 정의에 대 한 정책 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-157">Specifies a policy rule for the policy definition.</span></span>
<span data-ttu-id="0d56e-158">Json 파일의 경로 또는 정책 (JSON 형식)을 포함 하는 문자열을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-158">You can specify the path of a .json file or a string that contains the policy in JSON format.</span></span>

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

### <span data-ttu-id="0d56e-159">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d56e-159">-Pre</span></span>
<span data-ttu-id="0d56e-160">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-160">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d56e-161">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d56e-161">-SubscriptionId</span></span>
<span data-ttu-id="0d56e-162">새 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-162">The subscription ID of the new policy definition.</span></span>

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

### <span data-ttu-id="0d56e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d56e-163">CommonParameters</span></span>
<span data-ttu-id="0d56e-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d56e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d56e-165">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d56e-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d56e-166">입력</span><span class="sxs-lookup"><span data-stu-id="0d56e-166">INPUTS</span></span>

## <span data-ttu-id="0d56e-167">출력</span><span class="sxs-lookup"><span data-stu-id="0d56e-167">OUTPUTS</span></span>

## <span data-ttu-id="0d56e-168">상속자</span><span class="sxs-lookup"><span data-stu-id="0d56e-168">NOTES</span></span>

## <span data-ttu-id="0d56e-169">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d56e-169">RELATED LINKS</span></span>

[<span data-ttu-id="0d56e-170">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56e-170">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="0d56e-171">제거-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56e-171">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="0d56e-172">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0d56e-172">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


