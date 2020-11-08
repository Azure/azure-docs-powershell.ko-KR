---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 441e47b4ef2a796fcdf5ee802cba83f0fce7e352
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047752"
---
# <span data-ttu-id="e88c4-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="e88c4-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="e88c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e88c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e88c4-103">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e88c4-103">Create WAF policy</span></span>

## <span data-ttu-id="e88c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e88c4-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e88c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e88c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e88c4-106">**AzFrontDoorWafPolicy** cmdlet은 현재 구독 아래의 지정 된 리소스 그룹에 새 AZURE waf 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="e88c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e88c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e88c4-108">예제 1: WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e88c4-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="e88c4-109">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="e88c4-109">Create WAF policy</span></span>

## <span data-ttu-id="e88c4-110">변수</span><span class="sxs-lookup"><span data-stu-id="e88c4-110">PARAMETERS</span></span>

### <span data-ttu-id="e88c4-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="e88c4-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="e88c4-112">사용자 지정 응답 본문</span><span class="sxs-lookup"><span data-stu-id="e88c4-112">Custom Response Body</span></span>

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

### <span data-ttu-id="e88c4-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="e88c4-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="e88c4-114">사용자 지정 응답 상태 코드</span><span class="sxs-lookup"><span data-stu-id="e88c4-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="e88c4-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="e88c4-115">-Customrule</span></span>
<span data-ttu-id="e88c4-116">정책 내의 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="e88c4-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="e88c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88c4-117">-DefaultProfile</span></span>
<span data-ttu-id="e88c4-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88c4-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="e88c4-119">-EnabledState</span></span>
<span data-ttu-id="e88c4-120">정책이 사용 상태로 설정 되어 있는지 또는 사용 안 함 상태 인지 여부</span><span class="sxs-lookup"><span data-stu-id="e88c4-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="e88c4-121">사용할 수 있는 값은 다음과 같습니다. ' Disabled ', ' Enabled '</span><span class="sxs-lookup"><span data-stu-id="e88c4-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="e88c4-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="e88c4-122">-ManagedRule</span></span>
<span data-ttu-id="e88c4-123">정책 내 관리 규칙</span><span class="sxs-lookup"><span data-stu-id="e88c4-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="e88c4-124">-모드</span><span class="sxs-lookup"><span data-stu-id="e88c4-124">-Mode</span></span>
<span data-ttu-id="e88c4-125">정책 수준의 검색 모드 또는 방지 모드에 있는 경우에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="e88c4-126">사용할 수 있는 값은 다음과 같습니다. ' 예방 ', ' 감지 '</span><span class="sxs-lookup"><span data-stu-id="e88c4-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="e88c4-127">-이름</span><span class="sxs-lookup"><span data-stu-id="e88c4-127">-Name</span></span>
<span data-ttu-id="e88c4-128">WebApplicationFireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="e88c4-129">로 RedirectUrl</span><span class="sxs-lookup"><span data-stu-id="e88c4-129">-RedirectUrl</span></span>
<span data-ttu-id="e88c4-130">리디렉션 URL</span><span class="sxs-lookup"><span data-stu-id="e88c4-130">Redirect URL</span></span>

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

### <span data-ttu-id="e88c4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e88c4-131">-ResourceGroupName</span></span>
<span data-ttu-id="e88c4-132">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e88c4-132">The resource group name</span></span>

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

### <span data-ttu-id="e88c4-133">-확인</span><span class="sxs-lookup"><span data-stu-id="e88c4-133">-Confirm</span></span>
<span data-ttu-id="e88c4-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e88c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e88c4-135">-WhatIf</span></span>
<span data-ttu-id="e88c4-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e88c4-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e88c4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88c4-138">CommonParameters</span></span>
<span data-ttu-id="e88c4-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e88c4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88c4-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e88c4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88c4-141">입력</span><span class="sxs-lookup"><span data-stu-id="e88c4-141">INPUTS</span></span>

### <span data-ttu-id="e88c4-142">않아야</span><span class="sxs-lookup"><span data-stu-id="e88c4-142">None</span></span>

## <span data-ttu-id="e88c4-143">출력</span><span class="sxs-lookup"><span data-stu-id="e88c4-143">OUTPUTS</span></span>

### <span data-ttu-id="e88c4-144">FrontDoor. PSPolicy.</span><span class="sxs-lookup"><span data-stu-id="e88c4-144">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="e88c4-145">상속자</span><span class="sxs-lookup"><span data-stu-id="e88c4-145">NOTES</span></span>

## <span data-ttu-id="e88c4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e88c4-146">RELATED LINKS</span></span>

<span data-ttu-id="e88c4-147">[업데이트-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [제거-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [새로운 AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [새로운 AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="e88c4-147">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
