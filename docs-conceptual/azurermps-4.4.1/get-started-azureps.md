---
title: Azure PowerShell 시작 | Microsoft Docs
description: ''
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/15/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: f38988139898c1023f018d9616a107cbc50adf57
ms.sourcegitcommit: 038cb42a3bd8c009bc57c8c1c252e66fa170c84b
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2020
ms.locfileid: "92523362"
---
# <a name="getting-started-with-azure-powershell"></a>Azure PowerShell 시작

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell은 명령줄에서 Azure 리소스를 관리하는 작업 및 Azure Resource Manager에 대해 작동하는 자동화 스크립트를 빌드하는 작업을 위해 만들어졌습니다. [Azure Cloud Shell](/azure/cloud-shell/overview)과 함께 브라우저에서 사용하거나 로컬 컴퓨터에 설치하여 PowerShell 세션에서 사용할 수 있습니다. 이 문서에서는 Azure CLI 2.0을 시작하는 방법 및 핵심 개념을 설명합니다.

## <a name="connect"></a>연결

가장 간단하게 시작하는 방법은 [Cloud Shell을 시작](/azure/cloud-shell/quickstart)하는 것입니다.

1. Azure Portal의 위쪽 탐색 모음에서 Cloud Shell을 시작합니다.

   ![셸 아이콘](~/media/get-started-azureps/shell-icon.png)

2. 사용하려는 구독을 선택하고 스토리지 계정을 만듭니다.

   ![스토리지 계정 만들기](~/media/get-started-azureps/storage-prompt.png)

스토리지를 만들면 Cloud Shell에서 PowerShell 세션을 브라우저에서 엽니다.

![PowerShell을 위한 Cloud Shell](~/media/get-started-azureps/cloud-powershell.png)

또한 Azure PowerShell을 설치하여 PowerShell 세션에서 로컬로 사용할 수 있습니다.

## <a name="install-azure-powershell"></a>Azure Powershell 설치

첫 번째 단계는 최신 버전의 Azure PowerShell을 설치하는 것입니다. 최신 릴리스에 대한 자세한 내용은 [릴리스 정보](./release-notes-azureps.md)를 참조하세요.

1. [Azure PowerShell 설치](install-azurerm-ps.md)

2. 설치가 완료되었는지 확인하려면 명령줄에서 `Get-InstalledModule AzureRM -AllVersions` 명령을 실행합니다.

## <a name="sign-in-to-azure"></a>Azure에 로그인

대화형으로 로그인합니다.

1. `Login-AzureRmAccount`. Azure 자격 증명을 묻는 대화 상자가 표시됩니다. '-EnvironmentName' 옵션을 사용하면 Azure China 또는 Azure Germany에 인증할 수 있습니다.

   예: Login-AzureRmAccount -EnvironmentName AzureChinaCloud

2. 계정과 연결된 메일 주소 및 암호를 입력합니다. Azure가 자격 증명 정보를 인증 및 저장한 후 창을 닫습니다.

Azure 계정에 로그인하면 Azure PowerShell cmdlet을 사용하여 구독에서 관리자 리소스에 액세스할 수 있습니다.

## <a name="create-a-resource-group"></a>리소스 그룹 만들기

모든 설정이 완료되었으니, 이제부터 Azure PowerShell을 사용하여 Azure 내에 리소스를 만들어 보겠습니다.

먼저 리소스 그룹을 만듭니다. Azure의 리소스 그룹은 논리적으로 그룹화하려는 여러 리소스를 관리하는 방법을 제공합니다. 예를 들어 애플리케이션 또는 프로젝트에 대한 리소스 그룹을 만들고 그 안에 가상 머신, 데이터베이스 및 CDN 서비스를 추가할 수 있습니다.

Azure의 westeurope 지역에 "MyResourceGroup"이라는 이름의 리소스 그룹을 만듭니다. 이렇게 하려면 다음 명령을 입력합니다.

```powershell-interactive
New-AzureRmResourceGroup -Name 'myResourceGroup' -Location 'westeurope'
```

