---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: f7f19a46a8a7f0bfd0e9ec20fe40201e4bea668a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882365"
---
# <span data-ttu-id="438b3-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-101">New-AzureRmVM</span></span>

## <span data-ttu-id="438b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="438b3-102">SYNOPSIS</span></span>
<span data-ttu-id="438b3-103">가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="438b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="438b3-104">SYNTAX</span></span>

### <span data-ttu-id="438b3-105">SimpleParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="438b3-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438b3-106">DefaultParameterSet</span><span class="sxs-lookup"><span data-stu-id="438b3-106">DefaultParameterSet</span></span>
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="438b3-107">DiskFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="438b3-107">DiskFileParameterSet</span></span>
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="438b3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="438b3-108">DESCRIPTION</span></span>
<span data-ttu-id="438b3-109">**AzureRmVM** Cmdlet은 Azure에서 가상 컴퓨터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-109">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="438b3-110">이 cmdlet은 가상 컴퓨터 개체를 입력으로 받습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-110">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="438b3-111">New-AzureRmVMConfig cmdlet을 사용 하 여 가상 컴퓨터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-111">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="438b3-112">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, Set-AzureRmVMOSDisk 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-112">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

<span data-ttu-id="438b3-113">는 `SimpleParameterSet` 일반적인 vm 생성 인수를 선택적으로 만들어 VM을 만드는 편리한 방법을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-113">The `SimpleParameterSet` provides a convenient method to create a VM by making common VM creation arguments optional.</span></span>

## <span data-ttu-id="438b3-114">예제의</span><span class="sxs-lookup"><span data-stu-id="438b3-114">EXAMPLES</span></span>

