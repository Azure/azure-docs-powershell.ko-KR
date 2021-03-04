---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkService.md
ms.openlocfilehash: 9ed82247ff0b1813293059a7608557184bdb18ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958256"
---
# <span data-ttu-id="056c9-101">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="056c9-101">New-AzPrivateLinkService</span></span>

## <span data-ttu-id="056c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="056c9-102">SYNOPSIS</span></span>
<span data-ttu-id="056c9-103">개인 링크 서비스 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-103">Creates a private link service</span></span>

## <span data-ttu-id="056c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="056c9-104">SYNTAX</span></span>

```
New-AzPrivateLinkService -Name <String> -ResourceGroupName <String> -Location <String>
 -LoadBalancerFrontendIpConfiguration <PSFrontendIPConfiguration[]>
 -IpConfiguration <PSPrivateLinkServiceIpConfiguration[]> [-Visibility <String[]>] [-AutoApproval <String[]>] [-EnableProxyProtocol]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="056c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="056c9-105">DESCRIPTION</span></span>
<span data-ttu-id="056c9-106">**New-AzPrivateLinkService** cmdlet은 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-106">The **New-AzPrivateLinkService** cmdlet creates a private link service</span></span>

## <span data-ttu-id="056c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="056c9-107">EXAMPLES</span></span>

### <span data-ttu-id="056c9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="056c9-108">Example 1</span></span>

<span data-ttu-id="056c9-109">다음 예제에서는 개인 링크 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-109">The following example creates a private link service.</span></span>

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

## <span data-ttu-id="056c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="056c9-110">PARAMETERS</span></span>

### <span data-ttu-id="056c9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="056c9-111">-AsJob</span></span>
<span data-ttu-id="056c9-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="056c9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="056c9-113">-AutoApproval</span><span class="sxs-lookup"><span data-stu-id="056c9-113">-AutoApproval</span></span>
<span data-ttu-id="056c9-114">개인 링크 서비스의 자동 승인 구독</span><span class="sxs-lookup"><span data-stu-id="056c9-114">The auto approval subscriptions of private link service</span></span>

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

### <span data-ttu-id="056c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="056c9-115">-DefaultProfile</span></span>
<span data-ttu-id="056c9-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="056c9-117">-EnableProxyProtocol</span><span class="sxs-lookup"><span data-stu-id="056c9-117">-EnableProxyProtocol</span></span>
<span data-ttu-id="056c9-118">개인 링크 서비스에 대한 프록시 프로토콜을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-118">Enable proxy protocol for the private link service.</span></span>

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

### <span data-ttu-id="056c9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="056c9-119">-Force</span></span>
<span data-ttu-id="056c9-120">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="056c9-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="056c9-121">-IpConfiguration</span></span>
<span data-ttu-id="056c9-122">IP 구성</span><span class="sxs-lookup"><span data-stu-id="056c9-122">The ip configurations</span></span>

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

### <span data-ttu-id="056c9-123">-LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="056c9-123">-LoadBalancerFrontendIpConfiguration</span></span>
<span data-ttu-id="056c9-124">프런트 엔드 IP 구성</span><span class="sxs-lookup"><span data-stu-id="056c9-124">The front end ip configurations</span></span>

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

### <span data-ttu-id="056c9-125">-Location</span><span class="sxs-lookup"><span data-stu-id="056c9-125">-Location</span></span>
<span data-ttu-id="056c9-126">위치.</span><span class="sxs-lookup"><span data-stu-id="056c9-126">location.</span></span>

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

### <span data-ttu-id="056c9-127">-Name</span><span class="sxs-lookup"><span data-stu-id="056c9-127">-Name</span></span>
<span data-ttu-id="056c9-128">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-128">The name of the service.</span></span>

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

### <span data-ttu-id="056c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="056c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="056c9-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-130">The resource group name.</span></span>

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

### <span data-ttu-id="056c9-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="056c9-131">-Tag</span></span>
<span data-ttu-id="056c9-132">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="056c9-133">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="056c9-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="056c9-134">-가시성</span><span class="sxs-lookup"><span data-stu-id="056c9-134">-Visibility</span></span>
<span data-ttu-id="056c9-135">개인 링크 서비스의 가시성 구독</span><span class="sxs-lookup"><span data-stu-id="056c9-135">The visibility subscriptions of private link service</span></span>

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

### <span data-ttu-id="056c9-136">-확인</span><span class="sxs-lookup"><span data-stu-id="056c9-136">-Confirm</span></span>
<span data-ttu-id="056c9-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="056c9-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="056c9-138">-WhatIf</span></span>
<span data-ttu-id="056c9-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="056c9-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="056c9-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="056c9-141">CommonParameters</span></span>
<span data-ttu-id="056c9-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="056c9-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="056c9-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="056c9-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="056c9-144">입력</span><span class="sxs-lookup"><span data-stu-id="056c9-144">INPUTS</span></span>

### <span data-ttu-id="056c9-145">System.String</span><span class="sxs-lookup"><span data-stu-id="056c9-145">System.String</span></span>

### <span data-ttu-id="056c9-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="056c9-146">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration[]</span></span>

### <span data-ttu-id="056c9-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="056c9-147">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceIpConfiguration[]</span></span>

## <span data-ttu-id="056c9-148">출력</span><span class="sxs-lookup"><span data-stu-id="056c9-148">OUTPUTS</span></span>

### <span data-ttu-id="056c9-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="056c9-149">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService</span></span>

## <span data-ttu-id="056c9-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="056c9-150">NOTES</span></span>

## <span data-ttu-id="056c9-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="056c9-151">RELATED LINKS</span></span>

[<span data-ttu-id="056c9-152">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="056c9-152">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="056c9-153">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="056c9-153">Remove-AzPrivateLinkService</span></span>](./Remove-AzPrivateLinkService.md)

[<span data-ttu-id="056c9-154">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="056c9-154">New-AzPrivateLinkServiceIpConfig</span></span>](./New-AzPrivateLinkServiceIpConfig.md)