```Output
ResourceGroupName : myResourceGroup
Location          : westeurope
ProvisioningState : Succeeded
Tags              :
ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/myResourceGroup
```

## <a name="create-a-windows-virtual-machine"></a>Windows Virtual Machine 만들기

리소스 그룹을 만들었으므로 그 안에 Windows VM을 만들어 보겠습니다. VM을 만들려면 새 먼저 필요한 리소스를 만들고 구성에 할당해야 했습니다. 그런 다음 해당 구성을 사용하여 VM을 만들 수 있습니다.

### <a name="create-the-required-network-resources"></a>필요한 네트워크 리소스 만들기

먼저 가상 네트워크 만들기 프로세스에 사용할 서브넷 구성을 만들어야 합니다. 또한 이 VM에 연결할 수 있도록 공용 IP 주소를 만듭니다. 네트워크 보안 그룹을 만들어서 공용 주소에 대한 액세스를 보호합니다. 마지막으로 이전 리소스를 모두 사용하여 가상 NIC를 만듭니다.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myWindowsVM"

# Create a subnet configuration
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet1 -AddressPrefix 192.168.1.0/24

# Create a virtual network
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName $resourceGroup -Location $location `
  -Name MYvNET1 -AddressPrefix 192.168.0.0/16 -Subnet $subnetConfig

# Create a public IP address and specify a DNS name
$publicIp = New-AzureRmPublicIpAddress -ResourceGroupName $resourceGroup -Location $location `
  -Name "mypublicdns$(Get-Random)" -AllocationMethod Static -IdleTimeoutInMinutes 4
$publicIp | Select-Object Name,IpAddress

# Create an inbound network security group rule for port 3389
$nsgRuleRDP = New-AzureRmNetworkSecurityRuleConfig -Name myNetworkSecurityGroupRuleRDP  -Protocol Tcp `
  -Direction Inbound -Priority 1000 -SourceAddressPrefix * -SourcePortRange * -DestinationAddressPrefix * `
  -DestinationPortRange 3389 -Access Allow

# Create a network security group
$nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName $resourceGroup -Location $location `
  -Name myNetworkSecurityGroup1 -SecurityRules $nsgRuleRDP

# Create a virtual network card and associate with public IP address and NSG
$nic = New-AzureRmNetworkInterface -Name myNic1 -ResourceGroupName $resourceGroup -Location $location `
  -SubnetId $vnet.Subnets[0].Id -PublicIpAddressId $publicIp.Id -NetworkSecurityGroupId $nsg.Id
```

### <a name="create-the-virtual-machine"></a>가상 머신 만들기

먼저 OS의 자격 증명 집합이 필요합니다.

```powershell-interactive
# Create user object
$cred = Get-Credential -Message "Enter a username and password for the virtual machine."
```

이제 필요한 리소스를 만들었으므로 VM을 만들 수 있습니다. 이 단계에서는 VM 구성 개체를 만든 다음 구성을 사용하여 VM을 만듭니다.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Windows -ComputerName $vmName -Credential $cred |
  Set-AzureRmVMSourceImage -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2016-Datacenter -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

VM이 완전히 생성되어 사용 준비를 마치면 `New-AzureRmVM` 명령이 결과를 출력합니다.

```Output
RequestId IsSuccessStatusCode StatusCode ReasonPhrase
--------- ------------------- ---------- ------------
                         True         OK OK
