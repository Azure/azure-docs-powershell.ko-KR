---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: c7d292a983090d8be22e159fbca6e423778b21f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204410"
---
# <span data-ttu-id="679c7-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="679c7-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="679c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679c7-102">SYNOPSIS</span></span>
<span data-ttu-id="679c7-103">정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-103">Removes a policy definition.</span></span>

## <span data-ttu-id="679c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="679c7-104">SYNTAX</span></span>

### <span data-ttu-id="679c7-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="679c7-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679c7-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="679c7-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679c7-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="679c7-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679c7-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="679c7-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="679c7-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="679c7-109">InputObjectParameterSet</span></span>
```
Remove-AzPolicyDefinition [-Force] -InputObject <PsPolicyDefinition> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679c7-110">설명은</span><span class="sxs-lookup"><span data-stu-id="679c7-110">DESCRIPTION</span></span>
<span data-ttu-id="679c7-111">**제거-AzPolicyDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-111">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="679c7-112">예제의</span><span class="sxs-lookup"><span data-stu-id="679c7-112">EXAMPLES</span></span>

### <span data-ttu-id="679c7-113">예제 1: 이름으로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="679c7-113">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="679c7-114">이 명령은 지정 된 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-114">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="679c7-115">예제 2: 리소스 ID 별 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="679c7-115">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="679c7-116">첫 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-116">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="679c7-117">명령이 $PolicyDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-117">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="679c7-118">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-118">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="679c7-119">변수</span><span class="sxs-lookup"><span data-stu-id="679c7-119">PARAMETERS</span></span>

### <span data-ttu-id="679c7-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="679c7-120">-ApiVersion</span></span>
<span data-ttu-id="679c7-121">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="679c7-122">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-122">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="679c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679c7-123">-DefaultProfile</span></span>
<span data-ttu-id="679c7-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="679c7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="679c7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="679c7-125">-Force</span></span>
<span data-ttu-id="679c7-126">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="679c7-127">-Id</span><span class="sxs-lookup"><span data-stu-id="679c7-127">-Id</span></span>
<span data-ttu-id="679c7-128">이 cmdlet이 제거 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-128">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="679c7-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679c7-129">-InputObject</span></span>
<span data-ttu-id="679c7-130">다른 cmdlet에서 출력 된 제거할 정책 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-130">The policy definition object to remove that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="679c7-131">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="679c7-131">-ManagementGroupName</span></span>
<span data-ttu-id="679c7-132">삭제할 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-132">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="679c7-133">-이름</span><span class="sxs-lookup"><span data-stu-id="679c7-133">-Name</span></span>
<span data-ttu-id="679c7-134">이 cmdlet이 제거 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-134">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="679c7-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="679c7-135">-Pre</span></span>
<span data-ttu-id="679c7-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="679c7-137">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="679c7-137">-SubscriptionId</span></span>
<span data-ttu-id="679c7-138">삭제할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-138">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="679c7-139">-확인</span><span class="sxs-lookup"><span data-stu-id="679c7-139">-Confirm</span></span>
<span data-ttu-id="679c7-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679c7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679c7-141">-WhatIf</span></span>
<span data-ttu-id="679c7-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679c7-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679c7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679c7-144">CommonParameters</span></span>
<span data-ttu-id="679c7-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="679c7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679c7-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="679c7-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679c7-147">입력</span><span class="sxs-lookup"><span data-stu-id="679c7-147">INPUTS</span></span>

### <span data-ttu-id="679c7-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="679c7-148">System.String</span></span>

### <span data-ttu-id="679c7-149">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="679c7-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="679c7-150">출력</span><span class="sxs-lookup"><span data-stu-id="679c7-150">OUTPUTS</span></span>

### <span data-ttu-id="679c7-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="679c7-151">System.Boolean</span></span>

## <span data-ttu-id="679c7-152">상속자</span><span class="sxs-lookup"><span data-stu-id="679c7-152">NOTES</span></span>

## <span data-ttu-id="679c7-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="679c7-153">RELATED LINKS</span></span>

[<span data-ttu-id="679c7-154">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="679c7-154">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="679c7-155">새로운 AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="679c7-155">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="679c7-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="679c7-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


