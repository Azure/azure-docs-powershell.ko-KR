---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFireWallPolicy.md
ms.openlocfilehash: b18f17830dd08f95c3d887ce272ff31e080001a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536656"
---
# <span data-ttu-id="0211d-101">New-AzureRmFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="0211d-101">New-AzureRmFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="0211d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0211d-102">SYNOPSIS</span></span>
<span data-ttu-id="0211d-103">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0211d-103">Create WAF policy</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0211d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0211d-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <PSMode>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0211d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0211d-105">DESCRIPTION</span></span>
<span data-ttu-id="0211d-106">**AzureRmFrontDoorFireWallPolicy** cmdlet은 현재 구독 아래의 지정 된 리소스 그룹에 새 AZURE waf 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-106">The **New-AzureRmFrontDoorFireWallPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="0211d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0211d-107">EXAMPLES</span></span>

### <span data-ttu-id="0211d-108">예제 1: WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0211d-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorFireWallPolicy -Name $Name -ResourceGroupName $resourceGroupName -Customrule $customRule1 -ManagedRule $managedRule1 -En
abledState Enabled -Mode Prevention


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

<span data-ttu-id="0211d-109">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0211d-109">Create WAF policy</span></span>

## <span data-ttu-id="0211d-110">변수</span><span class="sxs-lookup"><span data-stu-id="0211d-110">PARAMETERS</span></span>

### <span data-ttu-id="0211d-111">-Customrule</span><span class="sxs-lookup"><span data-stu-id="0211d-111">-Customrule</span></span>
<span data-ttu-id="0211d-112">정책 내의 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="0211d-112">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="0211d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0211d-113">-DefaultProfile</span></span>
<span data-ttu-id="0211d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0211d-115">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0211d-115">-EnabledState</span></span>
<span data-ttu-id="0211d-116">정책이 사용 상태로 설정 되어 있는지 또는 사용 안 함 상태 인지 여부</span><span class="sxs-lookup"><span data-stu-id="0211d-116">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="0211d-117">사용할 수 있는 값은 다음과 같습니다. ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="0211d-117">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="0211d-118">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0211d-118">-ManagedRule</span></span>
<span data-ttu-id="0211d-119">정책 내 관리 규칙</span><span class="sxs-lookup"><span data-stu-id="0211d-119">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="0211d-120">-모드</span><span class="sxs-lookup"><span data-stu-id="0211d-120">-Mode</span></span>
<span data-ttu-id="0211d-121">정책 수준의 검색 모드 또는 방지 모드에 있는 경우에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-121">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="0211d-122">사용할 수 있는 값은 다음과 같습니다. ' 예방 ', ' 감지 '</span><span class="sxs-lookup"><span data-stu-id="0211d-122">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="0211d-123">-이름</span><span class="sxs-lookup"><span data-stu-id="0211d-123">-Name</span></span>
<span data-ttu-id="0211d-124">WebApplicationFireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-124">WebApplicationFireWallPolicy name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0211d-125">-ResourceGroupName</span></span>
<span data-ttu-id="0211d-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0211d-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0211d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="0211d-127">-Confirm</span></span>
<span data-ttu-id="0211d-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0211d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0211d-129">-WhatIf</span></span>
<span data-ttu-id="0211d-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0211d-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0211d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0211d-132">CommonParameters</span></span>
<span data-ttu-id="0211d-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0211d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0211d-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0211d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0211d-135">입력</span><span class="sxs-lookup"><span data-stu-id="0211d-135">INPUTS</span></span>

### <span data-ttu-id="0211d-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0211d-136">System.String</span></span>

## <span data-ttu-id="0211d-137">출력</span><span class="sxs-lookup"><span data-stu-id="0211d-137">OUTPUTS</span></span>

### <span data-ttu-id="0211d-138">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="0211d-138">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="0211d-139">상속자</span><span class="sxs-lookup"><span data-stu-id="0211d-139">NOTES</span></span>

## <span data-ttu-id="0211d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0211d-140">RELATED LINKS</span></span>

<span data-ttu-id="0211d-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md) 
 [Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md) 
 [제거-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md) 
 [새로운 AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md) 
 [새로운 AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="0211d-141">[Set-AzureRmFrontDoorFireWallPolicy](./Set-AzureRmFrontDoorFireWallPolicy.md)
[Get-AzureRmFrontDoorFireWallPolicy](./Get-AzureRmFrontDoorFireWallPolicy.md)
[Remove-AzureRmFrontDoorFireWallPolicy](./Remove-AzureRmFrontDoorFireWallPolicy.md)
[New-AzureRmFrontDoorManagedRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)
[New-AzureRmFrontDoorCustomRuleObject](./New-AzureRmFrontDoorManagedRuleObject.md)</span></span>
