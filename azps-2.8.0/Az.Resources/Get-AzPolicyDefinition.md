---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: f799c22edb3bb6c09102575a05be53b21e28c3d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871845"
---
# <span data-ttu-id="9b46f-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b46f-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="9b46f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b46f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b46f-103">정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-103">Gets policy definitions.</span></span>

## <span data-ttu-id="9b46f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b46f-104">SYNTAX</span></span>

### <span data-ttu-id="9b46f-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b46f-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b46f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b46f-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b46f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b46f-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b46f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b46f-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b46f-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b46f-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b46f-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b46f-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b46f-111">설명은</span><span class="sxs-lookup"><span data-stu-id="9b46f-111">DESCRIPTION</span></span>
<span data-ttu-id="9b46f-112">**AzPolicyDefinition** cmdlet은 정책 정의의 컬렉션이 나 이름 또는 ID로 식별 되는 특정 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="9b46f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="9b46f-113">EXAMPLES</span></span>

### <span data-ttu-id="9b46f-114">예제 1: 모든 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b46f-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="9b46f-115">이 명령은 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="9b46f-116">예제 2: 이름으로 현재 구독에서 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b46f-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="9b46f-117">이 명령은 현재 기본 구독에서 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="9b46f-118">예제 3: 관리 그룹에서 이름별로 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b46f-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="9b46f-119">이 명령은 Dept42 이라는 관리 그룹에서 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="9b46f-120">예제 4: 구독에서 모든 기본 제공 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b46f-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="9b46f-121">이 명령은 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 구독에서 기본 제공 된 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="9b46f-122">예제 5: 지정 된 범주에서 정책 정의 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b46f-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="9b46f-123">이 명령은 범주 "가상 컴퓨터"의 모든 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="9b46f-124">변수</span><span class="sxs-lookup"><span data-stu-id="9b46f-124">PARAMETERS</span></span>

### <span data-ttu-id="9b46f-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9b46f-125">-ApiVersion</span></span>
<span data-ttu-id="9b46f-126">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9b46f-127">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9b46f-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="9b46f-128">-Builtin</span></span>
<span data-ttu-id="9b46f-129">결과 목록을 기본 제공 정책 정의로 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="9b46f-130">-사용자 지정</span><span class="sxs-lookup"><span data-stu-id="9b46f-130">-Custom</span></span>
<span data-ttu-id="9b46f-131">결과 목록을 사용자 지정 정책 정의로만 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="9b46f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b46f-132">-DefaultProfile</span></span>
<span data-ttu-id="9b46f-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9b46f-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b46f-134">-Id</span><span class="sxs-lookup"><span data-stu-id="9b46f-134">-Id</span></span>
<span data-ttu-id="9b46f-135">이 cmdlet이 가져오는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9b46f-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="9b46f-136">-ManagementGroupName</span></span>
<span data-ttu-id="9b46f-137">가져올 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="9b46f-138">-이름</span><span class="sxs-lookup"><span data-stu-id="9b46f-138">-Name</span></span>
<span data-ttu-id="9b46f-139">이 cmdlet이 가져오는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9b46f-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="9b46f-140">-Pre</span></span>
<span data-ttu-id="9b46f-141">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9b46f-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b46f-142">-SubscriptionId</span></span>
<span data-ttu-id="9b46f-143">가져올 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="9b46f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b46f-144">CommonParameters</span></span>
<span data-ttu-id="9b46f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b46f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b46f-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b46f-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b46f-147">입력</span><span class="sxs-lookup"><span data-stu-id="9b46f-147">INPUTS</span></span>

### <span data-ttu-id="9b46f-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b46f-148">System.String</span></span>

### <span data-ttu-id="9b46f-149">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9b46f-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9b46f-150">출력</span><span class="sxs-lookup"><span data-stu-id="9b46f-150">OUTPUTS</span></span>

### <span data-ttu-id="9b46f-151">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="9b46f-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9b46f-152">상속자</span><span class="sxs-lookup"><span data-stu-id="9b46f-152">NOTES</span></span>

## <span data-ttu-id="9b46f-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b46f-153">RELATED LINKS</span></span>

[<span data-ttu-id="9b46f-154">새로운 AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b46f-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="9b46f-155">제거-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b46f-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="9b46f-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9b46f-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


