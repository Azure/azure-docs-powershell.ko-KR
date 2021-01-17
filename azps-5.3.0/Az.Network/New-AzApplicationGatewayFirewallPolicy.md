---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379471"
---
# <span data-ttu-id="17290-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="17290-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="17290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17290-102">SYNOPSIS</span></span>
<span data-ttu-id="17290-103">애플리케이션 게이트웨이 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17290-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="17290-104">구문</span><span class="sxs-lookup"><span data-stu-id="17290-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17290-105">설명</span><span class="sxs-lookup"><span data-stu-id="17290-105">DESCRIPTION</span></span>
<span data-ttu-id="17290-106">**New-AzApplicationGatewayFirewallPolicy** cmdlet은 애플리케이션 게이트웨이 방화벽 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17290-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="17290-107">예제</span><span class="sxs-lookup"><span data-stu-id="17290-107">EXAMPLES</span></span>

### <span data-ttu-id="17290-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="17290-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="17290-109">이 명령은 리소스 그룹 "rg1"에 "wafResource1"이라는 새 Azure Application Gateway 방화벽 정책을 만듭니다. 이 정책 변수에 정의된 사용자 지정 규칙을 사용하여 "westus" $customRule 합니다.</span><span class="sxs-lookup"><span data-stu-id="17290-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="17290-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17290-110">PARAMETERS</span></span>

### <span data-ttu-id="17290-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17290-111">-AsJob</span></span>
<span data-ttu-id="17290-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="17290-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17290-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="17290-113">-CustomRule</span></span>
<span data-ttu-id="17290-114">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="17290-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17290-115">-DefaultProfile</span></span>
<span data-ttu-id="17290-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17290-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17290-117">-Force</span><span class="sxs-lookup"><span data-stu-id="17290-117">-Force</span></span>
<span data-ttu-id="17290-118">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17290-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="17290-119">-Location</span><span class="sxs-lookup"><span data-stu-id="17290-119">-Location</span></span>
<span data-ttu-id="17290-120">위치.</span><span class="sxs-lookup"><span data-stu-id="17290-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="17290-121">-ManagedRule</span></span>
<span data-ttu-id="17290-122">관리되는 규칙 설정</span><span class="sxs-lookup"><span data-stu-id="17290-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-123">-Name</span><span class="sxs-lookup"><span data-stu-id="17290-123">-Name</span></span>
<span data-ttu-id="17290-124">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17290-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="17290-125">-PolicySetting</span></span>
<span data-ttu-id="17290-126">웹 애플리케이션 방화벽에 대한 정책 설정</span><span class="sxs-lookup"><span data-stu-id="17290-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17290-127">-ResourceGroupName</span></span>
<span data-ttu-id="17290-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17290-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="17290-129">-Tag</span></span>
<span data-ttu-id="17290-130">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="17290-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17290-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17290-131">-Confirm</span></span>
<span data-ttu-id="17290-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17290-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17290-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17290-133">-WhatIf</span></span>
<span data-ttu-id="17290-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17290-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17290-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17290-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17290-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17290-136">CommonParameters</span></span>
<span data-ttu-id="17290-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17290-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17290-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17290-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17290-139">입력</span><span class="sxs-lookup"><span data-stu-id="17290-139">INPUTS</span></span>

### <span data-ttu-id="17290-140">System.String</span><span class="sxs-lookup"><span data-stu-id="17290-140">System.String</span></span>

### <span data-ttu-id="17290-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span><span class="sxs-lookup"><span data-stu-id="17290-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="17290-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="17290-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="17290-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="17290-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="17290-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="17290-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="17290-145">출력</span><span class="sxs-lookup"><span data-stu-id="17290-145">OUTPUTS</span></span>

### <span data-ttu-id="17290-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="17290-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="17290-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17290-147">NOTES</span></span>

## <span data-ttu-id="17290-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17290-148">RELATED LINKS</span></span>
