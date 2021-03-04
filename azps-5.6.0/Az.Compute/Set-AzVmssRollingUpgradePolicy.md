---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssRollingUpgradePolicy.md
ms.openlocfilehash: 16ea3a8754ef08e933412582f100296d07fcb430
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958880"
---
# <span data-ttu-id="a3197-101">Set-AzVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="a3197-101">Set-AzVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="a3197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3197-102">SYNOPSIS</span></span>
<span data-ttu-id="a3197-103">VMSS 롤링 업그레이드 정책 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-103">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="a3197-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3197-104">SYNTAX</span></span>

```
Set-AzVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3197-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3197-105">DESCRIPTION</span></span>
<span data-ttu-id="a3197-106">VMSS 롤링 업그레이드 정책 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="a3197-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3197-107">EXAMPLES</span></span>

### <span data-ttu-id="a3197-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a3197-108">Example 1</span></span>
```
PS C:\> Set-AzVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="a3197-109">이 명령은 MaxBatchInstance에 대해 40%, MaxUnhealthyInstance의 경우 35%, MaxUnhealthyUpgradedInstance의 경우 30%, VMSS 로컬 개체에 대한 일괄 처리 간에 30초의 일시 중지 시간을 $vmss.</span><span class="sxs-lookup"><span data-stu-id="a3197-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="a3197-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3197-110">PARAMETERS</span></span>

### <span data-ttu-id="a3197-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3197-111">-DefaultProfile</span></span>
<span data-ttu-id="a3197-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3197-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a3197-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="a3197-114">한 번의 일괄 처리로 롤링 업그레이드를 통해 동시에 업그레이드되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="a3197-115">이전 또는 향후 일괄 처리에서 최대의 이상한 인스턴스이기 때문에 일괄 처리의 인스턴스 백분율이 감소하여 더 높은 안정성을 보장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="a3197-116">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="a3197-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a3197-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="a3197-118">업그레이드가 중단되기 전에 가상 머신 상태 확인에 의해 위태로울 수 있는 확장 집합의 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="a3197-119">이 제약 조건은 일괄 처리를 시작하기 전에 검사됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="a3197-120">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="a3197-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="a3197-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="a3197-122">업그레이드된 가상 머신 인스턴스의 최대 백분율은 상태가 상태가 나타남을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="a3197-123">이 검사는 각 일괄 처리가 업그레이드된 후에 진행됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="a3197-124">이 백분율을 초과하면 롤링 업데이트가 중단됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="a3197-125">값을 지정하지 않으면 20으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="a3197-126">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="a3197-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="a3197-127">모든 가상 머신에 대한 업데이트를 한 일괄 처리로 완료하고 다음 일괄 처리를 시작하는 사이의 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="a3197-128">시간 기간은 ISO 8601 형식으로 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="a3197-129">기본값은 0초(PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="a3197-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3197-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="a3197-131">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="a3197-132">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-132">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="a3197-133">-확인</span><span class="sxs-lookup"><span data-stu-id="a3197-133">-Confirm</span></span>
<span data-ttu-id="a3197-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3197-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3197-135">-WhatIf</span></span>
<span data-ttu-id="a3197-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3197-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3197-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3197-138">CommonParameters</span></span>
<span data-ttu-id="a3197-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3197-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3197-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3197-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3197-141">입력</span><span class="sxs-lookup"><span data-stu-id="a3197-141">INPUTS</span></span>

### <span data-ttu-id="a3197-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3197-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="a3197-143">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a3197-143">System.Int32</span></span>

### <span data-ttu-id="a3197-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a3197-144">System.String</span></span>

## <span data-ttu-id="a3197-145">출력</span><span class="sxs-lookup"><span data-stu-id="a3197-145">OUTPUTS</span></span>

### <span data-ttu-id="a3197-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="a3197-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="a3197-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3197-147">NOTES</span></span>

## <span data-ttu-id="a3197-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3197-148">RELATED LINKS</span></span>
