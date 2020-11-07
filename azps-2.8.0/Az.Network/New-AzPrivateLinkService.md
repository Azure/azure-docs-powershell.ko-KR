---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 75c8f7b52fec0e429820d43f86a8a41798b1d5f7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869870"
---
# <span data-ttu-id="a722d-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a722d-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="a722d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a722d-102">SYNOPSIS</span></span>
<span data-ttu-id="a722d-103">개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-103">Creates a private link service</span></span>

## <span data-ttu-id="a722d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a722d-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a722d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a722d-105">DESCRIPTION</span></span>
<span data-ttu-id="a722d-106">**새 AzPrivateLinkService** cmdlet은 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="a722d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a722d-107">EXAMPLES</span></span>

### <span data-ttu-id="a722d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a722d-108">Example 1</span></span>
```
$vnet = Get-AzVirtualNetwork -ResourceName "myvnet" -ResourceGroupName "myresourcegroup"
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name "IP-Config" -Subnet $vnet.subnets[1] -PrivateIpAddress "10.0.0.5"
$publicip = Get-AzPublicIpAddress -ResourceGroupName "myresourcegroup"
$frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "myresourcegroup" -Location "West US" -FrontendIpConfiguration $frontend  
New-AzPrivateLinkService -Name "mypls" -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

<span data-ttu-id="a722d-109">이 예제에서는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-109">This example creates a private link service.</span></span>

## <span data-ttu-id="a722d-110">변수</span><span class="sxs-lookup"><span data-stu-id="a722d-110">PARAMETERS</span></span>

### <span data-ttu-id="a722d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a722d-111">-AsJob</span></span>
<span data-ttu-id="a722d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a722d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a722d-113">-자동 승인</span><span class="sxs-lookup"><span data-stu-id="a722d-113">-AutoApproval</span></span>
<span data-ttu-id="a722d-114">개인 링크 서비스의 자동 승인 구독</span><span class="sxs-lookup"><span data-stu-id="a722d-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="a722d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a722d-115">-DefaultProfile</span></span>
<span data-ttu-id="a722d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a722d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a722d-117">-Force</span></span>
<span data-ttu-id="a722d-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="a722d-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a722d-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a722d-119">-IpConfiguration</span></span>
<span data-ttu-id="a722d-120">Ip 구성</span><span class="sxs-lookup"><span data-stu-id="a722d-120">The ip configurations</span></span>

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

### <span data-ttu-id="a722d-121">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="a722d-121">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="a722d-122">프런트 엔드 ip 구성</span><span class="sxs-lookup"><span data-stu-id="a722d-122">The front end ip configurations</span></span>

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

### <span data-ttu-id="a722d-123">-위치</span><span class="sxs-lookup"><span data-stu-id="a722d-123">-Location</span></span>
<span data-ttu-id="a722d-124">location.</span><span class="sxs-lookup"><span data-stu-id="a722d-124">location.</span></span>

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

### <span data-ttu-id="a722d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="a722d-125">-Name</span></span>
<span data-ttu-id="a722d-126">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-126">The name of the service.</span></span>

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

### <span data-ttu-id="a722d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a722d-127">-ResourceGroupName</span></span>
<span data-ttu-id="a722d-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-128">The resource group name.</span></span>

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

### <span data-ttu-id="a722d-129">태그</span><span class="sxs-lookup"><span data-stu-id="a722d-129">-Tag</span></span>
<span data-ttu-id="a722d-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a722d-131">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a722d-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a722d-132">-표시 유형</span><span class="sxs-lookup"><span data-stu-id="a722d-132">-Visibility</span></span>
<span data-ttu-id="a722d-133">비공개 링크 서비스의 visibility 구독</span><span class="sxs-lookup"><span data-stu-id="a722d-133">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="a722d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="a722d-134">-Confirm</span></span>
<span data-ttu-id="a722d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a722d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a722d-136">-WhatIf</span></span>
<span data-ttu-id="a722d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a722d-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a722d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a722d-139">CommonParameters</span></span>
<span data-ttu-id="a722d-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a722d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a722d-141">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a722d-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a722d-142">입력</span><span class="sxs-lookup"><span data-stu-id="a722d-142">INPUTS</span></span>

### <span data-ttu-id="a722d-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a722d-143">System.String</span></span>

### <span data-ttu-id="a722d-144">PSFrontendIPConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a722d-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="a722d-145">PSPrivateLinkServiceIpConfiguration [] (으)로</span><span class="sxs-lookup"><span data-stu-id="a722d-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="a722d-146">출력</span><span class="sxs-lookup"><span data-stu-id="a722d-146">OUTPUTS</span></span>

### <span data-ttu-id="a722d-147">PSPrivateLinkService에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a722d-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="a722d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a722d-148">NOTES</span></span>

## <span data-ttu-id="a722d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a722d-149">RELATED LINKS</span></span>

[<span data-ttu-id="a722d-150">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a722d-150">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="a722d-151">제거-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="a722d-151">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="a722d-152">새로운 AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="a722d-152">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
