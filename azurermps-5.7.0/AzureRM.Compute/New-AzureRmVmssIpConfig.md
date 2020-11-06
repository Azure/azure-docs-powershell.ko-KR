---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529906"
---
# <span data-ttu-id="ebfda-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="ebfda-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="ebfda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebfda-102">SYNOPSIS</span></span>
<span data-ttu-id="ebfda-103">VMSS의 네트워크 인터페이스에 대 한 IP 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebfda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebfda-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebfda-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebfda-105">DESCRIPTION</span></span>
<span data-ttu-id="ebfda-106">**AzureRmVmssIpConfig** CMDLET은 Vmss (가상 컴퓨터 확장 집합)의 네트워크 인터페이스에 대 한 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ebfda-107">이 cmdlet의 구성을 Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet의 *IPConfiguration* 매개 변수로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="ebfda-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ebfda-108">EXAMPLES</span></span>

### <span data-ttu-id="ebfda-109">예제 1: VMSS 인터페이스에 대 한 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ebfda-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="ebfda-110">이 명령은 ContosoVmssInterface02 이라는 IP 구성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="ebfda-111">이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="ebfda-112">명령은 나중에 **AzureRmVmssNetworkInterfaceConfiguration 추가** 를 사용 하기 위해 $IPConfiguration 변수에 구성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="ebfda-113">예제 2: NAT 풀 설정을 포함 하는 IP 구성 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="ebfda-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="ebfda-114">이 명령은 ContosoVmssInterface03 이라는 IP 구성 개체를 만든 다음 나중에 사용 하기 위해이를 $IPConfiguration 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="ebfda-115">이 명령은 $SubnetId에 저장 되어 있는 이전에 정의 된 서브넷 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="ebfda-116">명령은 나중에 사용 하기 위해 $IPConfiguration 변수의 구성 설정을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="ebfda-117">명령에서 *LoadBalancerInboundNatPoolsId* 및 *LoadBalancerBackendAddressPoolsId* 매개 변수에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="ebfda-118">변수</span><span class="sxs-lookup"><span data-stu-id="ebfda-118">PARAMETERS</span></span>

### <span data-ttu-id="ebfda-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="ebfda-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="ebfda-120">부하 분산 장치의 백 엔드 주소 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="ebfda-121">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 백엔드 주소 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="ebfda-122">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="ebfda-123">-DnsSetting</span></span>
<span data-ttu-id="ebfda-124">PublicIP 주소에 적용 되는 dns 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="ebfda-125">PublicIP 주소에 적용 될 Dns 설정의 도메인 이름 레이블</span><span class="sxs-lookup"><span data-stu-id="ebfda-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="ebfda-126">도메인 이름 레이블과 vm 인덱스의 연결은 만들 공용 IP 주소 리소스의 도메인 이름 레이블이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-127">-Id</span><span class="sxs-lookup"><span data-stu-id="ebfda-127">-Id</span></span>
<span data-ttu-id="ebfda-128">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-128">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="ebfda-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="ebfda-130">부하 분산 장치의 들어오는 NAT (network address translation) 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="ebfda-131">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="ebfda-132">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-132">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="ebfda-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="ebfda-134">부하 분산 장치의 들어오는 NAT 풀에 대 한 참조 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="ebfda-135">확장 집합은 하나의 공용 및 하나의 내부 부하 분산 장치에 대 한 들어오는 NAT 풀을 참조할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="ebfda-136">여러 배율 집합은 동일한 부하 분산 장치를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-137">-이름</span><span class="sxs-lookup"><span data-stu-id="ebfda-137">-Name</span></span>
<span data-ttu-id="ebfda-138">IP 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-138">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="ebfda-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="ebfda-140">Ip 구성을 IPv4 또는 IPv6 중 하나로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="ebfda-141">기본값은 IPv4로 간주 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="ebfda-142">사용할 수 있는 값은 ' IPv4 ' 및 ' IPv6 '입니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ebfda-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="ebfda-144">공용 IP 주소의 유휴 시간 제한</span><span class="sxs-lookup"><span data-stu-id="ebfda-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ebfda-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="ebfda-146">PublicIP 주소 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-146">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ebfda-147">-SubnetId</span></span>
<span data-ttu-id="ebfda-148">구성에서 VMSS 네트워크 인터페이스를 만드는 서브넷 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-149">-확인</span><span class="sxs-lookup"><span data-stu-id="ebfda-149">-Confirm</span></span>
<span data-ttu-id="ebfda-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebfda-151">-WhatIf</span></span>
<span data-ttu-id="ebfda-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebfda-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebfda-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebfda-154">CommonParameters</span></span>
<span data-ttu-id="ebfda-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebfda-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebfda-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebfda-157">입력</span><span class="sxs-lookup"><span data-stu-id="ebfda-157">INPUTS</span></span>

### <span data-ttu-id="ebfda-158">않아야</span><span class="sxs-lookup"><span data-stu-id="ebfda-158">None</span></span>
<span data-ttu-id="ebfda-159">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ebfda-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ebfda-160">출력</span><span class="sxs-lookup"><span data-stu-id="ebfda-160">OUTPUTS</span></span>

## <span data-ttu-id="ebfda-161">상속자</span><span class="sxs-lookup"><span data-stu-id="ebfda-161">NOTES</span></span>

## <span data-ttu-id="ebfda-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebfda-162">RELATED LINKS</span></span>

[<span data-ttu-id="ebfda-163">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ebfda-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


