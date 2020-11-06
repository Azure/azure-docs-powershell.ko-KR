---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMNetworkInterface.md
ms.openlocfilehash: 11d2f8226e2cabba5fb431054a0e6c822e33af6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529926"
---
# <span data-ttu-id="89853-101">Add-AzureRmVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89853-101">Add-AzureRmVMNetworkInterface</span></span>

## <span data-ttu-id="89853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89853-102">SYNOPSIS</span></span>
<span data-ttu-id="89853-103">가상 컴퓨터에 네트워크 인터페이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-103">Adds a network interface to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89853-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89853-104">SYNTAX</span></span>

### <span data-ttu-id="89853-105">GetNicFromNicId (기본값)</span><span class="sxs-lookup"><span data-stu-id="89853-105">GetNicFromNicId (Default)</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary] [<CommonParameters>]
```

### <span data-ttu-id="89853-106">GetNicFromNicObject</span><span class="sxs-lookup"><span data-stu-id="89853-106">GetNicFromNicObject</span></span>
```
Add-AzureRmVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]>
 [<CommonParameters>]
```

## <span data-ttu-id="89853-107">설명은</span><span class="sxs-lookup"><span data-stu-id="89853-107">DESCRIPTION</span></span>
<span data-ttu-id="89853-108">**추가-AzureRmVMNetworkInterface** cmdlet은 가상 컴퓨터에 네트워크 인터페이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-108">The **Add-AzureRmVMNetworkInterface** cmdlet adds a network interface to a virtual machine.</span></span>
<span data-ttu-id="89853-109">가상 컴퓨터를 만들거나 기존 가상 컴퓨터에 추가할 때 인터페이스를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89853-109">You can add an interface when you create a virtual machine or add one to an existing virtual machine.</span></span>

## <span data-ttu-id="89853-110">예제의</span><span class="sxs-lookup"><span data-stu-id="89853-110">EXAMPLES</span></span>

### <span data-ttu-id="89853-111">예제 1: 새 가상 컴퓨터에 네트워크 인터페이스 추가</span><span class="sxs-lookup"><span data-stu-id="89853-111">Example 1: Add a network interface to a new virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" 
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

<span data-ttu-id="89853-112">첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-112">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="89853-113">명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-113">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="89853-114">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 네트워크 인터페이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-114">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

### <span data-ttu-id="89853-115">예제 2: 기존 가상 컴퓨터에 네트워크 인터페이스 추가</span><span class="sxs-lookup"><span data-stu-id="89853-115">Example 2: Add a network interface to an existing virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="89853-116">첫 번째 명령은 **AzureRmVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89853-116">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="89853-117">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-117">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="89853-118">두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 네트워크 인터페이스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-118">The second command adds a network interface to the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="89853-119">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-119">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="89853-120">변수</span><span class="sxs-lookup"><span data-stu-id="89853-120">PARAMETERS</span></span>

### <span data-ttu-id="89853-121">-Id</span><span class="sxs-lookup"><span data-stu-id="89853-121">-Id</span></span>
<span data-ttu-id="89853-122">가상 컴퓨터에 추가할 네트워크 인터페이스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-122">Specifies the ID of a network interface to add to a virtual machine.</span></span>
<span data-ttu-id="89853-123">[Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet을 사용 하 여 네트워크 인터페이스를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89853-123">You can use the [Get-AzureRmNetworkInterface](/powershell/module/azurerm.network/get-azurermnetworkinterface) cmdlet to obtain a network interface.</span></span>

```yaml
Type: String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89853-124">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="89853-124">-NetworkInterface</span></span>
<span data-ttu-id="89853-125">네트워크 인터페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-125">Specifies the network interface.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkInterface]
Parameter Sets: GetNicFromNicObject
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89853-126">-기본</span><span class="sxs-lookup"><span data-stu-id="89853-126">-Primary</span></span>
<span data-ttu-id="89853-127">이 cmdlet이 네트워크 인터페이스를 기본 인터페이스로 추가 했음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="89853-127">Indicates that this cmdlet adds the network interface as the primary interface.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89853-128">-VM</span><span class="sxs-lookup"><span data-stu-id="89853-128">-VM</span></span>
<span data-ttu-id="89853-129">네트워크 인터페이스를 추가할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-129">Specifies a local virtual machine object to which to add a network interface.</span></span>
<span data-ttu-id="89853-130">가상 컴퓨터를 만들려면 **AzureRmVMConfig** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-130">To create a virtual machine, use the **New-AzureRmVMConfig** cmdlet.</span></span>
<span data-ttu-id="89853-131">기존 가상 머신을 얻으려면 **AzureRmVM** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-131">To obtain an existing virtual machine, use the **Get-AzureRmVM** cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89853-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89853-132">CommonParameters</span></span>
<span data-ttu-id="89853-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89853-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89853-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89853-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89853-135">입력</span><span class="sxs-lookup"><span data-stu-id="89853-135">INPUTS</span></span>

### <span data-ttu-id="89853-136">않아야</span><span class="sxs-lookup"><span data-stu-id="89853-136">None</span></span>
<span data-ttu-id="89853-137">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89853-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="89853-138">출력</span><span class="sxs-lookup"><span data-stu-id="89853-138">OUTPUTS</span></span>

## <span data-ttu-id="89853-139">상속자</span><span class="sxs-lookup"><span data-stu-id="89853-139">NOTES</span></span>

## <span data-ttu-id="89853-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89853-140">RELATED LINKS</span></span>

[<span data-ttu-id="89853-141">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="89853-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="89853-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="89853-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="89853-143">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="89853-143">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)
