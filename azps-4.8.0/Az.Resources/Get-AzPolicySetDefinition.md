---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047669"
---
# <span data-ttu-id="14ee1-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="14ee1-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="14ee1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="14ee1-103">정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="14ee1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="14ee1-104">SYNTAX</span></span>

### <span data-ttu-id="14ee1-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="14ee1-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ee1-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14ee1-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ee1-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14ee1-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ee1-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14ee1-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14ee1-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="14ee1-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14ee1-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="14ee1-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ee1-111">설명은</span><span class="sxs-lookup"><span data-stu-id="14ee1-111">DESCRIPTION</span></span>
<span data-ttu-id="14ee1-112">**AzPolicySetDefinition** cmdlet은 이름 또는 ID로 식별 되는 특정 정책 집합 정의 또는 정책 집합 정의의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="14ee1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="14ee1-113">EXAMPLES</span></span>

### <span data-ttu-id="14ee1-114">예제 1: 모든 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="14ee1-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="14ee1-115">이 명령은 모든 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="14ee1-116">예제 2: 이름으로 현재 구독에서 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="14ee1-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="14ee1-117">이 명령은 현재 기본 구독에서 VMPolicySetDefinition 이라는 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="14ee1-118">예제 3: 이름으로 구독에서 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="14ee1-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="14ee1-119">이 명령은 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 인 구독에서 VMPolicySetDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="14ee1-120">예제 4: 관리 그룹에서 모든 사용자 지정 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="14ee1-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="14ee1-121">이 명령은 Dept42 이라는 관리 그룹에서 모든 사용자 지정 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="14ee1-122">예제 5: 지정 된 범주에서 정책 집합 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="14ee1-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="14ee1-123">이 명령은 "가상 컴퓨터" 범주에 있는 모든 정책 집합 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="14ee1-124">변수</span><span class="sxs-lookup"><span data-stu-id="14ee1-124">PARAMETERS</span></span>

### <span data-ttu-id="14ee1-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="14ee1-125">-ApiVersion</span></span>
<span data-ttu-id="14ee1-126">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="14ee1-127">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="14ee1-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="14ee1-128">-Builtin</span></span>
<span data-ttu-id="14ee1-129">결과 목록을 기본 제공 정책 집합 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="14ee1-130">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="14ee1-130">-Custom</span></span>
<span data-ttu-id="14ee1-131">결과 목록을 사용자 지정 정책 집합 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="14ee1-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ee1-132">-DefaultProfile</span></span>
<span data-ttu-id="14ee1-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="14ee1-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14ee1-134">-Id</span><span class="sxs-lookup"><span data-stu-id="14ee1-134">-Id</span></span>
<span data-ttu-id="14ee1-135">구독을 포함 하는 정규화 된 정책 집합 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="14ee1-136">예:/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="14ee1-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="14ee1-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="14ee1-137">-ManagementGroupName</span></span>
<span data-ttu-id="14ee1-138">가져올 정책 집합 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="14ee1-139">-이름</span><span class="sxs-lookup"><span data-stu-id="14ee1-139">-Name</span></span>
<span data-ttu-id="14ee1-140">정책 집합 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="14ee1-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="14ee1-141">-Pre</span></span>
<span data-ttu-id="14ee1-142">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="14ee1-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14ee1-143">-SubscriptionId</span></span>
<span data-ttu-id="14ee1-144">가져올 정책 집합 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="14ee1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ee1-145">CommonParameters</span></span>
<span data-ttu-id="14ee1-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="14ee1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ee1-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="14ee1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ee1-148">입력</span><span class="sxs-lookup"><span data-stu-id="14ee1-148">INPUTS</span></span>

### <span data-ttu-id="14ee1-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="14ee1-149">System.String</span></span>

### <span data-ttu-id="14ee1-150">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="14ee1-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="14ee1-151">출력</span><span class="sxs-lookup"><span data-stu-id="14ee1-151">OUTPUTS</span></span>

### <span data-ttu-id="14ee1-152">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="14ee1-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="14ee1-153">상속자</span><span class="sxs-lookup"><span data-stu-id="14ee1-153">NOTES</span></span>

## <span data-ttu-id="14ee1-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14ee1-154">RELATED LINKS</span></span>
