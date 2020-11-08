---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 0b4cc79358723e6249a0c9d4e22929e224165402
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043263"
---
# <span data-ttu-id="5fbb6-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5fbb6-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="5fbb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fbb6-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbb6-103">개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-103">Creates a private link service</span></span>

## <span data-ttu-id="5fbb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5fbb6-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbb6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5fbb6-105">DESCRIPTION</span></span>
<span data-ttu-id="5fbb6-106">**새 AzPrivateLinkService** cmdlet은 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="5fbb6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5fbb6-107">EXAMPLES</span></span>

### <span data-ttu-id="5fbb6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5fbb6-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="5fbb6-109">이 예제에서는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-109">This example creates a private link service.</span></span>

## <span data-ttu-id="5fbb6-110">변수</span><span class="sxs-lookup"><span data-stu-id="5fbb6-110">PARAMETERS</span></span>

### <span data-ttu-id="5fbb6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fbb6-111">-AsJob</span></span>
<span data-ttu-id="5fbb6-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5fbb6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fbb6-113">-자동 승인</span><span class="sxs-lookup"><span data-stu-id="5fbb6-113">-AutoApproval</span></span>
<span data-ttu-id="5fbb6-114">개인 링크 서비스의 자동 승인 구독</span><span class="sxs-lookup"><span data-stu-id="5fbb6-114">The auto approval subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbb6-115">-DefaultProfile</span></span>
<span data-ttu-id="5fbb6-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5fbb6-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="5fbb6-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="5fbb6-118">개인 링크 서비스에 대해 프록시 프로토콜을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="5fbb6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5fbb6-119">-Force</span></span>
<span data-ttu-id="5fbb6-120">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="5fbb6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5fbb6-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fbb6-121">-IpConfiguration</span></span>
<span data-ttu-id="5fbb6-122">Ip 구성</span><span class="sxs-lookup"><span data-stu-id="5fbb6-122">The ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb6-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="5fbb6-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="5fbb6-124">프런트 엔드 ip 구성</span><span class="sxs-lookup"><span data-stu-id="5fbb6-124">The front end ip configurations</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb6-125">-위치</span><span class="sxs-lookup"><span data-stu-id="5fbb6-125">-Location</span></span>
<span data-ttu-id="5fbb6-126">location.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-126">location.</span></span>

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

### <span data-ttu-id="5fbb6-127">-이름</span><span class="sxs-lookup"><span data-stu-id="5fbb6-127">-Name</span></span>
<span data-ttu-id="5fbb6-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbb6-129">-ResourceGroupName</span></span>
<span data-ttu-id="5fbb6-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-130">The resource group name.</span></span>

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

### <span data-ttu-id="5fbb6-131">태그</span><span class="sxs-lookup"><span data-stu-id="5fbb6-131">-Tag</span></span>
<span data-ttu-id="5fbb6-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5fbb6-133">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5fbb6-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5fbb6-134">-표시 유형</span><span class="sxs-lookup"><span data-stu-id="5fbb6-134">-Visibility</span></span>
<span data-ttu-id="5fbb6-135">비공개 링크 서비스의 visibility 구독</span><span class="sxs-lookup"><span data-stu-id="5fbb6-135">The visibility subscriptions of private link service</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fbb6-136">-확인</span><span class="sxs-lookup"><span data-stu-id="5fbb6-136">-Confirm</span></span>
<span data-ttu-id="5fbb6-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fbb6-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbb6-138">-WhatIf</span></span>
<span data-ttu-id="5fbb6-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fbb6-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fbb6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbb6-141">CommonParameters</span></span>
<span data-ttu-id="5fbb6-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbb6-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbb6-144">입력</span><span class="sxs-lookup"><span data-stu-id="5fbb6-144">INPUTS</span></span>

### <span data-ttu-id="5fbb6-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5fbb6-145">System.String</span></span>

### <span data-ttu-id="5fbb6-146">PSFrontendIPConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="5fbb6-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="5fbb6-147">PSPrivateLinkServiceIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="5fbb6-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="5fbb6-148">출력</span><span class="sxs-lookup"><span data-stu-id="5fbb6-148">OUTPUTS</span></span>

### <span data-ttu-id="5fbb6-149">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5fbb6-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="5fbb6-150">상속자</span><span class="sxs-lookup"><span data-stu-id="5fbb6-150">NOTES</span></span>

## <span data-ttu-id="5fbb6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5fbb6-151">RELATED LINKS</span></span>

[<span data-ttu-id="5fbb6-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5fbb6-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="5fbb6-153">제거-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="5fbb6-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="5fbb6-154">새로운 AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="5fbb6-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)