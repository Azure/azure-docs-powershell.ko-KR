---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876480"
---
# <span data-ttu-id="8d6e2-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d6e2-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="8d6e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d6e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8d6e2-103">정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-103">Gets policy definitions.</span></span>

## <span data-ttu-id="8d6e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d6e2-104">SYNTAX</span></span>

### <span data-ttu-id="8d6e2-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d6e2-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d6e2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6e2-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d6e2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6e2-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d6e2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6e2-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d6e2-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6e2-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8d6e2-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d6e2-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8d6e2-111">설명은</span><span class="sxs-lookup"><span data-stu-id="8d6e2-111">DESCRIPTION</span></span>
<span data-ttu-id="8d6e2-112">**AzPolicyDefinition** cmdlet은 정책 정의의 컬렉션이 나 이름 또는 ID로 식별 되는 특정 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="8d6e2-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8d6e2-113">EXAMPLES</span></span>

### <span data-ttu-id="8d6e2-114">예제 1: 모든 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="8d6e2-115">이 명령은 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="8d6e2-116">예제 2: 이름으로 현재 구독에서 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="8d6e2-117">이 명령은 현재 기본 구독에서 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="8d6e2-118">예제 3: 관리 그룹에서 이름별로 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="8d6e2-119">이 명령은 Dept42 이라는 관리 그룹에서 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="8d6e2-120">예제 4: 구독에서 모든 기본 제공 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="8d6e2-121">이 명령은 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 구독에서 기본 제공 된 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="8d6e2-122">변수</span><span class="sxs-lookup"><span data-stu-id="8d6e2-122">PARAMETERS</span></span>

### <span data-ttu-id="8d6e2-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8d6e2-123">-ApiVersion</span></span>
<span data-ttu-id="8d6e2-124">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8d6e2-125">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8d6e2-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="8d6e2-126">-Builtin</span></span>
<span data-ttu-id="8d6e2-127">결과 목록을 기본 제공 정책 정의로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="8d6e2-128">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="8d6e2-128">-Custom</span></span>
<span data-ttu-id="8d6e2-129">결과 목록을 사용자 지정 정책 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="8d6e2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d6e2-130">-DefaultProfile</span></span>
<span data-ttu-id="8d6e2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8d6e2-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d6e2-132">-Id</span><span class="sxs-lookup"><span data-stu-id="8d6e2-132">-Id</span></span>
<span data-ttu-id="8d6e2-133">이 cmdlet이 가져오는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8d6e2-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8d6e2-134">-InformationAction</span></span>
<span data-ttu-id="8d6e2-135">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8d6e2-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d6e2-137">하기로</span><span class="sxs-lookup"><span data-stu-id="8d6e2-137">Continue</span></span>
- <span data-ttu-id="8d6e2-138">숨기기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-138">Ignore</span></span>
- <span data-ttu-id="8d6e2-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="8d6e2-139">Inquire</span></span>
- <span data-ttu-id="8d6e2-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8d6e2-140">SilentlyContinue</span></span>
- <span data-ttu-id="8d6e2-141">중지가</span><span class="sxs-lookup"><span data-stu-id="8d6e2-141">Stop</span></span>
- <span data-ttu-id="8d6e2-142">대기</span><span class="sxs-lookup"><span data-stu-id="8d6e2-142">Suspend</span></span>

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

### <span data-ttu-id="8d6e2-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8d6e2-143">-InformationVariable</span></span>
<span data-ttu-id="8d6e2-144">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8d6e2-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8d6e2-145">-ManagementGroupName</span></span>
<span data-ttu-id="8d6e2-146">가져올 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="8d6e2-147">-이름</span><span class="sxs-lookup"><span data-stu-id="8d6e2-147">-Name</span></span>
<span data-ttu-id="8d6e2-148">이 cmdlet이 가져오는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8d6e2-149">-Pre</span><span class="sxs-lookup"><span data-stu-id="8d6e2-149">-Pre</span></span>
<span data-ttu-id="8d6e2-150">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8d6e2-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d6e2-151">-SubscriptionId</span></span>
<span data-ttu-id="8d6e2-152">가져올 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="8d6e2-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d6e2-153">CommonParameters</span></span>
<span data-ttu-id="8d6e2-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d6e2-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d6e2-155">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d6e2-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d6e2-156">입력</span><span class="sxs-lookup"><span data-stu-id="8d6e2-156">INPUTS</span></span>

## <span data-ttu-id="8d6e2-157">출력</span><span class="sxs-lookup"><span data-stu-id="8d6e2-157">OUTPUTS</span></span>

## <span data-ttu-id="8d6e2-158">상속자</span><span class="sxs-lookup"><span data-stu-id="8d6e2-158">NOTES</span></span>

## <span data-ttu-id="8d6e2-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d6e2-159">RELATED LINKS</span></span>

[<span data-ttu-id="8d6e2-160">새로운 AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d6e2-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8d6e2-161">제거-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d6e2-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="8d6e2-162">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8d6e2-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


