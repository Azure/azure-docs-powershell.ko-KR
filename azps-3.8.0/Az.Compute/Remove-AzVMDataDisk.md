---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 6b618511c5d3d8a636fb96fa335314bf3c4ee5bb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042106"
---
# <span data-ttu-id="126f4-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="126f4-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="126f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="126f4-102">SYNOPSIS</span></span>
<span data-ttu-id="126f4-103">가상 컴퓨터에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="126f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="126f4-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="126f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="126f4-105">DESCRIPTION</span></span>
<span data-ttu-id="126f4-106">**AzVMDataDisk** cmdlet은 가상 컴퓨터에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="126f4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="126f4-107">EXAMPLES</span></span>

### <span data-ttu-id="126f4-108">예제 1: 가상 머신에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="126f4-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="126f4-109">첫 번째 명령은 **AzVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="126f4-110">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="126f4-111">두 번째 명령은 $VirtualMachine에 저장 된 가상 머신에서 Disk3 이라는 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="126f4-112">마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="126f4-113">변수</span><span class="sxs-lookup"><span data-stu-id="126f4-113">PARAMETERS</span></span>

### <span data-ttu-id="126f4-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="126f4-114">-DataDiskNames</span></span>
<span data-ttu-id="126f4-115">이 cmdlet이 제거 하는 하나 이상의 데이터 디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="126f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="126f4-116">-DefaultProfile</span></span>
<span data-ttu-id="126f4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="126f4-118">-VM</span><span class="sxs-lookup"><span data-stu-id="126f4-118">-VM</span></span>
<span data-ttu-id="126f4-119">데이터 디스크를 제거할 로컬 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="126f4-120">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="126f4-121">-확인</span><span class="sxs-lookup"><span data-stu-id="126f4-121">-Confirm</span></span>
<span data-ttu-id="126f4-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="126f4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="126f4-123">-WhatIf</span></span>
<span data-ttu-id="126f4-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="126f4-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="126f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="126f4-126">CommonParameters</span></span>
<span data-ttu-id="126f4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="126f4-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="126f4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="126f4-129">입력</span><span class="sxs-lookup"><span data-stu-id="126f4-129">INPUTS</span></span>

### <span data-ttu-id="126f4-130">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="126f4-131">출력</span><span class="sxs-lookup"><span data-stu-id="126f4-131">OUTPUTS</span></span>

### <span data-ttu-id="126f4-132">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="126f4-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="126f4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="126f4-133">NOTES</span></span>

## <span data-ttu-id="126f4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="126f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="126f4-135">추가-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="126f4-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="126f4-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="126f4-136">Get-AzVM</span></span>](./Get-AzVM.md)


