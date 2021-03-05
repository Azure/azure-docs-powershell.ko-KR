---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983291"
---
# <span data-ttu-id="20f9d-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="20f9d-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="20f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="20f9d-103">가상 머신에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="20f9d-104">구문</span><span class="sxs-lookup"><span data-stu-id="20f9d-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f9d-105">설명</span><span class="sxs-lookup"><span data-stu-id="20f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="20f9d-106">**Remove-AzVMDataDisk** cmdlet은 가상 머신에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="20f9d-107">예제</span><span class="sxs-lookup"><span data-stu-id="20f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="20f9d-108">예제 1: 가상 머신에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="20f9d-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="20f9d-109">첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="20f9d-110">명령은 가상 머신을 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="20f9d-111">두 번째 명령은 디스크3이라는 데이터 디스크를 디스크에 저장된 가상 머신에서 $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="20f9d-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="20f9d-112">마지막 명령은 ResourceGroup11에 저장된 가상 머신의 $VirtualMachine 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="20f9d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="20f9d-113">PARAMETERS</span></span>

### <span data-ttu-id="20f9d-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="20f9d-114">-DataDiskNames</span></span>
<span data-ttu-id="20f9d-115">이 cmdlet이 제거한 하나 이상의 데이터 디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="20f9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f9d-116">-DefaultProfile</span></span>
<span data-ttu-id="20f9d-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f9d-118">-VM</span><span class="sxs-lookup"><span data-stu-id="20f9d-118">-VM</span></span>
<span data-ttu-id="20f9d-119">데이터 디스크를 제거할 로컬 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="20f9d-120">가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="20f9d-121">-확인</span><span class="sxs-lookup"><span data-stu-id="20f9d-121">-Confirm</span></span>
<span data-ttu-id="20f9d-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f9d-123">-WhatIf</span></span>
<span data-ttu-id="20f9d-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20f9d-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f9d-126">CommonParameters</span></span>
<span data-ttu-id="20f9d-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="20f9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f9d-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20f9d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f9d-129">입력</span><span class="sxs-lookup"><span data-stu-id="20f9d-129">INPUTS</span></span>

### <span data-ttu-id="20f9d-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="20f9d-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="20f9d-131">출력</span><span class="sxs-lookup"><span data-stu-id="20f9d-131">OUTPUTS</span></span>

### <span data-ttu-id="20f9d-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="20f9d-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="20f9d-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="20f9d-133">NOTES</span></span>

## <span data-ttu-id="20f9d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20f9d-134">RELATED LINKS</span></span>

[<span data-ttu-id="20f9d-135">Add-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="20f9d-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="20f9d-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="20f9d-136">Get-AzVM</span></span>](./Get-AzVM.md)


