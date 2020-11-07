---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 1A2C843C-6962-4B0E-ACBF-A5EFF609A5BE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVmss.md
ms.openlocfilehash: fc788d40cbcd807ef05be4ab43fcda4371aaa084
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876991"
---
# <span data-ttu-id="b2538-101">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-101">New-AzVmss</span></span>

## <span data-ttu-id="b2538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2538-102">SYNOPSIS</span></span>
<span data-ttu-id="b2538-103">VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-103">Creates a VMSS.</span></span>

## <span data-ttu-id="b2538-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2538-104">SYNTAX</span></span>

### <span data-ttu-id="b2538-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="b2538-105">DefaultParameter (Default)</span></span>
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2538-106">SimpleParameterSet</span><span class="sxs-lookup"><span data-stu-id="b2538-106">SimpleParameterSet</span></span>
```
New-AzVmss [[-ResourceGroupName] <String>] [-VMScaleSetName] <String> [-AsJob] [-ImageName <String>]
 -Credential <PSCredential> [-InstanceCount <Int32>] [-VirtualNetworkName <String>] [-SubnetName <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-SecurityGroupName <String>]
 [-LoadBalancerName <String>] [-BackendPort <Int32[]>] [-Location <String>] [-VmSize <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-AllocationMethod <String>] [-VnetAddressPrefix <String>]
 [-SubnetAddressPrefix <String>] [-FrontendPoolName <String>] [-BackendPoolName <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-NatBackendPort <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2538-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b2538-107">DESCRIPTION</span></span>
<span data-ttu-id="b2538-108">**AzVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-108">The **New-AzVmss** cmdlet creates a Virtual Machine Scale Set (VMSS) in Azure.</span></span>
<span data-ttu-id="b2538-109">이 cmdlet은 **VirtualMachineScaleSet** 개체를 입력으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-109">This cmdlet takes a **VirtualMachineScaleSet** object as input.</span></span>

## <span data-ttu-id="b2538-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b2538-110">EXAMPLES</span></span>

### <span data-ttu-id="b2538-111">예제 1: VMSS 만들기</span><span class="sxs-lookup"><span data-stu-id="b2538-111">Example 1: Create a VMSS</span></span>
```
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

