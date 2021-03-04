---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: a163854838dcb8e41b7a8b65d1be9e1aca088d55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990439"
---
# <span data-ttu-id="ef44d-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ef44d-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="ef44d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef44d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef44d-103">가상 머신의 부팅 진단 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ef44d-104">구문</span><span class="sxs-lookup"><span data-stu-id="ef44d-104">SYNTAX</span></span>

### <span data-ttu-id="ef44d-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef44d-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef44d-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ef44d-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef44d-107">설명</span><span class="sxs-lookup"><span data-stu-id="ef44d-107">DESCRIPTION</span></span>
<span data-ttu-id="ef44d-108">**Set-AzVMBootDiagnostic** cmdlet은 가상 머신의 부팅 진단 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="ef44d-109">예제</span><span class="sxs-lookup"><span data-stu-id="ef44d-109">EXAMPLES</span></span>

### <span data-ttu-id="ef44d-110">예제 1: 부팅 진단 사용</span><span class="sxs-lookup"><span data-stu-id="ef44d-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="ef44d-111">첫 번째 명령은 **Get-AzVM을** 사용하여 ContosoVM07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="ef44d-112">명령은 이 변수를 $VM 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="ef44d-113">두 번째 명령은 가상 머신에 대한 부팅 진단을 $VM.</span><span class="sxs-lookup"><span data-stu-id="ef44d-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="ef44d-114">진단 데이터는 지정된 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="ef44d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ef44d-115">PARAMETERS</span></span>

### <span data-ttu-id="ef44d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef44d-116">-DefaultProfile</span></span>
<span data-ttu-id="ef44d-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef44d-118">-사용 안</span><span class="sxs-lookup"><span data-stu-id="ef44d-118">-Disable</span></span>
<span data-ttu-id="ef44d-119">이 cmdlet은 가상 머신에 대한 부팅 진단을 사용하지 않도록 설정하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef44d-120">-사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="ef44d-120">-Enable</span></span>
<span data-ttu-id="ef44d-121">이 cmdlet을 사용하여 가상 머신에 대한 부팅 진단을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef44d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef44d-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef44d-123">저장소 계정의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef44d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ef44d-124">-StorageAccountName</span></span>
<span data-ttu-id="ef44d-125">부팅 진단 데이터를 저장할 저장소 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef44d-126">-VM</span><span class="sxs-lookup"><span data-stu-id="ef44d-126">-VM</span></span>
<span data-ttu-id="ef44d-127">이 cmdlet이 부팅 진단을 변경하는 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="ef44d-128">가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="ef44d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef44d-129">CommonParameters</span></span>
<span data-ttu-id="ef44d-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ef44d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef44d-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef44d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef44d-132">입력</span><span class="sxs-lookup"><span data-stu-id="ef44d-132">INPUTS</span></span>

### <span data-ttu-id="ef44d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ef44d-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="ef44d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="ef44d-134">System.String</span></span>

## <span data-ttu-id="ef44d-135">출력</span><span class="sxs-lookup"><span data-stu-id="ef44d-135">OUTPUTS</span></span>

### <span data-ttu-id="ef44d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ef44d-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ef44d-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ef44d-137">NOTES</span></span>

## <span data-ttu-id="ef44d-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef44d-138">RELATED LINKS</span></span>

[<span data-ttu-id="ef44d-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ef44d-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ef44d-140">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ef44d-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


