---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssrollingupgradepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmssRollingUpgradePolicy.md
ms.openlocfilehash: 872012c6d00f5251c53b289e99ee4a4436f4b8aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534416"
---
# <span data-ttu-id="7a0f5-101">Set-AzureRmVmssRollingUpgradePolicy</span><span class="sxs-lookup"><span data-stu-id="7a0f5-101">Set-AzureRmVmssRollingUpgradePolicy</span></span>

## <span data-ttu-id="7a0f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a0f5-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0f5-103">VMSS 롤링 업그레이드 정책 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-103">Sets the VMSS rolling upgrade policy properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a0f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a0f5-104">SYNTAX</span></span>

```
Set-AzureRmVmssRollingUpgradePolicy [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-MaxBatchInstancePercent] <Int32>] [[-MaxUnhealthyInstancePercent] <Int32>]
 [[-MaxUnhealthyUpgradedInstancePercent] <Int32>] [-PauseTimeBetweenBatches <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0f5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a0f5-105">DESCRIPTION</span></span>
<span data-ttu-id="7a0f5-106">VMSS 롤링 업그레이드 정책 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-106">Sets the VMSS rolling upgrade policy properties.</span></span>

## <span data-ttu-id="7a0f5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a0f5-107">EXAMPLES</span></span>

### <span data-ttu-id="7a0f5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a0f5-108">Example 1</span></span>
```
PS C:\> Set-AzureRmVmssRollingUpgradePolicy -VirtualMachineScaleSet $vmss -VirtualMachineScaleSet $vmss -MaxBatchInstancePercent 40 -MaxUnhealthyInstancePercent 35 -MaxUnhealthyUpgradedInstancePercent 30 -PauseTimeBetweenBatches "PT30S"
```

<span data-ttu-id="7a0f5-109">이 명령은 MaxBatchInstance의 40 퍼센트, MaxUnhealthyInstance의 경우 35%, MaxUnhealthyUpgradedInstance의 경우 30%, VMSS 로컬 개체 $vmss 일괄 처리 사이에는 30 초 일시 중지 시간을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-109">This command sets 40 percent for MaxBatchInstance, 35 percent for MaxUnhealthyInstance, 30 percent for MaxUnhealthyUpgradedInstance and 30 second pause time between batches for VMSS local object $vmss.</span></span>

## <span data-ttu-id="7a0f5-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a0f5-110">PARAMETERS</span></span>

### <span data-ttu-id="7a0f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0f5-111">-DefaultProfile</span></span>
<span data-ttu-id="7a0f5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f5-113">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7a0f5-113">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="7a0f5-114">한 일괄 처리에서 롤링 업그레이드에 의해 동시에 업그레이드 되는 총 가상 머신 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-114">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="7a0f5-115">이는 최대이 고 이전 또는 이후 일괄 처리에서 비정상적인 인스턴스가 있으면 일괄 처리에서 인스턴스의 백분율이 더 높은 안정성을 유지할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-115">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="7a0f5-116">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-116">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7a0f5-117">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7a0f5-117">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="7a0f5-118">업그레이드 결과 또는 롤링 업그레이드 중단 전에 가상 컴퓨터 상태 검사를 통해 비정상 상태에 있는 것으로 볼 수 있는 배율 집합의 총 가상 머신 인스턴스 중 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-118">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="7a0f5-119">일괄 처리를 시작 하기 전에이 제약 조건을 검사 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-119">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="7a0f5-120">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-120">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7a0f5-121">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="7a0f5-121">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="7a0f5-122">비정상 상태에 있는 것으로 확인 될 수 있는 업그레이드 된 가상 컴퓨터 인스턴스의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-122">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="7a0f5-123">이 검사는 각 일괄 처리가 업그레이드 된 후에 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-123">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="7a0f5-124">이 백분율이 초과 되 면 롤링 업데이트가 중단 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-124">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="7a0f5-125">값을 지정 하지 않으면 20으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-125">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="7a0f5-126">-Pausetimeenwe일괄 처리</span><span class="sxs-lookup"><span data-stu-id="7a0f5-126">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="7a0f5-127">한 일괄 처리의 모든 가상 컴퓨터에 대 한 업데이트를 완료 하 고 다음 일괄 처리를 시작 하는 대기 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-127">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="7a0f5-128">기간을 ISO 8601 형식으로 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-128">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="7a0f5-129">기본값은 0 초 (PT0S)입니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-129">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="7a0f5-130">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7a0f5-130">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7a0f5-131">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-131">Specifies the VMSS object.</span></span>
<span data-ttu-id="7a0f5-132">New-AzureRmVmssConfig cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-132">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="7a0f5-133">-확인</span><span class="sxs-lookup"><span data-stu-id="7a0f5-133">-Confirm</span></span>
<span data-ttu-id="7a0f5-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0f5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0f5-135">-WhatIf</span></span>
<span data-ttu-id="7a0f5-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0f5-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0f5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0f5-138">CommonParameters</span></span>
<span data-ttu-id="7a0f5-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0f5-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0f5-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0f5-141">입력</span><span class="sxs-lookup"><span data-stu-id="7a0f5-141">INPUTS</span></span>

### <span data-ttu-id="7a0f5-142">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="7a0f5-143">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-143">System.Int32</span></span>

### <span data-ttu-id="7a0f5-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a0f5-144">System.String</span></span>

## <span data-ttu-id="7a0f5-145">출력</span><span class="sxs-lookup"><span data-stu-id="7a0f5-145">OUTPUTS</span></span>

### <span data-ttu-id="7a0f5-146">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="7a0f5-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="7a0f5-147">상속자</span><span class="sxs-lookup"><span data-stu-id="7a0f5-147">NOTES</span></span>

## <span data-ttu-id="7a0f5-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a0f5-148">RELATED LINKS</span></span>
