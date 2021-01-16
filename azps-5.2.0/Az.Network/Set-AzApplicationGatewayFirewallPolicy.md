---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351830"
---
# <span data-ttu-id="a500b-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a500b-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="a500b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a500b-102">SYNOPSIS</span></span>
<span data-ttu-id="a500b-103">애플리케이션 게이트웨이 방화벽 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="a500b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a500b-104">SYNTAX</span></span>

### <span data-ttu-id="a500b-105">ByFactoryObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="a500b-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a500b-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="a500b-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a500b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a500b-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a500b-108">설명</span><span class="sxs-lookup"><span data-stu-id="a500b-108">DESCRIPTION</span></span>
<span data-ttu-id="a500b-109">**Set-AzApplicationGatewayFirewallPolicy** cmdlet은 Azure Application Gateway 방화벽 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="a500b-110">예제</span><span class="sxs-lookup"><span data-stu-id="a500b-110">EXAMPLES</span></span>

### <span data-ttu-id="a500b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a500b-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="a500b-112">이 명령은 $AppGwFirewallPolicy 변수의 설정으로 애플리케이션 게이트웨이 방화벽 정책을 업데이트하고 업데이트된 게이트웨이를 $UpdatedAppGwFirewallPolicy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="a500b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a500b-113">PARAMETERS</span></span>

### <span data-ttu-id="a500b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a500b-114">-AsJob</span></span>
<span data-ttu-id="a500b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a500b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a500b-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="a500b-116">-CustomRule</span></span>
<span data-ttu-id="a500b-117">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="a500b-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="a500b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a500b-118">-DefaultProfile</span></span>
<span data-ttu-id="a500b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a500b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a500b-120">-InputObject</span></span>
<span data-ttu-id="a500b-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a500b-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a500b-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="a500b-122">-ManagedRule</span></span>
<span data-ttu-id="a500b-123">방화벽 정책의 ManagedRules</span><span class="sxs-lookup"><span data-stu-id="a500b-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="a500b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a500b-124">-Name</span></span>
<span data-ttu-id="a500b-125">방화벽 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a500b-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="a500b-126">-PolicySetting</span></span>
<span data-ttu-id="a500b-127">방화벽 정책의 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a500b-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="a500b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a500b-128">-ResourceGroupName</span></span>
<span data-ttu-id="a500b-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a500b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a500b-130">-ResourceId</span></span>
<span data-ttu-id="a500b-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a500b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a500b-132">-Confirm</span></span>
<span data-ttu-id="a500b-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a500b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a500b-134">-WhatIf</span></span>
<span data-ttu-id="a500b-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a500b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a500b-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a500b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a500b-137">CommonParameters</span></span>
<span data-ttu-id="a500b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a500b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a500b-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a500b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a500b-140">입력</span><span class="sxs-lookup"><span data-stu-id="a500b-140">INPUTS</span></span>

### <span data-ttu-id="a500b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a500b-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="a500b-142">출력</span><span class="sxs-lookup"><span data-stu-id="a500b-142">OUTPUTS</span></span>

### <span data-ttu-id="a500b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a500b-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="a500b-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a500b-144">NOTES</span></span>

## <span data-ttu-id="a500b-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a500b-145">RELATED LINKS</span></span>