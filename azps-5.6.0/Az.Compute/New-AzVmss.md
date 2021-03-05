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
# New-AzVmss

## SYNOPSIS
VMSS를 만듭니다.

## 구문

### DefaultParameter(기본값)
```
New-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SimpleParameterSet
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

## 설명
**New-AzVmss** cmdlet은 Azure에서 VMSS(Virtual Machine Scale Set)를 만듭니다.
간단한 매개 변수 집합() 을 사용하여 미리 설정된 VMSS 및 관련 리소스를 빠르게 `SimpleParameterSet` 만들 수 있습니다. 만들기 전에 VMSS의 각 구성 요소 및 연결된 각 리소스를 정확하게 구성해야 하는 경우 더 고급 시나리오의 경우 기본 매개 변수 `DefaultParameter` 집합() 을 사용합니다.

## 예제

### 예제 1: 다음을 사용하여 VMSS 만들기 **`SimpleParameterSet`**
```powershell
$vmssName = <VMSSNAME>
# Create credentials, I am using one way to create credentials, there are others as well. 
# Pick one that makes the most sense according to your use case.
$vmPassword = ConvertTo-SecureString <PASSWORD_HERE> -AsPlainText -Force
$vmCred = New-Object System.Management.Automation.PSCredential(<USERNAME_HERE>, $vmPassword)

