---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332241"
---
# <span data-ttu-id="cf463-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="cf463-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="cf463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf463-102">SYNOPSIS</span></span>
<span data-ttu-id="cf463-103">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cf463-103">Create WAF policy</span></span>

## <span data-ttu-id="cf463-104">구문</span><span class="sxs-lookup"><span data-stu-id="cf463-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf463-105">설명</span><span class="sxs-lookup"><span data-stu-id="cf463-105">DESCRIPTION</span></span>
<span data-ttu-id="cf463-106">**New-AzFrontDoorWafPolicy** cmdlet은 현재 구독의 지정된 리소스 그룹에 새 Azure WAF 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="cf463-107">예제</span><span class="sxs-lookup"><span data-stu-id="cf463-107">EXAMPLES</span></span>

### <span data-ttu-id="cf463-108">예제 1: WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cf463-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="cf463-109">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="cf463-109">Create WAF policy</span></span>

## <span data-ttu-id="cf463-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf463-110">PARAMETERS</span></span>

### <span data-ttu-id="cf463-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="cf463-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="cf463-112">사용자 지정 응답 본문</span><span class="sxs-lookup"><span data-stu-id="cf463-112">Custom Response Body</span></span>

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

### <span data-ttu-id="cf463-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="cf463-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="cf463-114">사용자 지정 응답 상태 코드</span><span class="sxs-lookup"><span data-stu-id="cf463-114">Custom Response Status Code</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf463-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="cf463-115">-Customrule</span></span>
<span data-ttu-id="cf463-116">정책 내 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="cf463-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="cf463-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf463-117">-DefaultProfile</span></span>
<span data-ttu-id="cf463-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf463-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cf463-119">-EnabledState</span></span>
<span data-ttu-id="cf463-120">정책이 활성화된 상태인지 또는 비활성화 상태인지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="cf463-121">가능한 값은 'Disabled', 'Enabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="cf463-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cf463-122">-ManagedRule</span></span>
<span data-ttu-id="cf463-123">정책 내에서 관리되는 규칙</span><span class="sxs-lookup"><span data-stu-id="cf463-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="cf463-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="cf463-124">-Mode</span></span>
<span data-ttu-id="cf463-125">정책 수준에서 검색 모드 또는 방지 모드에 있는 경우를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="cf463-126">가능한 값은 다음과 같습니다. '방지', '검색'</span><span class="sxs-lookup"><span data-stu-id="cf463-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="cf463-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cf463-127">-Name</span></span>
<span data-ttu-id="cf463-128">WebApplicationFireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="cf463-129">-RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="cf463-129">-RedirectUrl</span></span>
<span data-ttu-id="cf463-130">리디렉션 URL</span><span class="sxs-lookup"><span data-stu-id="cf463-130">Redirect URL</span></span>

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

### <span data-ttu-id="cf463-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf463-131">-ResourceGroupName</span></span>
<span data-ttu-id="cf463-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cf463-132">The resource group name</span></span>

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

### <span data-ttu-id="cf463-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf463-133">-Confirm</span></span>
<span data-ttu-id="cf463-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf463-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf463-135">-WhatIf</span></span>
<span data-ttu-id="cf463-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cf463-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf463-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf463-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf463-138">CommonParameters</span></span>
<span data-ttu-id="cf463-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cf463-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf463-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cf463-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf463-141">입력</span><span class="sxs-lookup"><span data-stu-id="cf463-141">INPUTS</span></span>

### <span data-ttu-id="cf463-142">없음</span><span class="sxs-lookup"><span data-stu-id="cf463-142">None</span></span>

## <span data-ttu-id="cf463-143">출력</span><span class="sxs-lookup"><span data-stu-id="cf463-143">OUTPUTS</span></span>

### <span data-ttu-id="cf463-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="cf463-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="cf463-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cf463-145">NOTES</span></span>

## <span data-ttu-id="cf463-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf463-146">RELATED LINKS</span></span>

<span data-ttu-id="cf463-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="cf463-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
