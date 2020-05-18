---
title: Azure PowerShell 시작
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 61d6d19336dd0e1885570c3a4e8874a849317fa3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 05/05/2020
ms.locfileid: "75722427"
---
# <a name="get-started-with-azure-powershell"></a><span data-ttu-id="c1487-102">Azure PowerShell 시작</span><span class="sxs-lookup"><span data-stu-id="c1487-102">Get started with Azure PowerShell</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="c1487-103">Azure PowerShell은 명령줄에서 Azure 리소스를 관리하는 작업 및 Azure Resource Manager에 대해 작동하는 자동화 스크립트를 빌드하는 작업을 위해 만들어졌습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-103">Azure PowerShell is designed for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="c1487-104">[Azure Cloud Shell](/azure/cloud-shell/overview)과 함께 브라우저에서 사용하거나 로컬 컴퓨터에 설치하여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-104">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview) or you install it on your local machine.</span></span> <span data-ttu-id="c1487-105">이 문서에서는 Azure PowerShell을 시작하는 방법 및 핵심 개념을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-105">This article helps get you started with Azure PowerShell and teaches the core concepts behind it.</span></span>

## <a name="install-azure-powershell"></a><span data-ttu-id="c1487-106">Azure Powershell 설치</span><span class="sxs-lookup"><span data-stu-id="c1487-106">Install Azure PowerShell</span></span>

<span data-ttu-id="c1487-107">첫 번째 단계는 최신 버전의 Azure PowerShell을 설치하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-107">The first step is to make sure you have the latest version of the Azure PowerShell installed.</span></span> <span data-ttu-id="c1487-108">최신 릴리스에 대한 자세한 내용은 [릴리스 정보](./release-notes-azureps.md)를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c1487-108">For information about the latest release, see the [release notes](./release-notes-azureps.md).</span></span>

1. <span data-ttu-id="c1487-109">[Azure PowerShell 설치](install-azurerm-ps.md)</span><span class="sxs-lookup"><span data-stu-id="c1487-109">[Install Azure PowerShell](install-azurerm-ps.md).</span></span>

2. <span data-ttu-id="c1487-110">설치가 완료되었는지 확인하려면 명령줄에서 `Get-InstalledModule AzureRM -AllVersions` 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-110">To verify the installation was successful, run `Get-InstalledModule AzureRM -AllVersions` from your command line.</span></span>

## <a name="azure-cloud-shell"></a><span data-ttu-id="c1487-111">Azure Cloud Shell</span><span class="sxs-lookup"><span data-stu-id="c1487-111">Azure Cloud Shell</span></span>

<span data-ttu-id="c1487-112">가장 간단하게 시작하는 방법은 [Cloud Shell을 시작](/azure/cloud-shell/quickstart)하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-112">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="c1487-113">Azure Portal의 위쪽 탐색 모음에서 Cloud Shell을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-113">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![셸 아이콘](~/media/get-started-azureps/shell-icon.png)

2. <span data-ttu-id="c1487-115">사용하려는 구독을 선택하고 스토리지 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-115">Choose the subscription you want to use and create a storage account.</span></span>

   ![스토리지 계정 만들기](~/media/get-started-azureps/storage-prompt.png)

<span data-ttu-id="c1487-117">스토리지를 만들면 Cloud Shell에서 PowerShell 세션을 브라우저에서 엽니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-117">Once your storage has been created, the Cloud Shell will open a PowerShell session in the browser.</span></span>

