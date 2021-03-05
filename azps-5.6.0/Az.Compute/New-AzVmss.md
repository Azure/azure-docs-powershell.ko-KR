---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: f80441cb3555d78974c5a838e829cb2ab350183f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988442"
---
# <span data-ttu-id="fd21c-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-101">New-AzVmss</span></span>

## <span data-ttu-id="fd21c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd21c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd21c-103">VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-103">Creates a VMSS.</span></span>

## <span data-ttu-id="fd21c-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd21c-104">SYNTAX</span></span>

### <span data-ttu-id="fd21c-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd21c-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd21c-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-EnableUltraSSD]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DataDiskSizeInGb <Int32[]>] [-ProximityPlacementGroupId <String>] [-HostGroupId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-ScaleInPolicy <String[]>]
 [-SkipExtensionsOnOverprovisionedVMs] [-EncryptionAtHost] [-PlatformFaultDomainCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-SinglePlacementGroup] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd21c-107">설명</span><span class="sxs-lookup"><span data-stu-id="fd21c-107">DESCRIPTION</span></span>
<span data-ttu-id="fd21c-108">**New-AzVmss** cmdlet은 Azure에서 VMSS(Virtual Machine Scale Set)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="fd21c-109">간단한 매개 변수 집합() 을 사용하여 미리 설정된 VMSS 및 관련 리소스를 빠르게 `SimpleParameterSet` 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-109">Use the simple parameter set (`SimpleParameterSet`) to quickly create a pre-set VMSS and associated resources.</span></span> <span data-ttu-id="fd21c-110">만들기 전에 VMSS의 각 구성 요소 및 연결된 각 리소스를 정확하게 구성해야 하는 경우 더 고급 시나리오의 경우 기본 매개 변수 `DefaultParameter` 집합() 을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-110">Use the default parameter set (`DefaultParameter`) for more advanced scenarios when you need to precisely configure each component of the VMSS and each associated resource before creation.</span></span>

## <span data-ttu-id="fd21c-111">예제</span><span class="sxs-lookup"><span data-stu-id="fd21c-111">EXAMPLES</span></span>

### <span data-ttu-id="fd21c-112">예제 1: 다음을 사용하여 VMSS 만들기 **`SimpleParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fd21c-112">Example 1: Create a VMSS using the **`SimpleParameterSet`**</span></span>
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

<span data-ttu-id="fd21c-113">위의 명령은 이름과 함께 다음을 `$vmssName` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-113">The command above creates the following with the name `$vmssName` :</span></span>
* <span data-ttu-id="fd21c-114">리소스 그룹</span><span class="sxs-lookup"><span data-stu-id="fd21c-114">A Resource Group</span></span>
* <span data-ttu-id="fd21c-115">가상 네트워크</span><span class="sxs-lookup"><span data-stu-id="fd21c-115">A virtual network</span></span>
* <span data-ttu-id="fd21c-116">부하 균형 조정기</span><span class="sxs-lookup"><span data-stu-id="fd21c-116">A load balancer</span></span>
* <span data-ttu-id="fd21c-117">공용 IP</span><span class="sxs-lookup"><span data-stu-id="fd21c-117">A public IP</span></span>
* <span data-ttu-id="fd21c-118">인스턴스가 2개인 VMSS</span><span class="sxs-lookup"><span data-stu-id="fd21c-118">the VMSS with 2 instances</span></span>

<span data-ttu-id="fd21c-119">VMSS에서 VM에 대해 선택한 기본 이미지는 `2016-Datacenter Windows Server` SKU입니다. `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="fd21c-119">The default image chosen for the VMs in the VMSS is `2016-Datacenter Windows Server` and the SKU is `Standard_DS1_v2`</span></span>

### <span data-ttu-id="fd21c-120">예제 2: 다음을 사용하여 VMSS 만들기 **`DefaultParameterSet`**</span><span class="sxs-lookup"><span data-stu-id="fd21c-120">Example 2: Create a VMSS using the **`DefaultParameterSet`**</span></span>
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
$VMSS = New-AzVmssConfig -Location $LOC -SkuCapacity 2 -SkuName "Standard_E4-2ds_v4" -UpgradePolicyMode "Automatic" `
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

