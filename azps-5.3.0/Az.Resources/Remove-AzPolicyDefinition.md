---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492396"
---
# <span data-ttu-id="00011-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00011-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="00011-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00011-102">SYNOPSIS</span></span>
<span data-ttu-id="00011-103">정책 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-103">Removes a policy definition.</span></span>

## <span data-ttu-id="00011-104">구문</span><span class="sxs-lookup"><span data-stu-id="00011-104">SYNTAX</span></span>

### <span data-ttu-id="00011-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="00011-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00011-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00011-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00011-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00011-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00011-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00011-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00011-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00011-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00011-110">설명</span><span class="sxs-lookup"><span data-stu-id="00011-110">DESCRIPTION</span></span>
<span data-ttu-id="00011-111">**Remove-AzPolicyDefinition** cmdlet은 정책 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="00011-112">예제</span><span class="sxs-lookup"><span data-stu-id="00011-112">EXAMPLES</span></span>

### <span data-ttu-id="00011-113">예제 1: 이름으로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="00011-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="00011-114">이 명령은 지정된 정책 정의를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="00011-115">예제 2: 리소스 ID로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="00011-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="00011-116">첫 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VMPolicyDefinition이라는 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00011-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="00011-117">이 명령은 $PolicyDefinition 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="00011-118">두 번째 명령은 리소스의 **ResourceId** 속성으로 식별되는 정책 정의를 $PolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="00011-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="00011-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00011-119">PARAMETERS</span></span>

### <span data-ttu-id="00011-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="00011-120">-ApiVersion</span></span>
<span data-ttu-id="00011-121">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="00011-122">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="00011-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="00011-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00011-123">-DefaultProfile</span></span>
<span data-ttu-id="00011-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="00011-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00011-125">-Force</span><span class="sxs-lookup"><span data-stu-id="00011-125">-Force</span></span>
<span data-ttu-id="00011-126">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="00011-127">-Id</span><span class="sxs-lookup"><span data-stu-id="00011-127">-Id</span></span>
<span data-ttu-id="00011-128">이 cmdlet이 제거하는 정책 정의에 대한 정식 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00011-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00011-129">-InputObject</span></span>
<span data-ttu-id="00011-130">다른 cmdlet에서 출력된 개체를 제거할 정책 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="00011-130">The policy definition object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00011-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="00011-131">-ManagementGroupName</span></span>
<span data-ttu-id="00011-132">삭제할 정책 정의의 관리 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00011-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="00011-133">-Name</span><span class="sxs-lookup"><span data-stu-id="00011-133">-Name</span></span>
<span data-ttu-id="00011-134">이 cmdlet이 제거하는 정책 정의의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00011-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="00011-135">-Pre</span></span>
<span data-ttu-id="00011-136">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="00011-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="00011-137">-SubscriptionId</span></span>
<span data-ttu-id="00011-138">삭제할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="00011-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="00011-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00011-139">-Confirm</span></span>
<span data-ttu-id="00011-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00011-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00011-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00011-141">-WhatIf</span></span>
<span data-ttu-id="00011-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00011-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00011-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00011-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00011-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00011-144">CommonParameters</span></span>
<span data-ttu-id="00011-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00011-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00011-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00011-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00011-147">입력</span><span class="sxs-lookup"><span data-stu-id="00011-147">INPUTS</span></span>

### <span data-ttu-id="00011-148">System.String</span><span class="sxs-lookup"><span data-stu-id="00011-148">System.String</span></span>

### <span data-ttu-id="00011-149">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00011-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="00011-150">출력</span><span class="sxs-lookup"><span data-stu-id="00011-150">OUTPUTS</span></span>

### <span data-ttu-id="00011-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00011-151">System.Boolean</span></span>

## <span data-ttu-id="00011-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00011-152">NOTES</span></span>

## <span data-ttu-id="00011-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00011-153">RELATED LINKS</span></span>

[<span data-ttu-id="00011-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00011-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="00011-155">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00011-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="00011-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="00011-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