<span data-ttu-id="b2538-112">다음 복잡 한 예제는 VMSS를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-112">The following complex example creates a VMSS.</span></span>
<span data-ttu-id="b2538-113">첫 번째 명령은 지정 된 이름과 위치를 사용 하 여 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-113">The first command creates a resource group with the specified name and location.</span></span>
<span data-ttu-id="b2538-114">두 번째 명령은 **새 AzStorageAccount** cmdlet을 사용 하 여 저장소 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-114">The second command uses the **New-AzStorageAccount** cmdlet to create a storage account.</span></span>
<span data-ttu-id="b2538-115">세 번째 명령은 **AzStorageAccount** cmdlet을 사용 하 여 두 번째 명령에서 만든 저장소 계정을 가져오고 결과를 $STOAccount 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-115">The third command then uses the **Get-AzStorageAccount** cmdlet to get the storage account created in the second command and stores the result in the $STOAccount variable.</span></span>
<span data-ttu-id="b2538-116">다섯 번째 명령은 **AzVirtualNetworkSubnetConfig** cmdlet을 사용 하 여 서브넷을 만들고 결과를 $SubNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-116">The fifth command uses the **New-AzVirtualNetworkSubnetConfig** cmdlet to create a subnet and stores the result in the variable named $SubNet.</span></span>
<span data-ttu-id="b2538-117">여섯 번째 명령은 **AzVirtualNetwork** cmdlet을 사용 하 여 가상 네트워크를 만들고 결과를 $VNet 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-117">The sixth command uses the **New-AzVirtualNetwork** cmdlet to create a virtual network and stores the result in the variable named $VNet.</span></span>
<span data-ttu-id="b2538-118">일곱 번째 명령은 **AzVirtualNetwork** 를 사용 하 여 여섯 번째 명령에서 만든 가상 네트워크에 대 한 정보를 가져오고이 정보를 $VNet 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-118">The seventh command uses the **Get-AzVirtualNetwork** to get information about the virtual network created in the sixth command and stores the information in the variable named $VNet.</span></span>
<span data-ttu-id="b2538-119">여덟째 및 아홉 번째 명령은 **New-AzPublicIpAddress** 및 **get-AzureRmPublicIpAddress** 를 사용 하 여 해당 공용 IP 주소에서 정보를 만들고 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-119">The eighth and ninth command uses the **New-AzPublicIpAddress** and **Get- AzureRmPublicIpAddress** to create and get information from that public IP address.</span></span>
<span data-ttu-id="b2538-120">명령은 $PubIP 라는 변수에 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-120">The commands store the information in the variable named $PubIP.</span></span>
<span data-ttu-id="b2538-121">10 번째 명령은 **AzureRmLoadBalancerFrontendIpConfig** cmdlet을 사용 하 여 프런트 엔드 부하 분산 장치를 만들고 결과를 $Frontend 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-121">The tenth command uses the **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet to create a frontend load balancer and stores the result in the variable named $Frontend.</span></span>
<span data-ttu-id="b2538-122">11 번째 명령은 **AzLoadBalancerBackendAddressPoolConfig** 를 사용 하 여 백 엔드 주소 풀 구성을 만들고 그 결과를 $BackendAddressPool 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-122">The eleventh command uses the **New-AzLoadBalancerBackendAddressPoolConfig** to create a backend address pool configuration and stores the result in the variable named $BackendAddressPool.</span></span>
<span data-ttu-id="b2538-123">12 번째 명령은 **New-AzLoadBalancerProbeConfig** 를 사용 하 여 프로브를 만들고 $Probe 이라는 변수에 프로브 정보를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-123">The twelfth command uses the **New-AzLoadBalancerProbeConfig** to create a probe and stores the probe information in the variable named $Probe.</span></span>
<span data-ttu-id="b2538-124">Thirteenth 명령은 **New-AzLoadBalancerInboundNatPoolConfig** cmdlet을 사용 하 여 부하 분산 장치 인바운드 NAT (network address translation) 풀 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-124">The thirteenth command uses the **New-AzLoadBalancerInboundNatPoolConfig** cmdlet to create a load balancer inbound network address translation (NAT) pool configuration.</span></span>
<span data-ttu-id="b2538-125">14 번째 명령은 **AzLoadBalancerRuleConfig** 를 사용 하 여 부하 분산 장치 규칙 구성을 만들고 그 결과를 $LBRule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-125">The fourteenth command uses the **New-AzLoadBalancerRuleConfig** to create a load balancer rule configuration and stores the result in the variable named $LBRule.</span></span>
<span data-ttu-id="b2538-126">15 번째 명령은 **새 AzLoadBalancer** cmdlet을 사용 하 여 부하 분산 장치를 만들고 결과를 $ActualLb 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-126">The fifteenth command uses the **New-AzLoadBalancer** cmdlet to create a load balancer and stores the result in the variable named $ActualLb.</span></span>
<span data-ttu-id="b2538-127">16 번째 명령은 **AzLoadBalancer** 를 사용 하 여 15 번째 명령에서 만든 부하 분산 장치에 대 한 정보를 가져오고이 정보를 $ExpectedLb 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-127">The sixteenth command uses the **Get-AzLoadBalancer** to get information about the load balancer that was created in the fifteenth command and stores the information in the variable named $ExpectedLb.</span></span>
<span data-ttu-id="b2538-128">Seventeenth 명령은 **새 AzVmssIPConfig** cmdlet을 사용 하 여 VMSS IP 구성을 만들고이 정보를 $IPCfg 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-128">The seventeenth command uses the **New-AzVmssIPConfig** cmdlet to create a VMSS IP configuration and stores the information in the variable named $IPCfg.</span></span>
<span data-ttu-id="b2538-129">Eighteenth 명령은 **새 AzVmssConfig** cmdlet을 사용 하 여 vmss 구성 개체를 만들고 결과를 $VMSS 이라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-129">The eighteenth command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="b2538-130">19 명령은 **새 AzVmss** cmdlet을 사용 하 여 vmss를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-130">The nineteenth command uses the **New-AzVmss** cmdlet to create the VMSS.</span></span>

