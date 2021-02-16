---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: 358b24c403c4b08b221f97ad99271112ee0852be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204824"
---
# <span data-ttu-id="de3f1-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-101">Restart-AzVM</span></span>

## <span data-ttu-id="de3f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="de3f1-103">Azure 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="de3f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="de3f1-104">SYNTAX</span></span>

### <span data-ttu-id="de3f1-105">RestartResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="de3f1-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3f1-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de3f1-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de3f1-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de3f1-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de3f1-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="de3f1-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-PerformMaintenance] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de3f1-109">설명</span><span class="sxs-lookup"><span data-stu-id="de3f1-109">DESCRIPTION</span></span>
<span data-ttu-id="de3f1-110">**Restart-AzVM** cmdlet은 Azure 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="de3f1-111">예제</span><span class="sxs-lookup"><span data-stu-id="de3f1-111">EXAMPLES</span></span>

### <span data-ttu-id="de3f1-112">예제 1: 가상 머신 다시 시작</span><span class="sxs-lookup"><span data-stu-id="de3f1-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="de3f1-113">이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="de3f1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de3f1-114">PARAMETERS</span></span>

### <span data-ttu-id="de3f1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de3f1-115">-AsJob</span></span>
<span data-ttu-id="de3f1-116">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="de3f1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3f1-117">-DefaultProfile</span></span>
<span data-ttu-id="de3f1-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de3f1-119">-Id</span><span class="sxs-lookup"><span data-stu-id="de3f1-119">-Id</span></span>
<span data-ttu-id="de3f1-120">가상 머신의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="de3f1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de3f1-121">-Name</span></span>
<span data-ttu-id="de3f1-122">가상 머신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="de3f1-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de3f1-123">-NoWait</span></span>
<span data-ttu-id="de3f1-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="de3f1-125">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="de3f1-126">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="de3f1-126">-PerformMaintenance</span></span>
<span data-ttu-id="de3f1-127">가상 머신의 유지 관리 수행</span><span class="sxs-lookup"><span data-stu-id="de3f1-127">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="de3f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="de3f1-129">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-129">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="de3f1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de3f1-130">-Confirm</span></span>
<span data-ttu-id="de3f1-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3f1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3f1-132">-WhatIf</span></span>
<span data-ttu-id="de3f1-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="de3f1-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3f1-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3f1-135">CommonParameters</span></span>
<span data-ttu-id="de3f1-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="de3f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3f1-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de3f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3f1-138">입력</span><span class="sxs-lookup"><span data-stu-id="de3f1-138">INPUTS</span></span>

### <span data-ttu-id="de3f1-139">System.String</span><span class="sxs-lookup"><span data-stu-id="de3f1-139">System.String</span></span>

### <span data-ttu-id="de3f1-140">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="de3f1-140">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="de3f1-141">출력</span><span class="sxs-lookup"><span data-stu-id="de3f1-141">OUTPUTS</span></span>

### <span data-ttu-id="de3f1-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="de3f1-142">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="de3f1-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="de3f1-143">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="de3f1-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="de3f1-144">NOTES</span></span>

## <span data-ttu-id="de3f1-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de3f1-145">RELATED LINKS</span></span>

[<span data-ttu-id="de3f1-146">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-146">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="de3f1-147">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-147">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="de3f1-148">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-148">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="de3f1-149">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-149">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="de3f1-150">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-150">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="de3f1-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="de3f1-151">Update-AzVM</span></span>](./Update-AzVM.md)


