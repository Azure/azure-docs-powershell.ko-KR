---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyDefinition.md
ms.openlocfilehash: f932e566d9fe6639e19e4f906775282cd17315d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873297"
---
# <span data-ttu-id="8da88-101">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8da88-101">Remove-AzPolicyDefinition</span></span>

## <span data-ttu-id="8da88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da88-102">SYNOPSIS</span></span>
<span data-ttu-id="8da88-103">정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-103">Removes a policy definition.</span></span>

## <span data-ttu-id="8da88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8da88-104">SYNTAX</span></span>

### <span data-ttu-id="8da88-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8da88-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da88-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da88-106">ManagementGroupNameParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da88-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da88-107">SubscriptionIdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Name <String> [-Force] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da88-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8da88-108">IdParameterSet</span></span>
```
Remove-AzPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da88-109">설명은</span><span class="sxs-lookup"><span data-stu-id="8da88-109">DESCRIPTION</span></span>
<span data-ttu-id="8da88-110">**제거-AzPolicyDefinition** cmdlet은 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-110">The **Remove-AzPolicyDefinition** cmdlet removes a policy definition.</span></span>

## <span data-ttu-id="8da88-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8da88-111">EXAMPLES</span></span>

### <span data-ttu-id="8da88-112">예제 1: 이름으로 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="8da88-112">Example 1: Remove the policy definition by name</span></span>
```
PS C:\> Remove-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="8da88-113">이 명령은 지정 된 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-113">This command removes the specified policy definition.</span></span>

### <span data-ttu-id="8da88-114">예제 2: 리소스 ID 별 정책 정의 제거</span><span class="sxs-lookup"><span data-stu-id="8da88-114">Example 2: Remove policy definition by resource ID</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition' 
PS C:\> Remove-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

<span data-ttu-id="8da88-115">첫 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VMPolicyDefinition 이라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-115">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8da88-116">명령이 $PolicyDefinition 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-116">The command stores it in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="8da88-117">두 번째 명령은 $PolicyDefinition의 **ResourceId** 속성으로 식별 되는 정책 정의를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-117">The second command removes the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

## <span data-ttu-id="8da88-118">변수</span><span class="sxs-lookup"><span data-stu-id="8da88-118">PARAMETERS</span></span>

### <span data-ttu-id="8da88-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8da88-119">-ApiVersion</span></span>
<span data-ttu-id="8da88-120">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8da88-121">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8da88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da88-122">-DefaultProfile</span></span>
<span data-ttu-id="8da88-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8da88-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da88-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8da88-124">-Force</span></span>
<span data-ttu-id="8da88-125">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8da88-126">-Id</span><span class="sxs-lookup"><span data-stu-id="8da88-126">-Id</span></span>
<span data-ttu-id="8da88-127">이 cmdlet이 제거 하는 정책 정의에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-127">Specifies the fully qualified resource ID for the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8da88-128">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8da88-128">-ManagementGroupName</span></span>
<span data-ttu-id="8da88-129">삭제할 정책 정의의 관리 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-129">The name of the management group of the policy definition to delete.</span></span>

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

### <span data-ttu-id="8da88-130">-이름</span><span class="sxs-lookup"><span data-stu-id="8da88-130">-Name</span></span>
<span data-ttu-id="8da88-131">이 cmdlet이 제거 하는 정책 정의의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-131">Specifies the name of the policy definition that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8da88-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="8da88-132">-Pre</span></span>
<span data-ttu-id="8da88-133">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-133">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8da88-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8da88-134">-SubscriptionId</span></span>
<span data-ttu-id="8da88-135">삭제할 정책 정의의 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-135">The subscription ID of the policy definition to delete.</span></span>

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

### <span data-ttu-id="8da88-136">-확인</span><span class="sxs-lookup"><span data-stu-id="8da88-136">-Confirm</span></span>
<span data-ttu-id="8da88-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8da88-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da88-138">-WhatIf</span></span>
<span data-ttu-id="8da88-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da88-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8da88-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da88-141">CommonParameters</span></span>
<span data-ttu-id="8da88-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8da88-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da88-143">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8da88-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da88-144">입력</span><span class="sxs-lookup"><span data-stu-id="8da88-144">INPUTS</span></span>

### <span data-ttu-id="8da88-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8da88-145">System.String</span></span>

### <span data-ttu-id="8da88-146">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8da88-146">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8da88-147">출력</span><span class="sxs-lookup"><span data-stu-id="8da88-147">OUTPUTS</span></span>

### <span data-ttu-id="8da88-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8da88-148">System.Boolean</span></span>

## <span data-ttu-id="8da88-149">상속자</span><span class="sxs-lookup"><span data-stu-id="8da88-149">NOTES</span></span>

## <span data-ttu-id="8da88-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8da88-150">RELATED LINKS</span></span>

[<span data-ttu-id="8da88-151">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8da88-151">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8da88-152">새로운 AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8da88-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8da88-153">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8da88-153">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