<span data-ttu-id="fd21c-121">위의 복잡한 예제에서는 VMSS를 만듭니다. 다음은 일어나는 일에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-121">The complex example above creates a VMSS, following is an explanation of what is happening:</span></span>
* <span data-ttu-id="fd21c-122">첫 번째 명령은 지정된 이름과 위치를 사용하여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-122">The first command creates a resource group with the specified name and location.</span></span>
* <span data-ttu-id="fd21c-123">두 번째 명령은 **New-AzStorageAccount** cmdlet을 사용하여 저장소 계정을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-123">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
* <span data-ttu-id="fd21c-124">그런 다음 세 번째 명령은 **Get-AzStorageAccount** cmdlet을 사용하여 두 번째 명령에서 만든 저장소 계정을 얻게 하여 결과를 $STOAccount 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-124">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
* <span data-ttu-id="fd21c-125">다섯 번째 명령은 **New-AzVirtualNetworkSubnetConfig** cmdlet을 사용하여 서브넷을 만들고 결과를 $SubNet.</span><span class="sxs-lookup"><span data-stu-id="fd21c-125">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
* <span data-ttu-id="fd21c-126">여섯 번째 명령은 **New-AzVirtualNetwork** cmdlet을 사용하여 가상 네트워크를 만들고 결과를 $VNet.</span><span class="sxs-lookup"><span data-stu-id="fd21c-126">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
* <span data-ttu-id="fd21c-127">일곱 번째 명령은 **Get-AzVirtualNetwork를** 사용하여 여섯 번째 명령에서 만든 가상 네트워크에 대한 정보를 얻게 하여 이라는 변수에 정보를 $VNet.</span><span class="sxs-lookup"><span data-stu-id="fd21c-127">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
* <span data-ttu-id="fd21c-128">8번째 및 9번째 명령은 **New-AzPublicIpAddress** 및 **Get-AzureRmPublicIpAddress를** 사용하여 해당 공용 IP 주소에서 정보를 만들고 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-128">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
* <span data-ttu-id="fd21c-129">명령은 이름의 변수에 정보를 $PubIP.</span><span class="sxs-lookup"><span data-stu-id="fd21c-129">The commands store the information in the variable named $PubIP.</span></span>
* <span data-ttu-id="fd21c-130">10번째 명령은 **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet을 사용하여 프런트 엔드 부하 분산을 만들고 결과를 $Frontend.</span><span class="sxs-lookup"><span data-stu-id="fd21c-130">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
* <span data-ttu-id="fd21c-131">열한 번째 명령은 **New-AzLoadBalancerBackendAddressPoolConfig를** 사용하여 백던드 주소 풀 구성을 만들고 결과를 새 이름의 변수에 $BackendAddressPool.</span><span class="sxs-lookup"><span data-stu-id="fd21c-131">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
* <span data-ttu-id="fd21c-132">12번째 명령은 **New-AzLoadBalancerProbeConfig를** 사용하여 프로브를 만들고 프로브 정보를 프로브라는 변수에 $Probe.</span><span class="sxs-lookup"><span data-stu-id="fd21c-132">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
* <span data-ttu-id="fd21c-133">13번째 명령은 **New-AzLoadBalancerInboundNatPoolConfig** cmdlet을 사용하여 NAT(부하 분산기 인바운드 네트워크 주소 변환) 풀 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-133">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
* <span data-ttu-id="fd21c-134">14번째 명령은 **New-AzLoadBalancerRuleConfig를** 사용하여 부하 분산기 규칙 구성을 만들고 결과를 $LBRule.</span><span class="sxs-lookup"><span data-stu-id="fd21c-134">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
* <span data-ttu-id="fd21c-135">15번째 명령은 **New-AzLoadBalancer** cmdlet을 사용하여 부하 분산을 만들고 결과를 $ActualLb.</span><span class="sxs-lookup"><span data-stu-id="fd21c-135">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
* <span data-ttu-id="fd21c-136">16번째 명령은 **Get-AzLoadBalancer를** 사용하여 15번째 명령에서 만든 부하 분산기에 대한 정보를 얻게 하여 해당 변수의 정보를 $ExpectedLb.</span><span class="sxs-lookup"><span data-stu-id="fd21c-136">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
* <span data-ttu-id="fd21c-137">17번째 명령은 **New-AzVmssIPConfig** cmdlet을 사용하여 VMSS IP 구성을 만들고 해당 정보를 새 이름의 변수에 $IPCfg.</span><span class="sxs-lookup"><span data-stu-id="fd21c-137">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
* <span data-ttu-id="fd21c-138">18번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="fd21c-138">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
* <span data-ttu-id="fd21c-139">19번째 명령은 **New-AzVmss** cmdlet을 사용하여 VMSS를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-139">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="fd21c-140">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fd21c-140">PARAMETERS</span></span>

