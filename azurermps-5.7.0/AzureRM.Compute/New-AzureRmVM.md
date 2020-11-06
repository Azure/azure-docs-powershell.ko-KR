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
# <span data-ttu-id="f8cca-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-101">New-AzureRmVM</span></span>

## <span data-ttu-id="f8cca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8cca-102">SYNOPSIS</span></span>
<span data-ttu-id="f8cca-103">가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8cca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f8cca-104">SYNTAX</span></span>

### <span data-ttu-id="f8cca-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f8cca-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cca-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8cca-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8cca-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8cca-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8cca-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f8cca-108">DESCRIPTION</span></span>
<span data-ttu-id="f8cca-109">**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="f8cca-110">이 cmdlet은 가상 컴퓨터 개체를 입력으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="f8cca-111">New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="f8cca-112">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="f8cca-113">는 `SimpleParameterSet` 일반적인 vm 생성 인수를 선택적으로 만들어 VM을 만드는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="f8cca-114">예제의</span><span class="sxs-lookup"><span data-stu-id="f8cca-114">EXAMPLES</span></span>

### <span data-ttu-id="f8cca-115">예제 1: 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="f8cca-115">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="f8cca-116">이 예제 스크립트는 가상 컴퓨터를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="f8cca-117">스크립트는 VM에 대 한 사용자 이름 및 암호를 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-117">The script will ask a user name and password for the VM.</span></span>
<span data-ttu-id="f8cca-118">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-118">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="f8cca-119">예제 2: 사용자 지정 사용자 이미지에서 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="f8cca-119">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="f8cca-120">이 예제에서는 기존 sys-prepped, 일반화 된 사용자 지정 운영 체제 이미지를 가져와 데이터 디스크를 연결 하 고, 새 네트워크를 프로 비전 하 고, VHD를 배포 하 고, 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-120">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="f8cca-121">이 스크립트는 사용자 조작이 필요한 **Get 자격 증명** 을 호출 하는 대신 로컬 가상 컴퓨터 관리자 자격 증명을 인라인으로 사용 하므로 자동 프로 비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-121">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="f8cca-122">이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-122">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="f8cca-123">**AzureSubscription** cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-123">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="f8cca-124">변수</span><span class="sxs-lookup"><span data-stu-id="f8cca-124">PARAMETERS</span></span>

### <span data-ttu-id="f8cca-125">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8cca-125">-AddressPrefix</span></span>
<span data-ttu-id="f8cca-126">VM에 대해 생성 될 가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-126">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="f8cca-127">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="f8cca-127">-AllocationMethod</span></span>
<span data-ttu-id="f8cca-128">VM에 대해 생성 되는 공용 IP의 IP 할당 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-128">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="f8cca-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8cca-129">-AsJob</span></span>
<span data-ttu-id="f8cca-130">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-130">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f8cca-131">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="f8cca-131">-AvailabilitySetName</span></span>
<span data-ttu-id="f8cca-132">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-132">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="f8cca-133">-Credential</span><span class="sxs-lookup"><span data-stu-id="f8cca-133">-Credential</span></span>
<span data-ttu-id="f8cca-134">VM에 대 한 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-134">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="f8cca-135">-DataDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="f8cca-135">-DataDiskSizeInGb</span></span>
<span data-ttu-id="f8cca-136">데이터 디스크의 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-136">Specifies the sizes of data disks in GB.</span></span>

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

### <span data-ttu-id="f8cca-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8cca-137">-DefaultProfile</span></span>
<span data-ttu-id="f8cca-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8cca-139">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="f8cca-139">-DisableBginfoExtension</span></span>
<span data-ttu-id="f8cca-140">이 cmdlet이 가상 컴퓨터에 **Bg-bg&platform 정보** 확장을 설치 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-140">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="f8cca-141">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="f8cca-141">-DiskFile</span></span>
<span data-ttu-id="f8cca-142">클라우드에 업로드 하 고 VM을 만들기 위해 가상 하드 디스크 파일에 대 한 로컬 경로를 사용 하 고 접미사로 ' .vhd '을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-142">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="f8cca-143">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="f8cca-143">-DomainNameLabel</span></span>
<span data-ttu-id="f8cca-144">VM의 정규화 된 도메인 이름 (FQDN)에 대 한 하위 도메인 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-144">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="f8cca-145">이는 양식을 사용 `{domainNameLabel}.{location}.cloudapp.azure.com` 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-145">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="f8cca-146">-ImageName</span><span class="sxs-lookup"><span data-stu-id="f8cca-146">-ImageName</span></span>
<span data-ttu-id="f8cca-147">VM이 빌드될 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-147">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="f8cca-148">여기에는 Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-148">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="f8cca-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f8cca-149">-LicenseType</span></span>
<span data-ttu-id="f8cca-150">가상 컴퓨터의 이미지나 디스크에 온-프레미스 라이선스가 부여 되었음을 나타내는 라이선스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-150">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="f8cca-151">이 값은 Windows Server 운영 체제를 포함 하는 이미지에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-151">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="f8cca-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-152">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f8cca-153">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="f8cca-153">Windows_Client</span></span>
- <span data-ttu-id="f8cca-154">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="f8cca-154">Windows_Server</span></span>

