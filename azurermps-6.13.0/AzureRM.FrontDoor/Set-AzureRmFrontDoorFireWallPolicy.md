---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: a02510cc72b9e674f9d4fded1355ae5b2cadc807
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93701968"
---
# <span data-ttu-id="06a24-101">Set-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="06a24-101">Set-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="06a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a24-102">SYNOPSIS</span></span>
<span data-ttu-id="06a24-103">WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-103">update WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06a24-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06a24-104">SYNTAX</span></span>

### <span data-ttu-id="06a24-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="06a24-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a24-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06a24-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06a24-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06a24-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoorFireWallPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <PSMode>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a24-108">설명은</span><span class="sxs-lookup"><span data-stu-id="06a24-108">DESCRIPTION</span></span>
<span data-ttu-id="06a24-109">**AzureRmFrontDoor** cmdlet은 기존 waf 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-109">The **Set-AzureRmFrontDoor** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="06a24-110">입력 매개 변수를 제공 하지 않으면 기존 WAF 정책의 이전 매개 변수가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="06a24-111">예제의</span><span class="sxs-lookup"><span data-stu-id="06a24-111">EXAMPLES</span></span>

### <span data-ttu-id="06a24-112">예제 1: 기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-112">Example 1: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -Name $name -ResourceGroupName $resourceGroup -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $node

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="06a24-113">기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-113">update an existing WAF policy</span></span>

### <span data-ttu-id="06a24-114">예제 2: 기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-114">Example 2: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -InputObject $policy1 -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="06a24-115">기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-115">update an existing WAF policy</span></span>

### <span data-ttu-id="06a24-116">예제 3: 기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-116">Example 3: update an existing WAF policy</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoorFireWallPolicy -ResourceId $resourcdId -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode

PolicyMode         : Prevention
PolicyEnabledState : Enabled
CustomRules        : {Rule1}
ManagedRules       : {Microsoft.Azure.Commands.FrontDoor.Models.PSAzureManagedRule}
Etag               :
ProvisioningState  : Succeeded
Tags               :
Id                 : /subscriptions/{subid}/resourcegroups/{resourceGroupName}/providers/Micr
                     osoft.Network/frontdoorwebapplicationfirewallpolicies/{Name}
Name               : {Name}
Type               :
```

<span data-ttu-id="06a24-117">기존 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-117">update an existing WAF policy</span></span>

### <span data-ttu-id="06a24-118">예제 4: $resourceGroup에서 모든 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-118">Example 4: update all WAF policies in $resourceGroup</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoorFireWallPolicy -ResourceGroupName $resourceGroup | Set-AzureRmFrontDoorFireWallPolicy -Customrule $customRule -ManagedRule $managedRule -EnabledState $enabledState -Mode $mode
```

<span data-ttu-id="06a24-119">$resourceGroup의 모든 WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="06a24-119">update all WAF policies in $resourceGroup</span></span>

## <span data-ttu-id="06a24-120">변수</span><span class="sxs-lookup"><span data-stu-id="06a24-120">PARAMETERS</span></span>

### <span data-ttu-id="06a24-121">-Customrule</span><span class="sxs-lookup"><span data-stu-id="06a24-121">-Customrule</span></span>
<span data-ttu-id="06a24-122">정책 내의 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="06a24-122">Custom rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a24-123">-DefaultProfile</span></span>
<span data-ttu-id="06a24-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-125">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="06a24-125">-EnabledState</span></span>
<span data-ttu-id="06a24-126">정책이 사용 상태로 설정 되어 있는지 또는 사용 안 함 상태 인지 여부</span><span class="sxs-lookup"><span data-stu-id="06a24-126">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="06a24-127">사용할 수 있는 값은 다음과 같습니다. ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="06a24-127">Possible values include: 'Disabled', 'Enabled'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06a24-128">-InputObject</span></span>
<span data-ttu-id="06a24-129">업데이트할 FireWallPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-129">The FireWallPolicy object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-130">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="06a24-130">-ManagedRule</span></span>
<span data-ttu-id="06a24-131">정책 내 관리 규칙</span><span class="sxs-lookup"><span data-stu-id="06a24-131">Managed rules inside the policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSManagedRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-132">-모드</span><span class="sxs-lookup"><span data-stu-id="06a24-132">-Mode</span></span>
<span data-ttu-id="06a24-133">정책 수준의 검색 모드 또는 방지 모드에 있는 경우에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-133">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="06a24-134">사용할 수 있는 값은 다음과 같습니다. ' 예방 ', ' 감지 '</span><span class="sxs-lookup"><span data-stu-id="06a24-134">Possible values include:'Prevention', 'Detection'</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSMode
Parameter Sets: (All)
Aliases:
Accepted values: Prevention, Detection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-135">-이름</span><span class="sxs-lookup"><span data-stu-id="06a24-135">-Name</span></span>
<span data-ttu-id="06a24-136">업데이트할 FireWallPolicy의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-136">The name of the FireWallPolicy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a24-137">-ResourceGroupName</span></span>
<span data-ttu-id="06a24-138">FireWallPolicy 속해 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-138">The resource group to which the FireWallPolicy belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06a24-139">-ResourceId</span></span>
<span data-ttu-id="06a24-140">업데이트할 FireWallPolicy의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-140">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-141">-확인</span><span class="sxs-lookup"><span data-stu-id="06a24-141">-Confirm</span></span>
<span data-ttu-id="06a24-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a24-143">-WhatIf</span></span>
<span data-ttu-id="06a24-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a24-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06a24-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a24-146">CommonParameters</span></span>
<span data-ttu-id="06a24-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06a24-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a24-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a24-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a24-149">입력</span><span class="sxs-lookup"><span data-stu-id="06a24-149">INPUTS</span></span>

### <span data-ttu-id="06a24-150">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="06a24-150">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="06a24-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="06a24-151">System.String</span></span>

## <span data-ttu-id="06a24-152">출력</span><span class="sxs-lookup"><span data-stu-id="06a24-152">OUTPUTS</span></span>

### <span data-ttu-id="06a24-153">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="06a24-153">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="06a24-154">상속자</span><span class="sxs-lookup"><span data-stu-id="06a24-154">NOTES</span></span>

## <span data-ttu-id="06a24-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06a24-155">RELATED LINKS</span></span>

<span data-ttu-id="06a24-156">[새로운 AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [새로운 AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [새로운 AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="06a24-156">[New-AzureRmFrontDoorFireWallPolicy](./New-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
