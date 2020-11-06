---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 36399302-3EA5-45A3-A042-536CC7EC2E6D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyAssignment.md
ms.openlocfilehash: d78cf9d28c453626c26656b9f9280f5c52695434
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529722"
---
# <span data-ttu-id="545d7-101">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="545d7-101">Remove-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="545d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545d7-102">SYNOPSIS</span></span>
<span data-ttu-id="545d7-103">정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-103">Removes a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="545d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="545d7-104">SYNTAX</span></span>

### <span data-ttu-id="545d7-105">RemoveByPolicyAssignmentName (기본값)</span><span class="sxs-lookup"><span data-stu-id="545d7-105">RemoveByPolicyAssignmentName (Default)</span></span>
```
Remove-AzureRmPolicyAssignment -Name <String> -Scope <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545d7-106">RemoveByPolicyAssignmentId</span><span class="sxs-lookup"><span data-stu-id="545d7-106">RemoveByPolicyAssignmentId</span></span>
```
Remove-AzureRmPolicyAssignment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545d7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="545d7-107">DESCRIPTION</span></span>
<span data-ttu-id="545d7-108">**AzureRmPolicyAssignment** cmdlet은 지정 된 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-108">The **Remove-AzureRmPolicyAssignment** cmdlet removes the specified policy assignment.</span></span>

## <span data-ttu-id="545d7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="545d7-109">EXAMPLES</span></span>

### <span data-ttu-id="545d7-110">예제 1: 이름 및 범위로 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="545d7-110">Example 1: Remove policy assignment by name and scope</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> Remove-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId -Force
```

<span data-ttu-id="545d7-111">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-111">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="545d7-112">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-112">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="545d7-113">두 번째 명령은 리소스 그룹 수준에서 할당 된 PolicyAssignment07 라는 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-113">The second command removes the policy assignment named PolicyAssignment07 that was assigned at a resource group level.</span></span>
<span data-ttu-id="545d7-114">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-114">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="545d7-115">예제 2: ID 별 정책 할당 제거</span><span class="sxs-lookup"><span data-stu-id="545d7-115">Example 2: Remove policy assignment by ID</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11" 
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name "PolicyAssignment07" -Scope $ResourceGroup.ResourceId
PS C:\> Remove-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -Force
```

<span data-ttu-id="545d7-116">첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹을 가져온 다음 해당 개체를 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-116">The first command gets a resource group named ResourceGroup11, and then stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="545d7-117">두 번째 명령은 리소스 그룹 수준에서 정책 할당을 가져온 다음 $PolicyAssignment 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-117">The second command gets the policy assignment at a resource group level, and then stores it in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="545d7-118">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-118">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

<span data-ttu-id="545d7-119">마지막 명령은 $PolicyAssignment **ResourceId** 속성이 식별 하는 정책 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-119">The final command removes the policy assignment that the **ResourceId** property of $PolicyAssignment identifies.</span></span>

## <span data-ttu-id="545d7-120">변수</span><span class="sxs-lookup"><span data-stu-id="545d7-120">PARAMETERS</span></span>

### <span data-ttu-id="545d7-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="545d7-121">-ApiVersion</span></span>
<span data-ttu-id="545d7-122">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="545d7-123">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545d7-124">-DefaultProfile</span></span>
<span data-ttu-id="545d7-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="545d7-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-126">-Id</span><span class="sxs-lookup"><span data-stu-id="545d7-126">-Id</span></span>
<span data-ttu-id="545d7-127">이 cmdlet이 제거 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-127">Specifies the fully qualified resource ID for the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="545d7-128">-InformationAction</span></span>
<span data-ttu-id="545d7-129">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="545d7-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="545d7-131">하기로</span><span class="sxs-lookup"><span data-stu-id="545d7-131">Continue</span></span>
- <span data-ttu-id="545d7-132">숨기기</span><span class="sxs-lookup"><span data-stu-id="545d7-132">Ignore</span></span>
- <span data-ttu-id="545d7-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="545d7-133">Inquire</span></span>
- <span data-ttu-id="545d7-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="545d7-134">SilentlyContinue</span></span>
- <span data-ttu-id="545d7-135">중지가</span><span class="sxs-lookup"><span data-stu-id="545d7-135">Stop</span></span>
- <span data-ttu-id="545d7-136">대기</span><span class="sxs-lookup"><span data-stu-id="545d7-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="545d7-137">-InformationVariable</span></span>
<span data-ttu-id="545d7-138">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-139">-이름</span><span class="sxs-lookup"><span data-stu-id="545d7-139">-Name</span></span>
<span data-ttu-id="545d7-140">이 cmdlet이 제거 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-140">Specifies the name of the policy assignment that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="545d7-141">-Pre</span></span>
<span data-ttu-id="545d7-142">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-143">-범위</span><span class="sxs-lookup"><span data-stu-id="545d7-143">-Scope</span></span>
<span data-ttu-id="545d7-144">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-144">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByPolicyAssignmentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-145">-확인</span><span class="sxs-lookup"><span data-stu-id="545d7-145">-Confirm</span></span>
<span data-ttu-id="545d7-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545d7-147">-WhatIf</span></span>
<span data-ttu-id="545d7-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545d7-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="545d7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545d7-150">CommonParameters</span></span>
<span data-ttu-id="545d7-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545d7-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="545d7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545d7-153">입력</span><span class="sxs-lookup"><span data-stu-id="545d7-153">INPUTS</span></span>

### <span data-ttu-id="545d7-154">않아야</span><span class="sxs-lookup"><span data-stu-id="545d7-154">None</span></span>
<span data-ttu-id="545d7-155">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="545d7-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="545d7-156">출력</span><span class="sxs-lookup"><span data-stu-id="545d7-156">OUTPUTS</span></span>

### <span data-ttu-id="545d7-157">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="545d7-157">System.Boolean</span></span>

## <span data-ttu-id="545d7-158">상속자</span><span class="sxs-lookup"><span data-stu-id="545d7-158">NOTES</span></span>

## <span data-ttu-id="545d7-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="545d7-159">RELATED LINKS</span></span>

[<span data-ttu-id="545d7-160">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="545d7-160">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="545d7-161">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="545d7-161">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="545d7-162">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="545d7-162">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


