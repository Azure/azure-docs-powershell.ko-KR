---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: a98818a855ef7bc75fb27c466dd0ba555d53a10f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493791"
---
# <span data-ttu-id="32bdf-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="32bdf-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="32bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="32bdf-103">이 cmdlet은 제공된 Virtual Machine Scale Set의 모든 확장에 대해 사용 가능한 최신 버전으로 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="32bdf-104">구문</span><span class="sxs-lookup"><span data-stu-id="32bdf-104">SYNTAX</span></span>

### <span data-ttu-id="32bdf-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="32bdf-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bdf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="32bdf-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32bdf-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="32bdf-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32bdf-108">설명</span><span class="sxs-lookup"><span data-stu-id="32bdf-108">DESCRIPTION</span></span>
<span data-ttu-id="32bdf-109">이 가상 머신 확장 집합의 모든 확장을 사용 가능한 최신 버전으로 이동하는 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="32bdf-110">사용 가능한 최신 버전을 이미 실행 중인 확장은 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="32bdf-111">예제</span><span class="sxs-lookup"><span data-stu-id="32bdf-111">EXAMPLES</span></span>

### <span data-ttu-id="32bdf-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="32bdf-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="32bdf-113">이 예제에서는 기존 VM 확장 집합 "MyVmssName"을 얻게 하여 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="32bdf-114">마지막 명령은 확장 롤링 업그레이드 프로세스를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="32bdf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32bdf-115">PARAMETERS</span></span>

### <span data-ttu-id="32bdf-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32bdf-116">-AsJob</span></span>
<span data-ttu-id="32bdf-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32bdf-117">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32bdf-118">-DefaultProfile</span></span>
<span data-ttu-id="32bdf-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32bdf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32bdf-120">-ResourceGroupName</span></span>
<span data-ttu-id="32bdf-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32bdf-122">-ResourceId</span></span>
<span data-ttu-id="32bdf-123">VM 확장 집합 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-123">The resource Id of the VM scale set object.</span></span> 

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32bdf-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="32bdf-125">VM 확장 집합 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-125">The VM scale set object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="32bdf-126">-VMScaleSetName</span></span>
<span data-ttu-id="32bdf-127">VM 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-127">The name of the VM scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32bdf-128">-Confirm</span></span>
<span data-ttu-id="32bdf-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32bdf-130">-WhatIf</span></span>
<span data-ttu-id="32bdf-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32bdf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32bdf-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32bdf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32bdf-133">CommonParameters</span></span>
<span data-ttu-id="32bdf-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32bdf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32bdf-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32bdf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32bdf-136">입력</span><span class="sxs-lookup"><span data-stu-id="32bdf-136">INPUTS</span></span>

### <span data-ttu-id="32bdf-137">System.String</span><span class="sxs-lookup"><span data-stu-id="32bdf-137">System.String</span></span>

### <span data-ttu-id="32bdf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="32bdf-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="32bdf-139">출력</span><span class="sxs-lookup"><span data-stu-id="32bdf-139">OUTPUTS</span></span>

### <span data-ttu-id="32bdf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="32bdf-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="32bdf-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32bdf-141">NOTES</span></span>

## <span data-ttu-id="32bdf-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32bdf-142">RELATED LINKS</span></span>