```

이제 원격 데스크톱 및 VM의 공용 IP 주소를 사용하여 새로 만든 Windows Server VM에 로그인합니다. 다음 명령은 이전 스크립트에서 만든 공용 IP 주소를 표시합니다.

```powershell-interactive
$publicIp | Select-Object Name,IpAddress
```

```Output
Name                  IpAddress
----                  ---------
mypublicdns1400512543 xx.xx.xx.xx
```

Windows 기반 시스템을 사용하는 경우 명령줄에서 mstsc 명령을 사용하여 다음과 같은 일을 할 수 있습니다.

```powershell-interactive
mstsc /v:xx.xxx.xx.xxx
```

로그인 시, VM을 만들 때 사용한 것과 동일한 사용자 이름/암호 조합을 제공합니다.

## <a name="create-a-linux-virtual-machine"></a>Linux Virtual Machine 만들기

Linux VM을 만들려면 새 먼저 필요한 리소스를 만들고 구성에 할당해야 했습니다. 그런 다음 해당 구성을 사용하여 VM을 만들 수 있습니다. 이미 이전에 설명한 대로 리소스 그룹을 만들었다고 가정합니다. 또한 `id_rsa.pub`라는 이름의 SSH 공개 키가 사용자 프로필의 .ssh 디렉터리에 있어야 합니다.

### <a name="create-the-required-network-resources"></a>필요한 네트워크 리소스 만들기

먼저 가상 네트워크 만들기 프로세스에 사용할 서브넷 구성을 만들어야 합니다. 또한 이 VM에 연결할 수 있도록 공용 IP 주소를 만듭니다. 네트워크 보안 그룹을 만들어서 공용 주소에 대한 액세스를 보호합니다. 마지막으로 이전 리소스를 모두 사용하여 가상 NIC를 만듭니다.

```powershell-interactive
# Variables for common values
$resourceGroup = "myResourceGroup"
$location = "westeurope"
$vmName = "myLinuxVM"

# Definer user name and blank password
$securePassword = ConvertTo-SecureString ' ' -AsPlainText -Force
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

### <a name="create-the-virtual-machine"></a>가상 머신 만들기

이제 필요한 리소스를 만들었으므로 VM을 만들 수 있습니다. 이 단계에서는 VM 구성 개체를 만든 다음 구성을 사용하여 VM을 만듭니다.

```powershell-interactive
# Create a virtual machine configuration
$vmConfig = New-AzureRmVMConfig -VMName $vmName -VMSize Standard_D1 |
  Set-AzureRmVMOperatingSystem -Linux -ComputerName $vmName -Credential $cred -DisablePasswordAuthentication |
  Set-AzureRmVMSourceImage -PublisherName Canonical -Offer UbuntuServer -Skus 14.04.2-LTS -Version latest |
  Add-AzureRmVMNetworkInterface -Id $nic.Id

# Configure SSH Keys
$sshPublicKey = Get-Content "$env:USERPROFILE\.ssh\id_rsa.pub"
Add-AzureRmVMSshPublicKey -VM $vmConfig -KeyData $sshPublicKey -Path "/home/azureuser/.ssh/authorized_keys"

# Create a virtual machine
New-AzureRmVM -ResourceGroupName $resourceGroup -Location $location -VM $vmConfig
```

이제 VM을 만들었으므로 SSH를 사용하여 앞에서 만든 VM의 공용 IP 주소로 새 Linux VM에 로그온할 수 있습니다.

```bash
ssh xx.xxx.xxx.xxx
```

```Output
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

## <a name="creating-other-resources-in-azure"></a>Azure에서 다른 리소스 만들기

지금까지 리소스 그룹, Linux VM 및 Windows Server VM을 만드는 방법을 살펴보았습니다. 여러 다른 유형의 Azure 리소스도 만들 수 있습니다.

예를 들어 Azure 네트워크 부하 분산 장치를 만든 후 새로 만든 VM과 연결하려면 다음 만들기 명령을 사용합니다.

```powershell-interactive
New-AzureRmLoadBalancer -Name MyLoadBalancer -ResourceGroupName myResourceGroup -Location westeurope
```

다음 명령을 사용하여 인프라에 대한 새 프라이빗 Virtual Network(일반적으로 Azure 내에서는 "VNet"이라고 함)를 만들 수도 있습니다.

```powershell-interactive
$subnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name mySubnet2 -AddressPrefix 10.0.0.0/16
$vnet = New-AzureRmVirtualNetwork -ResourceGroupName myResourceGroup -Location westeurope `
  -Name MYvNET3 -AddressPrefix 10.0.0.0/16 -Subnet $subnetConfig
```