### <span data-ttu-id="438b3-115">예제 1: 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="438b3-115">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureRmVM -Name MyVm
```

<span data-ttu-id="438b3-116">이 예제 스크립트는 가상 컴퓨터를 만드는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-116">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="438b3-117">이 스크립트는 여러 다른 cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-117">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="438b3-118">예제 2: 사용자 지정 사용자 이미지에서 가상 컴퓨터 만들기</span><span class="sxs-lookup"><span data-stu-id="438b3-118">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="438b3-119">이 예제에서는 기존 sys-prepped, 일반화 된 사용자 지정 운영 체제 이미지를 가져와 데이터 디스크를 연결 하 고, 새 네트워크를 프로 비전 하 고, VHD를 배포 하 고, 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-119">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="438b3-120">이 스크립트는 사용자 조작이 필요한 **Get 자격 증명** 을 호출 하는 대신 로컬 가상 컴퓨터 관리자 자격 증명을 인라인으로 사용 하므로 자동 프로 비전에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-120">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="438b3-121">이 스크립트는 사용자가 Azure 계정에 이미 로그인 한 것으로 가정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-121">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="438b3-122">**AzureSubscription** cmdlet을 사용 하 여 로그인 상태를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-122">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="438b3-123">변수</span><span class="sxs-lookup"><span data-stu-id="438b3-123">PARAMETERS</span></span>

### <span data-ttu-id="438b3-124">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="438b3-124">-AddressPrefix</span></span>
<span data-ttu-id="438b3-125">VM에 대해 생성 될 가상 네트워크의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-125">The address prefix for the virtual network which will be created for the VM.</span></span>

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

### <span data-ttu-id="438b3-126">-AllocationMethod</span><span class="sxs-lookup"><span data-stu-id="438b3-126">-AllocationMethod</span></span>
<span data-ttu-id="438b3-127">VM에 대해 생성 되는 공용 IP의 IP 할당 방법입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-127">The IP allocation method for the public IP which will be created for the VM.</span></span>

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

### <span data-ttu-id="438b3-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="438b3-128">-AsJob</span></span>
<span data-ttu-id="438b3-129">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-129">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="438b3-130">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="438b3-130">-AvailabilitySetName</span></span>
<span data-ttu-id="438b3-131">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-131">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="438b3-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="438b3-132">-Credential</span></span>
<span data-ttu-id="438b3-133">VM에 대 한 관리자 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-133">The administrator credentials for the VM.</span></span>

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

### <span data-ttu-id="438b3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="438b3-134">-DefaultProfile</span></span>
<span data-ttu-id="438b3-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="438b3-136">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="438b3-136">-DisableBginfoExtension</span></span>
<span data-ttu-id="438b3-137">이 cmdlet이 가상 컴퓨터에 **Bg-bg&platform 정보** 확장을 설치 하지 않음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-137">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="438b3-138">-DiskFile</span><span class="sxs-lookup"><span data-stu-id="438b3-138">-DiskFile</span></span>
<span data-ttu-id="438b3-139">클라우드에 업로드 하 고 VM을 만들기 위해 가상 하드 디스크 파일에 대 한 로컬 경로를 사용 하 고 접미사로 ' .vhd '을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-139">The local path to the virtual hard disk file to be uploaded to the cloud and for creating the VM, and it must have '.vhd' as its suffix.</span></span>

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

### <span data-ttu-id="438b3-140">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="438b3-140">-DomainNameLabel</span></span>
<span data-ttu-id="438b3-141">VM의 정규화 된 도메인 이름 (FQDN)에 대 한 하위 도메인 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-141">The subdomain label for the fully-qualified domain name (FQDN) of the VM.</span></span>  <span data-ttu-id="438b3-142">이는 양식을 사용 `{domainNameLabel}.{location}.cloudapp.azure.com` 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-142">This will take the form `{domainNameLabel}.{location}.cloudapp.azure.com`.</span></span>

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

### <span data-ttu-id="438b3-143">-ImageName</span><span class="sxs-lookup"><span data-stu-id="438b3-143">-ImageName</span></span>
<span data-ttu-id="438b3-144">VM이 빌드될 이미지 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-144">The friendly image name upon which the VM will be built.</span></span>  <span data-ttu-id="438b3-145">여기에는 Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-145">These include: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, Debian, openSUSE-Leap, RHEL, SLES.</span></span>

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

### <span data-ttu-id="438b3-146">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="438b3-146">-LicenseType</span></span>
<span data-ttu-id="438b3-147">가상 컴퓨터의 이미지나 디스크에 온-프레미스 라이선스가 부여 되었음을 나타내는 라이선스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-147">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="438b3-148">이 값은 Windows Server 운영 체제를 포함 하는 이미지에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-148">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="438b3-149">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="438b3-150">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="438b3-150">Windows_Client</span></span> 
- <span data-ttu-id="438b3-151">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="438b3-151">Windows_Server</span></span>

<span data-ttu-id="438b3-152">이 값을 업데이트할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-152">This value cannot be updated.</span></span>
<span data-ttu-id="438b3-153">업데이트에이 매개 변수를 지정 하면 해당 값이 가상 컴퓨터의 초기 값과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-153">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="438b3-154">-Linux</span><span class="sxs-lookup"><span data-stu-id="438b3-154">-Linux</span></span>
<span data-ttu-id="438b3-155">디스크 파일이 Linux VM (지정 된 경우)에 대 한 것인지 여부를 나타냅니다. 또는 Windows가 기본적으로 지정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-155">Indicates whether the disk file is for Linux VM, if specified; or Windows, if not specified by default.</span></span>

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

### <span data-ttu-id="438b3-156">-위치</span><span class="sxs-lookup"><span data-stu-id="438b3-156">-Location</span></span>
<span data-ttu-id="438b3-157">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-157">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="438b3-158">-이름</span><span class="sxs-lookup"><span data-stu-id="438b3-158">-Name</span></span>
<span data-ttu-id="438b3-159">VM 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-159">The name of the VM resource.</span></span>

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

### <span data-ttu-id="438b3-160">-OpenPorts</span><span class="sxs-lookup"><span data-stu-id="438b3-160">-OpenPorts</span></span>
<span data-ttu-id="438b3-161">생성 된 VM에 대 한 NSG (네트워크 보안 그룹)에서 열리는 포트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-161">A list of ports to open on the network security group (NSG) for the created VM.</span></span>  <span data-ttu-id="438b3-162">기본값은 선택한 이미지의 종류 (즉, Windows: 3389, 5985, Linux: 22)에 따라 달라 집니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-162">The default value depends on the type of image chosen (i.e., Windows: 3389, 5985 and Linux: 22).</span></span>

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

### <span data-ttu-id="438b3-163">-PublicIpAddressName</span><span class="sxs-lookup"><span data-stu-id="438b3-163">-PublicIpAddressName</span></span>
<span data-ttu-id="438b3-164">만든 VM에서 사용할 새 공용 IP 주소 (또는 기존)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-164">The name of a new (or existing) public IP address for the created VM to use.</span></span>  <span data-ttu-id="438b3-165">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-165">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="438b3-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="438b3-166">-ResourceGroupName</span></span>
<span data-ttu-id="438b3-167">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-167">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="438b3-168">-SecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="438b3-168">-SecurityGroupName</span></span>
<span data-ttu-id="438b3-169">사용할 생성 된 VM에 대 한 새 (또는 기존) 네트워크 보안 그룹 (NSG)의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-169">The name of a new (or existing) network security group (NSG) for the created VM to use.</span></span>  <span data-ttu-id="438b3-170">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-170">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="438b3-171">-크기</span><span class="sxs-lookup"><span data-stu-id="438b3-171">-Size</span></span>
<span data-ttu-id="438b3-172">가상 컴퓨터 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-172">The Virtual Machine Size.</span></span>  <span data-ttu-id="438b3-173">기본값은 Standard_DS1_v2입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-173">The Default Value is: Standard_DS1_v2.</span></span>

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

### <span data-ttu-id="438b3-174">-SubnetAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="438b3-174">-SubnetAddressPrefix</span></span>
<span data-ttu-id="438b3-175">VM에 대해 생성 될 서브넷의 주소 접두사입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-175">The address prefix for the subnet which will be created for the VM.</span></span>

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

### <span data-ttu-id="438b3-176">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="438b3-176">-SubnetName</span></span>
<span data-ttu-id="438b3-177">생성 된 VM에서 사용할 새 (또는 기존) 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-177">The name of a new (or existing) subnet for the created VM to use.</span></span>  <span data-ttu-id="438b3-178">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-178">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="438b3-179">태그</span><span class="sxs-lookup"><span data-stu-id="438b3-179">-Tag</span></span>
<span data-ttu-id="438b3-180">리소스 및 리소스 그룹에 이름-값 쌍 집합을 태깅 할 수 있도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-180">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="438b3-181">리소스에 태그를 추가 하면 리소스 그룹에서 리소스를 그룹화 하 고 고유한 보기를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-181">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="438b3-182">각 리소스 또는 리소스 그룹은 최대 15 개의 태그를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-182">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="438b3-183">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="438b3-183">-VirtualNetworkName</span></span>
<span data-ttu-id="438b3-184">생성 된 VM에서 사용할 새 (또는 기존) 가상 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-184">The name of a new (or existing) virtual network for the created VM to use.</span></span>  <span data-ttu-id="438b3-185">지정 하지 않으면 이름이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-185">If not specified, a name will be generated.</span></span>

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

### <span data-ttu-id="438b3-186">-VM</span><span class="sxs-lookup"><span data-stu-id="438b3-186">-VM</span></span>
<span data-ttu-id="438b3-187">만들 로컬 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-187">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="438b3-188">가상 컴퓨터 개체를 가져오려면 New-AzureRmVMConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-188">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="438b3-189">다른 cmdlet을 사용 하 여 AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface 등의 가상 컴퓨터를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-189">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="438b3-190">-Zone</span><span class="sxs-lookup"><span data-stu-id="438b3-190">-Zone</span></span>
<span data-ttu-id="438b3-191">가상 컴퓨터의 영역 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-191">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="438b3-192">-확인</span><span class="sxs-lookup"><span data-stu-id="438b3-192">-Confirm</span></span>
<span data-ttu-id="438b3-193">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-193">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="438b3-194">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="438b3-194">-WhatIf</span></span>
<span data-ttu-id="438b3-195">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-195">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="438b3-196">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-196">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="438b3-197">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="438b3-197">CommonParameters</span></span>
<span data-ttu-id="438b3-198">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-198">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="438b3-199">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="438b3-199">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="438b3-200">입력</span><span class="sxs-lookup"><span data-stu-id="438b3-200">INPUTS</span></span>

### <span data-ttu-id="438b3-201">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="438b3-201">PSVirtualMachine</span></span>
<span data-ttu-id="438b3-202">' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-202">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="438b3-203">출력</span><span class="sxs-lookup"><span data-stu-id="438b3-203">OUTPUTS</span></span>

### <span data-ttu-id="438b3-204">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="438b3-204">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="438b3-205">상속자</span><span class="sxs-lookup"><span data-stu-id="438b3-205">NOTES</span></span>

## <span data-ttu-id="438b3-206">관련 링크</span><span class="sxs-lookup"><span data-stu-id="438b3-206">RELATED LINKS</span></span>

[<span data-ttu-id="438b3-207">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-207">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="438b3-208">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-208">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="438b3-209">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-209">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="438b3-210">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-210">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="438b3-211">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-211">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="438b3-212">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="438b3-212">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="438b3-213">추가-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="438b3-213">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="438b3-214">추가-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="438b3-214">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="438b3-215">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="438b3-215">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="438b3-216">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="438b3-216">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="438b3-217">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="438b3-217">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="438b3-218">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="438b3-218">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