#Create a VMSS using the default settings
New-AzVmss -Credential $vmCred -VMScaleSetName $vmssName
```

위의 명령은 이름과 함께 다음을 `$vmssName` 만듭니다.
* 리소스 그룹
* 가상 네트워크
* 부하 균형 조정기
* 공용 IP
* 인스턴스가 2개인 VMSS

VMSS에서 VM에 대해 선택한 기본 이미지는 `2016-Datacenter Windows Server` SKU입니다. `Standard_DS1_v2`

### 예제 2: 다음을 사용하여 VMSS 만들기 **`DefaultParameterSet`**
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

위의 복잡한 예제에서는 VMSS를 만듭니다. 다음은 일어나는 일에 대한 설명입니다.
* 첫 번째 명령은 지정된 이름과 위치를 사용하여 리소스 그룹을 만듭니다.
* 두 번째 명령은 **New-AzStorageAccount** cmdlet을 사용하여 저장소 계정을 생성합니다.
* 그런 다음 세 번째 명령은 **Get-AzStorageAccount** cmdlet을 사용하여 두 번째 명령에서 만든 저장소 계정을 얻게 하여 결과를 $STOAccount 변수에 저장합니다.
* 다섯 번째 명령은 **New-AzVirtualNetworkSubnetConfig** cmdlet을 사용하여 서브넷을 만들고 결과를 $SubNet.
* 여섯 번째 명령은 **New-AzVirtualNetwork** cmdlet을 사용하여 가상 네트워크를 만들고 결과를 $VNet.
* 일곱 번째 명령은 **Get-AzVirtualNetwork를** 사용하여 여섯 번째 명령에서 만든 가상 네트워크에 대한 정보를 얻게 하여 이라는 변수에 정보를 $VNet.
* 8번째 및 9번째 명령은 **New-AzPublicIpAddress** 및 **Get-AzureRmPublicIpAddress를** 사용하여 해당 공용 IP 주소에서 정보를 만들고 얻을 수 있습니다.
* 명령은 이름의 변수에 정보를 $PubIP.
* 10번째 명령은 **New- AzureRmLoadBalancerFrontendIpConfig** cmdlet을 사용하여 프런트 엔드 부하 분산을 만들고 결과를 $Frontend.
* 열한 번째 명령은 **New-AzLoadBalancerBackendAddressPoolConfig를** 사용하여 백던드 주소 풀 구성을 만들고 결과를 새 이름의 변수에 $BackendAddressPool.
* 12번째 명령은 **New-AzLoadBalancerProbeConfig를** 사용하여 프로브를 만들고 프로브 정보를 프로브라는 변수에 $Probe.
* 13번째 명령은 **New-AzLoadBalancerInboundNatPoolConfig** cmdlet을 사용하여 NAT(부하 분산기 인바운드 네트워크 주소 변환) 풀 구성을 생성합니다.
* 14번째 명령은 **New-AzLoadBalancerRuleConfig를** 사용하여 부하 분산기 규칙 구성을 만들고 결과를 $LBRule.
* 15번째 명령은 **New-AzLoadBalancer** cmdlet을 사용하여 부하 분산을 만들고 결과를 $ActualLb.
* 16번째 명령은 **Get-AzLoadBalancer를** 사용하여 15번째 명령에서 만든 부하 분산기에 대한 정보를 얻게 하여 해당 변수의 정보를 $ExpectedLb.
* 17번째 명령은 **New-AzVmssIPConfig** cmdlet을 사용하여 VMSS IP 구성을 만들고 해당 정보를 새 이름의 변수에 $IPCfg.
* 18번째 명령은 **New-AzVmssConfig** cmdlet을 사용하여 VMSS 구성 개체를 만들고 결과를 $VMSS.
* 19번째 명령은 **New-AzVmss** cmdlet을 사용하여 VMSS를 생성합니다.

## 매개 변수

### -AllocationMethod
확장 집합(정적 또는 동적)의 공용 IP 주소에 대한 할당 메서드입니다.  값이 제공되지 않는 경우 할당은 정적입니다.

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

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

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

### -BackendPoolName
이 확장 집합의 부하 균형 조정기에서 사용할 백end 주소 풀의 이름입니다.  값이 제공되지 않고 확장 집합과 이름이 같은 새 백end 풀이 만들어집니다.

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

### -BackendPort
확장 집합에서 VM과 통신하기 위해 확장 집합 부하 균형 조정기에서 사용하는 백end 포트 번호입니다.  값이 지정되지 않으면 Windows VMS에 3389 및 5985 포트가 사용되어 Linux VM에 포트 22가 사용됩니다.

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

### -자격 증명
이 확장 집합의 VM에 대한 관리자 자격 증명(사용자 이름 및 암호)입니다.

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

### -DataDiskSizeInGb
GB의 데이터 디스크 크기를 지정합니다.

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

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -DomainNameLabel
이 확장 집합에 대한 공용 Fully-Qualified 도메인 이름(FQDN)의 도메인 이름 레이블입니다. 확장 집합에 자동으로 할당되는 도메인 이름의 첫 번째 구성 요소입니다. 자동으로 할당된 도메인 이름은 폼을 사용 합니다. <DomainNameLabel> <Location> . cloudapp.azure.com). 값이 제공되지 않습니다. 기본 도메인 이름 레이블은 및 의 의 수가 <ScaleSetName> <ResourceGroupName> 됩니다.

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

### -EnableUltraSSD
확장 집합의 VM에 UltraSSD 디스크를 사용 합니다.

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

### -EncryptionAtHost
이 매개 변수는 호스트 자체에서 Resource/Temp 디스크를 포함하여 모든 디스크에 대한 암호화를 사용하도록 설정됩니다. 기본값: 이 속성이 리소스에 대해 true로 설정되지 않는 한 호스트의 암호화를 사용하지 않도록 설정됩니다.

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

### -EvictionPolicy
우선 순위가 낮은 가상 머신 확장 집합에 대한 eviction 정책입니다.  지원되는 값만 'Deallocate' 및 'Delete'입니다.

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

### -FrontendPoolName
확장 집합 부하 균형 조정기에서 사용할 프런트 엔드 주소 풀의 이름입니다.  값이 제공되지되면 확장 집합과 동일한 이름으로 새 프런트 엔드 주소 풀이 만들어집니다.

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

### -HostGroupId
가상 머신 확장 집합이 상주할 전용 호스트 그룹을 지정합니다.

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

### -ImageName
이 확장 집합의 VM에 대한 이미지의 이름입니다. 값이 제공되지 않고 "Windows Server 2016 DataCenter" 이미지가 사용됩니다.

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

### -InstanceCount
확장 집합의 VM 이미지 수입니다.  값이 제공되지 않고 2개 인스턴스가 생성됩니다.

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

### -LoadBalancerName
이 확장 집합에 사용할 부하 균형 조정기 이름입니다.  값이 지정되지 않은 경우 확장 집합과 동일한 이름을 사용하는 새 부하 균형 조정기가 만들어집니다.

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

### -Location
이 확장 집합을 만들 Azure 위치입니다.  값이 지정되지 않으면 매개 변수에 참조된 다른 리소스의 위치에서 위치가 유추됩니다.

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

### -MaxPrice
우선 순위가 낮은 가상 머신 확장 집합의 청구의 최대 가격입니다.

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

### -NatBackendPort
인바운드 네트워크 주소 변환에 대한 백end 포트입니다.

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

### -PlatformFaultDomainCount
각 배치 그룹에 대한 장애 도메인 수입니다.

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

### -Priority
확장 집합의 가상 머신에 대한 우선 순위입니다.  지원되는 값만 '일반', 'Spot' 및 'Low'입니다.
'일반'은 일반 가상 머신용입니다.
'Spot'은 가상 머신을 위한 것입니다.
'Low'은 스팟 가상 머신용이지만 'Spot'으로 바 대체됩니다. 'Low' 대신 'Spot'을 사용하세요.

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

### -ProximityPlacementGroupId
이 확장 집합에 사용할 근접 배치 그룹의 리소스 ID입니다.

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

### -PublicIpAddressName
이 확장 집합에 사용할 공용 IP 주소의 이름입니다.  값이 제공되지 않고 확장 집합과 이름이 같은 새 공용 IPAddress가 생성됩니다.

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

### -ResourceGroupName
VMSS의 리소스 그룹의 이름을 지정합니다.  값이 지정되지 않으면 확장 집합과 동일한 이름을 사용하여 새 ResourceGroup이 만들어집니다.

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

### -ScaleInPolicy
가상 머신 확장 집합의 크기 조정 시 따라야 할 규칙입니다.  가능한 값은 'Default', 'OldestVM' 및 'NewestVM'입니다.  가상 머신 확장 집합이 확장될 때 '기본값'은 크기 조정 집합이 영역 전체에 분산됩니다.  그런 다음 오류 도메인에서 가능한 한 균형이 조정됩니다.  각 장애 도메인 내에서 제거를 위해 선택한 가상 머신은 확장으로부터 보호되지 않는 가장 최근의 컴퓨터입니다.  가상 머신 확장 집합이 확장되는 경우 'OldestVM'은 확장으로부터 보호되지 않는 가장 오래된 가상 머신을 제거하기 위해 선택됩니다.  zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.  각 영역 내에서 보호되지 않는 가장 오래된 가상 머신은 제거를 위해 선택됩니다.  가상 머신 확장 집합이 확장되는 경우 'NewestVM'은 확장으로부터 보호되지 않는 가장 최근 가상 머신을 제거하기 위해 선택됩니다.  zonal 가상 머신 확장 집합의 경우 먼저 확장 집합이 영역 전체에서 분산됩니다.  각 영역 내에서 보호되지 않는 가장 새로운 가상 머신은 제거를 위해 선택됩니다.

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

### -SecurityGroupName
이 확장 집합에 적용할 네트워크 보안 그룹의 이름입니다.  값이 제공되지 않고 확장 집합과 이름이 같은 기본 네트워크 보안 그룹이 만들어지며 확장 집합에 적용됩니다.

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

### -SinglePlacementGroup
이 기능을 사용하여 단일 배치 그룹에서 확장 집합을 만들면 기본값은 여러 그룹입니다.

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

### -SkipExtensionsOnOverprovisionedVM
확장이 추가 오버프로비전된 VM에서 실행되지 않는지 지정합니다.

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

### -SubnetAddressPrefix
이 ScaleSet이 사용할 서브넷의 주소 연결선입니다. 값이 제공되지 않고 기본 서브넷 설정(192.168.1.0/24)이 적용됩니다.

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

### -SubnetName
이 확장 집합에 사용할 서브넷의 이름입니다.  값이 제공되지 않고 확장 집합과 동일한 이름으로 새 서브넷이 만들어집니다.

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

### -SystemAssignedIdentity
매개 변수가 있는 경우 확장 집합의 VM은 자동 생성되는 관리되는 시스템 ID를 할당합니다.

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

### -UpgradePolicyMode
이 확장 집합의 VM 인스턴스에 대한 업그레이드 정책 모드입니다.  업그레이드 정책은 자동, 수동 또는 롤링 업그레이드를 지정할 수 있습니다.

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

### -UserAssignedIdentity
확장 집합의 VM에 할당해야 하는 관리 서비스 ID의 이름입니다.

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

### -VirtualMachineScaleSet
이 cmdlet이 만드는 VMSS의 속성을 포함하는 **VirtualMachineScaleSet** 개체를 지정합니다.

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

### -VirtualNetworkName
이름은 이 확장 집합과 함께 사용할 Virtual Network를 엽니 다.  값이 제공되지 않습니다. 확장 집합과 이름이 같은 새 가상 네트워크가 생성됩니다.

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

### -VMScaleSetName
이 cmdlet이 만드는 VMSS의 이름을 지정합니다.

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

### -VmSize
이 확장 집합의 VM 인스턴스의 크기입니다.  크기를 지정하지 Standard_DS1_v2 기본 크기(Standard_DS1_v2)가 사용됩니다.

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

### -VnetAddressPrefix
이 확장 집합과 함께 사용되는 가상 네트워크에 대한 주소 연결선입니다.  값이 제공되지 않습니다. 기본 가상 네트워크 주소 설정(192.168.0.0/16)이 사용됩니다.

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

### -Zone
리소스에 할당된 IP를 표시하는 가용성 영역 목록이 필요합니다.

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

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

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

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## 참고 사항

## 관련 링크

[Get-AzVmss](./Get-AzVmss.md)

[Remove-AzVmss](./Remove-AzVmss.md)

[다시 시작-AzVmss](./Restart-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[Start-AzVmss](./Start-AzVmss.md)

[Stop-AzVmss](./Stop-AzVmss.md)

[Update-AzVmss](./Update-AzVmss.md)