Azure 및 Azure PowerShell이 강력한 이유는 클라우드 기반 인프라를 가져오는 데 사용할 수 있을 뿐 아니라 관리형 플랫폼 서비스를 만드는 데도 사용할 수 있기 때문입니다. 관리형 플랫폼 서비스를 인프라와 결합하면 더욱 강력한 솔루션을 구축할 수 있습니다.

예를 들어 Azure PowerShell을 사용하여 Azure AppService를 만들 수 있습니다. Azure AppService는 인프라에 대한 걱정 없이 웹앱을 호스트하는 훌륭한 방법을 제공하는 관리형 플랫폼 서비스입니다. Azure AppService를 만든 후에는 다음 명령을 사용하여 AppService 내에서 두 개의 새 Azure Web Apps를 만들 수 있습니다.

```powershell-interactive
# Create an Azure AppService that we can host any number of web apps within
New-AzureRmAppServicePlan -Name MyAppServicePlan -Tier Basic -NumberofWorkers 2 -WorkerSize Small -ResourceGroupName myResourceGroup -Location westeurope

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
New-AzureRmWebApp -Name MyWebApp43432 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
New-AzureRmWebApp -Name MyWebApp43433 -AppServicePlan MyAppServicePlan -ResourceGroupName myResourceGroup -Location westeurope
```

## <a name="listing-deployed-resources"></a>배포된 리소스 나열

`Get-AzureRmResource` cmdlet을 사용하여 Azure에서 실행되는 리소스를 나열할 수 있습니다. 다음 예제에서는 새 리소스 그룹에서 생성된 리소스를 표시합니다.

```powershell-interactive
Get-AzureRmResource |
  Where-Object ResourceGroupName -eq myResourceGroup |
    Select-Object Name,Location,ResourceType
```

```Output
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

## <a name="deleting-resources"></a>리소스 삭제

Azure 계정을 정리하려면 이 예제에서 만든 리소스를 제거합니다. `Remove-AzureRm*` cmdlet을 사용하여 더 이상 필요 없는 리소스를 삭제할 수 있습니다. 만든 Windows VM을 제거하려면 다음 명령을 사용합니다.

```powershell-interactive
Remove-AzureRmVM -Name myWindowsVM -ResourceGroupName myResourceGroup
```

리소스를 제거하려는지 확인하는 메시지가 표시됩니다.

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

여러 리소스를 한 번에 삭제할 수도 있습니다. 예를 들어 다음 명령은 이 시작 자습서의 모든 샘플에 사용한 "MyResourceGroup" 리소스 그룹을 모두 삭제합니다. 그러면 리소스 그룹 및 내부의 모든 리소스를 제거합니다.

```powershell-interactive
Remove-AzureRmResourceGroup -Name myResourceGroup
```

```Output
Confirm
Are you sure you want to remove resource group 'myResourceGroup'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

이 작업을 완료하는 데 몇 분 정도 걸릴 수 있습니다.

## <a name="get-samples"></a>샘플 받기

Azure PowerShell을 사용하는 방법에 대해 자세히 알아보려면 [Linux VM](/azure/virtual-machines/linux/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Windows VM](/azure/virtual-machines/windows/powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json), [Web Apps](/azure/app-service-web/app-service-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json) 및 [SQL Database](/azure/sql-database/sql-database-powershell-samples?toc=%2fpowershell%2fazure%%2ftoc.json)에 대한 가장 일반적인 스크립트를 확인하세요.

## <a name="next-steps"></a>다음 단계

* [Azure PowerShell로 로그인](authenticate-azureps.md)
* [Azure PowerShell을 사용하여 Azure 구독 관리](manage-subscriptions-azureps.md)
* [Azure PowerShell을 사용하여 Azure에서 서비스 주체 만들기](create-azure-service-principal-azureps.md)
* 이전 릴리스에서 마이그레이션하는 방법은 [릴리스 노트](./release-notes-azureps.md)를 참조하세요.
* 커뮤니티에서 도움말을 가져옵니다.
  * [MSDN의 azure 포럼](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [stackoverflow](https://go.microsoft.com/fwlink/?LinkId=320213)
