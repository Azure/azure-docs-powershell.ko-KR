---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526951"
---
# New-AzureRmVM

## SYNOPSIS
가상 컴퓨터를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### SimpleParameterSet (기본값)
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DefaultParameterSet
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DiskFileParameterSet
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 만듭니다.
이 cmdlet은 가상 컴퓨터 개체를 입력으로 받습니다.
New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.
다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터를 구성할 수 있습니다.

는 `SimpleParameterSet` 일반적인 vm 생성 인수를 선택적으로 만들어 VM을 만드는 편리한 방법을 제공 합니다.

## 예제의

### 예제 1: 가상 컴퓨터 만들기
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

이 예제 스크립트는 가상 컴퓨터를 만드는 방법을 보여 줍니다.
스크립트는 VM에 대 한 사용자 이름 및 암호를 요청 합니다.
이 스크립트는 여러 다른 cmdlet을 사용 합니다.

### 예제 2: 사용자 지정 사용자 이미지에서 가상 컴퓨터 만들기
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account.
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance.
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3"
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

이 예제에서는 기존 sys-prepped, 일반화 된 사용자 지정 운영 체제 이미지를 가져와 데이터 디스크를 연결 하 고, 새 네트워크를 프로 비전 하 고, VHD를 배포 하 고, 실행 합니다.

이 스크립트는 사용자 조작이 필요한 **Get 자격 증명** 을 호출 하는 대신 로컬 가상 컴퓨터 관리자 자격 증명을 인라인으로 사용 하므로 자동 프로 비전에 사용할 수 있습니다.

이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.
**AzureSubscription** cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.

## 변수

### -AddressPrefix
VM에 대해 생성 될 가상 네트워크의 주소 접두사입니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllocationMethod
VM에 대해 생성 되는 공용 IP의 IP 할당 방법입니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.

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

### -AvailabilitySetName
가용성 집합의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
VM에 대 한 관리자 자격 증명입니다.

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

### -DataDiskSizeInGb
데이터 디스크의 크기 (GB)를 지정 합니다.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -DisableBginfoExtension
이 cmdlet이 가상 컴퓨터에 **Bg-bg&platform 정보** 확장을 설치 하지 않음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskFile
클라우드에 업로드 하 고 VM을 만들기 위해 가상 하드 디스크 파일에 대 한 로컬 경로를 사용 하 고 접미사로 ' .vhd '을 사용 해야 합니다.

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
VM의 정규화 된 도메인 이름 (FQDN)에 대 한 하위 도메인 레이블입니다.  이는 양식을 사용 `{domainNameLabel}.{location}.cloudapp.azure.com` 합니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
VM이 빌드될 이미지 이름입니다.  여기에는 Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES이 포함 됩니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
가상 컴퓨터의 이미지나 디스크에 온-프레미스 라이선스가 부여 되었음을 나타내는 라이선스 유형을 지정 합니다.
이 값은 Windows Server 운영 체제를 포함 하는 이미지에만 사용 됩니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- Windows_Client
- Windows_Server

이 값을 업데이트할 수 없습니다.
업데이트에이 매개 변수를 지정 하면 해당 값이 가상 컴퓨터의 초기 값과 일치 해야 합니다.

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
디스크 파일이 Linux VM (지정 된 경우)에 대 한 것인지 여부를 나타냅니다. 또는 Windows가 기본적으로 지정 되어 있지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
가상 컴퓨터의 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
VM 리소스의 이름입니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenPorts
생성 된 VM에 대 한 NSG (네트워크 보안 그룹)에서 열리는 포트 목록입니다.  기본값은 선택한 이미지의 종류 (즉, Windows: 3389, 5985, Linux: 22)에 따라 달라 집니다.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicIpAddressName
만든 VM에서 사용할 새 공용 IP 주소 (또는 기존)의 이름입니다.  지정 하지 않으면 이름이 생성 됩니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
사용할 생성 된 VM에 대 한 새 (또는 기존) 네트워크 보안 그룹 (NSG)의 이름입니다.  지정 하지 않으면 이름이 생성 됩니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -크기
가상 컴퓨터 크기입니다.  기본값은 Standard_DS1_v2입니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
VM에 대해 생성 될 서브넷의 주소 접두사입니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
생성 된 VM에서 사용할 새 (또는 기존) 서브넷의 이름입니다.  지정 하지 않으면 이름이 생성 됩니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 태그
리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.
리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.
각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
생성 된 VM에서 사용할 새 (또는 기존) 가상 네트워크의 이름입니다.  지정 하지 않으면 이름이 생성 됩니다.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
만들 로컬 가상 컴퓨터를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 New-AzureRmVMConfig cmdlet을 사용 합니다.
다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface 등의 가상 컴퓨터를 구성할 수 있습니다.

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Zone
가상 컴퓨터의 영역 목록을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.

Cmdlet이 실행 되지 않습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualMachine
' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.

## 출력

### 이는 PSAzureOperationResponse를 계산 하는 명령입니다.

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)

[제거-AzureRmVM](./Remove-AzureRmVM.md)

[다시 시작-AzureRmVM](./Restart-AzureRmVM.md)

[시작-AzureRmVM](./Start-AzureRmVM.md)

[중지-AzureRmVM](./Stop-AzureRmVM.md)

[업데이트-AzureRmVM](./Update-AzureRmVM.md)

[추가-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[추가-AzureRmVMNetworkInterface](./Add-AzureRmVMNetworkInterface.md)

[새로운 AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Set-AzureRmVMSourceImage](./Set-AzureRmVMSourceImage.md)

[Set-AzureRmVMOSDisk](./Set-AzureRmVMOSDisk.md)


