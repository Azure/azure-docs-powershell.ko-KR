---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: eca73d71d213b31c0bbc339708cc744b3bf64d2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963248"
---
# <span data-ttu-id="7e035-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-101">Restart-AzVM</span></span>

## <span data-ttu-id="7e035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e035-102">SYNOPSIS</span></span>
<span data-ttu-id="7e035-103">Azure 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="7e035-104">구문</span><span class="sxs-lookup"><span data-stu-id="7e035-104">SYNTAX</span></span>

### <span data-ttu-id="7e035-105">RestartResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="7e035-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e035-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7e035-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e035-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7e035-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7e035-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7e035-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e035-109">설명</span><span class="sxs-lookup"><span data-stu-id="7e035-109">DESCRIPTION</span></span>
<span data-ttu-id="7e035-110">다시 **시작-AzVM** cmdlet은 Azure 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="7e035-111">예제</span><span class="sxs-lookup"><span data-stu-id="7e035-111">EXAMPLES</span></span>

### <span data-ttu-id="7e035-112">예제 1: 가상 머신 다시 시작</span><span class="sxs-lookup"><span data-stu-id="7e035-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="7e035-113">이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="7e035-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7e035-114">PARAMETERS</span></span>

### <span data-ttu-id="7e035-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e035-115">-AsJob</span></span>
<span data-ttu-id="7e035-116">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7e035-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e035-117">-DefaultProfile</span></span>
<span data-ttu-id="7e035-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e035-119">-Id</span><span class="sxs-lookup"><span data-stu-id="7e035-119">-Id</span></span>
<span data-ttu-id="7e035-120">가상 머신의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e035-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e035-121">-Name</span></span>
<span data-ttu-id="7e035-122">가상 머신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e035-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="7e035-123">-NoWait</span></span>
<span data-ttu-id="7e035-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="7e035-125">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="7e035-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="7e035-126">-PerformMaintenance</span></span>
<span data-ttu-id="7e035-127">가상 머신의 유지 보수를 수행하기 위해</span><span class="sxs-lookup"><span data-stu-id="7e035-127">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e035-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e035-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e035-129">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-129">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e035-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7e035-130">-Confirm</span></span>
<span data-ttu-id="7e035-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e035-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e035-132">-WhatIf</span></span>
<span data-ttu-id="7e035-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e035-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e035-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e035-135">CommonParameters</span></span>
<span data-ttu-id="7e035-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7e035-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e035-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e035-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e035-138">입력</span><span class="sxs-lookup"><span data-stu-id="7e035-138">INPUTS</span></span>

### <span data-ttu-id="7e035-139">System.String</span><span class="sxs-lookup"><span data-stu-id="7e035-139">System.String</span></span>

### <span data-ttu-id="7e035-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7e035-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7e035-141">출력</span><span class="sxs-lookup"><span data-stu-id="7e035-141">OUTPUTS</span></span>

### <span data-ttu-id="7e035-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="7e035-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="7e035-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7e035-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7e035-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7e035-144">NOTES</span></span>

## <span data-ttu-id="7e035-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e035-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e035-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="7e035-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="7e035-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="7e035-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="7e035-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="7e035-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="7e035-151">Update-AzVM</span></span>](./Update-AzVM.md)


