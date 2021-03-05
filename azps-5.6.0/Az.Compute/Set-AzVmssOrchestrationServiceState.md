---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssorchestrationservicestate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOrchestrationServiceState.md
ms.openlocfilehash: 84f208a18061d7a682fc1662c97811a19590ca65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983744"
---
# <span data-ttu-id="37e0d-101">Set-AzVmssOrchestrationServiceState</span><span class="sxs-lookup"><span data-stu-id="37e0d-101">Set-AzVmssOrchestrationServiceState</span></span>

## <span data-ttu-id="37e0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="37e0d-103">VMSS에 대한 오케스트레이션 서비스 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-103">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="37e0d-104">구문</span><span class="sxs-lookup"><span data-stu-id="37e0d-104">SYNTAX</span></span>

### <span data-ttu-id="37e0d-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="37e0d-105">DefaultParameter (Default)</span></span>
```
Set-AzVmssOrchestrationServiceState [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-ServiceName] <String> [-Action] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e0d-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="37e0d-106">ResourceIdParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String> [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37e0d-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="37e0d-107">ObjectParameter</span></span>
```
Set-AzVmssOrchestrationServiceState [-ServiceName] <String> [-Action] <String>
 [-InputObject] <PSVirtualMachineScaleSet> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37e0d-108">설명</span><span class="sxs-lookup"><span data-stu-id="37e0d-108">DESCRIPTION</span></span>
<span data-ttu-id="37e0d-109">VMSS에 대한 오케스트레이션 서비스 상태를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-109">Sets the orchestration service state for the VMSS.</span></span>

## <span data-ttu-id="37e0d-110">예제</span><span class="sxs-lookup"><span data-stu-id="37e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="37e0d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="37e0d-111">Example 1</span></span>
```
PS C:\> Set-AzVmssOrchestrationServiceState -ResourceGroupName "rg" -VMScaleSetName "vmss1" -ServiceName "AutomaticRepairs" -Action "Suspend"
```

<span data-ttu-id="37e0d-112">이 명령은 리소스 그룹 "rg"의 VMSS "vmss1"에서 자동 복구 서비스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-112">This command suspends Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

### <span data-ttu-id="37e0d-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="37e0d-113">Example 2</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "rg" -VMScaleSetName "vmss1" | Set-AzVmssOrchestrationServiceState -ServiceName "AutomaticRepairs" -Action "Resume"
```

<span data-ttu-id="37e0d-114">이 명령은 리소스 그룹 "rg"의 VMSS "vmss1"에서 자동 복구 서비스를 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-114">This command resumes Automatic Repairs service on the VMSS "vmss1" in the resource group "rg".</span></span>

## <span data-ttu-id="37e0d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="37e0d-115">PARAMETERS</span></span>

### <span data-ttu-id="37e0d-116">-Action</span><span class="sxs-lookup"><span data-stu-id="37e0d-116">-Action</span></span>
<span data-ttu-id="37e0d-117">수행할 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-117">The action to be performed.</span></span>  <span data-ttu-id="37e0d-118">가능한 값은 다시 시작, 일시 중단입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-118">Possible values are: Resume, Suspend.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e0d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37e0d-119">-AsJob</span></span>
<span data-ttu-id="37e0d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="37e0d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37e0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e0d-121">-DefaultProfile</span></span>
<span data-ttu-id="37e0d-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e0d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37e0d-123">-InputObject</span></span>
<span data-ttu-id="37e0d-124">가상 머신 확장 집합의 로컬 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-124">The local object of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="37e0d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37e0d-125">-ResourceGroupName</span></span>
<span data-ttu-id="37e0d-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="37e0d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37e0d-127">-ResourceId</span></span>
<span data-ttu-id="37e0d-128">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-128">The ID of the resource.</span></span>

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

### <span data-ttu-id="37e0d-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="37e0d-129">-ServiceName</span></span>
<span data-ttu-id="37e0d-130">서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-130">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37e0d-131">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="37e0d-131">-VMScaleSetName</span></span>
<span data-ttu-id="37e0d-132">가상 머신 확장 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-132">The name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="37e0d-133">-확인</span><span class="sxs-lookup"><span data-stu-id="37e0d-133">-Confirm</span></span>
<span data-ttu-id="37e0d-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e0d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e0d-135">-WhatIf</span></span>
<span data-ttu-id="37e0d-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e0d-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e0d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e0d-138">CommonParameters</span></span>
<span data-ttu-id="37e0d-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="37e0d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e0d-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37e0d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e0d-141">입력</span><span class="sxs-lookup"><span data-stu-id="37e0d-141">INPUTS</span></span>

### <span data-ttu-id="37e0d-142">System.String</span><span class="sxs-lookup"><span data-stu-id="37e0d-142">System.String</span></span>

### <span data-ttu-id="37e0d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="37e0d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="37e0d-144">출력</span><span class="sxs-lookup"><span data-stu-id="37e0d-144">OUTPUTS</span></span>

### <span data-ttu-id="37e0d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="37e0d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="37e0d-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="37e0d-146">NOTES</span></span>

## <span data-ttu-id="37e0d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37e0d-147">RELATED LINKS</span></span>
