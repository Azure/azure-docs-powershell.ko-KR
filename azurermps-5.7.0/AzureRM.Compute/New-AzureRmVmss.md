---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmss.md
ms.openlocfilehash: e94cc565c2f22134f6bd4092247fbfa1f5a98b8b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529016"
---
# <span data-ttu-id="04ff7-101">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-101">New-AzureRmVmss</span></span>

## <span data-ttu-id="04ff7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="04ff7-103">VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-103">Creates a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ff7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04ff7-104">SYNTAX</span></span>

```
New-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ff7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="04ff7-106">**AzureRmVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-106">The **New-AzureRmVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="04ff7-107">이 cmdlet은 **VirtualMachineScaleSet** 개체를 입력으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-107">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="04ff7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="04ff7-108">EXAMPLES</span></span>

### <span data-ttu-id="04ff7-109">예제 1: VMSS 만들기</span><span class="sxs-lookup"><span data-stu-id="04ff7-109">Example 1: Create a VMSS</span></span>
```
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzureRmResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzureRmStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzureRmVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzureRmVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzureRmVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzureRmPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzureRmPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzureRmLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzureRmLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzureRmLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzureRmLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzureRmLoadBalancer -Name $LBName -ResourceGroupName $RGName

# New VMSS Parameters
$VMSSName = "VMSS" + $RGName;

$AdminUsername = "Admin01";
$AdminPassword = "p4ssw0rd@123" + $RGName;

$PublisherName = "MicrosoftWindowsServer" 
$Offer         = "WindowsServer" 
$Sku           = "2012-R2-Datacenter" 
$Version       = "latest"
        
$VHDContainer = "https://" + $STOName + ".blob.core.contoso.net/" + $VMSSName;

$ExtName = "CSETest";
$Publisher = "Microsoft.Compute";
$ExtType = "BGInfo";
$ExtVer = "2.1";

