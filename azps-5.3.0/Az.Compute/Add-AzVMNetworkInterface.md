---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: 3c0a88d53ea1d2c6b77e08ab29a7def3ae9ee445
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493917"
---
# <span data-ttu-id="39b14-101">Add-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39b14-101">Add-AzVMNetworkInterface</span></span>

## <span data-ttu-id="39b14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39b14-102">SYNOPSIS</span></span>
<span data-ttu-id="39b14-103">가상 머신에 네트워크 인터페이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-103">Adds a network interface to a virtual machine.</span></span>

## <span data-ttu-id="39b14-104">구문</span><span class="sxs-lookup"><span data-stu-id="39b14-104">SYNTAX</span></span>

### <span data-ttu-id="39b14-105">GetNicFromNicId(기본값)</span><span class="sxs-lookup"><span data-stu-id="39b14-105">GetNicFromNicId (Default)</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="39b14-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="39b14-106">GetNicFromNicObject</span></span>
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39b14-107">설명</span><span class="sxs-lookup"><span data-stu-id="39b14-107">DESCRIPTION</span></span>
<span data-ttu-id="39b14-108">**Add-AzVMNetworkInterface** cmdlet은 가상 머신에 네트워크 인터페이스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-108">The **Add-AzVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="39b14-109">가상 머신을 만들 때 인터페이스를 추가하거나 기존 가상 머신에 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="39b14-110">예제</span><span class="sxs-lookup"><span data-stu-id="39b14-110">EXAMPLES</span></span>

### <span data-ttu-id="39b14-111">예제 1: 새 가상 머신에 네트워크 인터페이스 추가</span><span class="sxs-lookup"><span data-stu-id="39b14-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="39b14-112">첫 번째 명령은 가상 머신 개체를 만든 다음 가상 머신 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="39b14-113">이 명령은 가상 머신에 이름 및 크기를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-113">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="39b14-114">두 번째 명령은 네트워크 인터페이스를 네트워크 인터페이스에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="39b14-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="39b14-115">예제 2: 기존 가상 머신에 네트워크 인터페이스 추가</span><span class="sxs-lookup"><span data-stu-id="39b14-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="39b14-116">첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="39b14-117">이 명령은 가상 머신을 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="39b14-118">두 번째 명령은 네트워크 인터페이스를 네트워크 인터페이스에 저장된 가상 머신에 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="39b14-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="39b14-119">마지막 명령은 ResourceGroup11에 저장된 가상 머신의 $VirtualMachine 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="39b14-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39b14-120">PARAMETERS</span></span>

### <span data-ttu-id="39b14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39b14-121">-DefaultProfile</span></span>
<span data-ttu-id="39b14-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39b14-123">-Id</span><span class="sxs-lookup"><span data-stu-id="39b14-123">-Id</span></span>
<span data-ttu-id="39b14-124">가상 머신에 추가할 네트워크 인터페이스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-124">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="39b14-125">[Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet을 사용하여 네트워크 인터페이스를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-125">You can use the [Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b14-126">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="39b14-126">-NetworkInterface</span></span>
<span data-ttu-id="39b14-127">네트워크 인터페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-127">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39b14-128">-Primary</span><span class="sxs-lookup"><span data-stu-id="39b14-128">-Primary</span></span>
<span data-ttu-id="39b14-129">이 cmdlet이 네트워크 인터페이스를 기본 인터페이스로 추가하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-129">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39b14-130">-VM</span><span class="sxs-lookup"><span data-stu-id="39b14-130">-VM</span></span>
<span data-ttu-id="39b14-131">네트워크 인터페이스를 추가할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-131">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="39b14-132">가상 머신을 만들 경우 **New-AzVMConfig** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="39b14-132">To create a virtual machine, use the **New-AzVMConfig** cmdlet.</span></span>
<span data-ttu-id="39b14-133">기존 가상 머신을 얻습니다. **Get-AzVM** cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="39b14-133">To obtain an existing virtual machine, use the **Get-AzVM** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39b14-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39b14-134">CommonParameters</span></span>
<span data-ttu-id="39b14-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39b14-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39b14-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39b14-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39b14-137">입력</span><span class="sxs-lookup"><span data-stu-id="39b14-137">INPUTS</span></span>

### <span data-ttu-id="39b14-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39b14-138">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="39b14-139">System.String</span><span class="sxs-lookup"><span data-stu-id="39b14-139">System.String</span></span>

### <span data-ttu-id="39b14-140">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="39b14-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="39b14-141">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39b14-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39b14-142">출력</span><span class="sxs-lookup"><span data-stu-id="39b14-142">OUTPUTS</span></span>

### <span data-ttu-id="39b14-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="39b14-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="39b14-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39b14-144">NOTES</span></span>

## <span data-ttu-id="39b14-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39b14-145">RELATED LINKS</span></span>

[<span data-ttu-id="39b14-146">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="39b14-146">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="39b14-147">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="39b14-147">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="39b14-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="39b14-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)