## <span data-ttu-id="b2538-131">변수</span><span class="sxs-lookup"><span data-stu-id="b2538-131">PARAMETERS</span></span>

### <span data-ttu-id="b2538-132">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="b2538-132">-AllocationMethod</span></span>
<span data-ttu-id="b2538-133">확장 집합의 공용 IP 주소에 대 한 배정 방법 (정적 또는 동적)입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-133">Allocation method for the Public IP Address of the Scale Set (Static or Dynamic).</span></span>  <span data-ttu-id="b2538-134">값을 지정 하지 않으면 정적 할당이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-134">If no value is supplied, allocation will be static.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b2538-135">-AsJob</span></span>
<span data-ttu-id="b2538-136">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-136">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-137">-BackendPoolName</span><span class="sxs-lookup"><span data-stu-id="b2538-137">-BackendPoolName</span></span>
<span data-ttu-id="b2538-138">이 배율 집합에 대 한 부하 분산에 사용할 백 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-138">The name of the backend address pool to use in the load balancer for this Scale Set.</span></span>  <span data-ttu-id="b2538-139">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 새 백엔드 풀이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-139">If no value is provided, a new backend pool will be created, with the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-140">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="b2538-140">-BackendPort</span></span>
<span data-ttu-id="b2538-141">배율 집합 부하 분산 장치에서 확장 집합의 Vm과 통신 하는 데 사용 하는 백 엔드 포트 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-141">Backend port numbers used by the Scale Set load balancer to communicate with VMs in the Scale Set.</span></span>  <span data-ttu-id="b2538-142">값을 지정 하지 않으면 포트 3389 및 5985이 Windows VM에 사용 되 고, 포트 22가 Linux 용 Vm에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-142">If no values are specified, ports 3389 and 5985 will be used for Windows VMS, and port 22 will be used for Linux VMs.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-143">-Credential</span><span class="sxs-lookup"><span data-stu-id="b2538-143">-Credential</span></span>
<span data-ttu-id="b2538-144">이 확장 집합의 Vm에 대 한 관리자 자격 증명 (사용자 이름 및 암호)입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-144">The administrator credentials (username and password) for VMs in this Scale Set.</span></span>

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2538-145">-DefaultProfile</span></span>
<span data-ttu-id="b2538-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-147">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="b2538-147">-DomainNameLabel</span></span>
<span data-ttu-id="b2538-148">이 배율 집합에 대 한 FQDN (공용 Fully-Qualified 도메인 이름)의 도메인 이름 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-148">The domain name label for the public Fully-Qualified domain name (FQDN) for this Scale Set.</span></span> <span data-ttu-id="b2538-149">이는 자동으로 크기 조정 집합에 assiged는 도메인 이름의 첫 번째 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-149">This is the first component of the domain name that is automatically assiged to the Scale Set.</span></span> <span data-ttu-id="b2538-150">자동으로 할당 된 도메인 이름에는 양식 (.)을 사용 합니다 <DomainNameLabel> . <Location> cloudapp.azure.com).</span><span class="sxs-lookup"><span data-stu-id="b2538-150">Automatically assigned Domain names use the form (<DomainNameLabel>.<Location>.cloudapp.azure.com).</span></span> <span data-ttu-id="b2538-151">값을 지정 하지 않으면 기본 도메인 이름 레이블이 and로 연결 됩니다 <ScaleSetName> <ResourceGroupName> .</span><span class="sxs-lookup"><span data-stu-id="b2538-151">If no value is supplied, the default domain name label will be the concatenation of <ScaleSetName> and <ResourceGroupName>.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-152">-FrontendPoolName</span><span class="sxs-lookup"><span data-stu-id="b2538-152">-FrontendPoolName</span></span>
<span data-ttu-id="b2538-153">확장 집합 locad 분산 장치에 설정할 프런트 엔드 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-153">The name of the frontend address pool to usein the Scale Set locad balancer.</span></span>  <span data-ttu-id="b2538-154">값을 지정 하지 않으면 새 프런트 엔드 주소 풀이 생성 되며, 여기에는 배율 집합과 동일한 이름이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-154">If no value is supplied, a new Frontend Address Pool will be created, with the same name as the scale set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-155">-ImageName</span><span class="sxs-lookup"><span data-stu-id="b2538-155">-ImageName</span></span>
<span data-ttu-id="b2538-156">이 배율 집합의 Vm에 대 한 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-156">The name of the image for VMs in this Scale Set.</span></span> <span data-ttu-id="b2538-157">값을 제공 하지 않으면 "Windows Server 2016 DataCenter" 이미지가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-157">If no value is provided, the "Windows Server 2016 DataCenter" image will be used.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-158">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="b2538-158">-InstanceCount</span></span>
<span data-ttu-id="b2538-159">확장 집합의 VM 이미지 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-159">The number of VM images in the Scale Set.</span></span>  <span data-ttu-id="b2538-160">값을 지정 하지 않으면 2 인스턴스가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-160">If no value is provided, 2 instances will be created.</span></span>

