---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965040"
---
# <span data-ttu-id="43070-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="43070-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="43070-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43070-102">SYNOPSIS</span></span>
<span data-ttu-id="43070-103">VMSS의 네트워크 인터페이스에 대한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43070-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="43070-104">구문</span><span class="sxs-lookup"><span data-stu-id="43070-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43070-105">설명</span><span class="sxs-lookup"><span data-stu-id="43070-105">DESCRIPTION</span></span>
<span data-ttu-id="43070-106">**New-AzVmssIpConfig** cmdlet은 VMSS(Virtual Machine Scale Set)의 네트워크 인터페이스에 대한 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43070-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="43070-107">이 cmdlet에서 구성을 Add-AzVmssNetworkInterfaceConfiguration *ipConfiguration* 매개 변수로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="43070-108">예제</span><span class="sxs-lookup"><span data-stu-id="43070-108">EXAMPLES</span></span>

### <span data-ttu-id="43070-109">예제 1: VMSS 인터페이스에 대한 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="43070-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="43070-110">이 명령은 ContosoVmssInterface02라는 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="43070-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="43070-111">명령은 이전에 정의된 서브넷 ID를 $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="43070-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="43070-112">명령은 **Add-AzVmssNetworkInterfaceConfiguration** 에서 나중에 사용할 $IPConfiguration 변수에 구성 설정을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="43070-113">예제 2: NAT 풀 설정을 포함하는 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="43070-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="43070-114">이 명령은 ContosoVmssInterface03이라는 IP 구성 개체를 만든 다음 나중에 사용할 $IPConfiguration 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="43070-115">명령은 이전에 정의된 서브넷 ID를 $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="43070-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="43070-116">명령은 나중에 사용할 $IPConfiguration 변수에 구성 설정을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="43070-117">명령은 *LoadBalancerInboundNatPoolsId* 및 *LoadBalancerBackendAddressPoolsId* 매개 변수에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="43070-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="43070-118">PARAMETERS</span></span>

### <span data-ttu-id="43070-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="43070-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="43070-120">부하 저울의 백END 주소 풀에 대한 참조 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="43070-121">확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기의 백던드 주소 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="43070-122">여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43070-123">-DefaultProfile</span></span>
<span data-ttu-id="43070-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43070-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="43070-125">-DnsSetting</span></span>
<span data-ttu-id="43070-126">publicIP 주소에 적용할 dns 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="43070-127">공용IP 주소에 적용할 Dns 설정의 도메인 이름 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="43070-128">도메인 이름 레이블 및 vm 인덱스의 연결은 만들 공용 IP 주소 리소스의 도메인 이름 레이블이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43070-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-129">-Id</span><span class="sxs-lookup"><span data-stu-id="43070-129">-Id</span></span>
<span data-ttu-id="43070-130">ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="43070-131">-IpTag</span></span>
<span data-ttu-id="43070-132">IP 태그 개체의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="43070-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="43070-134">부하 저울의 들어오는 NAT(네트워크 주소 변환) 풀에 대한 참조 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="43070-135">확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기에서 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="43070-136">여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="43070-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="43070-138">부하 저울의 들어오는 NAT 풀에 대한 참조 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="43070-139">확장 집합은 하나의 공용 및 하나의 내부 부하 균형 조정기에서 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="43070-140">여러 확장 집합은 동일한 부하 저울을 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-141">-Name</span><span class="sxs-lookup"><span data-stu-id="43070-141">-Name</span></span>
<span data-ttu-id="43070-142">IP 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-143">-Primary</span><span class="sxs-lookup"><span data-stu-id="43070-143">-Primary</span></span>
<span data-ttu-id="43070-144">네트워크 인터페이스에 IP 구성이 두 개 이상 있는 경우 기본 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="43070-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="43070-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="43070-146">개인 IP 주소에 대한 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="43070-147">기본값은 IPv4로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="43070-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="43070-148">가능한 값은 'IPv4' 및 'IPv6'입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="43070-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="43070-150">공용 IP 주소의 유휴 시간 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="43070-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="43070-152">publicIP 주소 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="43070-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="43070-154">공용 IP 주소에 대한 IP 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="43070-155">기본값은 IPv4로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="43070-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="43070-156">가능한 값은 'IPv4' 및 'IPv6'입니다.</span><span class="sxs-lookup"><span data-stu-id="43070-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="43070-157">-PublicIPPrefix</span></span>
<span data-ttu-id="43070-158">공용 IP 연결선의 ID</span><span class="sxs-lookup"><span data-stu-id="43070-158">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="43070-159">-SubnetId</span></span>
<span data-ttu-id="43070-160">구성에서 VMSS 네트워크 인터페이스를 만드는 서브넷 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43070-161">-확인</span><span class="sxs-lookup"><span data-stu-id="43070-161">-Confirm</span></span>
<span data-ttu-id="43070-162">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="43070-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43070-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43070-163">-WhatIf</span></span>
<span data-ttu-id="43070-164">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="43070-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43070-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="43070-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43070-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43070-166">CommonParameters</span></span>
<span data-ttu-id="43070-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43070-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43070-168">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43070-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43070-169">입력</span><span class="sxs-lookup"><span data-stu-id="43070-169">INPUTS</span></span>

### <span data-ttu-id="43070-170">System.String</span><span class="sxs-lookup"><span data-stu-id="43070-170">System.String</span></span>

### <span data-ttu-id="43070-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="43070-171">System.String[]</span></span>

### <span data-ttu-id="43070-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="43070-172">System.Int32</span></span>

### <span data-ttu-id="43070-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="43070-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="43070-174">출력</span><span class="sxs-lookup"><span data-stu-id="43070-174">OUTPUTS</span></span>

### <span data-ttu-id="43070-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="43070-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="43070-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43070-176">NOTES</span></span>

## <span data-ttu-id="43070-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43070-177">RELATED LINKS</span></span>

[<span data-ttu-id="43070-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="43070-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


