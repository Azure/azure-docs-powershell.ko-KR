---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702544"
---
# <span data-ttu-id="83dde-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="83dde-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="83dde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83dde-102">SYNOPSIS</span></span>
<span data-ttu-id="83dde-103">가상 컴퓨터에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83dde-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83dde-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83dde-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83dde-105">DESCRIPTION</span></span>
<span data-ttu-id="83dde-106">**AzureRmVMDataDisk** cmdlet은 가상 컴퓨터에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="83dde-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83dde-107">EXAMPLES</span></span>

### <span data-ttu-id="83dde-108">예제 1: 가상 머신에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="83dde-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="83dde-109">첫 번째 명령은 **AzureRmVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="83dde-110">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="83dde-111">두 번째 명령은 $VirtualMachine에 저장 된 가상 머신에서 Disk3 이라는 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="83dde-112">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="83dde-113">변수</span><span class="sxs-lookup"><span data-stu-id="83dde-113">PARAMETERS</span></span>

### <span data-ttu-id="83dde-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="83dde-114">-DataDiskNames</span></span>
<span data-ttu-id="83dde-115">이 cmdlet이 제거 하는 하나 이상의 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83dde-116">-VM</span><span class="sxs-lookup"><span data-stu-id="83dde-116">-VM</span></span>
<span data-ttu-id="83dde-117">데이터 디스크를 제거할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="83dde-118">가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="83dde-119">-확인</span><span class="sxs-lookup"><span data-stu-id="83dde-119">-Confirm</span></span>
<span data-ttu-id="83dde-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-120">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="83dde-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83dde-121">-WhatIf</span></span>
<span data-ttu-id="83dde-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83dde-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-123">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="83dde-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83dde-124">CommonParameters</span></span>
<span data-ttu-id="83dde-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83dde-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83dde-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83dde-127">입력</span><span class="sxs-lookup"><span data-stu-id="83dde-127">INPUTS</span></span>

### <span data-ttu-id="83dde-128">않아야</span><span class="sxs-lookup"><span data-stu-id="83dde-128">None</span></span>
<span data-ttu-id="83dde-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83dde-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83dde-130">출력</span><span class="sxs-lookup"><span data-stu-id="83dde-130">OUTPUTS</span></span>

## <span data-ttu-id="83dde-131">상속자</span><span class="sxs-lookup"><span data-stu-id="83dde-131">NOTES</span></span>

## <span data-ttu-id="83dde-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83dde-132">RELATED LINKS</span></span>

[<span data-ttu-id="83dde-133">추가-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="83dde-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="83dde-134">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="83dde-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


