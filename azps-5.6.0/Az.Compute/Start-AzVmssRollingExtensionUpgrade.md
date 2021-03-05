---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/start-azvmssrollingextensionupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmssRollingExtensionUpgrade.md
ms.openlocfilehash: 2816f34c8a6148d67a5bed397e573b07fa2e7004
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986916"
---
# <span data-ttu-id="d85ba-101">Start-AzVmssRollingExtensionUpgrade</span><span class="sxs-lookup"><span data-stu-id="d85ba-101">Start-AzVmssRollingExtensionUpgrade</span></span>

## <span data-ttu-id="d85ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d85ba-103">이 cmdlet은 주어진 Virtual Machine Scale Set의 모든 확장에 대한 롤링 업그레이드를 사용 가능한 최신 버전으로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-103">This cmdlet starts a rolling upgrade for all extensions on the given Virtual Machine Scale Set to the latest available version.</span></span> 

## <span data-ttu-id="d85ba-104">구문</span><span class="sxs-lookup"><span data-stu-id="d85ba-104">SYNTAX</span></span>

### <span data-ttu-id="d85ba-105">DefaultParameter</span><span class="sxs-lookup"><span data-stu-id="d85ba-105">DefaultParameter</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceGroupName <String> -VMScaleSetName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d85ba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d85ba-106">ByInputObject</span></span>
```
Start-AzVmssRollingExtensionUpgrade -VirtualMachineScaleSet <PSVirtualMachineScaleSet> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d85ba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d85ba-107">ByResourceId</span></span>
```
Start-AzVmssRollingExtensionUpgrade -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d85ba-108">설명</span><span class="sxs-lookup"><span data-stu-id="d85ba-108">DESCRIPTION</span></span>
<span data-ttu-id="d85ba-109">이 가상 머신 확장 집합의 모든 확장을 사용 가능한 최신 버전으로 이동하려면 롤링 업그레이드를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-109">Starts a rolling upgrade to move all extensions on this virtual machine scale set to the latest available version.</span></span>
<span data-ttu-id="d85ba-110">이미 사용 가능한 최신 버전을 실행 중인 확장은 영향을 받지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-110">Extensions which are already running the latest available version are not affected.</span></span>

## <span data-ttu-id="d85ba-111">예제</span><span class="sxs-lookup"><span data-stu-id="d85ba-111">EXAMPLES</span></span>

### <span data-ttu-id="d85ba-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d85ba-112">Example 1</span></span>
```powershell
PS C:\> $vmss = Get-AzVM -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name "testExtension" -Publisher Microsoft.CPlat.Core -Type "NullWindows" -TypeHandlerVersion "3.0" -AutoUpgradeMinorVersion $True  -Setting "";
PS C:\> Start-AzVmssRollingExtensionUpgrade -ResourceGroupName "MyResourceGroupName" -VMScaleSetName "MyVmssName";
```

<span data-ttu-id="d85ba-113">이 예제에서는 기존 VM 확장 집합 "MyVmssName"을 얻게 하여 확장을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-113">This example gets the existing VM scale set "MyVmssName", and adds an extension to it.</span></span> <span data-ttu-id="d85ba-114">최종 명령은 확장 롤링 업그레이드 프로세스를 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-114">The final command runs the extension rolling upgrade process.</span></span> 

## <span data-ttu-id="d85ba-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d85ba-115">PARAMETERS</span></span>

### <span data-ttu-id="d85ba-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d85ba-116">-AsJob</span></span>
<span data-ttu-id="d85ba-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d85ba-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d85ba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85ba-118">-DefaultProfile</span></span>
<span data-ttu-id="d85ba-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="d85ba-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="d85ba-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d85ba-122">-ResourceId</span></span>
<span data-ttu-id="d85ba-123">VM 확장 집합 개체의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-123">The resource Id of the VM scale set object.</span></span> 

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

### <span data-ttu-id="d85ba-124">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d85ba-124">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d85ba-125">VM 확장 집합 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-125">The VM scale set object.</span></span>

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

### <span data-ttu-id="d85ba-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="d85ba-126">-VMScaleSetName</span></span>
<span data-ttu-id="d85ba-127">VM 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-127">The name of the VM scale set.</span></span>

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

### <span data-ttu-id="d85ba-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d85ba-128">-Confirm</span></span>
<span data-ttu-id="d85ba-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d85ba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d85ba-130">-WhatIf</span></span>
<span data-ttu-id="d85ba-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d85ba-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d85ba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85ba-133">CommonParameters</span></span>
<span data-ttu-id="d85ba-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d85ba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85ba-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d85ba-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85ba-136">입력</span><span class="sxs-lookup"><span data-stu-id="d85ba-136">INPUTS</span></span>

### <span data-ttu-id="d85ba-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d85ba-137">System.String</span></span>

### <span data-ttu-id="d85ba-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d85ba-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d85ba-139">출력</span><span class="sxs-lookup"><span data-stu-id="d85ba-139">OUTPUTS</span></span>

### <span data-ttu-id="d85ba-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="d85ba-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="d85ba-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d85ba-141">NOTES</span></span>

## <span data-ttu-id="d85ba-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d85ba-142">RELATED LINKS</span></span>
