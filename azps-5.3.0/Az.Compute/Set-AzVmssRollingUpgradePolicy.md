---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 7274067b2f8daa916a0021f0ea2fd7985e1914ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495897"
---
# <span data-ttu-id="340f3-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="340f3-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="340f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340f3-102">SYNOPSIS</span></span>
<span data-ttu-id="340f3-103">VMSS 롤링 업그레이드 정책 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="340f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="340f3-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="340f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="340f3-105">DESCRIPTION</span></span>
<span data-ttu-id="340f3-106">VMSS 롤링 업그레이드 정책 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="340f3-107">예제</span><span class="sxs-lookup"><span data-stu-id="340f3-107">EXAMPLES</span></span>

### <span data-ttu-id="340f3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="340f3-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="340f3-109">이 명령은 MaxBatchInstance에 대해 40%, MaxUnhealthyInstance의 경우 35%, MaxUnhealthyUpgradedInstance의 경우 30%, VMSS 로컬 개체에 대한 배치 간 30초 일시 중지 시간을 $vmss.</span><span class="sxs-lookup"><span data-stu-id="340f3-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="340f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="340f3-110">PARAMETERS</span></span>

### <span data-ttu-id="340f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340f3-111">-DefaultProfile</span></span>
<span data-ttu-id="340f3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340f3-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="340f3-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="340f3-114">롤링 업그레이드를 통해 동시에 업그레이드될 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="340f3-115">이전 또는 미래의 일괄 처리에서 최대의 이상 인스턴스이기 때문에 안정성을 높이기 위해 일괄 처리의 인스턴스 비율이 감소할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="340f3-116">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-116">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340f3-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="340f3-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="340f3-118">업그레이드 결과로 또는 롤링 업그레이드가 중단되기 전에 가상 머신 상태 검사에 의해 이상 상태로 발견되어 동시에 이상이 될 수 있는 확장 집합의 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="340f3-119">이 제약 조건은 일괄 처리를 시작하기 전에 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="340f3-120">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-120">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340f3-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="340f3-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="340f3-122">업그레이드된 가상 머신 인스턴스의 최대 백분율은 상태가 상태가 아쉬운 것으로 나타남</span><span class="sxs-lookup"><span data-stu-id="340f3-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="340f3-123">이 검사는 각 일괄 처리가 업그레이드된 후에 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="340f3-124">이 비율을 초과하면 롤링 업데이트가 중단됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="340f3-125">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-125">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340f3-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="340f3-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="340f3-127">모든 가상 머신에 대한 업데이트를 한 번의 일괄 처리로 완료하고 다음 일괄 처리를 시작하는 사이의 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="340f3-128">기간은 ISO 8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="340f3-129">기본값은 0초(PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-129">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340f3-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="340f3-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="340f3-131">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="340f3-132">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="340f3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="340f3-133">-Confirm</span></span>
<span data-ttu-id="340f3-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="340f3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="340f3-135">-WhatIf</span></span>
<span data-ttu-id="340f3-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="340f3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="340f3-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="340f3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340f3-138">CommonParameters</span></span>
<span data-ttu-id="340f3-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="340f3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340f3-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="340f3-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340f3-141">입력</span><span class="sxs-lookup"><span data-stu-id="340f3-141">INPUTS</span></span>

### <span data-ttu-id="340f3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="340f3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="340f3-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="340f3-143">System.Int32</span></span>

### <span data-ttu-id="340f3-144">System.String</span><span class="sxs-lookup"><span data-stu-id="340f3-144">System.String</span></span>

## <span data-ttu-id="340f3-145">출력</span><span class="sxs-lookup"><span data-stu-id="340f3-145">OUTPUTS</span></span>

### <span data-ttu-id="340f3-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="340f3-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="340f3-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="340f3-147">NOTES</span></span>

## <span data-ttu-id="340f3-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="340f3-148">RELATED LINKS</span></span>