![PowerShell을 위한 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

<span data-ttu-id="c1487-119">또한 Azure PowerShell을 설치하여 PowerShell 세션에서 로컬로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-119">You can also install Azure PowerShell and use it locally in a PowerShell session.</span></span>

## <a name="sign-in-to-azure"></a><span data-ttu-id="c1487-120">Azure에 로그인</span><span class="sxs-lookup"><span data-stu-id="c1487-120">Sign in to Azure</span></span>

<span data-ttu-id="c1487-121">대화형으로 로그인합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-121">Sign on interactively:</span></span>

1. <span data-ttu-id="c1487-122">`Connect-AzureRmAccount`.</span><span class="sxs-lookup"><span data-stu-id="c1487-122">Type `Connect-AzureRmAccount`.</span></span> <span data-ttu-id="c1487-123">Azure 자격 증명을 묻는 대화 상자가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-123">You'll get a dialog box asking for your Azure credentials.</span></span> <span data-ttu-id="c1487-124">'-Environment' 옵션을 사용하면 Azure China 또는 Azure Germany에 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-124">Option '-Environment' can let you authenticate for Azure China or Azure Germany.</span></span>

   <span data-ttu-id="c1487-125">예: Connect-AzureRmAccount -Environment AzureChinaCloud</span><span class="sxs-lookup"><span data-stu-id="c1487-125">for example, Connect-AzureRmAccount -Environment AzureChinaCloud</span></span>

2. <span data-ttu-id="c1487-126">계정과 연결된 메일 주소 및 암호를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-126">Type the email address and password associated with your account.</span></span> <span data-ttu-id="c1487-127">Azure가 자격 증명 정보를 인증 및 저장한 후 창을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-127">Azure authenticates and saves the credential information, and then closes the window.</span></span>

<span data-ttu-id="c1487-128">Azure 계정에 로그인하면 Azure PowerShell cmdlet을 사용하여 구독에서 관리자 리소스에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-128">Once you have signed in to an Azure account, you can use the Azure PowerShell cmdlets to access and manage the resources in your subscription.</span></span>

## <a name="create-a-windows-virtual-machine-using-simple-defaults"></a><span data-ttu-id="c1487-129">간단한 기본값을 사용하여 Windows 가상 머신 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-129">Create a Windows virtual machine using simple defaults</span></span>

<span data-ttu-id="c1487-130">`New-AzureRmVM` cmdlet에서는 새 가상 머신을 쉽게 만들 수 있는 간소화된 구문을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-130">The `New-AzureRmVM` cmdlet provides a simplified syntax making it easy to create a new virtual machine.</span></span> <span data-ttu-id="c1487-131">VM의 이름 및 VM의 로컬 관리자 계정에 대한 자격 증명 집합이라는 두 개의 매개 변수 값을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-131">There are only two parameter values you must provide: the name of the VM and a set of credentials for the local administrator account on the VM.</span></span>

<span data-ttu-id="c1487-132">먼저 자격 증명 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-132">First, create the credential object.</span></span>

```azurepowershell-interactive
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

```output
Windows PowerShell credential request.
Enter a username and password for the virtual machine.
User: localAdmin
Password for user localAdmin: *********
```

<span data-ttu-id="c1487-133">다음으로 VM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-133">Next, create the VM.</span></span>

```azurepowershell-interactive
New-AzureRmVM -Name SampleVM -Credential $cred
```

```output
ResourceGroupName        : SampleVM
Id                       : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/SampleVM/providers/Microsoft.Compute/virtualMachines/SampleVM
VmId                     : 43f6275d-ce50-49c8-a831-5d5974006e63
Name                     : SampleVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : samplevm-2c0867.eastus.cloudapp.azure.com
```

<span data-ttu-id="c1487-134">생성된 다른 항목 및 VM을 구성하는 방법이 궁금할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-134">You may wonder what else is created and how is the VM configured.</span></span> <span data-ttu-id="c1487-135">먼저 리소스 그룹에 대해 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-135">First, let's look at our resource groups.</span></span>

```azurepowershell-interactive
Get-AzureRmResourceGroup | Select-Object ResourceGroupName,Location
```

```output
ResourceGroupName          Location
-----------------          --------
cloud-shell-storage-westus westus
SampleVM                   eastus
```

<span data-ttu-id="c1487-136">**cloud-shell-storage-westus** 리소스 그룹은 Cloud Shell을 처음 사용할 때 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-136">The **cloud-shell-storage-westus** resource group is created the first time you use the Cloud Shell.</span></span> <span data-ttu-id="c1487-137">`New-AzureRmVM` cmdlet으로 **SampleVM** 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-137">The **SampleVM** resource group was created by the `New-AzureRmVM` cmdlet.</span></span>

<span data-ttu-id="c1487-138">이제 이 새 리소스 그룹에서 만든 다른 리소스는 무엇인가요?</span><span class="sxs-lookup"><span data-stu-id="c1487-138">Now, what other resources were created in this new resource group?</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where ResourceGroupName -eq SampleVM |
    Select-Object ResourceGroupName,Location,ResourceType,Name
```

```output
ResourceGroupName          Location ResourceType                            Name
-----------------          -------- ------------                            ----
SAMPLEVM                   eastus   Microsoft.Compute/disks                 SampleVM_OsDisk_1_9b286c54b168457fa1f8c47...
SampleVM                   eastus   Microsoft.Compute/virtualMachines       SampleVM
SampleVM                   eastus   Microsoft.Network/networkInterfaces     SampleVM
SampleVM                   eastus   Microsoft.Network/networkSecurityGroups SampleVM
SampleVM                   eastus   Microsoft.Network/publicIPAddresses     SampleVM
SampleVM                   eastus   Microsoft.Network/virtualNetworks       SampleVM
```

<span data-ttu-id="c1487-139">VM에 대한 자세한 내용을 살펴보겠습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-139">Let's get some more details about the VM.</span></span> <span data-ttu-id="c1487-140">이 예제에서는 VM을 만드는 데 사용되는 OS 이미지에 대한 정보를 검색하는 방법을 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-140">This example shows how to retrieve information about the OS Image used to create the VM.</span></span>

```azurepowershell-interactive
Get-AzureRmVM -Name SampleVM -ResourceGroupName SampleVM |
  Select-Object -ExpandProperty StorageProfile |
    Select-Object -ExpandProperty ImageReference
```

```output
Publisher : MicrosoftWindowsServer
Offer     : WindowsServer
Sku       : 2016-Datacenter
Version   : latest
Id        :
```

## <a name="create-a-fully-configured-linux-virtual-machine"></a><span data-ttu-id="c1487-141">완벽히 구성된 Linux Virtual Machine 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-141">Create a fully configured Linux Virtual Machine</span></span>

<span data-ttu-id="c1487-142">이전에 사용된 예제에서는 간소화된 구문 및 기본 매개 변수 값을 사용하여 Windows 가상 머신을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-142">The previous example used the simplified syntax and default parameter values to create a Windows virtual machine.</span></span> <span data-ttu-id="c1487-143">이 예제에서는 가상 머신의 모든 옵션에 대한 값을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-143">In this example, we provide values for all options of the virtual machine.</span></span>

### <a name="create-a-resource-group"></a><span data-ttu-id="c1487-144">리소스 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-144">Create a resource group</span></span>

<span data-ttu-id="c1487-145">이 예제에 리소스 그룹을 만들려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-145">In this example, we want to create a Resource Group.</span></span> <span data-ttu-id="c1487-146">Azure의 리소스 그룹은 논리적으로 그룹화하려는 여러 리소스를 관리하는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-146">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group together.</span></span> <span data-ttu-id="c1487-147">예를 들어 애플리케이션 또는 프로젝트에 대한 리소스 그룹을 만들고 그 안에 가상 머신, 데이터베이스 및 CDN 서비스를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-147">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="c1487-148">Azure의 westeurope 지역에 "MyResourceGroup"이라는 이름의 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-148">Let's create a resource group named "MyResourceGroup" in the westeurope region of Azure.</span></span> <span data-ttu-id="c1487-149">이렇게 하려면 다음 명령을 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-149">To do so type the following command:</span></span>

```azurepowershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

<span data-ttu-id="c1487-150">이 새 리소스 그룹을 사용하여 새 VM에 필요한 리소스를 모두 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-150">This new resource group will be used to contain all of the resources needed for the new VM we create.</span></span> <span data-ttu-id="c1487-151">Linux VM을 만들려면 새 먼저 필요한 리소스를 만들고 구성에 할당해야 했습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-151">To create a new Linux VM, we must first create the other required resources and assign them to a configuration.</span></span> <span data-ttu-id="c1487-152">그런 다음 해당 구성을 사용하여 VM을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-152">Then we can use that configuration to create the VM.</span></span> <span data-ttu-id="c1487-153">또한 `id_rsa.pub`라는 이름의 SSH 공개 키가 사용자 프로필의 .ssh 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-153">Also, you will need to have an SSH public key named `id_rsa.pub` in the .ssh directory of your user profile.</span></span>

#### <a name="create-the-required-network-resources"></a><span data-ttu-id="c1487-154">필요한 네트워크 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-154">Create the required network resources</span></span>

<span data-ttu-id="c1487-155">먼저 가상 네트워크 만들기 프로세스에 사용할 서브넷 구성을 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-155">First we need to create a subnet configuration to be used with the virtual network creation process.</span></span> <span data-ttu-id="c1487-156">또한 이 VM에 연결할 수 있도록 공용 IP 주소를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-156">We also create a public IP address so that we can connect to this VM.</span></span> <span data-ttu-id="c1487-157">네트워크 보안 그룹을 만들어서 공용 주소에 대한 액세스를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-157">We create a network security group to secure access to the public address.</span></span> <span data-ttu-id="c1487-158">마지막으로 이전 리소스를 모두 사용하여 가상 NIC를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-158">Finally we create the virtual NIC using all of the previous resources.</span></span>

```azurepowershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString 'azurepassword' -AsPlainText -Force
$cred = New-Object System.Management.Automation.PSCredential ("azureuser", $securePassword)

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 192.168.2.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET2 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 22
$nsgRuleSSH = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleSSH  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 22 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup2 -SecurityRules $nsgRuleSSH

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic2 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-vm-configuration"></a><span data-ttu-id="c1487-159">VM 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-159">Create the VM configuration</span></span>

<span data-ttu-id="c1487-160">이제 필요한 리소스가 있으므로 VM 구성 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-160">Now that we have the required resources we can create the VM configuration object.</span></span>

```azurepowershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content -Raw "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"
```

### <a name="create-the-virtual-machine"></a><span data-ttu-id="c1487-161">가상 머신 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-161">Create the virtual machine</span></span>

<span data-ttu-id="c1487-162">이제 VM 구성 개체를 사용하여 VM을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-162">Now we can create the VM using the VM configuration object.</span></span>

```azurepowershell-interactive
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

<span data-ttu-id="c1487-163">VM을 만들었으니, SSH를 사용하여 앞에서 만든 VM의 공용 IP 주소로 새 Linux VM에 로그온할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-163">Now that the VM has been created, you can sign in to your new Linux VM using SSH with the public IP address of the VM you created:</span></span>

```bash
ssh xx.xxx.xxx.xxx
```

```output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:../../..$
```

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="c1487-164">Azure에서 다른 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-164">Creating other resources in Azure</span></span>

<span data-ttu-id="c1487-165">지금까지 리소스 그룹, Linux VM 및 Windows Server VM을 만드는 방법을 살펴보았습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-165">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="c1487-166">여러 다른 유형의 Azure 리소스도 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-166">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="c1487-167">예를 들어 Azure 네트워크 부하 분산 장치를 만든 후 새로 만든 VM과 연결하려면 다음 만들기 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-167">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurepowershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

<span data-ttu-id="c1487-168">다음 명령을 사용하여 인프라에 대한 새 프라이빗 Virtual Network(일반적으로 Azure 내에서는 "VNet"이라고 함)를 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-168">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following command:</span></span>

```azurepowershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

<span data-ttu-id="c1487-169">Azure 및 Azure PowerShell이 강력한 이유는 클라우드 기반 인프라를 가져오는 데 사용할 수 있을 뿐 아니라 관리형 플랫폼 서비스를 만드는 데도 사용할 수 있기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-169">What makes Azure and the Azure PowerShell powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span> <span data-ttu-id="c1487-170">관리형 플랫폼 서비스를 인프라와 결합하면 더욱 강력한 솔루션을 구축할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-170">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="c1487-171">예를 들어 Azure PowerShell을 사용하여 Azure AppService를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-171">For example, you can use the Azure PowerShell to create an Azure AppService.</span></span> <span data-ttu-id="c1487-172">Azure AppService는 인프라에 대한 걱정 없이 웹앱을 호스트하는 훌륭한 방법을 제공하는 관리형 플랫폼 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-172">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span> <span data-ttu-id="c1487-173">Azure AppService를 만든 후에는 다음 명령을 사용하여 AppService 내에서 두 개의 새 Azure Web Apps를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-173">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following commands:</span></span>

```azurepowershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a><span data-ttu-id="c1487-174">배포된 리소스 나열</span><span class="sxs-lookup"><span data-stu-id="c1487-174">Listing deployed resources</span></span>

<span data-ttu-id="c1487-175">`Get-AzureRmResource` cmdlet을 사용하여 Azure에서 실행되는 리소스를 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-175">You can use the `Get-AzureRmResource` cmdlet to list the resources running in Azure.</span></span> <span data-ttu-id="c1487-176">다음 예제에서는 새 리소스 그룹에서 생성된 리소스를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-176">The following example shows the resources we created in the new resource group.</span></span>

```azurepowershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```output
Name                                                  Location   ResourceType
----                                                  --------   ------------
myLinuxVM_OsDisk_1_36ca038791f642ba91270879088c249a   westeurope Microsoft.Compute/disks
myWindowsVM_OsDisk_1_f627e6e2bb454c72897d72e9632adf9a westeurope Microsoft.Compute/disks
myLinuxVM                                             westeurope Microsoft.Compute/virtualMachines
myWindowsVM                                           westeurope Microsoft.Compute/virtualMachines
myWindowsVM/BGInfo                                    westeurope Microsoft.Compute/virtualMachines/extensions
myNic1                                                westeurope Microsoft.Network/networkInterfaces
myNic2                                                westeurope Microsoft.Network/networkInterfaces
myNetworkSecurityGroup1                               westeurope Microsoft.Network/networkSecurityGroups
myNetworkSecurityGroup2                               westeurope Microsoft.Network/networkSecurityGroups
mypublicdns245369171                                  westeurope Microsoft.Network/publicIPAddresses
mypublicdns779537141                                  westeurope Microsoft.Network/publicIPAddresses
MYvNET1                                               westeurope Microsoft.Network/virtualNetworks
MYvNET2                                               westeurope Microsoft.Network/virtualNetworks
micromyresomywi032907510                              westeurope Microsoft.Storage/storageAccounts
```

## <a name="deleting-resources"></a><span data-ttu-id="c1487-177">리소스 삭제</span><span class="sxs-lookup"><span data-stu-id="c1487-177">Deleting resources</span></span>

<span data-ttu-id="c1487-178">Azure 계정을 정리하려면 이 예제에서 만든 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-178">To clean up your Azure account, you want to remove the resources we created in this example.</span></span> <span data-ttu-id="c1487-179">`Remove-AzureRm*` cmdlet을 사용하여 더 이상 필요 없는 리소스를 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-179">You can use the `Remove-AzureRm*` cmdlets to delete the resources you no longer need.</span></span> <span data-ttu-id="c1487-180">만든 Windows VM을 제거하려면 다음 명령을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-180">To remove the Windows VM we created, using the following command:</span></span>

```azurepowershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

<span data-ttu-id="c1487-181">리소스를 제거하려는지 확인하는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-181">You'll be prompted to confirm that you want to remove the resource.</span></span>

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c1487-182">여러 리소스를 한 번에 삭제할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-182">You can also delete many resources at once.</span></span> <span data-ttu-id="c1487-183">예를 들어 다음 명령은 지금까지 모든 샘플에 사용한 "MyResourceGroup" 리소스 그룹을 모두 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-183">For example, the following command deletes the resource group "MyResourceGroup" that we've used for all the samples so far.</span></span>
<span data-ttu-id="c1487-184">그룹의 모든 리소스도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-184">All resources in the group are also deleted.</span></span>

```azurepowershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

<span data-ttu-id="c1487-185">리소스 수 및 유형에 따라 작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-185">The task can take several minutes to complete, depending on the number and type of resources.</span></span>

## <a name="get-samples"></a><span data-ttu-id="c1487-186">샘플 받기</span><span class="sxs-lookup"><span data-stu-id="c1487-186">Get samples</span></span>

<span data-ttu-id="c1487-187">Azure PowerShell을 사용하는 방법에 대해 자세히 알아보려면 [Linux VM](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 및 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)에 대한 가장 일반적인 스크립트를 확인하세요.</span><span class="sxs-lookup"><span data-stu-id="c1487-187">To learn more about ways to use the Azure PowerShell, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), and [SQL Databases](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c1487-188">다음 단계</span><span class="sxs-lookup"><span data-stu-id="c1487-188">Next steps</span></span>

* [<span data-ttu-id="c1487-189">Azure PowerShell로 로그인</span><span class="sxs-lookup"><span data-stu-id="c1487-189">Sign in with Azure PowerShell</span></span>](authenticate-azureps.md)
* [<span data-ttu-id="c1487-190">Azure PowerShell을 사용하여 Azure 구독 관리</span><span class="sxs-lookup"><span data-stu-id="c1487-190">Manage Azure subscriptions with Azure PowerShell</span></span>](manage-subscriptions-azureps.md)
* [<span data-ttu-id="c1487-191">Azure PowerShell을 사용하여 Azure에서 서비스 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="c1487-191">Create service principals in Azure using Azure PowerShell</span></span>](create-azure-service-principal-azureps.md)
* <span data-ttu-id="c1487-192">이전 릴리스에서 마이그레이션하는 방법은 릴리스 노트를 참조합니다.[https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes)</span><span class="sxs-lookup"><span data-stu-id="c1487-192">Read the release notes about migrating from an older release: [https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes](https://github.com/Azure/azure-powershell/tree/dev/documentation/release-notes).</span></span>
* <span data-ttu-id="c1487-193">커뮤니티에서 도움말을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1487-193">Get help from the community:</span></span>
  * [<span data-ttu-id="c1487-194">MSDN의 azure 포럼</span><span class="sxs-lookup"><span data-stu-id="c1487-194">Azure forum on MSDN</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [<span data-ttu-id="c1487-195">stackoverflow</span><span class="sxs-lookup"><span data-stu-id="c1487-195">stackoverflow</span></span>](https://go.microsoft.com/fwlink/?LinkId=320213)
