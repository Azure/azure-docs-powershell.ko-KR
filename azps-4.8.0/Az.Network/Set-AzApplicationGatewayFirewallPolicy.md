---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048857"
---
# <span data-ttu-id="2404e-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2404e-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="2404e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2404e-102">SYNOPSIS</span></span>
<span data-ttu-id="2404e-103">응용 프로그램 게이트웨이 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="2404e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2404e-104">SYNTAX</span></span>

### <span data-ttu-id="2404e-105">ByFactoryObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="2404e-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2404e-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="2404e-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2404e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2404e-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2404e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2404e-108">DESCRIPTION</span></span>
<span data-ttu-id="2404e-109">**AzApplicationGatewayFirewallPolicy** Cmdlet은 Azure application gateway 방화벽 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="2404e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2404e-110">EXAMPLES</span></span>

### <span data-ttu-id="2404e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2404e-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="2404e-112">이 명령은 $AppGwFirewallPolicy 변수의 설정을 사용 하 여 응용 프로그램 게이트웨이 방화벽 정책을 업데이트 하 고 업데이트 된 게이트웨이를 $UpdatedAppGwFirewallPolicy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="2404e-113">변수</span><span class="sxs-lookup"><span data-stu-id="2404e-113">PARAMETERS</span></span>

### <span data-ttu-id="2404e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2404e-114">-AsJob</span></span>
<span data-ttu-id="2404e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2404e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2404e-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="2404e-116">-CustomRule</span></span>
<span data-ttu-id="2404e-117">CustomRules 목록</span><span class="sxs-lookup"><span data-stu-id="2404e-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="2404e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2404e-118">-DefaultProfile</span></span>
<span data-ttu-id="2404e-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2404e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2404e-120">-InputObject</span></span>
<span data-ttu-id="2404e-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="2404e-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="2404e-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="2404e-122">-ManagedRule</span></span>
<span data-ttu-id="2404e-123">방화벽 정책의 ManagedRules</span><span class="sxs-lookup"><span data-stu-id="2404e-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="2404e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="2404e-124">-Name</span></span>
<span data-ttu-id="2404e-125">방화벽 정책 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="2404e-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="2404e-126">-PolicySetting</span></span>
<span data-ttu-id="2404e-127">방화벽 정책의 policysettings</span><span class="sxs-lookup"><span data-stu-id="2404e-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="2404e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2404e-128">-ResourceGroupName</span></span>
<span data-ttu-id="2404e-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-129">The resource group name.</span></span>

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

### <span data-ttu-id="2404e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2404e-130">-ResourceId</span></span>
<span data-ttu-id="2404e-131">Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="2404e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="2404e-132">-Confirm</span></span>
<span data-ttu-id="2404e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2404e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2404e-134">-WhatIf</span></span>
<span data-ttu-id="2404e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2404e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2404e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2404e-137">CommonParameters</span></span>
<span data-ttu-id="2404e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2404e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2404e-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2404e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2404e-140">입력</span><span class="sxs-lookup"><span data-stu-id="2404e-140">INPUTS</span></span>

### <span data-ttu-id="2404e-141">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2404e-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="2404e-142">출력</span><span class="sxs-lookup"><span data-stu-id="2404e-142">OUTPUTS</span></span>

### <span data-ttu-id="2404e-143">PSApplicationGatewayWebApplicationFirewallPolicy에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2404e-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="2404e-144">상속자</span><span class="sxs-lookup"><span data-stu-id="2404e-144">NOTES</span></span>

## <span data-ttu-id="2404e-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2404e-145">RELATED LINKS</span></span>
