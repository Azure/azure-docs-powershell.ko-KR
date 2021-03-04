---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/repair-azvmssservicefabricupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Repair-AzVmssServiceFabricUpdateDomain.md
ms.openlocfilehash: e0edd9ad095f6f7887e0e3f4951828844d2521c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955984"
---
# <span data-ttu-id="1b853-101">Repair-AzVmssServiceFabricUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="1b853-101">Repair-AzVmssServiceFabricUpdateDomain</span></span>

## <span data-ttu-id="1b853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b853-102">SYNOPSIS</span></span>
<span data-ttu-id="1b853-103">서비스 패브릭 가상 머신 확장 집합에서 가상 머신을 업데이트하는 수동 플랫폼 업데이트 도메인 워크입니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-103">Manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="1b853-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b853-104">SYNTAX</span></span>

### <span data-ttu-id="1b853-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="1b853-105">DefaultParameter (Default)</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-PlatformUpdateDomain] <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b853-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1b853-106">ResourceIdParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b853-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="1b853-107">ObjectParameter</span></span>
```
Repair-AzVmssServiceFabricUpdateDomain [-PlatformUpdateDomain] <Int32>
 [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b853-108">설명</span><span class="sxs-lookup"><span data-stu-id="1b853-108">DESCRIPTION</span></span>
<span data-ttu-id="1b853-109">수동 플랫폼 업데이트 도메인 워크를 강제로 적용하여 서비스 패브릭 가상 머신 확장 집합에서 가상 머신을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-109">Force manual platform update domain walk to update virtual machines in a service fabric virtual machine scale set.</span></span>

## <span data-ttu-id="1b853-110">예제</span><span class="sxs-lookup"><span data-stu-id="1b853-110">EXAMPLES</span></span>

### <span data-ttu-id="1b853-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1b853-111">Example 1</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceGroupName $rgname -VMScaleSetName $vmssName -PlatformUpdateDomain 0
```

<span data-ttu-id="1b853-112">이 명령은 리소스 그룹 이름 및 확장 집합 이름으로 지정된 가상 머신 확장 집합에 대해 UD 0에서 서비스 패브릭 업데이트 워크를 강제합니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-112">This command forces service fabric update walk on UD 0 for the virtual machine scale set specified by resource group name and scale set name.</span></span>

### <span data-ttu-id="1b853-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1b853-113">Example 2</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $rgname -VMScaleSetName $vmssName
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -VirtualMachineScaleSet $vmss -PlatformUpdateDomain 1
```

<span data-ttu-id="1b853-114">이 명령은 VM 확장 집합 개체에 지정된 가상 머신 확장 집합에 대해 UD 1에서 서비스 패브릭 업데이트 워크를 강제합니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-114">This command forces service fabric update walk on UD 1 for the virtual machine scale set specified by VM scale set object.</span></span>

### <span data-ttu-id="1b853-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="1b853-115">Example 3</span></span>
```
PS C:\> Repair-AzVmssServiceFabricUpdateDomain -ResourceId $resourceId  -PlatformUpdateDomain 2;
```

<span data-ttu-id="1b853-116">이 명령은 리소스 ID로 지정된 가상 머신 확장 집합에 대해 UD 2에서 서비스 패브릭 업데이트 워크를 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-116">This command forces service fabric update walk on UD 2 for the virtual machine scale set specified by resource id.</span></span>

## <span data-ttu-id="1b853-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1b853-117">PARAMETERS</span></span>

### <span data-ttu-id="1b853-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b853-118">-AsJob</span></span>
<span data-ttu-id="1b853-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1b853-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b853-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b853-120">-DefaultProfile</span></span>
<span data-ttu-id="1b853-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b853-122">-PlatformUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="1b853-122">-PlatformUpdateDomain</span></span>
<span data-ttu-id="1b853-123">수동 복구 워크가 요청되는 플랫폼 업데이트 도메인입니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-123">The platform update domain for which a manual recovery walk is requested.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b853-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b853-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b853-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b853-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b853-126">-ResourceId</span></span>
<span data-ttu-id="1b853-127">가상 머신 확장 집합에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-127">The resource id for the virtual machine scale set.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b853-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b853-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1b853-129">로컬 가상 머신 확장 집합 개체</span><span class="sxs-lookup"><span data-stu-id="1b853-129">Local virtual machine scale set object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b853-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1b853-130">-VMScaleSetName</span></span>
<span data-ttu-id="1b853-131">가상 머신 확장 집합의 이름</span><span class="sxs-lookup"><span data-stu-id="1b853-131">The name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b853-132">-확인</span><span class="sxs-lookup"><span data-stu-id="1b853-132">-Confirm</span></span>
<span data-ttu-id="1b853-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b853-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b853-134">-WhatIf</span></span>
<span data-ttu-id="1b853-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b853-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b853-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b853-137">CommonParameters</span></span>
<span data-ttu-id="1b853-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b853-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b853-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b853-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b853-140">입력</span><span class="sxs-lookup"><span data-stu-id="1b853-140">INPUTS</span></span>

### <span data-ttu-id="1b853-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1b853-141">System.String</span></span>

### <span data-ttu-id="1b853-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b853-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="1b853-143">출력</span><span class="sxs-lookup"><span data-stu-id="1b853-143">OUTPUTS</span></span>

### <span data-ttu-id="1b853-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span><span class="sxs-lookup"><span data-stu-id="1b853-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSRecoveryWalkResponse</span></span>

## <span data-ttu-id="1b853-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b853-145">NOTES</span></span>

## <span data-ttu-id="1b853-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b853-146">RELATED LINKS</span></span>
