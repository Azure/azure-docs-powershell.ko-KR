---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310325"
---
# <span data-ttu-id="46f6e-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-101">Get-AzVmss</span></span>

## <span data-ttu-id="46f6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="46f6e-103">VMSS의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="46f6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46f6e-104">SYNTAX</span></span>

### <span data-ttu-id="46f6e-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="46f6e-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f6e-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="46f6e-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46f6e-107">OSUpgradeHistoryMethodParameter</span><span class="sxs-lookup"><span data-stu-id="46f6e-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46f6e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="46f6e-108">DESCRIPTION</span></span>
<span data-ttu-id="46f6e-109">**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)의 모델 및 인스턴스 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="46f6e-110">모델 보기는 사용자가 가상 컴퓨터 크기 조정 집합의 속성을 지정 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="46f6e-111">인스턴스 뷰는 가상 머신 배율 집합의 인스턴스 수준 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="46f6e-112">가상 컴퓨터 배율 집합의 인스턴스 보기만 가져오려면 *instanceview* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="46f6e-113">예제의</span><span class="sxs-lookup"><span data-stu-id="46f6e-113">EXAMPLES</span></span>

### <span data-ttu-id="46f6e-114">예제 1: VMSS의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="46f6e-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="46f6e-115">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS VMSS001의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="46f6e-116">Command는 *instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터 배율 집합의 모델 뷰를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="46f6e-117">예제 2: 리소스 그룹의 모든 Vmss 가져오기</span><span class="sxs-lookup"><span data-stu-id="46f6e-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="46f6e-118">리소스 그룹 "Group001"에서 모든 Vmss 가져오기</span><span class="sxs-lookup"><span data-stu-id="46f6e-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="46f6e-119">예제 3: 구독에서 모든 Vmss 가져오기</span><span class="sxs-lookup"><span data-stu-id="46f6e-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="46f6e-120">구독에서 모든 Vmss를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="46f6e-121">예제 4: 필터링을 사용 하 여 모든 Vmss 가져오기</span><span class="sxs-lookup"><span data-stu-id="46f6e-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="46f6e-122">"VMSS00"로 시작 하는 구독의 모든 Vmss를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="46f6e-123">변수</span><span class="sxs-lookup"><span data-stu-id="46f6e-123">PARAMETERS</span></span>

### <span data-ttu-id="46f6e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46f6e-124">-DefaultProfile</span></span>
<span data-ttu-id="46f6e-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46f6e-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="46f6e-126">-InstanceView</span></span>
<span data-ttu-id="46f6e-127">이 cmdlet이 가상 컴퓨터 배율 집합의 인스턴스 보기만 가져오고 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="46f6e-128">-OSUpgradeHistory</span><span class="sxs-lookup"><span data-stu-id="46f6e-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="46f6e-129">이 cmdlet에 가상 머신 크기 집합의 os 업그레이드 기록이 나열 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="46f6e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46f6e-130">-ResourceGroupName</span></span>
<span data-ttu-id="46f6e-131">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="46f6e-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="46f6e-132">-VMScaleSetName</span></span>
<span data-ttu-id="46f6e-133">VMSS의 이름을 종류로 합니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="46f6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46f6e-134">CommonParameters</span></span>
<span data-ttu-id="46f6e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46f6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46f6e-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46f6e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46f6e-137">입력</span><span class="sxs-lookup"><span data-stu-id="46f6e-137">INPUTS</span></span>

### <span data-ttu-id="46f6e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46f6e-138">System.String</span></span>

## <span data-ttu-id="46f6e-139">출력</span><span class="sxs-lookup"><span data-stu-id="46f6e-139">OUTPUTS</span></span>

### <span data-ttu-id="46f6e-140">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="46f6e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="46f6e-141">상속자</span><span class="sxs-lookup"><span data-stu-id="46f6e-141">NOTES</span></span>

## <span data-ttu-id="46f6e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46f6e-142">RELATED LINKS</span></span>

[<span data-ttu-id="46f6e-143">새로운 AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="46f6e-144">제거-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="46f6e-145">다시 시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="46f6e-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="46f6e-147">시작-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="46f6e-148">중지-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="46f6e-149">업데이트-AzVmss</span><span class="sxs-lookup"><span data-stu-id="46f6e-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


