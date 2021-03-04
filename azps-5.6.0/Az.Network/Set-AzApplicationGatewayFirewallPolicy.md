---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981707"
---
# <span data-ttu-id="96244-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96244-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="96244-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96244-102">SYNOPSIS</span></span>
<span data-ttu-id="96244-103">애플리케이션 게이트웨이 방화벽 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="96244-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="96244-104">구문</span><span class="sxs-lookup"><span data-stu-id="96244-104">SYNTAX</span></span>

### <span data-ttu-id="96244-105">ByFactoryObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="96244-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96244-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="96244-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96244-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96244-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96244-108">설명</span><span class="sxs-lookup"><span data-stu-id="96244-108">DESCRIPTION</span></span>
<span data-ttu-id="96244-109">**Set-AzApplicationGatewayFirewallPolicy** cmdlet은 Azure 애플리케이션 게이트웨이 방화벽 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="96244-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="96244-110">예제</span><span class="sxs-lookup"><span data-stu-id="96244-110">EXAMPLES</span></span>

### <span data-ttu-id="96244-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="96244-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="96244-112">이 명령은 애플리케이션 게이트웨이 방화벽 정책을 $AppGwFirewallPolicy 설정으로 업데이트하고 업데이트된 게이트웨이를 $UpdatedAppGwFirewallPolicy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="96244-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="96244-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="96244-113">PARAMETERS</span></span>

### <span data-ttu-id="96244-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96244-114">-AsJob</span></span>
<span data-ttu-id="96244-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="96244-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96244-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="96244-116">-CustomRule</span></span>
<span data-ttu-id="96244-117">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="96244-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="96244-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96244-118">-DefaultProfile</span></span>
<span data-ttu-id="96244-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96244-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96244-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96244-120">-InputObject</span></span>
<span data-ttu-id="96244-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96244-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="96244-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="96244-122">-ManagedRule</span></span>
<span data-ttu-id="96244-123">방화벽 정책의 ManagedRules</span><span class="sxs-lookup"><span data-stu-id="96244-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="96244-124">-Name</span><span class="sxs-lookup"><span data-stu-id="96244-124">-Name</span></span>
<span data-ttu-id="96244-125">방화벽 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96244-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="96244-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="96244-126">-PolicySetting</span></span>
<span data-ttu-id="96244-127">방화벽 정책의 정책 설정</span><span class="sxs-lookup"><span data-stu-id="96244-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="96244-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96244-128">-ResourceGroupName</span></span>
<span data-ttu-id="96244-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96244-129">The resource group name.</span></span>

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

### <span data-ttu-id="96244-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96244-130">-ResourceId</span></span>
<span data-ttu-id="96244-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="96244-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="96244-132">-확인</span><span class="sxs-lookup"><span data-stu-id="96244-132">-Confirm</span></span>
<span data-ttu-id="96244-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96244-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96244-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96244-134">-WhatIf</span></span>
<span data-ttu-id="96244-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="96244-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96244-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96244-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96244-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96244-137">CommonParameters</span></span>
<span data-ttu-id="96244-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96244-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96244-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="96244-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96244-140">입력</span><span class="sxs-lookup"><span data-stu-id="96244-140">INPUTS</span></span>

### <span data-ttu-id="96244-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96244-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="96244-142">출력</span><span class="sxs-lookup"><span data-stu-id="96244-142">OUTPUTS</span></span>

### <span data-ttu-id="96244-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="96244-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="96244-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96244-144">NOTES</span></span>

## <span data-ttu-id="96244-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96244-145">RELATED LINKS</span></span>
