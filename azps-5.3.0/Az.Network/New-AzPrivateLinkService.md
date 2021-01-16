---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 2723ca0f5bebfbf65fefbfbd94fa995d544d9f71
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490996"
---
# <span data-ttu-id="23ff1-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23ff1-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="23ff1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="23ff1-103">개인 링크 서비스 생성</span><span class="sxs-lookup"><span data-stu-id="23ff1-103">Creates a private link service</span></span>

## <span data-ttu-id="23ff1-104">구문</span><span class="sxs-lookup"><span data-stu-id="23ff1-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23ff1-105">설명</span><span class="sxs-lookup"><span data-stu-id="23ff1-105">DESCRIPTION</span></span>
<span data-ttu-id="23ff1-106">**New-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="23ff1-107">예제</span><span class="sxs-lookup"><span data-stu-id="23ff1-107">EXAMPLES</span></span>

### <span data-ttu-id="23ff1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="23ff1-108">Example 1</span></span>

<span data-ttu-id="23ff1-109">다음 예제에서는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-109">The following example creates a private link service.</span></span>

```powershell
$vnet = Get-AzVirtualNetwork -ResourceName 'myvnet' -ResourceGroupName 'myresourcegroup'
# View the results of $vnet and change 'mysubnet' in the following line to the appropriate subnet name.
$subnet = $vnet | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mysubnet'
$IPConfig = New-AzPrivateLinkServiceIpConfig -Name 'IP-Config' -Subnet $subnet -PrivateIpAddress '10.0.0.5'
$publicip = Get-AzPublicIpAddress -ResourceGroupName 'myresourcegroup'
$frontend = New-AzLoadBalancerFrontendIpConfig -Name 'FrontendIpConfig01' -PublicIpAddress $publicip
$lb = New-AzLoadBalancer -Name 'MyLoadBalancer' -ResourceGroupName 'myresourcegroup' -Location 'West US' -FrontendIpConfiguration $frontend
New-AzPrivateLinkService -Name 'mypls' -ResourceGroupName myresourcegroup -Location "West US" -LoadBalancerFrontendIpConfiguration $frontend -IpConfiguration $IPConfig
```

## <span data-ttu-id="23ff1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23ff1-110">PARAMETERS</span></span>

### <span data-ttu-id="23ff1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23ff1-111">-AsJob</span></span>
<span data-ttu-id="23ff1-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="23ff1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23ff1-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="23ff1-113">-AutoApproval</span></span>
<span data-ttu-id="23ff1-114">개인 링크 서비스의 자동 승인 구독</span><span class="sxs-lookup"><span data-stu-id="23ff1-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="23ff1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ff1-115">-DefaultProfile</span></span>
<span data-ttu-id="23ff1-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ff1-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="23ff1-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="23ff1-118">개인 링크 서비스에 대한 프록시 프로토콜을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="23ff1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="23ff1-119">-Force</span></span>
<span data-ttu-id="23ff1-120">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="23ff1-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ff1-121">-IpConfiguration</span></span>
<span data-ttu-id="23ff1-122">IP 구성</span><span class="sxs-lookup"><span data-stu-id="23ff1-122">The ip configurations</span></span>

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

### <span data-ttu-id="23ff1-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ff1-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="23ff1-124">프런트 엔드 IP 구성</span><span class="sxs-lookup"><span data-stu-id="23ff1-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="23ff1-125">-Location</span><span class="sxs-lookup"><span data-stu-id="23ff1-125">-Location</span></span>
<span data-ttu-id="23ff1-126">위치.</span><span class="sxs-lookup"><span data-stu-id="23ff1-126">location.</span></span>

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

### <span data-ttu-id="23ff1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="23ff1-127">-Name</span></span>
<span data-ttu-id="23ff1-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-128">The name of the service.</span></span>

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

### <span data-ttu-id="23ff1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ff1-129">-ResourceGroupName</span></span>
<span data-ttu-id="23ff1-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-130">The resource group name.</span></span>

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

### <span data-ttu-id="23ff1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="23ff1-131">-Tag</span></span>
<span data-ttu-id="23ff1-132">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="23ff1-133">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="23ff1-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="23ff1-134">-Visibility</span><span class="sxs-lookup"><span data-stu-id="23ff1-134">-Visibility</span></span>
<span data-ttu-id="23ff1-135">개인 링크 서비스의 가시성 구독</span><span class="sxs-lookup"><span data-stu-id="23ff1-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="23ff1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23ff1-136">-Confirm</span></span>
<span data-ttu-id="23ff1-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ff1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ff1-138">-WhatIf</span></span>
<span data-ttu-id="23ff1-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="23ff1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23ff1-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ff1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ff1-141">CommonParameters</span></span>
<span data-ttu-id="23ff1-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23ff1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ff1-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23ff1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ff1-144">입력</span><span class="sxs-lookup"><span data-stu-id="23ff1-144">INPUTS</span></span>

### <span data-ttu-id="23ff1-145">System.String</span><span class="sxs-lookup"><span data-stu-id="23ff1-145">System.String</span></span>

### <span data-ttu-id="23ff1-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="23ff1-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="23ff1-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="23ff1-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="23ff1-148">출력</span><span class="sxs-lookup"><span data-stu-id="23ff1-148">OUTPUTS</span></span>

### <span data-ttu-id="23ff1-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23ff1-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="23ff1-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23ff1-150">NOTES</span></span>

## <span data-ttu-id="23ff1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23ff1-151">RELATED LINKS</span></span>

[<span data-ttu-id="23ff1-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23ff1-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="23ff1-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23ff1-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="23ff1-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="23ff1-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