### <span data-ttu-id="fd21c-141">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="fd21c-141">-AllocationMethod</span></span>
<span data-ttu-id="fd21c-142">확장 집합(정적 또는 동적)의 공용 IP 주소에 대한 할당 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-142">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="fd21c-143">값이 제공되지 않는 경우 할당은 정적입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-143">If no value is supplied, allocation will be static.</span></span>

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

### <span data-ttu-id="fd21c-144">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd21c-144">-AsJob</span></span>
<span data-ttu-id="fd21c-145">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-145">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fd21c-146">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="fd21c-146">-BackendPoolName</span></span>
<span data-ttu-id="fd21c-147">이 확장 집합의 부하 균형 조정기에서 사용할 백end 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-147">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="fd21c-148">값이 제공되지 않고 확장 집합과 이름이 같은 새 백end 풀이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-148">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fd21c-149">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="fd21c-149">-BackendPort</span></span>
<span data-ttu-id="fd21c-150">확장 집합에서 VM과 통신하기 위해 확장 집합 부하 균형 조정기에서 사용하는 백end 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-150">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="fd21c-151">값이 지정되지 않으면 Windows VMS에 3389 및 5985 포트가 사용되어 Linux VM에 포트 22가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-151">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

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

### <span data-ttu-id="fd21c-152">-자격 증명</span><span class="sxs-lookup"><span data-stu-id="fd21c-152">-Credential</span></span>
<span data-ttu-id="fd21c-153">이 확장 집합의 VM에 대한 관리자 자격 증명(사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-153">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

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

### <span data-ttu-id="fd21c-154">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="fd21c-154">-DataDiskSizeInGb</span></span>
<span data-ttu-id="fd21c-155">GB의 데이터 디스크 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-155">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="fd21c-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd21c-156">-DefaultProfile</span></span>
<span data-ttu-id="fd21c-157">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd21c-158">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="fd21c-158">-DomainNameLabel</span></span>
<span data-ttu-id="fd21c-159">이 확장 집합에 대한 공용 Fully-Qualified 도메인 이름(FQDN)의 도메인 이름 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-159">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="fd21c-160">확장 집합에 자동으로 할당되는 도메인 이름의 첫 번째 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-160">This is the first component of the domain name that is automatically assigned to the Scale Set.</span></span> <span data-ttu-id="fd21c-161">자동으로 할당된 도메인 이름은 폼을 사용 합니다. <DomainNameLabel> <Location> . cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="fd21c-161">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="fd21c-162">값이 제공되지 않습니다. 기본 도메인 이름 레이블은 및 의 의 수가 <ScaleSetName> <ResourceGroupName> 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-162">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

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

### <span data-ttu-id="fd21c-163">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="fd21c-163">-EnableUltraSSD</span></span>
<span data-ttu-id="fd21c-164">확장 집합의 VM에 UltraSSD 디스크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-164">Use UltraSSD disks for the VMs in the scale set.</span></span>

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

### <span data-ttu-id="fd21c-165">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="fd21c-165">-EncryptionAtHost</span></span>
<span data-ttu-id="fd21c-166">이 매개 변수는 호스트 자체에서 Resource/Temp 디스크를 포함하여 모든 디스크에 대한 암호화를 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-166">This parameter will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="fd21c-167">기본값: 이 속성이 리소스에 대해 true로 설정되지 않는 한 호스트의 암호화를 사용하지 않도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-167">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

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

### <span data-ttu-id="fd21c-168">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="fd21c-168">-EvictionPolicy</span></span>
<span data-ttu-id="fd21c-169">우선 순위가 낮은 가상 머신 확장 집합에 대한 eviction 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-169">The eviction policy for the low priority virtual machine scale set.</span></span>  <span data-ttu-id="fd21c-170">지원되는 값만 'Deallocate' 및 'Delete'입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-170">Only supported values are 'Deallocate' and 'Delete'.</span></span>

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

### <span data-ttu-id="fd21c-171">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="fd21c-171">-FrontendPoolName</span></span>
<span data-ttu-id="fd21c-172">확장 집합 부하 균형 조정기에서 사용할 프런트 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-172">The name of the frontend address pool to use in the Scale Set load balancer.</span></span>  <span data-ttu-id="fd21c-173">값이 제공되지되면 확장 집합과 동일한 이름으로 새 프런트 엔드 주소 풀이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-173">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

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

### <span data-ttu-id="fd21c-174">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="fd21c-174">-HostGroupId</span></span>
<span data-ttu-id="fd21c-175">가상 머신 확장 집합이 상주할 전용 호스트 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-175">Specifies the dedicated host group the virtual machine scale set will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: HostGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="fd21c-176">-ImageName</span><span class="sxs-lookup"><span data-stu-id="fd21c-176">-ImageName</span></span>
<span data-ttu-id="fd21c-177">이 확장 집합의 VM에 대한 이미지의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-177">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="fd21c-178">값이 제공되지 않고 "Windows Server 2016 DataCenter" 이미지가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-178">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

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

### <span data-ttu-id="fd21c-179">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="fd21c-179">-InstanceCount</span></span>
<span data-ttu-id="fd21c-180">확장 집합의 VM 이미지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-180">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="fd21c-181">값이 제공되지 않고 2개 인스턴스가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-181">If no value is provided, 2 instances will be created.</span></span>

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

### <span data-ttu-id="fd21c-182">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="fd21c-182">-LoadBalancerName</span></span>
<span data-ttu-id="fd21c-183">이 확장 집합에 사용할 부하 균형 조정기 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-183">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="fd21c-184">값이 지정되지 않은 경우 확장 집합과 동일한 이름을 사용하는 새 부하 균형 조정기가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-184">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

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

### <span data-ttu-id="fd21c-185">-Location</span><span class="sxs-lookup"><span data-stu-id="fd21c-185">-Location</span></span>
<span data-ttu-id="fd21c-186">이 확장 집합을 만들 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-186">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="fd21c-187">값이 지정되지 않으면 매개 변수에 참조된 다른 리소스의 위치에서 위치가 유추됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-187">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

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

### <span data-ttu-id="fd21c-188">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="fd21c-188">-MaxPrice</span></span>
<span data-ttu-id="fd21c-189">우선 순위가 낮은 가상 머신 확장 집합의 청구의 최대 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-189">The max price of the billing of a low priority virtual machine scale set.</span></span>

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

### <span data-ttu-id="fd21c-190">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="fd21c-190">-NatBackendPort</span></span>
<span data-ttu-id="fd21c-191">인바운드 네트워크 주소 변환에 대한 백end 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-191">Backend port for inbound network address translation.</span></span>

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

### <span data-ttu-id="fd21c-192">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="fd21c-192">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="fd21c-193">각 배치 그룹에 대한 장애 도메인 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-193">Fault Domain count for each placement group.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd21c-194">-Priority</span><span class="sxs-lookup"><span data-stu-id="fd21c-194">-Priority</span></span>
<span data-ttu-id="fd21c-195">확장 집합의 가상 머신에 대한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-195">The priority for the virtual machine in the scale set.</span></span>  <span data-ttu-id="fd21c-196">지원되는 값만 '일반', 'Spot' 및 'Low'입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-196">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="fd21c-197">'일반'은 일반 가상 머신용입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-197">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="fd21c-198">'Spot'은 가상 머신을 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-198">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="fd21c-199">'Low'은 스팟 가상 머신용이지만 'Spot'으로 바 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-199">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="fd21c-200">'Low' 대신 'Spot'을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="fd21c-200">Please use 'Spot' instead of 'Low'.</span></span>

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

### <span data-ttu-id="fd21c-201">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fd21c-201">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="fd21c-202">이 확장 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-202">The resource id of the Proximity Placement Group to use with this scale set.</span></span>

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

### <span data-ttu-id="fd21c-203">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="fd21c-203">-PublicIpAddressName</span></span>
<span data-ttu-id="fd21c-204">이 확장 집합에 사용할 공용 IP 주소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-204">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="fd21c-205">값이 제공되지 않고 확장 집합과 이름이 같은 새 공용 IPAddress가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-205">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

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

### <span data-ttu-id="fd21c-206">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd21c-206">-ResourceGroupName</span></span>
<span data-ttu-id="fd21c-207">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-207">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="fd21c-208">값이 지정되지 않으면 확장 집합과 동일한 이름을 사용하여 새 ResourceGroup이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-208">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

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

### <span data-ttu-id="fd21c-209">-ScaleInPolicy</span><span class="sxs-lookup"><span data-stu-id="fd21c-209">-ScaleInPolicy</span></span>
<span data-ttu-id="fd21c-210">가상 머신 확장 집합의 크기 조정 시 따라야 할 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-210">The rules to be followed when scaling-in a virtual machine scale set.</span></span>  <span data-ttu-id="fd21c-211">가능한 값은 'Default', 'OldestVM' 및 'NewestVM'입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-211">Possible values are: 'Default', 'OldestVM' and 'NewestVM'.</span></span>  <span data-ttu-id="fd21c-212">가상 머신 확장 집합이 확장될 때 '기본값'은 크기 조정 집합이 영역 전체에 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-212">'Default' when a virtual machine scale set is scaled in, the scale set will first be balanced across zones if it is a zonal scale set.</span></span>  <span data-ttu-id="fd21c-213">그런 다음 오류 도메인에서 가능한 한 균형이 조정됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-213">Then, it will be balanced across Fault Domains as far as possible.</span></span>  <span data-ttu-id="fd21c-214">각 장애 도메인 내에서 제거를 위해 선택한 가상 머신은 확장으로부터 보호되지 않는 가장 최근의 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-214">Within each Fault Domain, the virtual machines chosen for removal will be the newest ones that are not protected from scale-in.</span></span>  <span data-ttu-id="fd21c-215">가상 머신 확장 집합이 확장되는 경우 'OldestVM'은 확장으로부터 보호되지 않는 가장 오래된 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-215">'OldestVM' when a virtual machine scale set is being scaled-in, the oldest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fd21c-216">zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-216">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fd21c-217">각 영역 내에서 보호되지 않는 가장 오래된 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-217">Within each zone, the oldest virtual machines that are not protected will be chosen for removal.</span></span>  <span data-ttu-id="fd21c-218">가상 머신 확장 집합이 확장되는 경우 'NewestVM'은 확장으로부터 보호되지 않는 가장 최근 가상 머신을 제거하기 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-218">'NewestVM' when a virtual machine scale set is being scaled-in, the newest virtual machines that are not protected from scale-in will be chosen for removal.</span></span>  <span data-ttu-id="fd21c-219">zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-219">For zonal virtual machine scale sets, the scale set will first be balanced across zones.</span></span>  <span data-ttu-id="fd21c-220">각 영역 내에서 보호되지 않는 가장 새로운 가상 머신은 제거를 위해 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-220">Within each zone, the newest virtual machines that are not protected will be chosen for removal.</span></span>

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

### <span data-ttu-id="fd21c-221">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fd21c-221">-SecurityGroupName</span></span>
<span data-ttu-id="fd21c-222">이 확장 집합에 적용할 네트워크 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-222">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="fd21c-223">값이 제공되지 않고 확장 집합과 이름이 같은 기본 네트워크 보안 그룹이 만들어지며 확장 집합에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-223">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

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

### <span data-ttu-id="fd21c-224">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="fd21c-224">-SinglePlacementGroup</span></span>
<span data-ttu-id="fd21c-225">이 기능을 사용하여 단일 배치 그룹에서 확장 집합을 만들면 기본값은 여러 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-225">Use this to create the Scale set in a single placement group, default is multiple groups</span></span>

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

### <span data-ttu-id="fd21c-226">-SkipExtensionsOnOverprovisionedVM</span><span class="sxs-lookup"><span data-stu-id="fd21c-226">-SkipExtensionsOnOverprovisionedVMs</span></span>
<span data-ttu-id="fd21c-227">확장이 추가 오버프로비전된 VM에서 실행되지 않는지 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-227">Specifies that the extensions do not run on the extra overprovisioned VMs.</span></span>

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

### <span data-ttu-id="fd21c-228">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd21c-228">-SubnetAddressPrefix</span></span>
<span data-ttu-id="fd21c-229">이 ScaleSet이 사용할 서브넷의 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-229">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="fd21c-230">값이 제공되지 않고 기본 서브넷 설정(192.168.1.0/24)이 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-230">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

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

### <span data-ttu-id="fd21c-231">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="fd21c-231">-SubnetName</span></span>
<span data-ttu-id="fd21c-232">이 확장 집합에 사용할 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-232">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="fd21c-233">값이 제공되지 않고 확장 집합과 동일한 이름으로 새 서브넷이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-233">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

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

### <span data-ttu-id="fd21c-234">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd21c-234">-SystemAssignedIdentity</span></span>
<span data-ttu-id="fd21c-235">매개 변수가 있는 경우 확장 집합의 VM은 자동 생성되는 관리되는 시스템 ID를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-235">If the parameter is present then the VM(s) in the scale set is(are) assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="fd21c-236">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="fd21c-236">-UpgradePolicyMode</span></span>
<span data-ttu-id="fd21c-237">이 확장 집합의 VM 인스턴스에 대한 업그레이드 정책 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-237">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="fd21c-238">업그레이드 정책은 자동, 수동 또는 롤링 업그레이드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-238">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

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

### <span data-ttu-id="fd21c-239">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="fd21c-239">-UserAssignedIdentity</span></span>
<span data-ttu-id="fd21c-240">확장 집합의 VM에 할당해야 하는 관리 서비스 ID의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-240">The name of a managed service identity that should be assigned to the VM(s) in the scale set.</span></span>

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

### <span data-ttu-id="fd21c-241">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-241">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fd21c-242">이 cmdlet이 만드는 VMSS의 속성을 포함하는 **VirtualMachineScaleSet** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-242">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fd21c-243">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="fd21c-243">-VirtualNetworkName</span></span>
<span data-ttu-id="fd21c-244">이름은 이 확장 집합과 함께 사용할 Virtual Network를 엽니 다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-244">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="fd21c-245">값이 제공되지 않습니다. 확장 집합과 이름이 같은 새 가상 네트워크가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-245">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

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

### <span data-ttu-id="fd21c-246">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fd21c-246">-VMScaleSetName</span></span>
<span data-ttu-id="fd21c-247">이 cmdlet이 만드는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-247">Specifies the name of the VMSS that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fd21c-248">-VmSize</span><span class="sxs-lookup"><span data-stu-id="fd21c-248">-VmSize</span></span>
<span data-ttu-id="fd21c-249">이 확장 집합의 VM 인스턴스의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-249">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="fd21c-250">크기를 지정하지 Standard_DS1_v2 기본 크기(Standard_DS1_v2)가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-250">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

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

### <span data-ttu-id="fd21c-251">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fd21c-251">-VnetAddressPrefix</span></span>
<span data-ttu-id="fd21c-252">이 확장 집합과 함께 사용되는 가상 네트워크에 대한 주소 연결선입니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-252">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="fd21c-253">값이 제공되지 않습니다. 기본 가상 네트워크 주소 설정(192.168.0.0/16)이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-253">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

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

### <span data-ttu-id="fd21c-254">-Zone</span><span class="sxs-lookup"><span data-stu-id="fd21c-254">-Zone</span></span>
<span data-ttu-id="fd21c-255">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-255">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="fd21c-256">-확인</span><span class="sxs-lookup"><span data-stu-id="fd21c-256">-Confirm</span></span>
<span data-ttu-id="fd21c-257">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd21c-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd21c-258">-WhatIf</span></span>
<span data-ttu-id="fd21c-259">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-259">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd21c-260">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd21c-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd21c-261">CommonParameters</span></span>
<span data-ttu-id="fd21c-262">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd21c-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd21c-263">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd21c-263">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd21c-264">입력</span><span class="sxs-lookup"><span data-stu-id="fd21c-264">INPUTS</span></span>

### <span data-ttu-id="fd21c-265">System.String</span><span class="sxs-lookup"><span data-stu-id="fd21c-265">System.String</span></span>

### <span data-ttu-id="fd21c-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-266">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="fd21c-267">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fd21c-267">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fd21c-268">출력</span><span class="sxs-lookup"><span data-stu-id="fd21c-268">OUTPUTS</span></span>

### <span data-ttu-id="fd21c-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fd21c-269">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="fd21c-270">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd21c-270">NOTES</span></span>

## <span data-ttu-id="fd21c-271">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd21c-271">RELATED LINKS</span></span>

[<span data-ttu-id="fd21c-272">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-272">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="fd21c-273">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-273">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="fd21c-274">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-274">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="fd21c-275">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-275">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="fd21c-276">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-276">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="fd21c-277">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-277">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="fd21c-278">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="fd21c-278">Update-AzVmss</span></span>](./Update-AzVmss.md)


