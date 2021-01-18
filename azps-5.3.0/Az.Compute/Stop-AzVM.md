---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493788"
---
# <span data-ttu-id="8fe1b-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-101">Stop-AzVM</span></span>

## <span data-ttu-id="8fe1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8fe1b-102">SYNOPSIS</span></span>
<span data-ttu-id="8fe1b-103">Azure 가상 머신을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8fe1b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8fe1b-104">SYNTAX</span></span>

### <span data-ttu-id="8fe1b-105">ResourceGroupNameParameterSetName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8fe1b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8fe1b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8fe1b-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8fe1b-107">설명</span><span class="sxs-lookup"><span data-stu-id="8fe1b-107">DESCRIPTION</span></span>
<span data-ttu-id="8fe1b-108">**Stop-AzVM** cmdlet은 Azure 가상 머신을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8fe1b-109">예제</span><span class="sxs-lookup"><span data-stu-id="8fe1b-109">EXAMPLES</span></span>

### <span data-ttu-id="8fe1b-110">예제 1: 가상 머신 중지</span><span class="sxs-lookup"><span data-stu-id="8fe1b-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8fe1b-111">이 명령은 ResourceGroup11에서 VirtualMachine07이라는 가상 머신을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8fe1b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8fe1b-112">PARAMETERS</span></span>

### <span data-ttu-id="8fe1b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8fe1b-113">-AsJob</span></span>
<span data-ttu-id="8fe1b-114">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8fe1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fe1b-115">-DefaultProfile</span></span>
<span data-ttu-id="8fe1b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fe1b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8fe1b-117">-Force</span></span>
<span data-ttu-id="8fe1b-118">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8fe1b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="8fe1b-119">-Id</span></span>
<span data-ttu-id="8fe1b-120">가상 머신의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe1b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8fe1b-121">-Name</span></span>
<span data-ttu-id="8fe1b-122">가상 머신 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe1b-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8fe1b-123">-NoWait</span></span>
<span data-ttu-id="8fe1b-124">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8fe1b-125">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8fe1b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fe1b-126">-ResourceGroupName</span></span>
<span data-ttu-id="8fe1b-127">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8fe1b-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="8fe1b-128">-SkipShutdown</span></span>
<span data-ttu-id="8fe1b-129">VM을 프로비전된 유지 시 비보상 VM 종료를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="8fe1b-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8fe1b-130">-StayProvisioned</span></span>
<span data-ttu-id="8fe1b-131">cmdlet은 VMSS 내의 모든 가상 머신을 중지하지만 해당 가상 머신의 재배포는 중지하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8fe1b-132">계정에 중지된 가상 머신에 대한 요금이 청구됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="8fe1b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8fe1b-133">-Confirm</span></span>
<span data-ttu-id="8fe1b-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8fe1b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8fe1b-135">-WhatIf</span></span>
<span data-ttu-id="8fe1b-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8fe1b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8fe1b-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8fe1b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fe1b-138">CommonParameters</span></span>
<span data-ttu-id="8fe1b-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fe1b-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8fe1b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fe1b-141">입력</span><span class="sxs-lookup"><span data-stu-id="8fe1b-141">INPUTS</span></span>

### <span data-ttu-id="8fe1b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8fe1b-142">System.String</span></span>

## <span data-ttu-id="8fe1b-143">출력</span><span class="sxs-lookup"><span data-stu-id="8fe1b-143">OUTPUTS</span></span>

### <span data-ttu-id="8fe1b-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8fe1b-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="8fe1b-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8fe1b-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8fe1b-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8fe1b-146">NOTES</span></span>

## <span data-ttu-id="8fe1b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8fe1b-147">RELATED LINKS</span></span>

[<span data-ttu-id="8fe1b-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8fe1b-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8fe1b-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8fe1b-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8fe1b-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8fe1b-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8fe1b-153">Update-AzVM</span></span>](./Update-AzVM.md)


