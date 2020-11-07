---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVM.md
ms.openlocfilehash: 4350a1bca25d94f2d3fab27c202eda4392180027
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697360"
---
# <span data-ttu-id="839bf-101">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-101">New-AzVM</span></span>

## <span data-ttu-id="839bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="839bf-102">SYNOPSIS</span></span>
<span data-ttu-id="839bf-103">가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="839bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="839bf-104">SYNTAX</span></span>

### <span data-ttu-id="839bf-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="839bf-105">SimpleParameterSet (Default)</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] [[-Zone] <String[]>] -Name <String>
 -Credential <PSCredential> [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-Image <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>]
 [-AsJob] [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>]
 [-HostId <String>] [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="839bf-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="839bf-106">DefaultParameterSet</span></span>
```
New-AzVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="839bf-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="839bf-107">DiskFileParameterSet</span></span>
```
New-AzVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> [-VirtualNetworkName <String>]
 [-AddressPrefix <String>] [-SubnetName <String>] [-SubnetAddressPrefix <String>]
 [-PublicIpAddressName <String>] [-DomainNameLabel <String>] [-AllocationMethod <String>]
 [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux] [-Size <String>]
 [-AvailabilitySetName <String>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-AsJob]
 [-DataDiskSizeInGb <Int32[]>] [-EnableUltraSSD] [-ProximityPlacementGroup <String>] [-HostId <String>]
 [-Priority <String>] [-EvictionPolicy <String>] [-MaxPrice <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="839bf-108">설명은</span><span class="sxs-lookup"><span data-stu-id="839bf-108">DESCRIPTION</span></span>
<span data-ttu-id="839bf-109">**AzVM** Cmdlet은 Azure에서 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-109">The **New-AzVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="839bf-110">이 cmdlet은 가상 컴퓨터 개체를 입력으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="839bf-111">New-AzVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-111">Use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="839bf-112">다른 cmdlet을 사용 하 여 AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, Set-AzVMOSDisk 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface, and Set-AzVMOSDisk.</span></span>
<span data-ttu-id="839bf-113">는 `SimpleParameterSet` 일반적인 vm 생성 인수를 선택적으로 만들어 VM을 만드는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="839bf-114">예제의</span><span class="sxs-lookup"><span data-stu-id="839bf-114">EXAMPLES</span></span>

### <span data-ttu-id="839bf-115">예제 1: 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="839bf-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="839bf-116">이 예제 스크립트는 가상 컴퓨터를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="839bf-117">스크립트는 VM에 대 한 사용자 이름 및 암호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="839bf-118">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="839bf-119">예제 2: 사용자 지정 사용자 이미지에서 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="839bf-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="839bf-120">이 예제에서는 기존 sys-prepped, 일반화 된 사용자 지정 운영 체제 이미지를 가져와 데이터 디스크를 연결 하 고, 새 네트워크를 프로 비전 하 고, VHD를 배포 하 고, 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>
<span data-ttu-id="839bf-121">이 스크립트는 사용자 조작이 필요한 **Get 자격 증명** 을 호출 하는 대신 로컬 가상 컴퓨터 관리자 자격 증명을 인라인으로 사용 하므로 자동 프로 비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>
<span data-ttu-id="839bf-122">이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="839bf-123">**AzSubscription** cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-123">You can confirm your login status by using the **Get-AzSubscription** cmdlet.</span></span>

### <span data-ttu-id="839bf-124">예제 3: 공용 IP 없이 marketplace 이미지에서 VM 만들기</span><span class="sxs-lookup"><span data-stu-id="839bf-124">Example 3: Create a VM from a marketplace image without a Public IP</span></span>
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

<span data-ttu-id="839bf-125">이 예제에서는 공용 IP 주소 또는 네트워크 보안 그룹을 만들지 않고 새 네트워크를 프로 비전 하 고 마켓플레이스에서 Windows VM을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-125">This example provisions a new network and deploys a Windows VM from the Marketplace without creating a public IP address or Network Security Group.</span></span>
<span data-ttu-id="839bf-126">이 스크립트는 사용자 조작이 필요한 **Get 자격 증명** 을 호출 하는 대신 로컬 가상 컴퓨터 관리자 자격 증명을 인라인으로 사용 하므로 자동 프로 비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-126">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

## <span data-ttu-id="839bf-127">변수</span><span class="sxs-lookup"><span data-stu-id="839bf-127">PARAMETERS</span></span>

### <span data-ttu-id="839bf-128">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="839bf-128">-AddressPrefix</span></span>
<span data-ttu-id="839bf-129">VM에 대해 생성 될 가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-129">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="839bf-130">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="839bf-130">-AllocationMethod</span></span>
<span data-ttu-id="839bf-131">VM에 대해 생성 되는 공용 IP의 IP 할당 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-131">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="839bf-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="839bf-132">-AsJob</span></span>
<span data-ttu-id="839bf-133">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-133">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="839bf-134">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="839bf-134">-AvailabilitySetName</span></span>
<span data-ttu-id="839bf-135">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-135">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="839bf-136">-Credential</span><span class="sxs-lookup"><span data-stu-id="839bf-136">-Credential</span></span>
<span data-ttu-id="839bf-137">VM에 대 한 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-137">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="839bf-138">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="839bf-138">-DataDiskSizeInGb</span></span>
<span data-ttu-id="839bf-139">데이터 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-139">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="839bf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839bf-140">-DefaultProfile</span></span>
<span data-ttu-id="839bf-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="839bf-142">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="839bf-142">-DisableBginfoExtension</span></span>
<span data-ttu-id="839bf-143">이 cmdlet이 가상 컴퓨터에 **Bg-bg&platform 정보** 확장을 설치 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-143">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="839bf-144">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="839bf-144">-DiskFile</span></span>
<span data-ttu-id="839bf-145">클라우드에 업로드 하 고 VM을 만들기 위해 가상 하드 디스크 파일에 대 한 로컬 경로를 사용 하 고 접미사로 ' .vhd '을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-145">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="839bf-146">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="839bf-146">-DomainNameLabel</span></span>
<span data-ttu-id="839bf-147">VM의 정규화 된 도메인 이름 (FQDN)에 대 한 하위 도메인 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-147">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="839bf-148">이는 양식을 사용 `{domainNameLabel}.{location}.cloudapp.azure.com` 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-148">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="839bf-149">-EnableUltraSSD</span><span class="sxs-lookup"><span data-stu-id="839bf-149">-EnableUltraSSD</span></span>
<span data-ttu-id="839bf-150">Vm에 UltraSSD 디스크를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-150">Use UltraSSD disks for the vm.</span></span>

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

### <span data-ttu-id="839bf-151">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="839bf-151">-EvictionPolicy</span></span>
<span data-ttu-id="839bf-152">낮은 우선 순위의 가상 컴퓨터에 대 한 제거 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-152">The eviction policy for the low priority virtual machine.</span></span>  <span data-ttu-id="839bf-153">' 할당 되지 않음 ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-153">Only supported value is 'Deallocate'.</span></span>

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

### <span data-ttu-id="839bf-154">-HostId</span><span class="sxs-lookup"><span data-stu-id="839bf-154">-HostId</span></span>
<span data-ttu-id="839bf-155">호스트의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-155">The Id of Host</span></span>

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

### <span data-ttu-id="839bf-156">-이미지</span><span class="sxs-lookup"><span data-stu-id="839bf-156">-Image</span></span>
<span data-ttu-id="839bf-157">VM이 빌드될 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-157">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="839bf-158">여기에는 Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-158">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="839bf-159">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="839bf-159">-LicenseType</span></span>
<span data-ttu-id="839bf-160">가상 컴퓨터의 이미지나 디스크에 온-프레미스 라이선스가 부여 되었음을 나타내는 라이선스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-160">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="839bf-161">이 값은 Windows Server 운영 체제를 포함 하는 이미지에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-161">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="839bf-162">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-162">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="839bf-163">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="839bf-163">Windows_Client</span></span>
- <span data-ttu-id="839bf-164">Windows_Server이 값을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-164">Windows_Server This value cannot be updated.</span></span>
<span data-ttu-id="839bf-165">업데이트에이 매개 변수를 지정 하면 해당 값이 가상 컴퓨터의 초기 값과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-165">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="839bf-166">-Linux</span><span class="sxs-lookup"><span data-stu-id="839bf-166">-Linux</span></span>
<span data-ttu-id="839bf-167">디스크 파일이 Linux VM (지정 된 경우)에 대 한 것인지 여부를 나타냅니다. 또는 Windows가 기본적으로 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-167">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="839bf-168">-위치</span><span class="sxs-lookup"><span data-stu-id="839bf-168">-Location</span></span>
<span data-ttu-id="839bf-169">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-169">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="839bf-170">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="839bf-170">-MaxPrice</span></span>
<span data-ttu-id="839bf-171">낮은 우선 순위의 가상 컴퓨터 청구에 대 한 최대 가격입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-171">The max price of the billing of a low priority virtual machine.</span></span>

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

### <span data-ttu-id="839bf-172">-이름</span><span class="sxs-lookup"><span data-stu-id="839bf-172">-Name</span></span>
<span data-ttu-id="839bf-173">VM 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-173">The name of the VM resource.</span></span>

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

### <span data-ttu-id="839bf-174">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="839bf-174">-OpenPorts</span></span>
<span data-ttu-id="839bf-175">생성 된 VM에 대 한 NSG (네트워크 보안 그룹)에서 열리는 포트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-175">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="839bf-176">기본값은 선택한 이미지의 종류 (즉, Windows: 3389, 5985, Linux: 22)에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-176">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="839bf-177">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="839bf-177">-Priority</span></span>
<span data-ttu-id="839bf-178">가상 컴퓨터에 대 한 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-178">The priority for the virtual machine.</span></span>  <span data-ttu-id="839bf-179">' 일반 ' 및 ' 낮음 ' 값만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-179">Only supported values are 'Regular' and 'Low'.</span></span>

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

### <span data-ttu-id="839bf-180">-ProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="839bf-180">-ProximityPlacementGroup</span></span>
<span data-ttu-id="839bf-181">이 VM에 사용할 근접 배치 그룹의 이름 또는 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-181">The name or resource id of the Proximity Placement Group to use with this VM.</span></span>

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

### <span data-ttu-id="839bf-182">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="839bf-182">-PublicIpAddressName</span></span>
<span data-ttu-id="839bf-183">만든 VM에서 사용할 새 공용 IP 주소 (또는 기존)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-183">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="839bf-184">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-184">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="839bf-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839bf-185">-ResourceGroupName</span></span>
<span data-ttu-id="839bf-186">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-186">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="839bf-187">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="839bf-187">-SecurityGroupName</span></span>
<span data-ttu-id="839bf-188">사용할 생성 된 VM에 대 한 새 (또는 기존) 네트워크 보안 그룹 (NSG)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-188">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="839bf-189">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-189">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="839bf-190">-크기</span><span class="sxs-lookup"><span data-stu-id="839bf-190">-Size</span></span>
<span data-ttu-id="839bf-191">가상 컴퓨터 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-191">The Virtual Machine Size.</span></span>  <span data-ttu-id="839bf-192">기본값은 Standard_DS1_v2입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-192">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="839bf-193">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="839bf-193">-SubnetAddressPrefix</span></span>
<span data-ttu-id="839bf-194">VM에 대해 생성 될 서브넷의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-194">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="839bf-195">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="839bf-195">-SubnetName</span></span>
<span data-ttu-id="839bf-196">생성 된 VM에서 사용할 새 (또는 기존) 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-196">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="839bf-197">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-197">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="839bf-198">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="839bf-198">-SystemAssignedIdentity</span></span>
<span data-ttu-id="839bf-199">매개 변수가 있으면 VM에 자동으로 생성 되는 관리 시스템 id가 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-199">If the parameter is present then the VM is assigned a managed system identity that is auto generated.</span></span>

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

### <span data-ttu-id="839bf-200">태그</span><span class="sxs-lookup"><span data-stu-id="839bf-200">-Tag</span></span>
<span data-ttu-id="839bf-201">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-201">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="839bf-202">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-202">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="839bf-203">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-203">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="839bf-204">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="839bf-204">-UserAssignedIdentity</span></span>
<span data-ttu-id="839bf-205">VM에 할당 해야 하는 관리 되는 서비스 id의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-205">The name of a managed service identity that should be assigned to the VM.</span></span>

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

### <span data-ttu-id="839bf-206">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="839bf-206">-VirtualNetworkName</span></span>
<span data-ttu-id="839bf-207">생성 된 VM에서 사용할 새 (또는 기존) 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-207">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="839bf-208">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-208">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="839bf-209">-VM</span><span class="sxs-lookup"><span data-stu-id="839bf-209">-VM</span></span>
<span data-ttu-id="839bf-210">만들 로컬 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-210">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="839bf-211">가상 컴퓨터 개체를 가져오려면 New-AzVMConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-211">To obtain a virtual machine object, use the New-AzVMConfig cmdlet.</span></span>
<span data-ttu-id="839bf-212">다른 cmdlet을 사용 하 여 AzVMOperatingSystem, Set-AzVMSourceImage, Add-AzVMNetworkInterface 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-212">Other cmdlets can be used to configure the virtual machine, such as Set-AzVMOperatingSystem, Set-AzVMSourceImage, and Add-AzVMNetworkInterface.</span></span>

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

### <span data-ttu-id="839bf-213">-Zone</span><span class="sxs-lookup"><span data-stu-id="839bf-213">-Zone</span></span>
<span data-ttu-id="839bf-214">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-214">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="839bf-215">-확인</span><span class="sxs-lookup"><span data-stu-id="839bf-215">-Confirm</span></span>
<span data-ttu-id="839bf-216">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="839bf-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="839bf-217">-WhatIf</span></span>
<span data-ttu-id="839bf-218">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="839bf-219">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="839bf-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839bf-220">CommonParameters</span></span>
<span data-ttu-id="839bf-221">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839bf-222">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="839bf-222">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839bf-223">입력</span><span class="sxs-lookup"><span data-stu-id="839bf-223">INPUTS</span></span>

### <span data-ttu-id="839bf-224">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="839bf-224">System.String</span></span>

### <span data-ttu-id="839bf-225">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-225">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="839bf-226">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="839bf-226">System.String[]</span></span>

### <span data-ttu-id="839bf-227">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="839bf-227">System.Collections.Hashtable</span></span>

## <span data-ttu-id="839bf-228">출력</span><span class="sxs-lookup"><span data-stu-id="839bf-228">OUTPUTS</span></span>

### <span data-ttu-id="839bf-229">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-229">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

### <span data-ttu-id="839bf-230">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="839bf-230">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="839bf-231">상속자</span><span class="sxs-lookup"><span data-stu-id="839bf-231">NOTES</span></span>

## <span data-ttu-id="839bf-232">관련 링크</span><span class="sxs-lookup"><span data-stu-id="839bf-232">RELATED LINKS</span></span>

[<span data-ttu-id="839bf-233">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-233">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="839bf-234">제거-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-234">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="839bf-235">다시 시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-235">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="839bf-236">시작-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-236">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="839bf-237">중지-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-237">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="839bf-238">업데이트-AzVM</span><span class="sxs-lookup"><span data-stu-id="839bf-238">Update-AzVM</span></span>](./Update-AzVM.md)

[<span data-ttu-id="839bf-239">추가-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="839bf-239">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="839bf-240">추가-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="839bf-240">Add-AzVMNetworkInterface</span></span>](./Add-AzVMNetworkInterface.md)

[<span data-ttu-id="839bf-241">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="839bf-241">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="839bf-242">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="839bf-242">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="839bf-243">Set-AzVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="839bf-243">Set-AzVMSourceImage</span></span>](./Set-AzVMSourceImage.md)

[<span data-ttu-id="839bf-244">Set-AzVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="839bf-244">Set-AzVMOSDisk</span></span>](./Set-AzVMOSDisk.md)

