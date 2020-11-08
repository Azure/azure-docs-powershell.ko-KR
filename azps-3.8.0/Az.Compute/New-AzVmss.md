---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: 914d942620eea7517b2bac635399fd7d1b3c1307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043675"
---
# <span data-ttu-id="a2c8d-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-101">New-AzVmss</span></span>

## <span data-ttu-id="a2c8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2c8d-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c8d-103">VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-103">Creates a VMSS.</span></span>

## <span data-ttu-id="a2c8d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a2c8d-104">SYNTAX</span></span>

### <span data-ttu-id="a2c8d-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2c8d-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c8d-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="a2c8d-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-Priority <String>]
 [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c8d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a2c8d-107">DESCRIPTION</span></span>
<span data-ttu-id="a2c8d-108">**AzVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="a2c8d-109">간단한 매개 변수 집합 ()을 사용 `SimpleParameterSet` 하 여 미리 설정 된 VMSS 및 연결 된 리소스를 빠르게 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="a2c8d-110">기본 매개 변수 집합 ()을 사용 하 여 `DefaultParameter` 추가 하기 전에 VMSS 및 연결 된 각 리소스의 각 구성 요소를 세부적으로 구성 해야 하는 고급 시나리오를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="a2c8d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a2c8d-111">EXAMPLES</span></span>

### <span data-ttu-id="a2c8d-112">예제 1: 다음을 사용 하 여 VMSS 만들기 **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a2c8d-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="a2c8d-113">위의 명령은 이름으로 다음을 만듭니다 `$vmssName` .</span><span class="sxs-lookup"><span data-stu-id="a2c8d-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="a2c8d-114">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="a2c8d-114">A Resource Group</span></span>
* <span data-ttu-id="a2c8d-115">가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="a2c8d-115">A virtual network</span></span>
* <span data-ttu-id="a2c8d-116">부하 분산 장치</span><span class="sxs-lookup"><span data-stu-id="a2c8d-116">A load balancer</span></span>
* <span data-ttu-id="a2c8d-117">공용 IP</span><span class="sxs-lookup"><span data-stu-id="a2c8d-117">A public IP</span></span>
* <span data-ttu-id="a2c8d-118">2 개의 인스턴스가 있는 VMSS</span><span class="sxs-lookup"><span data-stu-id="a2c8d-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="a2c8d-119">VMSS의 Vm에 대해 선택 된 기본 이미지 `2016-Datacenter Windows Server` 와 SKU는 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="a2c8d-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="a2c8d-120">예제 2: 다음을 사용 하 여 VMSS 만들기 **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="a2c8d-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
```powershell
# Common
$LOC = "WestUs";
$RGName = "rgkyvms";

New-AzResourceGroup -Name $RGName -Location $LOC -Force;

# SRP
$STOName = "STO" + $RGName;
$STOType = "Standard_GRS";
New-AzStorageAccount -ResourceGroupName $RGName -Name $STOName -Location $LOC -Type $STOType;
$STOAccount = Get-AzStorageAccount -ResourceGroupName $RGName -Name $STOName; 

# NRP
$SubNet = New-AzVirtualNetworkSubnetConfig -Name ("subnet" + $RGName) -AddressPrefix "10.0.0.0/24";
$VNet = New-AzVirtualNetwork -Force -Name ("vnet" + $RGName) -ResourceGroupName $RGName -Location $LOC -AddressPrefix "10.0.0.0/16" -DnsServer "10.1.1.1" -Subnet $SubNet;
$VNet = Get-AzVirtualNetwork -Name ('vnet' + $RGName) -ResourceGroupName $RGName;
$SubNetId = $VNet.Subnets[0].Id;

$PubIP = New-AzPublicIpAddress -Force -Name ("PubIP" + $RGName) -ResourceGroupName $RGName -Location $LOC -AllocationMethod Dynamic -DomainNameLabel ("PubIP" + $RGName);
$PubIP = Get-AzPublicIpAddress -Name ("PubIP"  + $RGName) -ResourceGroupName $RGName;

# Create LoadBalancer
$FrontendName = "fe" + $RGName
$BackendAddressPoolName = "bepool" + $RGName
$ProbeName = "vmssprobe" + $RGName
$InboundNatPoolName  = "innatpool" + $RGName
$LBRuleName = "lbrule" + $RGName
$LBName = "vmsslb" + $RGName

$Frontend = New-AzLoadBalancerFrontendIpConfig -Name $FrontendName -PublicIpAddress $PubIP
$BackendAddressPool = New-AzLoadBalancerBackendAddressPoolConfig -Name $BackendAddressPoolName
$Probe = New-AzLoadBalancerProbeConfig -Name $ProbeName -RequestPath healthcheck.aspx -Protocol http -Port 80 -IntervalInSeconds 15 -ProbeCount 2
$InboundNatPool = New-AzLoadBalancerInboundNatPoolConfig -Name $InboundNatPoolName  -FrontendIPConfigurationId `
    $Frontend.Id -Protocol Tcp -FrontendPortRangeStart 3360 -FrontendPortRangeEnd 3362 -BackendPort 3370;
$LBRule = New-AzLoadBalancerRuleConfig -Name $LBRuleName `
    -FrontendIPConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -Protocol Tcp -FrontendPort 80 -BackendPort 80 `
    -IdleTimeoutInMinutes 15 -EnableFloatingIP -LoadDistribution SourceIP;
$ActualLb = New-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName -Location $LOC `
    -FrontendIpConfiguration $Frontend -BackendAddressPool $BackendAddressPool `
    -Probe $Probe -LoadBalancingRule $LBRule -InboundNatPool $InboundNatPool;
$ExpectedLb = Get-AzLoadBalancer -Name $LBName -ResourceGroupName $RGName

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
$IPCfg = New-AzVmssIPConfig -Name "Test" `
    -LoadBalancerInboundNatPoolsId $ExpectedLb.InboundNatPools[0].Id `
    -LoadBalancerBackendAddressPoolsId $ExpectedLb.BackendAddressPools[0].Id `
    -SubnetId $SubNetId;
            
#VMSS Config
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_A2" -UpgradePolicyMode "Automatic" `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test" -Primary $True -IPConfiguration $IPCfg `
    | Add-AzVmssNetworkInterfaceConfiguration -Name "Test2"  -IPConfiguration $IPCfg `
    | Set-AzVmssOSProfile -ComputerNamePrefix "Test"  -AdminUsername $AdminUsername -AdminPassword $AdminPassword `
    | Set-AzVmssStorageProfile -Name "Test"  -OsDiskCreateOption 'FromImage' -OsDiskCaching "None" `
    -ImageReferenceOffer $Offer -ImageReferenceSku $Sku -ImageReferenceVersion $Version `
    -ImageReferencePublisher $PublisherName -VhdContainer $VHDContainer `
    | Add-AzVmssExtension -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True

#Create the VMSS
New-AzVmss -ResourceGroupName $RGName -Name $VMSSName -VirtualMachineScaleSet $VMSS;
```

<span data-ttu-id="a2c8d-121">위의 복잡 한 예에서는 VMSS를 만들며 다음은 발생 하는 작업에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="a2c8d-122">첫 번째 명령은 지정 된 이름과 위치를 사용 하 여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="a2c8d-123">두 번째 명령은 **새 AzStorageAccount** cmdlet을 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="a2c8d-124">세 번째 명령은 **AzStorageAccount** cmdlet을 사용 하 여 두 번째 명령에서 만든 저장소 계정을 가져오고 결과를 $STOAccount 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="a2c8d-125">다섯 번째 명령은 **AzVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 서브넷을 만들고 결과를 $SubNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="a2c8d-126">여섯 번째 명령은 **AzVirtualNetwork** cmdlet을 사용 하 여 가상 네트워크를 만들고 결과를 $VNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="a2c8d-127">일곱 번째 명령은 **AzVirtualNetwork** 를 사용 하 여 여섯 번째 명령에서 만든 가상 네트워크에 대 한 정보를 가져오고이 정보를 $VNet 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="a2c8d-128">여덟째 및 아홉 번째 명령은 **New-AzPublicIpAddress** 및 **get-AzureRmPublicIpAddress** 를 사용 하 여 해당 공용 IP 주소에서 정보를 만들고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="a2c8d-129">명령은 $PubIP 라는 변수에 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="a2c8d-130">10 번째 명령은 **AzureRmLoadBalancerFrontendIpConfig** cmdlet을 사용 하 여 프런트 엔드 부하 분산 장치를 만들고 결과를 $Frontend 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="a2c8d-131">11 번째 명령은 **AzLoadBalancerBackendAddressPoolConfig** 를 사용 하 여 백 엔드 주소 풀 구성을 만들고 그 결과를 $BackendAddressPool 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="a2c8d-132">12 번째 명령은 **New-AzLoadBalancerProbeConfig** 를 사용 하 여 프로브를 만들고 $Probe 이라는 변수에 프로브 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="a2c8d-133">Thirteenth 명령은 **New-AzLoadBalancerInboundNatPoolConfig** cmdlet을 사용 하 여 부하 분산 장치 인바운드 NAT (network address translation) 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="a2c8d-134">14 번째 명령은 **AzLoadBalancerRuleConfig** 를 사용 하 여 부하 분산 장치 규칙 구성을 만들고 그 결과를 $LBRule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="a2c8d-135">15 번째 명령은 **새 AzLoadBalancer** cmdlet을 사용 하 여 부하 분산 장치를 만들고 결과를 $ActualLb 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="a2c8d-136">16 번째 명령은 **AzLoadBalancer** 를 사용 하 여 15 번째 명령에서 만든 부하 분산 장치에 대 한 정보를 가져오고이 정보를 $ExpectedLb 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="a2c8d-137">Seventeenth 명령은 **새 AzVmssIPConfig** cmdlet을 사용 하 여 VMSS IP 구성을 만들고이 정보를 $IPCfg 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="a2c8d-138">Eighteenth 명령은 **새 AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="a2c8d-139">19 명령은 **새 AzVmss** cmdlet을 사용 하 여 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="a2c8d-140">변수</span><span class="sxs-lookup"><span data-stu-id="a2c8d-140">PARAMETERS</span></span>

### <span data-ttu-id="a2c8d-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="a2c8d-141">-AllocationMethod</span></span>
<span data-ttu-id="a2c8d-142">확장 집합의 공용 IP 주소에 대 한 배정 방법 (정적 또는 동적)입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="a2c8d-143">값을 지정 하지 않으면 정적 할당이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-143">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c8d-144">-AsJob</span></span>
<span data-ttu-id="a2c8d-145">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a2c8d-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-146">-BackendPoolName</span></span>
<span data-ttu-id="a2c8d-147">이 배율 집합에 대 한 부하 분산에 사용할 백 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="a2c8d-148">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 새 백엔드 풀이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="a2c8d-149">-BackendPort</span></span>
<span data-ttu-id="a2c8d-150">배율 집합 부하 분산 장치에서 확장 집합의 Vm과 통신 하는 데 사용 하는 백 엔드 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="a2c8d-151">값을 지정 하지 않으면 포트 3389 및 5985이 Windows VM에 사용 되 고, 포트 22가 Linux 용 Vm에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-152">-Credential</span><span class="sxs-lookup"><span data-stu-id="a2c8d-152">-Credential</span></span>
<span data-ttu-id="a2c8d-153">이 확장 집합의 Vm에 대 한 관리자 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="a2c8d-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="a2c8d-155">데이터 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-155">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c8d-156">-DefaultProfile</span></span>
<span data-ttu-id="a2c8d-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c8d-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="a2c8d-158">-DomainNameLabel</span></span>
<span data-ttu-id="a2c8d-159">이 배율 집합에 대 한 FQDN (공용 Fully-Qualified 도메인 이름)의 도메인 이름 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="a2c8d-160">이는 확장 집합에 자동으로 할당 되는 도메인 이름의 첫 번째 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="a2c8d-161">자동으로 할당 된 도메인 이름에는 양식 (.)을 사용 합니다 <DomainNameLabel> . <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a2c8d-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="a2c8d-162">값을 지정 하지 않으면 기본 도메인 이름 레이블이 and로 연결 됩니다 <ScaleSetName> <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="a2c8d-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="a2c8d-163">-EnableUltraSSD</span></span>
<span data-ttu-id="a2c8d-164">크기 조정 집합의 Vm에 대해 UltraSSD 디스크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-165">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c8d-165">-EvictionPolicy</span></span>
<span data-ttu-id="a2c8d-166">낮은 우선 순위의 가상 머신 확장 집합에 대 한 제거 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-166">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="a2c8d-167">' 할당 취소 ' 및 ' 삭제 ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-167">Only supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-168">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-168">-FrontendPoolName</span></span>
<span data-ttu-id="a2c8d-169">확장 집합 부하 분산 장치에서 사용할 프런트 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-169">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="a2c8d-170">값을 지정 하지 않으면 새 프런트 엔드 주소 풀이 생성 되며, 여기에는 배율 집합과 동일한 이름이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-170">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-171">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-171">-ImageName</span></span>
<span data-ttu-id="a2c8d-172">이 배율 집합의 Vm에 대 한 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-172">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="a2c8d-173">값을 제공 하지 않으면 "Windows Server 2016 DataCenter" 이미지가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-173">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-174">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="a2c8d-174">-InstanceCount</span></span>
<span data-ttu-id="a2c8d-175">확장 집합의 VM 이미지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-175">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="a2c8d-176">값을 지정 하지 않으면 2 인스턴스가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-176">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-177">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-177">-LoadBalancerName</span></span>
<span data-ttu-id="a2c8d-178">이 배율 집합에 사용할 부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-178">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="a2c8d-179">값을 지정 하지 않으면 배율 집합과 동일한 이름을 사용 하는 새 부하 분산이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-179">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-180">-위치</span><span class="sxs-lookup"><span data-stu-id="a2c8d-180">-Location</span></span>
<span data-ttu-id="a2c8d-181">이 배율 집합이 생성 되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-181">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="a2c8d-182">값을 지정 하지 않으면 매개 변수에서 참조 되는 다른 리소스의 위치에서 위치가 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-182">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-183">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="a2c8d-183">-MaxPrice</span></span>
<span data-ttu-id="a2c8d-184">낮은 우선 순위의 가상 컴퓨터 배율 집합에 대 한 최대 청구 금액입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-184">The max price of the billing of a low priority virtual machine scale set.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-185">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="a2c8d-185">-NatBackendPort</span></span>
<span data-ttu-id="a2c8d-186">인바운드 네트워크 주소 변환을 위한 백 엔드 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-186">Backend port for inbound network address translation.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-187">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="a2c8d-187">-Priority</span></span>
<span data-ttu-id="a2c8d-188">확장 집합의 가상 컴퓨터에 대 한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-188">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="a2c8d-189">' 일반 ', ' 스폿 ' 및 ' Low ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-189">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="a2c8d-190">' 일반 '은 일반 가상 컴퓨터에 대 한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-190">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="a2c8d-191">' 스폿 '은 가상 컴퓨터를 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-191">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="a2c8d-192">' Low '는 스폿 가상 컴퓨터에도 사용할 수 있지만 ' 스폿 '으로 대체 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-192">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="a2c8d-193">' 낮음 ' 대신 ' 스폿 '을 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-193">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-194">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="a2c8d-194">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="a2c8d-195">이 배율 집합에 사용할 근접 배치 그룹의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-195">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-196">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-196">-PublicIpAddressName</span></span>
<span data-ttu-id="a2c8d-197">이 배율 집합에 사용할 공용 IP 주소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-197">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="a2c8d-198">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 새 공용 IPAddress가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-198">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-199">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-199">-ResourceGroupName</span></span>
<span data-ttu-id="a2c8d-200">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-200">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="a2c8d-201">값을 지정 하지 않으면 새 ResourceGroup이 배율 집합과 동일한 이름을 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-201">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-202">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="a2c8d-202">-ScaleInPolicy</span></span>
<span data-ttu-id="a2c8d-203">가상 컴퓨터 배율 집합의 크기 조정을 할 때 따라야 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-203">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="a2c8d-204">사용할 수 있는 값은 ' Default ', ' OldestVM ' 및 ' NewestVM '입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-204">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="a2c8d-205">' Default ' 가상 컴퓨터 배율 집합이에서 크기를 조정 하면 영역에 대해 먼저 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-205">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="a2c8d-206">그런 다음, 최대한 다양 한 장애 도메인에 분산 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-206">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="a2c8d-207">각 장애 도메인 내에서 제거 하도록 선택 된 가상 머신은 확장 기능에서 보호 되지 않는 최신 것입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-207">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="a2c8d-208">' OldestVM ' 가상 컴퓨터 크기 조정 집합을 확장 하는 동안에는 스케일에서 보호 되지 않는 가장 오래 된 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-208">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="a2c8d-209">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-209">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="a2c8d-210">각 영역 내에서 보호 되지 않는 가장 오래 된 가상 컴퓨터는 제거 하도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-210">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="a2c8d-211">' NewestVM ' 가상 컴퓨터 배율 집합이 확장 되는 경우에는 스케일에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-211">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="a2c8d-212">영역 가상 컴퓨터 배율 집합의 경우에는 맨 먼저 범위에서 배율 집합이 조정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-212">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="a2c8d-213">각 영역 내에서 보호 되지 않는 최신 가상 컴퓨터가 제거 되도록 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-213">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-214">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-214">-SecurityGroupName</span></span>
<span data-ttu-id="a2c8d-215">이 배율 집합에 적용할 네트워크 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-215">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="a2c8d-216">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 기본 네트워크 보안 그룹이 만들어지고 배율 집합에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-216">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-217">-Single배치 그룹</span><span class="sxs-lookup"><span data-stu-id="a2c8d-217">-SinglePlacementGroup</span></span>
<span data-ttu-id="a2c8d-218">이를 사용 하 여 단일 배치 그룹의 배율 집합을 만들 수 있습니다. 기본값은 여러 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-218">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-219">-SkipExtensionsOnOverprovisionedVMs</span><span class="sxs-lookup"><span data-stu-id="a2c8d-219">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="a2c8d-220">추가 과잉 프로 비전 된 Vm에서 확장이 실행 되지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-220">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-221">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a2c8d-221">-SubnetAddressPrefix</span></span>
<span data-ttu-id="a2c8d-222">이 ScaleSet에서 사용할 서브넷의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-222">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="a2c8d-223">값을 제공 하지 않으면 기본 서브넷 설정 (192.168.1.0/24)이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-223">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-224">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-224">-SubnetName</span></span>
<span data-ttu-id="a2c8d-225">이 배율 집합에 사용할 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-225">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="a2c8d-226">값을 제공 하지 않으면 크기 조정 집합과 같은 이름으로 새 서브넷이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-226">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-227">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a2c8d-227">-SystemAssignedIdentity</span></span>
<span data-ttu-id="a2c8d-228">매개 변수가 있는 경우, 확장 집합의 VM이 자동으로 생성 되는 관리 시스템 id에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-228">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="a2c8d-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="a2c8d-230">이 확장 집합의 VM 인스턴스에 대 한 업그레이드 정책 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-230">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="a2c8d-231">업그레이드 정책은 자동, 수동 또는 롤링 업그레이드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-231">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-232">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a2c8d-232">-UserAssignedIdentity</span></span>
<span data-ttu-id="a2c8d-233">확장 집합의 VM에 할당 해야 하는 관리 되는 서비스 id의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-233">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a2c8d-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a2c8d-235">이 cmdlet이 만드는 VMSS의 속성을 포함 하는 **VirtualMachineScaleSet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-235">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-236">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-236">-VirtualNetworkName</span></span>
<span data-ttu-id="a2c8d-237">이 배율 집합에 사용할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-237">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="a2c8d-238">값을 지정 하지 않으면 배율 집합과 동일한 이름을 가진 새 가상 네트워크가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-238">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-239">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a2c8d-239">-VMScaleSetName</span></span>
<span data-ttu-id="a2c8d-240">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-240">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-241">-VmSize</span><span class="sxs-lookup"><span data-stu-id="a2c8d-241">-VmSize</span></span>
<span data-ttu-id="a2c8d-242">이 배율 집합의 VM 인스턴스 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-242">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="a2c8d-243">크기를 지정 하지 않으면 기본 크기 (Standard_DS1_v2)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-243">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-244">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a2c8d-244">-VnetAddressPrefix</span></span>
<span data-ttu-id="a2c8d-245">이 배율 집합에 사용 되는 가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-245">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="a2c8d-246">값을 제공 하지 않으면 기본 가상 네트워크 주소 접두사 설정 (192.168.0.0/16)이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-246">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-247">-Zone</span><span class="sxs-lookup"><span data-stu-id="a2c8d-247">-Zone</span></span>
<span data-ttu-id="a2c8d-248">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-248">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-249">-확인</span><span class="sxs-lookup"><span data-stu-id="a2c8d-249">-Confirm</span></span>
<span data-ttu-id="a2c8d-250">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-250">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-251">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c8d-251">-WhatIf</span></span>
<span data-ttu-id="a2c8d-252">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-252">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c8d-253">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-253">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c8d-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c8d-254">CommonParameters</span></span>
<span data-ttu-id="a2c8d-255">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c8d-256">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c8d-257">입력</span><span class="sxs-lookup"><span data-stu-id="a2c8d-257">INPUTS</span></span>

### <span data-ttu-id="a2c8d-258">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a2c8d-258">System.String</span></span>

### <span data-ttu-id="a2c8d-259">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-259">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a2c8d-260">System.webserver. List ' 1 [[System.webserver], CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a2c8d-260">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="a2c8d-261">출력</span><span class="sxs-lookup"><span data-stu-id="a2c8d-261">OUTPUTS</span></span>

### <span data-ttu-id="a2c8d-262">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="a2c8d-262">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a2c8d-263">상속자</span><span class="sxs-lookup"><span data-stu-id="a2c8d-263">NOTES</span></span>

## <span data-ttu-id="a2c8d-264">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2c8d-264">RELATED LINKS</span></span>

[<span data-ttu-id="a2c8d-265">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-265">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="a2c8d-266">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-266">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="a2c8d-267">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-267">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="a2c8d-268">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-268">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="a2c8d-269">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-269">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="a2c8d-270">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-270">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="a2c8d-271">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a2c8d-271">Update-AzVmss</span></span>](./Update-AzVmss.md)


