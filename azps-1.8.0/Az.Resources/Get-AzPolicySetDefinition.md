---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 3bfc546c39e46c4b3e7a5a504107c873c2e96888
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699429"
---
# <span data-ttu-id="3140b-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3140b-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="3140b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3140b-102">SYNOPSIS</span></span>
<span data-ttu-id="3140b-103">정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="3140b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3140b-104">SYNTAX</span></span>

### <span data-ttu-id="3140b-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3140b-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3140b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3140b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3140b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3140b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3140b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3140b-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3140b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="3140b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3140b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="3140b-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3140b-111">설명은</span><span class="sxs-lookup"><span data-stu-id="3140b-111">DESCRIPTION</span></span>
<span data-ttu-id="3140b-112">**AzPolicySetDefinition** cmdlet은 이름 또는 ID로 식별 되는 특정 정책 집합 정의 또는 정책 집합 정의의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="3140b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="3140b-113">EXAMPLES</span></span>

### <span data-ttu-id="3140b-114">예제 1: 모든 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="3140b-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="3140b-115">이 명령은 모든 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="3140b-116">예제 2: 이름으로 현재 구독에서 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="3140b-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="3140b-117">이 명령은 현재 기본 구독에서 VMPolicySetDefinition 이라는 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="3140b-118">예제 3: 이름으로 구독에서 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="3140b-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="3140b-119">이 명령은 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 인 구독에서 VMPolicySetDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="3140b-120">예제 4: 관리 그룹에서 모든 사용자 지정 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="3140b-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="3140b-121">이 명령은 Dept42 이라는 관리 그룹에서 모든 사용자 지정 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

## <span data-ttu-id="3140b-122">변수</span><span class="sxs-lookup"><span data-stu-id="3140b-122">PARAMETERS</span></span>

### <span data-ttu-id="3140b-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3140b-123">-ApiVersion</span></span>
<span data-ttu-id="3140b-124">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-124">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3140b-125">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-125">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3140b-126">-Builtin</span><span class="sxs-lookup"><span data-stu-id="3140b-126">-Builtin</span></span>
<span data-ttu-id="3140b-127">결과 목록을 기본 제공 정책 집합 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-127">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="3140b-128">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="3140b-128">-Custom</span></span>
<span data-ttu-id="3140b-129">결과 목록을 사용자 지정 정책 집합 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-129">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="3140b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3140b-130">-DefaultProfile</span></span>
<span data-ttu-id="3140b-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3140b-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3140b-132">-Id</span><span class="sxs-lookup"><span data-stu-id="3140b-132">-Id</span></span>
<span data-ttu-id="3140b-133">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-133">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="3140b-134">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="3140b-134">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="3140b-135">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="3140b-135">-ManagementGroupName</span></span>
<span data-ttu-id="3140b-136">가져올 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-136">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="3140b-137">-이름</span><span class="sxs-lookup"><span data-stu-id="3140b-137">-Name</span></span>
<span data-ttu-id="3140b-138">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-138">The policy set definition name.</span></span>

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

### <span data-ttu-id="3140b-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="3140b-139">-Pre</span></span>
<span data-ttu-id="3140b-140">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-140">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3140b-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3140b-141">-SubscriptionId</span></span>
<span data-ttu-id="3140b-142">가져올 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-142">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="3140b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3140b-143">CommonParameters</span></span>
<span data-ttu-id="3140b-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3140b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3140b-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3140b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3140b-146">입력</span><span class="sxs-lookup"><span data-stu-id="3140b-146">INPUTS</span></span>

### <span data-ttu-id="3140b-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3140b-147">System.String</span></span>

### <span data-ttu-id="3140b-148">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3140b-148">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3140b-149">출력</span><span class="sxs-lookup"><span data-stu-id="3140b-149">OUTPUTS</span></span>

### <span data-ttu-id="3140b-150">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="3140b-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3140b-151">상속자</span><span class="sxs-lookup"><span data-stu-id="3140b-151">NOTES</span></span>

## <span data-ttu-id="3140b-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3140b-152">RELATED LINKS</span></span>
