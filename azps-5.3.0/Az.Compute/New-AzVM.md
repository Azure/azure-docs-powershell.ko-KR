---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 21c15b0395479a1a22e6b8420a97a3a7c0b75bce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496033"
---
# <span data-ttu-id="5e433-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-101">New-AzVM</span></span>

## <span data-ttu-id="5e433-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e433-102">SYNOPSIS</span></span>
<span data-ttu-id="5e433-103">가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="5e433-104">구문</span><span class="sxs-lookup"><span data-stu-id="5e433-104">SYNTAX</span></span>

### <span data-ttu-id="5e433-105">SimpleParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5e433-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>]
 [-HostId <String>] [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e433-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e433-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e433-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e433-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-VmssId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>] [-EncryptionAtHost]
 [-HostGroupId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e433-108">설명</span><span class="sxs-lookup"><span data-stu-id="5e433-108">DESCRIPTION</span></span>
<span data-ttu-id="5e433-109">**New-AzVM** cmdlet은 Azure에서 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="5e433-110">이 cmdlet은 가상 머신 개체를 입력으로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="5e433-111">New-AzVMConfig cmdlet을 사용하여 가상 머신 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="5e433-112">다른 cmdlet을 사용하여 Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface 및 Set-AzVMOSDisk와 같은 가상 머신을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="5e433-113">이 기능은 공통 VM 만들기 인수를 선택적으로 만들어 `SimpleParameterSet` VM을 만드는 편리한 메서드를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="5e433-114">예제</span><span class="sxs-lookup"><span data-stu-id="5e433-114">EXAMPLES</span></span>

### <span data-ttu-id="5e433-115">예제 1: 가상 머신 만들기</span><span class="sxs-lookup"><span data-stu-id="5e433-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzVM -Name MyVm -Credential (Get-Credential)

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

<span data-ttu-id="5e433-116">이 예제 스크립트는 가상 머신을 만드는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="5e433-117">스크립트는 VM에 대한 사용자 이름 및 암호를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="5e433-118">이 스크립트는 다른 여러 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="5e433-119">예제 2: 사용자 지정 사용자 이미지에서 가상 머신 만들기</span><span class="sxs-lookup"><span data-stu-id="5e433-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5e433-120">이 예제에서는 기존 sys가 미리 제공된 일반화된 사용자 지정 운영 체제 이미지를 사용하여 데이터 디스크를 연결하고, 새 네트워크를 프로비전하고, VHD를 배포하고, 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="5e433-121">이 스크립트는 사용자 상호 작용이 필요한 **Get-Credential을** 호출하는 대신 로컬 가상 머신 관리자 자격 증명 인라인을 사용하기 때문에 자동 프로비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="5e433-122">이 스크립트는 Azure 계정에 이미 로그인되어 있는 것으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="5e433-123">**Get-AzSubscription** cmdlet을 사용하여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="5e433-124">예제 3: 공용 IP 없이 마켓플레이스 이미지에서 VM 만들기</span><span class="sxs-lookup"><span data-stu-id="5e433-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
```
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString <password> -AsPlainText -Force
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
$ComputerName = "MyVM"
$VMName = "MyVM"
$VMSize = "Standard_DS3"

$NetworkName = "MyNet"
$NICName = "MyNIC"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$NIC = New-AzNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

$VirtualMachine = New-AzVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName 'MicrosoftWindowsServer' -Offer 'WindowsServer' -Skus '2012-R2-Datacenter' -Version latest

New-AzVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

<span data-ttu-id="5e433-125">이 예제에서는 새 네트워크를 프로비전하고 공용 IP 주소 또는 네트워크 보안 그룹을 만들지 않고 Marketplace에서 Windows VM을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="5e433-126">이 스크립트는 사용자 상호 작용이 필요한 **Get-Credential을** 호출하는 대신 로컬 가상 머신 관리자 자격 증명 인라인을 사용하기 때문에 자동 프로비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="5e433-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e433-127">PARAMETERS</span></span>

### <span data-ttu-id="5e433-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e433-128">-AddressPrefix</span></span>
<span data-ttu-id="5e433-129">VM에 대해 만들어질 가상 네트워크에 대한 주소 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-129">The address prefix for the virtual network which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="5e433-130">-AllocationMethod</span></span>
<span data-ttu-id="5e433-131">VM에 대해 만들 공용 IP에 대한 IP 할당 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e433-132">-AsJob</span></span>
<span data-ttu-id="5e433-133">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5e433-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="5e433-134">-AvailabilitySetName</span></span>
<span data-ttu-id="5e433-135">가용성 집합의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-135">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="5e433-136">-Credential</span></span>
<span data-ttu-id="5e433-137">VM에 대한 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="5e433-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="5e433-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="5e433-139">데이터 디스크의 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-139">Specifies the sizes of data disks in GB.</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e433-140">-DefaultProfile</span></span>
<span data-ttu-id="5e433-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e433-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="5e433-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="5e433-143">이 cmdlet이 가상 머신에 **BG 정보** 확장을 설치하지 않는다는 의미입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="5e433-144">-DiskFile</span></span>
<span data-ttu-id="5e433-145">클라우드에 업로드하고 VM을 만들기 위한 가상 하드 디스크 파일의 로컬 경로로, 접미사로 '.vhd'가 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

```yaml
Type: System.String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="5e433-146">-DomainNameLabel</span></span>
<span data-ttu-id="5e433-147">VM의 FQDN(정식 도메인 이름)에 대한 하위 도메인 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="5e433-148">이렇게 하면 양식이 `{domainNameLabel}.{location}.cloudapp.azure.com` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-149">-EnableUltrassd</span><span class="sxs-lookup"><span data-stu-id="5e433-149">-EnableUltraSSD</span></span>
<span data-ttu-id="5e433-150">vm에 UltraSSD 디스크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-150">Use UltraSSD disks for the vm.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="5e433-151">-EvictionPolicy</span></span>
<span data-ttu-id="5e433-152">Azure Spot 가상 머신에 대한 지우기 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-152">The eviction policy for the Azure Spot virtual machine.</span></span>  <span data-ttu-id="5e433-153">지원되는 값은 'Deallocate' 및 'Delete'입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-153">Supported values are 'Deallocate' and 'Delete'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-154">-HostGroupId</span><span class="sxs-lookup"><span data-stu-id="5e433-154">-HostGroupId</span></span>
<span data-ttu-id="5e433-155">가상 머신이 상주할 전용 호스트 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-155">Specifies the dedicated host group the virtual machine will reside in.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-156">-HostId</span><span class="sxs-lookup"><span data-stu-id="5e433-156">-HostId</span></span>
<span data-ttu-id="5e433-157">호스트의 ID</span><span class="sxs-lookup"><span data-stu-id="5e433-157">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-158">-Image</span><span class="sxs-lookup"><span data-stu-id="5e433-158">-Image</span></span>
<span data-ttu-id="5e433-159">VM을 구축할 친숙한 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-159">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="5e433-160">여기에는 Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-160">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases: ImageName

Required: False
Position: Named
Default value: Win2016Datacenter
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-161">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5e433-161">-LicenseType</span></span>
<span data-ttu-id="5e433-162">가상 머신에 대한 이미지 또는 디스크의 사용이 허가된 경우를 나타내는 라이선스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-162">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="5e433-163">Windows Server에 사용할 수 있는 값은</span><span class="sxs-lookup"><span data-stu-id="5e433-163">Possible values for Windows Server are:</span></span>
- <span data-ttu-id="5e433-164">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="5e433-164">Windows_Client</span></span>
- <span data-ttu-id="5e433-165">Windows_Server Linux Server 운영 체제에 사용할 수 있는 값은</span><span class="sxs-lookup"><span data-stu-id="5e433-165">Windows_Server Possible values for Linux Server operating system are:</span></span> 
- <span data-ttu-id="5e433-166">RHEL_BYOS(RHEL의 경우)</span><span class="sxs-lookup"><span data-stu-id="5e433-166">RHEL_BYOS (for RHEL)</span></span> 
- <span data-ttu-id="5e433-167">SLES_BYOS(SUSE의 경우)</span><span class="sxs-lookup"><span data-stu-id="5e433-167">SLES_BYOS (for SUSE)</span></span> 

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-168">-Linux</span><span class="sxs-lookup"><span data-stu-id="5e433-168">-Linux</span></span>
<span data-ttu-id="5e433-169">지정된 경우 디스크 파일이 Linux VM용인지 여부를 나타냅니다. 또는 Windows(기본적으로 지정되지 않은 경우)입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-169">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-170">-Location</span><span class="sxs-lookup"><span data-stu-id="5e433-170">-Location</span></span>
<span data-ttu-id="5e433-171">가상 머신의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-171">Specifies a location for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-172">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="5e433-172">-MaxPrice</span></span>
<span data-ttu-id="5e433-173">우선 순위가 낮은 가상 머신에 대한 청구의 최대 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-173">The max price of the billing of a low priority virtual machine.</span></span>

```yaml
Type: System.Double
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-174">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="5e433-174">-EncryptionAtHost</span></span>
<span data-ttu-id="5e433-175">암호화AtHost 속성은 요청에서 사용자가 가상 머신 또는 가상 머신 확장 집합에 대한 호스트 암호화를 활성화하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-175">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="5e433-176">이렇게 하면 호스트 자체의 리소스/임시 디스크를 포함한 모든 디스크에 대한 암호화가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-176">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> <span data-ttu-id="5e433-177">기본값: 이 속성이 리소스에 대해 true로 설정되지 않으면 호스트의 암호화가 비활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-177">Default: The Encryption at host will be disabled unless this property is set to true for the resource.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskParameterSet
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="5e433-178">-Name</span><span class="sxs-lookup"><span data-stu-id="5e433-178">-Name</span></span>
<span data-ttu-id="5e433-179">VM 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-179">The name of the VM resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-180">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="5e433-180">-OpenPorts</span></span>
<span data-ttu-id="5e433-181">만든 VM에 대한 NSG(네트워크 보안 그룹)에서 열 포트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-181">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="5e433-182">기본값은 선택한 이미지 유형(예: Windows: 3389, 5985 및 Linux: 22)에 따라 다릅니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-182">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-183">-Priority</span><span class="sxs-lookup"><span data-stu-id="5e433-183">-Priority</span></span>
<span data-ttu-id="5e433-184">가상 머신에 대한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-184">The priority for the virtual machine.</span></span>  <span data-ttu-id="5e433-185">지원되는 값만 'Regular', 'Spot' 및 'Low'입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-185">Only supported values are 'Regular', 'Spot' and 'Low'.</span></span>
<span data-ttu-id="5e433-186">'일반'은 일반 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-186">'Regular' is for regular virtual machine.</span></span>
<span data-ttu-id="5e433-187">'Spot'은 스폿 가상 머신에 대한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-187">'Spot' is for spot virtual machine.</span></span>
<span data-ttu-id="5e433-188">'낮음'은 스폿 가상 머신에도 사용되지만 'Spot'로 대체됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-188">'Low' is also for spot virtual machine but is replaced by 'Spot'.</span></span> <span data-ttu-id="5e433-189">'낮음' 대신 'Spot'을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="5e433-189">Please use 'Spot' instead of 'Low'.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-190">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="5e433-190">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="5e433-191">이 가상 머신에 사용할 근접 배치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-191">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases: ProximityPlacementGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-192">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="5e433-192">-PublicIpAddressName</span></span>
<span data-ttu-id="5e433-193">만든 VM에서 사용할 새(또는 기존) 공용 IP 주소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-193">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="5e433-194">지정하지 않으면 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-194">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-195">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e433-195">-ResourceGroupName</span></span>
<span data-ttu-id="5e433-196">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-196">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-197">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="5e433-197">-SecurityGroupName</span></span>
<span data-ttu-id="5e433-198">사용할 만든 VM에 대한 새(또는 기존) NSG(네트워크 보안 그룹)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-198">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="5e433-199">지정하지 않으면 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-199">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-200">-Size</span><span class="sxs-lookup"><span data-stu-id="5e433-200">-Size</span></span>
<span data-ttu-id="5e433-201">가상 머신 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-201">The Virtual Machine Size.</span></span>  <span data-ttu-id="5e433-202">기본값은 다음 Standard_DS1_v2.</span><span class="sxs-lookup"><span data-stu-id="5e433-202">The Default Value is: Standard_DS1_v2.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-203">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5e433-203">-SubnetAddressPrefix</span></span>
<span data-ttu-id="5e433-204">VM에 대해 만들 서브넷에 대한 주소 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-204">The address prefix for the subnet which will be created for the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-205">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="5e433-205">-SubnetName</span></span>
<span data-ttu-id="5e433-206">만든 VM에 사용할 새(또는 기존) 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-206">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="5e433-207">지정하지 않으면 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-207">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-208">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5e433-208">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5e433-209">매개 변수가 있는 경우 VM에 자동 생성되는 관리 시스템 ID가 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-209">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-210">-Tag</span><span class="sxs-lookup"><span data-stu-id="5e433-210">-Tag</span></span>
<span data-ttu-id="5e433-211">리소스 및 리소스 그룹에 이름-값 쌍 집합으로 태그를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-211">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="5e433-212">리소스에 태그를 추가하면 리소스 그룹에서 리소스를 함께 그룹화하고 사용자 자신의 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-212">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="5e433-213">각 리소스 또는 리소스 그룹은 최대 15개 태그를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-213">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-214">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5e433-214">-UserAssignedIdentity</span></span>
<span data-ttu-id="5e433-215">VM에 할당해야 하는 관리 서비스 ID의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-215">The name of a managed service identity that should be assigned to the VM.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-216">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="5e433-216">-VirtualNetworkName</span></span>
<span data-ttu-id="5e433-217">만든 VM에서 사용할 새(또는 기존) 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-217">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="5e433-218">지정하지 않으면 이름이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-218">If not specified, a name will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-219">-VM</span><span class="sxs-lookup"><span data-stu-id="5e433-219">-VM</span></span>
<span data-ttu-id="5e433-220">만들 로컬 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-220">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="5e433-221">가상 머신 개체를 얻습니다. New-AzVMConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-221">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="5e433-222">다른 cmdlet을 사용하여 Set-AzVMOperatingSystem, Set-AzVMSourceImage 및 Add-AzVMNetworkInterface와 같은 가상 머신을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-222">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: DefaultParameterSet
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-223">-VmssId</span><span class="sxs-lookup"><span data-stu-id="5e433-223">-VmssId</span></span>
<span data-ttu-id="5e433-224">이 VM이 연결될 Virtual Machine Scale Set의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-224">The ID of Virtual Machine Scale Set that this VM will be associated with</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-225">-Zone</span><span class="sxs-lookup"><span data-stu-id="5e433-225">-Zone</span></span>
<span data-ttu-id="5e433-226">가상 머신의 영역 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-226">Specifies the zone list of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e433-227">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e433-227">-Confirm</span></span>
<span data-ttu-id="5e433-228">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-228">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e433-229">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e433-229">-WhatIf</span></span>
<span data-ttu-id="5e433-230">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5e433-230">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e433-231">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-231">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e433-232">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e433-232">CommonParameters</span></span>
<span data-ttu-id="5e433-233">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5e433-233">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e433-234">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e433-234">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e433-235">입력</span><span class="sxs-lookup"><span data-stu-id="5e433-235">INPUTS</span></span>

### <span data-ttu-id="5e433-236">System.String</span><span class="sxs-lookup"><span data-stu-id="5e433-236">System.String</span></span>

### <span data-ttu-id="5e433-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5e433-237">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="5e433-238">System.String[]</span><span class="sxs-lookup"><span data-stu-id="5e433-238">System.String[]</span></span>

### <span data-ttu-id="5e433-239">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5e433-239">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5e433-240">출력</span><span class="sxs-lookup"><span data-stu-id="5e433-240">OUTPUTS</span></span>

### <span data-ttu-id="5e433-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5e433-241">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="5e433-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5e433-242">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5e433-243">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5e433-243">NOTES</span></span>

## <span data-ttu-id="5e433-244">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e433-244">RELATED LINKS</span></span>

[<span data-ttu-id="5e433-245">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-245">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5e433-246">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-246">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="5e433-247">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-247">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="5e433-248">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-248">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="5e433-249">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-249">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="5e433-250">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5e433-250">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="5e433-251">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5e433-251">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="5e433-252">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="5e433-252">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="5e433-253">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="5e433-253">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="5e433-254">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5e433-254">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="5e433-255">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="5e433-255">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="5e433-256">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="5e433-256">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)