#IP Config for the NIC
$IPCfg = New-AzureRmVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzureRmVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzureRmVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzureRmVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzureRmVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzureRmVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzureRmVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="04ff7-110">다음 복잡 한 예제는 VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-110">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="04ff7-111">첫 번째 명령은 지정 된 이름과 위치를 사용 하 여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-111">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="04ff7-112">두 번째 명령은 **새 AzureRmStorageAccount** cmdlet을 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-112">The second command uses the **New-AzureRmStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="04ff7-113">세 번째 명령은 **AzureRmStorageAccount** cmdlet을 사용 하 여 두 번째 명령에서 만든 저장소 계정을 가져오고 결과를 $STOAccount 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-113">The third command then uses the **Get-AzureRmStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="04ff7-114">다섯 번째 명령은 **AzureRmVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 서브넷을 만들고 결과를 $SubNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-114">The fifth command uses the **New-AzureRmVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="04ff7-115">여섯 번째 명령은 **AzureRmVirtualNetwork** cmdlet을 사용 하 여 가상 네트워크를 만들고 결과를 $VNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-115">The sixth command uses the **New-AzureRmVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="04ff7-116">일곱 번째 명령은 **AzureRmVirtualNetwork** 를 사용 하 여 여섯 번째 명령에서 만든 가상 네트워크에 대 한 정보를 가져오고이 정보를 $VNet 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-116">The seventh command uses the **Get-AzureRmVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="04ff7-117">여덟째 및 아홉 번째 명령은 **New-AzureRmPublicIpAddress** 및 **get-AzureRmPublicIpAddress** 를 사용 하 여 해당 공용 IP 주소에서 정보를 만들고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-117">The eighth and ninth command uses the **New-AzureRmPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="04ff7-118">명령은 $PubIP 라는 변수에 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-118">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="04ff7-119">10 번째 명령은 **AzureRmLoadBalancerFrontendIpConfig** cmdlet을 사용 하 여 프런트 엔드 부하 분산 장치를 만들고 결과를 $Frontend 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-119">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="04ff7-120">11 번째 명령은 **AzureRmLoadBalancerBackendAddressPoolConfig** 를 사용 하 여 백 엔드 주소 풀 구성을 만들고 그 결과를 $BackendAddressPool 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-120">The eleventh command uses the **New-AzureRmLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="04ff7-121">12 번째 명령은 **New-AzureRmLoadBalancerProbeConfig** 를 사용 하 여 프로브를 만들고 $Probe 이라는 변수에 프로브 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-121">The twelfth command uses the **New-AzureRmLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="04ff7-122">Thirteenth 명령은 **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet을 사용 하 여 부하 분산 장치 인바운드 NAT (network address translation) 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-122">The thirteenth command uses the **New-AzureRmLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="04ff7-123">14 번째 명령은 **AzureRmLoadBalancerRuleConfig** 를 사용 하 여 부하 분산 장치 규칙 구성을 만들고 그 결과를 $LBRule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-123">The fourteenth command uses the **New-AzureRmLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="04ff7-124">15 번째 명령은 **새 AzureRmLoadBalancer** cmdlet을 사용 하 여 부하 분산 장치를 만들고 결과를 $ActualLb 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-124">The fifteenth command uses the **New-AzureRmLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="04ff7-125">16 번째 명령은 **AzureRmLoadBalancer** 를 사용 하 여 15 번째 명령에서 만든 부하 분산 장치에 대 한 정보를 가져오고이 정보를 $ExpectedLb 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-125">The sixteenth command uses the **Get-AzureRmLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="04ff7-126">Seventeenth 명령은 **새 AzureRmVmssIPConfig** cmdlet을 사용 하 여 VMSS IP 구성을 만들고이 정보를 $IPCfg 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-126">The seventeenth command uses the **New-AzureRmVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="04ff7-127">Eighteenth 명령은 **새 AzureRmVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-127">The eighteenth command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="04ff7-128">19 명령은 **새 AzureRmVmss** cmdlet을 사용 하 여 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-128">The nineteenth command uses the **New-AzureRmVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="04ff7-129">변수</span><span class="sxs-lookup"><span data-stu-id="04ff7-129">PARAMETERS</span></span>

### <span data-ttu-id="04ff7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ff7-130">-ResourceGroupName</span></span>
<span data-ttu-id="04ff7-131">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-131">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff7-132">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="04ff7-132">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="04ff7-133">이 cmdlet이 만드는 VMSS의 속성을 포함 하는 **VirtualMachineScaleSet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-133">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff7-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="04ff7-134">-VMScaleSetName</span></span>
<span data-ttu-id="04ff7-135">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-135">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04ff7-136">-확인</span><span class="sxs-lookup"><span data-stu-id="04ff7-136">-Confirm</span></span>
<span data-ttu-id="04ff7-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ff7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ff7-138">-WhatIf</span></span>
<span data-ttu-id="04ff7-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="04ff7-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ff7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ff7-141">CommonParameters</span></span>
<span data-ttu-id="04ff7-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ff7-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ff7-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ff7-144">입력</span><span class="sxs-lookup"><span data-stu-id="04ff7-144">INPUTS</span></span>

### <span data-ttu-id="04ff7-145">않아야</span><span class="sxs-lookup"><span data-stu-id="04ff7-145">None</span></span>
<span data-ttu-id="04ff7-146">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04ff7-147">출력</span><span class="sxs-lookup"><span data-stu-id="04ff7-147">OUTPUTS</span></span>

### <span data-ttu-id="04ff7-148">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04ff7-148">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="04ff7-149">상속자</span><span class="sxs-lookup"><span data-stu-id="04ff7-149">NOTES</span></span>

## <span data-ttu-id="04ff7-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04ff7-150">RELATED LINKS</span></span>

[<span data-ttu-id="04ff7-151">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-151">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="04ff7-152">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-152">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="04ff7-153">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-153">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="04ff7-154">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-154">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="04ff7-155">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-155">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="04ff7-156">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-156">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="04ff7-157">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="04ff7-157">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


