---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzPolicyAssignment.md
ms.openlocfilehash: 00ec24c13a5c51db7da63cd1d94c01f251a7e289
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204411"
---
# <span data-ttu-id="974b3-101">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="974b3-101">Remove-AzPolicyAssignment</span></span>

## <span data-ttu-id="974b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="974b3-102">SYNOPSIS</span></span>
<span data-ttu-id="974b3-103">정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-103">Removes a policy assignment.</span></span>

## <span data-ttu-id="974b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="974b3-104">SYNTAX</span></span>

### <span data-ttu-id="974b3-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="974b3-105">NameParameterSet (Default)</span></span>
```
Remove-AzPolicyAssignment -Name <String> [-Scope <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974b3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="974b3-106">IdParameterSet</span></span>
```
Remove-AzPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="974b3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="974b3-107">InputObjectParameterSet</span></span>
```
Remove-AzPolicyAssignment -InputObject <PsPolicyAssignment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="974b3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="974b3-108">DESCRIPTION</span></span>
<span data-ttu-id="974b3-109">**AzPolicyAssignment** cmdlet은 지정 된 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-109">The **Remove-AzPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="974b3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="974b3-110">EXAMPLES</span></span>

### <span data-ttu-id="974b3-111">예제 1: 이름 및 범위로 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="974b3-111">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Remove-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId -Confirm
```

<span data-ttu-id="974b3-112">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="974b3-113">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="974b3-114">두 번째 명령은 리소스 그룹 수준에서 할당 된 PolicyAssignment07 라는 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-114">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="974b3-115">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-115">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="974b3-116">예제 2: ID 별 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="974b3-116">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11' 
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -Confirm
```

<span data-ttu-id="974b3-117">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹을 가져온 다음 해당 개체를 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-117">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="974b3-118">두 번째 명령은 리소스 그룹 수준에서 정책 할당을 가져온 다음 $PolicyAssignment 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-118">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="974b3-119">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-119">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>
<span data-ttu-id="974b3-120">마지막 명령은 $PolicyAssignment **ResourceId** 속성이 식별 하는 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-120">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="974b3-121">변수</span><span class="sxs-lookup"><span data-stu-id="974b3-121">PARAMETERS</span></span>

### <span data-ttu-id="974b3-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="974b3-122">-ApiVersion</span></span>
<span data-ttu-id="974b3-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="974b3-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="974b3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="974b3-125">-DefaultProfile</span></span>
<span data-ttu-id="974b3-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="974b3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="974b3-127">-Id</span><span class="sxs-lookup"><span data-stu-id="974b3-127">-Id</span></span>
<span data-ttu-id="974b3-128">이 cmdlet이 제거 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="974b3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="974b3-129">-InputObject</span></span>
<span data-ttu-id="974b3-130">다른 cmdlet에서 출력 된 제거할 정책 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-130">The policy assignment object to remove that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="974b3-131">-이름</span><span class="sxs-lookup"><span data-stu-id="974b3-131">-Name</span></span>
<span data-ttu-id="974b3-132">이 cmdlet이 제거 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-132">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

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

### <span data-ttu-id="974b3-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="974b3-133">-Pre</span></span>
<span data-ttu-id="974b3-134">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="974b3-135">-범위</span><span class="sxs-lookup"><span data-stu-id="974b3-135">-Scope</span></span>
<span data-ttu-id="974b3-136">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-136">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="974b3-137">-확인</span><span class="sxs-lookup"><span data-stu-id="974b3-137">-Confirm</span></span>
<span data-ttu-id="974b3-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="974b3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="974b3-139">-WhatIf</span></span>
<span data-ttu-id="974b3-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="974b3-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="974b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="974b3-142">CommonParameters</span></span>
<span data-ttu-id="974b3-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="974b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="974b3-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="974b3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="974b3-145">입력</span><span class="sxs-lookup"><span data-stu-id="974b3-145">INPUTS</span></span>

### <span data-ttu-id="974b3-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="974b3-146">System.String</span></span>

## <span data-ttu-id="974b3-147">출력</span><span class="sxs-lookup"><span data-stu-id="974b3-147">OUTPUTS</span></span>

### <span data-ttu-id="974b3-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="974b3-148">System.Boolean</span></span>

## <span data-ttu-id="974b3-149">상속자</span><span class="sxs-lookup"><span data-stu-id="974b3-149">NOTES</span></span>

## <span data-ttu-id="974b3-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="974b3-150">RELATED LINKS</span></span>

[<span data-ttu-id="974b3-151">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="974b3-151">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="974b3-152">새로운 AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="974b3-152">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="974b3-153">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="974b3-153">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


