---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332114"
---
# <span data-ttu-id="e5255-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5255-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="e5255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5255-102">SYNOPSIS</span></span>
<span data-ttu-id="e5255-103">정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-103">Gets policy definitions.</span></span>

## <span data-ttu-id="e5255-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5255-104">SYNTAX</span></span>

### <span data-ttu-id="e5255-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e5255-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5255-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5255-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5255-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5255-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5255-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5255-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5255-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5255-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5255-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5255-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5255-111">설명</span><span class="sxs-lookup"><span data-stu-id="e5255-111">DESCRIPTION</span></span>
<span data-ttu-id="e5255-112">**Get-AzPolicyDefinition** cmdlet은 이름 또는 ID로 식별된 정책 정의 또는 특정 정책 정의의 컬렉션을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="e5255-113">예제</span><span class="sxs-lookup"><span data-stu-id="e5255-113">EXAMPLES</span></span>

### <span data-ttu-id="e5255-114">예제 1: 모든 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="e5255-115">이 명령은 모든 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="e5255-116">예제 2: 이름에 따라 현재 구독에서 정책 정의를 얻게</span><span class="sxs-lookup"><span data-stu-id="e5255-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="e5255-117">이 명령은 현재 기본 구독에서 VMPolicyDefinition이라는 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="e5255-118">예제 3: 이름에 따라 관리 그룹에서 정책 정의를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="e5255-119">이 명령은 Dept42라는 관리 그룹에서 VMPolicyDefinition이라는 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="e5255-120">예제 4: 구독에서 모든 기본 제공 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="e5255-121">이 명령은 ID가 3bf44b72-c631-427a-b8c8-53e2595398ca인 구독에서 모든 기본 제공 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="e5255-122">예제 5: 주어진 범주에서 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="e5255-123">이 명령은 "Virtual Machine" 범주의 모든 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="e5255-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5255-124">PARAMETERS</span></span>

### <span data-ttu-id="e5255-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e5255-125">-ApiVersion</span></span>
<span data-ttu-id="e5255-126">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e5255-127">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e5255-128">-Builtin</span><span class="sxs-lookup"><span data-stu-id="e5255-128">-Builtin</span></span>
<span data-ttu-id="e5255-129">결과 목록을 기본 제공 정책 정의로만 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="e5255-130">-Custom</span><span class="sxs-lookup"><span data-stu-id="e5255-130">-Custom</span></span>
<span data-ttu-id="e5255-131">결과 목록을 사용자 지정 정책 정의로만 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="e5255-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5255-132">-DefaultProfile</span></span>
<span data-ttu-id="e5255-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e5255-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5255-134">-Id</span><span class="sxs-lookup"><span data-stu-id="e5255-134">-Id</span></span>
<span data-ttu-id="e5255-135">이 cmdlet에서 얻을 정책 정의에 대한 정식 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e5255-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e5255-136">-ManagementGroupName</span></span>
<span data-ttu-id="e5255-137">얻을 정책 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="e5255-138">-Name</span><span class="sxs-lookup"><span data-stu-id="e5255-138">-Name</span></span>
<span data-ttu-id="e5255-139">이 cmdlet에서 얻을 정책 정의의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e5255-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e5255-140">-Pre</span></span>
<span data-ttu-id="e5255-141">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e5255-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e5255-142">-SubscriptionId</span></span>
<span data-ttu-id="e5255-143">얻을 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="e5255-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5255-144">CommonParameters</span></span>
<span data-ttu-id="e5255-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5255-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5255-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5255-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5255-147">입력</span><span class="sxs-lookup"><span data-stu-id="e5255-147">INPUTS</span></span>

### <span data-ttu-id="e5255-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e5255-148">System.String</span></span>

### <span data-ttu-id="e5255-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e5255-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e5255-150">출력</span><span class="sxs-lookup"><span data-stu-id="e5255-150">OUTPUTS</span></span>

### <span data-ttu-id="e5255-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e5255-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e5255-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5255-152">NOTES</span></span>

## <span data-ttu-id="e5255-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5255-153">RELATED LINKS</span></span>

[<span data-ttu-id="e5255-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5255-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="e5255-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5255-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="e5255-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e5255-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


