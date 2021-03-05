---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971440"
---
# <span data-ttu-id="5b689-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="5b689-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="5b689-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b689-102">SYNOPSIS</span></span>
<span data-ttu-id="5b689-103">가상 머신 확장 집합 VM에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="5b689-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="5b689-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b689-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b689-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b689-105">DESCRIPTION</span></span>
<span data-ttu-id="5b689-106">**Remove-AzVmssVMDataDisk** cmdlet은 VM 확장 집합 VM에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="5b689-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b689-107">EXAMPLES</span></span>

### <span data-ttu-id="5b689-108">예제 1: VM 확장 집합 VM에서 데이터 디스크 제거</span><span class="sxs-lookup"><span data-stu-id="5b689-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="5b689-109">첫 번째 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID가 지정한 기존 Vms VM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="5b689-110">두 번째 명령은 VM에 저장된 VM 확장 집합 VM에서 $VmssVM Vms VM을 제거된 데이터 디스크로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="5b689-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b689-111">PARAMETERS</span></span>

### <span data-ttu-id="5b689-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b689-112">-DefaultProfile</span></span>
<span data-ttu-id="5b689-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b689-114">-Lun</span><span class="sxs-lookup"><span data-stu-id="5b689-114">-Lun</span></span>
<span data-ttu-id="5b689-115">디스크의 논리 단위 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-115">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="5b689-116">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b689-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="5b689-117">가상 머신 확장 집합 VM 프로필입니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-117">The virtual machine scale set VM profile.</span></span>

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

### <span data-ttu-id="5b689-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b689-118">CommonParameters</span></span>
<span data-ttu-id="5b689-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b689-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b689-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b689-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b689-121">입력</span><span class="sxs-lookup"><span data-stu-id="5b689-121">INPUTS</span></span>

### <span data-ttu-id="5b689-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b689-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5b689-123">출력</span><span class="sxs-lookup"><span data-stu-id="5b689-123">OUTPUTS</span></span>

### <span data-ttu-id="5b689-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="5b689-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="5b689-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b689-125">NOTES</span></span>

## <span data-ttu-id="5b689-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b689-126">RELATED LINKS</span></span>