<span data-ttu-id="f8cca-155">이 값을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-155">This value cannot be updated.</span></span>
<span data-ttu-id="f8cca-156">업데이트에이 매개 변수를 지정 하면 해당 값이 가상 컴퓨터의 초기 값과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-156">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="f8cca-157">-Linux</span><span class="sxs-lookup"><span data-stu-id="f8cca-157">-Linux</span></span>
<span data-ttu-id="f8cca-158">디스크 파일이 Linux VM (지정 된 경우)에 대 한 것인지 여부를 나타냅니다. 또는 Windows가 기본적으로 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-158">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="f8cca-159">-위치</span><span class="sxs-lookup"><span data-stu-id="f8cca-159">-Location</span></span>
<span data-ttu-id="f8cca-160">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-160">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="f8cca-161">-이름</span><span class="sxs-lookup"><span data-stu-id="f8cca-161">-Name</span></span>
<span data-ttu-id="f8cca-162">VM 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-162">The name of the VM resource.</span></span>

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

### <span data-ttu-id="f8cca-163">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="f8cca-163">-OpenPorts</span></span>
<span data-ttu-id="f8cca-164">생성 된 VM에 대 한 NSG (네트워크 보안 그룹)에서 열리는 포트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-164">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="f8cca-165">기본값은 선택한 이미지의 종류 (즉, Windows: 3389, 5985, Linux: 22)에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-165">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="f8cca-166">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="f8cca-166">-PublicIpAddressName</span></span>
<span data-ttu-id="f8cca-167">만든 VM에서 사용할 새 공용 IP 주소 (또는 기존)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-167">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="f8cca-168">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-168">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f8cca-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cca-169">-ResourceGroupName</span></span>
<span data-ttu-id="f8cca-170">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-170">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f8cca-171">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="f8cca-171">-SecurityGroupName</span></span>
<span data-ttu-id="f8cca-172">사용할 생성 된 VM에 대 한 새 (또는 기존) 네트워크 보안 그룹 (NSG)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-172">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="f8cca-173">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-173">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f8cca-174">-크기</span><span class="sxs-lookup"><span data-stu-id="f8cca-174">-Size</span></span>
<span data-ttu-id="f8cca-175">가상 컴퓨터 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-175">The Virtual Machine Size.</span></span>  <span data-ttu-id="f8cca-176">기본값은 Standard_DS1_v2입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-176">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="f8cca-177">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="f8cca-177">-SubnetAddressPrefix</span></span>
<span data-ttu-id="f8cca-178">VM에 대해 생성 될 서브넷의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-178">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="f8cca-179">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="f8cca-179">-SubnetName</span></span>
<span data-ttu-id="f8cca-180">생성 된 VM에서 사용할 새 (또는 기존) 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-180">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="f8cca-181">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-181">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f8cca-182">태그</span><span class="sxs-lookup"><span data-stu-id="f8cca-182">-Tag</span></span>
<span data-ttu-id="f8cca-183">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-183">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="f8cca-184">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-184">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="f8cca-185">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-185">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="f8cca-186">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="f8cca-186">-VirtualNetworkName</span></span>
<span data-ttu-id="f8cca-187">생성 된 VM에서 사용할 새 (또는 기존) 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-187">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="f8cca-188">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-188">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="f8cca-189">-VM</span><span class="sxs-lookup"><span data-stu-id="f8cca-189">-VM</span></span>
<span data-ttu-id="f8cca-190">만들 로컬 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-190">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="f8cca-191">가상 컴퓨터 개체를 가져오려면 New-AzureRmVMConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-191">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="f8cca-192">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-192">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="f8cca-193">-Zone</span><span class="sxs-lookup"><span data-stu-id="f8cca-193">-Zone</span></span>
<span data-ttu-id="f8cca-194">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-194">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="f8cca-195">-확인</span><span class="sxs-lookup"><span data-stu-id="f8cca-195">-Confirm</span></span>
<span data-ttu-id="f8cca-196">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-196">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8cca-197">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8cca-197">-WhatIf</span></span>
<span data-ttu-id="f8cca-198">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-198">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="f8cca-199">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-199">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8cca-200">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8cca-200">CommonParameters</span></span>
<span data-ttu-id="f8cca-201">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-201">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8cca-202">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8cca-202">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8cca-203">입력</span><span class="sxs-lookup"><span data-stu-id="f8cca-203">INPUTS</span></span>

### <span data-ttu-id="f8cca-204">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="f8cca-204">PSVirtualMachine</span></span>
<span data-ttu-id="f8cca-205">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-205">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="f8cca-206">출력</span><span class="sxs-lookup"><span data-stu-id="f8cca-206">OUTPUTS</span></span>

### <span data-ttu-id="f8cca-207">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="f8cca-207">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f8cca-208">상속자</span><span class="sxs-lookup"><span data-stu-id="f8cca-208">NOTES</span></span>

## <span data-ttu-id="f8cca-209">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8cca-209">RELATED LINKS</span></span>

[<span data-ttu-id="f8cca-210">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-210">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="f8cca-211">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-211">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="f8cca-212">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-212">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="f8cca-213">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-213">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="f8cca-214">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-214">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="f8cca-215">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f8cca-215">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="f8cca-216">추가-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="f8cca-216">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="f8cca-217">추가-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f8cca-217">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="f8cca-218">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="f8cca-218">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="f8cca-219">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f8cca-219">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="f8cca-220">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="f8cca-220">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="f8cca-221">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="f8cca-221">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


