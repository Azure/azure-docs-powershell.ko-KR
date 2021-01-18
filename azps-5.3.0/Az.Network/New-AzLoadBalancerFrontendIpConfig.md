---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496668"
---
# <span data-ttu-id="8ac16-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac16-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="8ac16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ac16-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac16-103">부하 균형 조정에 대한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="8ac16-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ac16-104">SYNTAX</span></span>

### <span data-ttu-id="8ac16-105">SetByResourceSubnet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8ac16-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="8ac16-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ac16-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ac16-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ac16-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ac16-111">설명</span><span class="sxs-lookup"><span data-stu-id="8ac16-111">DESCRIPTION</span></span>
<span data-ttu-id="8ac16-112">**New-AzLoadBalancerFrontendIpConfig** cmdlet은 Azure Load Balancer에 대한 프런트 엔드 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8ac16-113">예제</span><span class="sxs-lookup"><span data-stu-id="8ac16-113">EXAMPLES</span></span>

### <span data-ttu-id="8ac16-114">예제 1: 부하 균형 조정에 대한 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="8ac16-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="8ac16-115">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 MyPublicIP라는 동적 공용 IP 주소를 만든 다음, $publicip 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="8ac16-116">두 번째 명령은 다음 명령의 공용 IP 주소를 사용하여 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 $publicip.</span><span class="sxs-lookup"><span data-stu-id="8ac16-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="8ac16-117">예제 2: IP 앞에 IP를 사용하여 부하 분배기용 프런트 엔드 IP 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="8ac16-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="8ac16-118">첫 번째 명령은 MyResourceGroup이라는 리소스 그룹에 길이 28의 MyPublicIP라는 공용 IP를 만든 다음, $publicipprefix 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="8ac16-119">두 번째 명령은 다음 명령에서 공용 IP 접두사로 FrontendIpConfig01이라는 프런트 엔드 IP 구성을 $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="8ac16-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="8ac16-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ac16-120">PARAMETERS</span></span>

### <span data-ttu-id="8ac16-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ac16-121">-DefaultProfile</span></span>
<span data-ttu-id="8ac16-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ac16-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8ac16-123">-Name</span></span>
<span data-ttu-id="8ac16-124">이 cmdlet에서 만드는 프런트 엔드 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="8ac16-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-125">-PrivateIpAddress</span></span>
<span data-ttu-id="8ac16-126">부하 균형 조정의 개인 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="8ac16-127">서브넷 매개 변수도 지정하는 경우 이 매개 *변수를 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="8ac16-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="8ac16-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="8ac16-129">IP 구성의 개인 IP 주소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-129">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-130">-PublicIpAddress</span></span>
<span data-ttu-id="8ac16-131">프런트 엔드 IP 구성과 연결하기 위한 **PublicIpAddress** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="8ac16-132">-PublicIpAddressId</span></span>
<span data-ttu-id="8ac16-133">프런트 엔드 IP 구성과 연결하기 위한 **PublicIpAddress** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="8ac16-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="8ac16-135">프런트 엔드 IP 구성과 연결하기 위한 **PublicIpAddressPrefix** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="8ac16-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="8ac16-137">프런트 엔드 IP 구성과 연결하기 위한 **PublicIpAddressPrefix** 개체의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="8ac16-138">-Subnet</span></span>
<span data-ttu-id="8ac16-139">프런트 엔드 IP **구성을** 만들 서브넷 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="8ac16-140">-SubnetId</span></span>
<span data-ttu-id="8ac16-141">프런트 엔드 IP 구성을 만들 서브넷의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac16-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="8ac16-142">-Zone</span></span>
<span data-ttu-id="8ac16-143">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="8ac16-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ac16-144">-Confirm</span></span>
<span data-ttu-id="8ac16-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ac16-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ac16-146">-WhatIf</span></span>
<span data-ttu-id="8ac16-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8ac16-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ac16-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ac16-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac16-149">CommonParameters</span></span>
<span data-ttu-id="8ac16-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ac16-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac16-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ac16-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac16-152">입력</span><span class="sxs-lookup"><span data-stu-id="8ac16-152">INPUTS</span></span>

### <span data-ttu-id="8ac16-153">System.String</span><span class="sxs-lookup"><span data-stu-id="8ac16-153">System.String</span></span>

### <span data-ttu-id="8ac16-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="8ac16-154">System.String[]</span></span>

### <span data-ttu-id="8ac16-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8ac16-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="8ac16-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="8ac16-157">출력</span><span class="sxs-lookup"><span data-stu-id="8ac16-157">OUTPUTS</span></span>

### <span data-ttu-id="8ac16-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ac16-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="8ac16-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ac16-159">NOTES</span></span>

## <span data-ttu-id="8ac16-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ac16-160">RELATED LINKS</span></span>

[<span data-ttu-id="8ac16-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac16-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8ac16-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac16-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8ac16-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="8ac16-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="8ac16-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac16-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="8ac16-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8ac16-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