```yaml
Type: Int32
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-161">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b2538-161">-LoadBalancerName</span></span>
<span data-ttu-id="b2538-162">이 배율 집합에 사용할 부하 분산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-162">The name of the load balancer to use with this Scale Set.</span></span>  <span data-ttu-id="b2538-163">값을 지정 하지 않으면 배율 집합과 동일한 이름을 사용 하는 새 부하 분산이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-163">A new load balancer using the same name as the Scale Set will be created if no value is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-164">-위치</span><span class="sxs-lookup"><span data-stu-id="b2538-164">-Location</span></span>
<span data-ttu-id="b2538-165">이 배율 집합이 생성 되는 Azure 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-165">The Azure location where this Scale Set will be created.</span></span>  <span data-ttu-id="b2538-166">값을 지정 하지 않으면 매개 변수에서 참조 되는 다른 리소스의 위치에서 위치가 유추 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-166">If no value is specified, the location will be inferred from the location of other resources referenced in the parameters.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-167">-NatBackendPort</span><span class="sxs-lookup"><span data-stu-id="b2538-167">-NatBackendPort</span></span>
<span data-ttu-id="b2538-168">인바운드 네트워크 주소 변환을 위한 백 엔드 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-168">Backend port for inbound network address translation.</span></span>

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-169">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="b2538-169">-PublicIpAddressName</span></span>
<span data-ttu-id="b2538-170">이 배율 집합에 사용할 공용 IP 주소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-170">The name of the public IP Address to use with this scale set.</span></span>  <span data-ttu-id="b2538-171">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 새 공용 IPAddress가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-171">A new Public IPAddress with the same name as the Scale Set will be created if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2538-172">-ResourceGroupName</span></span>
<span data-ttu-id="b2538-173">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-173">Specifies the name of the resource group of the VMSS.</span></span>  <span data-ttu-id="b2538-174">값을 지정 하지 않으면 새 ResourceGroup이 배율 집합과 동일한 이름을 사용 하 여 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-174">If no value is specified, a new ResourceGroup will be created using the same name as the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-175">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="b2538-175">-SecurityGroupName</span></span>
<span data-ttu-id="b2538-176">이 배율 집합에 적용할 네트워크 보안 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-176">The name of the network security group to apply to this Scale Set.</span></span>  <span data-ttu-id="b2538-177">값을 제공 하지 않으면 배율 집합과 동일한 이름을 가진 기본 네트워크 보안 그룹이 만들어지고 배율 집합에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-177">If no value is provided, a default network security group with the same name as the Scale Set will be created and applied to the Scale Set.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-178">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b2538-178">-SubnetAddressPrefix</span></span>
<span data-ttu-id="b2538-179">이 ScaleSet에서 사용할 서브넷의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-179">The address prefix of the Subnet this ScaleSet will use.</span></span> <span data-ttu-id="b2538-180">값을 제공 하지 않으면 기본 서브넷 설정 (192.168.1.0/24)이 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-180">Default Subnet settings (192.168.1.0/24) will be applied if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-181">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="b2538-181">-SubnetName</span></span>
<span data-ttu-id="b2538-182">이 배율 집합에 사용할 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-182">The name of the subnet to use with this Scale Set.</span></span>  <span data-ttu-id="b2538-183">값을 제공 하지 않으면 크기 조정 집합과 같은 이름으로 새 서브넷이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-183">A new Subnet will be created with the same name as the Scale Set if no value is provided.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-184">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="b2538-184">-UpgradePolicyMode</span></span>
<span data-ttu-id="b2538-185">이 확장 집합의 VM 인스턴스에 대 한 업그레이드 정책 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-185">The upgrade policy mode for VM instances in this Scale Set.</span></span>  <span data-ttu-id="b2538-186">업그레이드 정책은 자동, 수동 또는 롤링 업그레이드를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-186">Upgrade policy could specify Automatic, Manual, or Rolling upgrades.</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: SimpleParameterSet
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-187">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2538-187">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="b2538-188">이 cmdlet이 만드는 VMSS의 속성을 포함 하는 **VirtualMachineScaleSet** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-188">Specifies the **VirtualMachineScaleSet** object that contains the properties of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-189">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="b2538-189">-VirtualNetworkName</span></span>
<span data-ttu-id="b2538-190">이 배율 집합에 사용할 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-190">The name fo the Virtual Network to use with this scale set.</span></span>  <span data-ttu-id="b2538-191">값을 지정 하지 않으면 배율 집합과 동일한 이름을 가진 새 가상 네트워크가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-191">If no value is supplied, a new virtual network with the same name as the Scale Set will be created.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-192">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b2538-192">-VMScaleSetName</span></span>
<span data-ttu-id="b2538-193">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-193">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-194">-VmSize</span><span class="sxs-lookup"><span data-stu-id="b2538-194">-VmSize</span></span>
<span data-ttu-id="b2538-195">이 배율 집합의 VM 인스턴스 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-195">The size of the VM instances in this scale set.</span></span>  <span data-ttu-id="b2538-196">크기를 지정 하지 않으면 기본 크기 (Standard_DS1_v2)가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-196">A default size (Standard_DS1_v2) will be used if no Size is specified.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-197">-VnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="b2538-197">-VnetAddressPrefix</span></span>
<span data-ttu-id="b2538-198">이 배율 집합에 사용 되는 가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-198">The address prefix for the virtual network used with this Scale Set.</span></span>  <span data-ttu-id="b2538-199">값을 제공 하지 않으면 기본 가상 네트워크 주소 접두사 설정 (192.168.0.0/16)이 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-199">Default virtual network address prefix settings (192.168.0.0/16) will be used if no value is supplied.</span></span>

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases: 

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2538-200">-Zone</span><span class="sxs-lookup"><span data-stu-id="b2538-200">-Zone</span></span>
<span data-ttu-id="b2538-201">리소스에 대해 할당 된 IP를 나타내는 가용성 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-201">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="b2538-202">-확인</span><span class="sxs-lookup"><span data-stu-id="b2538-202">-Confirm</span></span>
<span data-ttu-id="b2538-203">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-203">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2538-204">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2538-204">-WhatIf</span></span>
<span data-ttu-id="b2538-205">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-205">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b2538-206">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-206">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2538-207">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2538-207">CommonParameters</span></span>
<span data-ttu-id="b2538-208">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-208">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2538-209">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2538-209">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2538-210">입력</span><span class="sxs-lookup"><span data-stu-id="b2538-210">INPUTS</span></span>

### <span data-ttu-id="b2538-211">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="b2538-211">VirtualMachineScaleSet</span></span>
<span data-ttu-id="b2538-212">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-212">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="b2538-213">출력</span><span class="sxs-lookup"><span data-stu-id="b2538-213">OUTPUTS</span></span>

### <span data-ttu-id="b2538-214">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2538-214">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b2538-215">상속자</span><span class="sxs-lookup"><span data-stu-id="b2538-215">NOTES</span></span>

## <span data-ttu-id="b2538-216">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2538-216">RELATED LINKS</span></span>

[<span data-ttu-id="b2538-217">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-217">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="b2538-218">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-218">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="b2538-219">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-219">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="b2538-220">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-220">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="b2538-221">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-221">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="b2538-222">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-222">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="b2538-223">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="b2538-223">Update-AzVmss</span></span>](./Update-AzVmss.md)


