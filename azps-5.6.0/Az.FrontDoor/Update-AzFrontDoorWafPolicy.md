---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/update-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Update-AzFrontDoorWafPolicy.md
ms.openlocfilehash: bc4aa72d202938b5727245386f3485fbc43a6ab5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969115"
---
# <span data-ttu-id="db124-101">Update-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="db124-101">Update-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="db124-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db124-102">SYNOPSIS</span></span>
<span data-ttu-id="db124-103">WAF 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="db124-103">Update WAF policy</span></span>

## <span data-ttu-id="db124-104">구문</span><span class="sxs-lookup"><span data-stu-id="db124-104">SYNTAX</span></span>

### <span data-ttu-id="db124-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="db124-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-EnabledState <PSEnabledState>]
 [-Mode <String>] [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db124-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db124-106">ByObjectParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db124-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db124-107">ByResourceIdParameterSet</span></span>
```
Update-AzFrontDoorWafPolicy -ResourceId <String> [-EnabledState <PSEnabledState>] [-Mode <String>]
 [-Customrule <PSCustomRule[]>] [-ManagedRule <PSManagedRule[]>] [-RedirectUrl <String>]
 [-CustomBlockResponseStatusCode <Int32>] [-CustomBlockResponseBody <String>] [-RequestBodyCheck <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db124-108">설명</span><span class="sxs-lookup"><span data-stu-id="db124-108">DESCRIPTION</span></span>
<span data-ttu-id="db124-109">**Update-AzFrontDoorWafPolicy** cmdlet은 기존 WAF 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-109">The **Update-AzFrontDoorWafPolicy** cmdlet updates an existing WAF policy.</span></span> <span data-ttu-id="db124-110">입력 매개 변수가 제공되지 않은 경우 기존 WAF 정책의 이전 매개 변수가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="db124-110">If input parameters are not provided, old parameters from the existing WAF policy will be used.</span></span>

## <span data-ttu-id="db124-111">예제</span><span class="sxs-lookup"><span data-stu-id="db124-111">EXAMPLES</span></span>

### <span data-ttu-id="db124-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="db124-112">Example 1</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -CustomBlockResponseStatusCode 403

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Prevention            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="db124-113">기존 WAF 정책 사용자 지정 상태 코드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-113">Update an existing WAF policy custom status code.</span></span>

### <span data-ttu-id="db124-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="db124-114">Example 2</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection

Name         PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----         ---------- ------------------ ----------------------------- -----------
{policyName} Detection            Enabled                           403 https://www.bing.com/
```

<span data-ttu-id="db124-115">기존 WAF 정책 모드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-115">Update an existing WAF policy mode.</span></span>

### <span data-ttu-id="db124-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="db124-116">Example 3</span></span>
```powershell
PS C:\> Update-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName -Mode Detection -EnabledState Disabled

Name          PolicyMode PolicyEnabledState CustomBlockResponseStatusCode RedirectUrl
----          ---------- ------------------ ----------------------------- -----------
{policyName}  Detection           Disabled                           403 https://www.bing.com/
```

<span data-ttu-id="db124-117">기존 WAF 정책을 사용하도록 설정된 상태 및 모드를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-117">Update an existing WAF policy enabled state and mode.</span></span>

### <span data-ttu-id="db124-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="db124-118">Example 4</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Update-AzFrontDoorWafPolicy -Mode Detection -EnabledState Disabled
```

<span data-ttu-id="db124-119">모든 WAF 정책을 $resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db124-119">Update all WAF policies in $resourceGroupName</span></span>

## <span data-ttu-id="db124-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="db124-120">PARAMETERS</span></span>

### <span data-ttu-id="db124-121">-CustomBlockResponseBody</span><span class="sxs-lookup"><span data-stu-id="db124-121">-CustomBlockResponseBody</span></span>
<span data-ttu-id="db124-122">사용자 지정 응답 본문</span><span class="sxs-lookup"><span data-stu-id="db124-122">Custom Response Body</span></span>

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

### <span data-ttu-id="db124-123">-CustomBlockResponseStatusCode</span><span class="sxs-lookup"><span data-stu-id="db124-123">-CustomBlockResponseStatusCode</span></span>
<span data-ttu-id="db124-124">사용자 지정 응답 상태 코드</span><span class="sxs-lookup"><span data-stu-id="db124-124">Custom Response Status Code</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db124-125">-Customrule</span><span class="sxs-lookup"><span data-stu-id="db124-125">-Customrule</span></span>
<span data-ttu-id="db124-126">정책 내에서 사용자 지정 규칙</span><span class="sxs-lookup"><span data-stu-id="db124-126">Custom rules inside the policy</span></span>

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

### <span data-ttu-id="db124-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db124-127">-DefaultProfile</span></span>
<span data-ttu-id="db124-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db124-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db124-129">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="db124-129">-EnabledState</span></span>
<span data-ttu-id="db124-130">정책이 사용 가능한 상태인지 또는 사용하지 않도록 설정되어 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="db124-130">Whether the policy is in enabled state or disabled state.</span></span>
<span data-ttu-id="db124-131">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="db124-131">Possible values include: 'Disabled', 'Enabled'</span></span>

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

### <span data-ttu-id="db124-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db124-132">-InputObject</span></span>
<span data-ttu-id="db124-133">업데이트할 FireWallPolicy 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="db124-133">The FireWallPolicy object to update.</span></span>

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

### <span data-ttu-id="db124-134">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="db124-134">-ManagedRule</span></span>
<span data-ttu-id="db124-135">정책 내에서 관리되는 규칙</span><span class="sxs-lookup"><span data-stu-id="db124-135">Managed rules inside the policy</span></span>

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

### <span data-ttu-id="db124-136">-Mode</span><span class="sxs-lookup"><span data-stu-id="db124-136">-Mode</span></span>
<span data-ttu-id="db124-137">정책 수준에서 감지 모드 또는 방지 모드에 있는 경우를 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-137">Describes if it is in detection mode  or prevention mode at policy level.</span></span>
<span data-ttu-id="db124-138">가능한 값은 다음과 같습니다. 'Prevention', 'Detection'</span><span class="sxs-lookup"><span data-stu-id="db124-138">Possible values include:'Prevention', 'Detection'</span></span>

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

### <span data-ttu-id="db124-139">-Name</span><span class="sxs-lookup"><span data-stu-id="db124-139">-Name</span></span>
<span data-ttu-id="db124-140">업데이트할 FireWallPolicy의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="db124-140">The name of the FireWallPolicy to update.</span></span>

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

### <span data-ttu-id="db124-141">-리디렉션Url</span><span class="sxs-lookup"><span data-stu-id="db124-141">-RedirectUrl</span></span>
<span data-ttu-id="db124-142">리디렉션 URL</span><span class="sxs-lookup"><span data-stu-id="db124-142">Redirect URL</span></span>

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

### <span data-ttu-id="db124-143">-RequestBodyCheck</span><span class="sxs-lookup"><span data-stu-id="db124-143">-RequestBodyCheck</span></span>
<span data-ttu-id="db124-144">본문을 관리되는 규칙에 의해 검사해야 하는지 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-144">Defines if the body should be inspected by managed rules.</span></span> <span data-ttu-id="db124-145">가능한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="db124-145">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="db124-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db124-146">-ResourceGroupName</span></span>
<span data-ttu-id="db124-147">FireWallPolicy가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="db124-147">The resource group to which the FireWallPolicy belongs.</span></span>

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

### <span data-ttu-id="db124-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db124-148">-ResourceId</span></span>
<span data-ttu-id="db124-149">업데이트할 FireWallPolicy의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="db124-149">Resource Id of the FireWallPolicy to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db124-150">-확인</span><span class="sxs-lookup"><span data-stu-id="db124-150">-Confirm</span></span>
<span data-ttu-id="db124-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db124-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db124-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db124-152">-WhatIf</span></span>
<span data-ttu-id="db124-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="db124-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db124-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db124-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db124-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db124-155">CommonParameters</span></span>
<span data-ttu-id="db124-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db124-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db124-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db124-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db124-158">입력</span><span class="sxs-lookup"><span data-stu-id="db124-158">INPUTS</span></span>

### <span data-ttu-id="db124-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="db124-159">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="db124-160">System.String</span><span class="sxs-lookup"><span data-stu-id="db124-160">System.String</span></span>

## <span data-ttu-id="db124-161">출력</span><span class="sxs-lookup"><span data-stu-id="db124-161">OUTPUTS</span></span>

### <span data-ttu-id="db124-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="db124-162">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

## <span data-ttu-id="db124-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db124-163">NOTES</span></span>

## <span data-ttu-id="db124-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db124-164">RELATED LINKS</span></span>

<span data-ttu-id="db124-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md) 
 [New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md) 
 [New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span><span class="sxs-lookup"><span data-stu-id="db124-165">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)
[New-AzFrontDoorWafManagedRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)
[New-AzFrontDoorWafCustomRuleObject](./New-AzFrontDoorWafManagedRuleObject.md)</span></span>
