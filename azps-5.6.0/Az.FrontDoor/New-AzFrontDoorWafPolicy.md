---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 5c39a86b29ce27ea57d51e7e3bfb048560ef1ee6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970832"
---
# <span data-ttu-id="b12b7-101">New-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="b12b7-101">New-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="b12b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b12b7-102">SYNOPSIS</span></span>
<span data-ttu-id="b12b7-103">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b12b7-103">Create WAF policy</span></span>

## <span data-ttu-id="b12b7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b12b7-104">SYNTAX</span></span>

```
New-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b12b7-105">설명</span><span class="sxs-lookup"><span data-stu-id="b12b7-105">DESCRIPTION</span></span>
<span data-ttu-id="b12b7-106">**New-AzFrontDoorWafPolicy** cmdlet은 현재 구독 아래 지정된 리소스 그룹에 새 Azure WAF 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-106">The **New-AzFrontDoorWafPolicy** cmdlet creates a new Azure WAF policy in the specified resource group under current subscription</span></span>

## <span data-ttu-id="b12b7-107">예제</span><span class="sxs-lookup"><span data-stu-id="b12b7-107">EXAMPLES</span></span>

### <span data-ttu-id="b12b7-108">예제 1: WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b12b7-108">Example 1: Create WAF policy</span></span>
```powershell
PS C:\> New-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Customrule $customRule1,$customRule2 -ManagedRule $managedRule1 -EnabledState Enabled -Mode Prevention -RedirectUrl "https://www.bing.com/" -CustomBlockResponseStatusCode 405 -CustomBlockResponseBody "<html><head><title>You are blocked!</title></head><body></body></html>"

Name         PolicyMode PolicyEnabledState RedirectUrl
----         ---------- ------------------ -----------
{policyName} Prevention            Enabled https://www.bing.com/
```

<span data-ttu-id="b12b7-109">WAF 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="b12b7-109">Create WAF policy</span></span>

## <span data-ttu-id="b12b7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b12b7-110">PARAMETERS</span></span>

### <span data-ttu-id="b12b7-111">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="b12b7-111">-CustomBlockResponseBody</span></span>
<span data-ttu-id="b12b7-112">사용자 지정 응답 본문</span><span class="sxs-lookup"><span data-stu-id="b12b7-112">Custom Response Body</span></span>

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

### <span data-ttu-id="b12b7-113">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="b12b7-113">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="b12b7-114">사용자 지정 응답 상태 코드</span><span class="sxs-lookup"><span data-stu-id="b12b7-114">Custom Response Status Code</span></span>

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

### <span data-ttu-id="b12b7-115">-Customrule</span><span class="sxs-lookup"><span data-stu-id="b12b7-115">-Customrule</span></span>
<span data-ttu-id="b12b7-116">정책 내에서 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="b12b7-116">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="b12b7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b12b7-117">-DefaultProfile</span></span>
<span data-ttu-id="b12b7-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b12b7-119">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b12b7-119">-EnabledState</span></span>
<span data-ttu-id="b12b7-120">정책이 사용 가능한 상태인지 또는 사용하지 않도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-120">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="b12b7-121">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-121">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="b12b7-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="b12b7-122">-ManagedRule</span></span>
<span data-ttu-id="b12b7-123">정책 내에서 관리되는 규칙</span><span class="sxs-lookup"><span data-stu-id="b12b7-123">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="b12b7-124">-Mode</span><span class="sxs-lookup"><span data-stu-id="b12b7-124">-Mode</span></span>
<span data-ttu-id="b12b7-125">정책 수준에서 감지 모드 또는 방지 모드에 있는 경우를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-125">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="b12b7-126">가능한 값은 다음과 같습니다. 'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="b12b7-126">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="b12b7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b12b7-127">-Name</span></span>
<span data-ttu-id="b12b7-128">WebApplicationFireWallPolicy 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-128">WebApplicationFireWallPolicy name.</span></span>

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

### <span data-ttu-id="b12b7-129">-리디렉션Url</span><span class="sxs-lookup"><span data-stu-id="b12b7-129">-RedirectUrl</span></span>
<span data-ttu-id="b12b7-130">리디렉션 URL</span><span class="sxs-lookup"><span data-stu-id="b12b7-130">Redirect URL</span></span>

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

### <span data-ttu-id="b12b7-131">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="b12b7-131">-RequestBodyCheck</span></span>
<span data-ttu-id="b12b7-132">본문을 관리되는 규칙에 의해 검사해야 하는지 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-132">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="b12b7-133">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-133">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="b12b7-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b12b7-134">-ResourceGroupName</span></span>
<span data-ttu-id="b12b7-135">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b12b7-135">The resource group name</span></span>

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

### <span data-ttu-id="b12b7-136">-확인</span><span class="sxs-lookup"><span data-stu-id="b12b7-136">-Confirm</span></span>
<span data-ttu-id="b12b7-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b12b7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b12b7-138">-WhatIf</span></span>
<span data-ttu-id="b12b7-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b12b7-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b12b7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b12b7-141">CommonParameters</span></span>
<span data-ttu-id="b12b7-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b12b7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b12b7-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b12b7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b12b7-144">입력</span><span class="sxs-lookup"><span data-stu-id="b12b7-144">INPUTS</span></span>

### <span data-ttu-id="b12b7-145">없음</span><span class="sxs-lookup"><span data-stu-id="b12b7-145">None</span></span>

## <span data-ttu-id="b12b7-146">출력</span><span class="sxs-lookup"><span data-stu-id="b12b7-146">OUTPUTS</span></span>

### <span data-ttu-id="b12b7-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="b12b7-147">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="b12b7-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b12b7-148">NOTES</span></span>

## <span data-ttu-id="b12b7-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b12b7-149">RELATED LINKS</span></span>

<span data-ttu-id="b12b7-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="b12b7-150">[Update-AzFrontDoorWafPolicy](./Update-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[Remove-AzFrontDoorWafPolicy](./Remove-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
