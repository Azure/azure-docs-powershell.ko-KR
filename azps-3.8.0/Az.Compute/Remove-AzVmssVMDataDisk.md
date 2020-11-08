---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: 534b565e7fc77b1c8764b372675a7d8c4674b571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043655"
---
# <span data-ttu-id="8e3a1-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="8e3a1-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="8e3a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e3a1-103">가상 머신 확장 집합 VM에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="8e3a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e3a1-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e3a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="8e3a1-106">**AzVmssVMDataDisk** CMDLET은 vm SCALE 집합 vm에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="8e3a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e3a1-107">EXAMPLES</span></span>

### <span data-ttu-id="8e3a1-108">예제 1: VM 확장 집합 VM에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="8e3a1-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="8e3a1-109">리소스 그룹 이름, vmss 이름 및 인스턴스 ID에 의해 제공 되는 첫 번째 command getsan의 기존 Vmss VM입니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="8e3a1-110">두 번째 명령은 마지막 명령이 제거 된 데이터 디스크를 사용 하 여 Vmss VM을 업데이트 $VmssVM에 저장 된 VM scale 집합 VM에서 데이터 디스크 lun 0을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="8e3a1-111">변수</span><span class="sxs-lookup"><span data-stu-id="8e3a1-111">PARAMETERS</span></span>

### <span data-ttu-id="8e3a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e3a1-112">-DefaultProfile</span></span>
<span data-ttu-id="8e3a1-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e3a1-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="8e3a1-114">-Lun</span></span>
<span data-ttu-id="8e3a1-115">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e3a1-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="8e3a1-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="8e3a1-117">가상 컴퓨터 크기 조정 VM 프로필을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e3a1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e3a1-118">CommonParameters</span></span>
<span data-ttu-id="8e3a1-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e3a1-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e3a1-121">입력</span><span class="sxs-lookup"><span data-stu-id="8e3a1-121">INPUTS</span></span>

### <span data-ttu-id="8e3a1-122">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8e3a1-123">출력</span><span class="sxs-lookup"><span data-stu-id="8e3a1-123">OUTPUTS</span></span>

### <span data-ttu-id="8e3a1-124">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="8e3a1-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="8e3a1-125">상속자</span><span class="sxs-lookup"><span data-stu-id="8e3a1-125">NOTES</span></span>

## <span data-ttu-id="8e3a1-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e3a1-126">RELATED LINKS</span></span>