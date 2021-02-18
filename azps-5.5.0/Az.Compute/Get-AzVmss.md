---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181689"
---
# <span data-ttu-id="7ee34-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-101">Get-AzVmss</span></span>

## <span data-ttu-id="7ee34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ee34-102">SYNOPSIS</span></span>
<span data-ttu-id="7ee34-103">VMSS의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="7ee34-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ee34-104">SYNTAX</span></span>

### <span data-ttu-id="7ee34-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ee34-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ee34-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="7ee34-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ee34-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="7ee34-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ee34-108">설명</span><span class="sxs-lookup"><span data-stu-id="7ee34-108">DESCRIPTION</span></span>
<span data-ttu-id="7ee34-109">**Get-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set)의 모델 및 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="7ee34-110">모델 보기는 가상 머신 확장 집합의 사용자 지정 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="7ee34-111">인스턴스 보기는 가상 머신 확장 집합의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="7ee34-112">가상 머신 확장 집합의 인스턴스 보기만 얻게 하는 *InstanceView* 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="7ee34-113">예제</span><span class="sxs-lookup"><span data-stu-id="7ee34-113">EXAMPLES</span></span>

### <span data-ttu-id="7ee34-114">예제 1: VMSS의 속성 얻음</span><span class="sxs-lookup"><span data-stu-id="7ee34-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="7ee34-115">이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="7ee34-116">이 명령은 *InstanceView* 스위치 매개 변수를 지정하지 않습니다. cmdlet은 가상 머신 확장 집합의 모델 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="7ee34-117">예제 2: 리소스 그룹의 모든 Vmss를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="7ee34-118">리소스 그룹 "Group001"에서 모든 VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="7ee34-119">예제 3: 구독의 모든 Vmss를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="7ee34-120">구독의 모든 VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="7ee34-121">예제 4: 필터링을 사용하여 모든 VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="7ee34-122">"VMSS00"으로 시작하는 구독의 모든 VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="7ee34-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ee34-123">PARAMETERS</span></span>

### <span data-ttu-id="7ee34-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ee34-124">-DefaultProfile</span></span>
<span data-ttu-id="7ee34-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ee34-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="7ee34-126">-InstanceView</span></span>
<span data-ttu-id="7ee34-127">이 cmdlet은 가상 머신 확장 집합의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee34-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="7ee34-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="7ee34-129">이 cmdlet은 가상 머신 확장 집합의 os 업그레이드 기록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ee34-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ee34-130">-ResourceGroupName</span></span>
<span data-ttu-id="7ee34-131">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7ee34-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7ee34-132">-VMScaleSetName</span></span>
<span data-ttu-id="7ee34-133">VMSS의 이름 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7ee34-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ee34-134">CommonParameters</span></span>
<span data-ttu-id="7ee34-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ee34-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ee34-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ee34-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ee34-137">입력</span><span class="sxs-lookup"><span data-stu-id="7ee34-137">INPUTS</span></span>

### <span data-ttu-id="7ee34-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7ee34-138">System.String</span></span>

## <span data-ttu-id="7ee34-139">출력</span><span class="sxs-lookup"><span data-stu-id="7ee34-139">OUTPUTS</span></span>

### <span data-ttu-id="7ee34-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7ee34-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7ee34-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ee34-141">NOTES</span></span>

## <span data-ttu-id="7ee34-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ee34-142">RELATED LINKS</span></span>

[<span data-ttu-id="7ee34-143">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="7ee34-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="7ee34-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="7ee34-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="7ee34-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="7ee34-148">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="7ee34-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7ee34-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


