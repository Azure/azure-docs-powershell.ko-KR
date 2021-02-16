---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: ac961b4e7032d793cecb46008fe62091dca052f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177465"
---
# <span data-ttu-id="4d717-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-101">Stop-AzVmss</span></span>

## <span data-ttu-id="4d717-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d717-102">SYNOPSIS</span></span>
<span data-ttu-id="4d717-103">VMSS 또는 VMSS 내의 가상 머신 집합을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="4d717-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d717-104">SYNTAX</span></span>

### <span data-ttu-id="4d717-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d717-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d717-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="4d717-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d717-107">설명</span><span class="sxs-lookup"><span data-stu-id="4d717-107">DESCRIPTION</span></span>
<span data-ttu-id="4d717-108">**Stop-AzVmss** cmdlet은 VMSS(Virtual Machine Scale Set) 또는 가상 머신 집합 내의 모든 가상 머신을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="4d717-109">InstanceId 매개 *변수를* 사용하여 가상 머신 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="4d717-110">예제</span><span class="sxs-lookup"><span data-stu-id="4d717-110">EXAMPLES</span></span>

### <span data-ttu-id="4d717-111">예제 1: VMSS 내의 모든 가상 머신 중지</span><span class="sxs-lookup"><span data-stu-id="4d717-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="4d717-112">이 명령은 ContosoVMSS라는 VMSS에 속하는 모든 가상 머신을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="4d717-113">예제 2: VMSS 내에서 특정 가상 머신 집합 중지</span><span class="sxs-lookup"><span data-stu-id="4d717-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="4d717-114">이 명령은 ContosoVMSS라는 VMSS에 속하는 인스턴스 ID 문자열 배열로 지정된 특정 가상 머신 집합을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4d717-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d717-115">PARAMETERS</span></span>

### <span data-ttu-id="4d717-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d717-116">-AsJob</span></span>
<span data-ttu-id="4d717-117">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4d717-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d717-118">-DefaultProfile</span></span>
<span data-ttu-id="4d717-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d717-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4d717-120">-Force</span></span>
<span data-ttu-id="4d717-121">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4d717-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4d717-122">-InstanceId</span></span>
<span data-ttu-id="4d717-123">문자열 배열로 이 cmdlet이 중지하는 가상 머신 인스턴스의 ID 또는 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="4d717-124">예: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="4d717-124">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d717-125">-ResourceGroupName</span></span>
<span data-ttu-id="4d717-126">VMSS의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-126">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="4d717-127">-SkipShutdown</span></span>
<span data-ttu-id="4d717-128">비보안 VM 종료를 요청하는 경우</span><span class="sxs-lookup"><span data-stu-id="4d717-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-129">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="4d717-129">-StayProvisioned</span></span>
<span data-ttu-id="4d717-130">지정된 경우 가상 머신이 중지된 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="4d717-131">지정하지 않으면 가상 머신이 중지된-위치가 지정되지 않은 상태가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="4d717-132">사용자는 중지된 상태의 VM에 대한 요금이 계속 청구되지만 중지된-재배치된 상태의 VM에 대한 요금은 청구되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4d717-133">-VMScaleSetName</span></span>
<span data-ttu-id="4d717-134">이 cmdlet이 가상 머신을 중지하는 VMSS의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d717-135">-Confirm</span></span>
<span data-ttu-id="4d717-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d717-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d717-137">-WhatIf</span></span>
<span data-ttu-id="4d717-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4d717-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d717-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d717-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d717-140">CommonParameters</span></span>
<span data-ttu-id="4d717-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d717-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d717-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d717-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d717-143">입력</span><span class="sxs-lookup"><span data-stu-id="4d717-143">INPUTS</span></span>

### <span data-ttu-id="4d717-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4d717-144">System.String</span></span>

### <span data-ttu-id="4d717-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4d717-145">System.String[]</span></span>

## <span data-ttu-id="4d717-146">출력</span><span class="sxs-lookup"><span data-stu-id="4d717-146">OUTPUTS</span></span>

### <span data-ttu-id="4d717-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4d717-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4d717-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d717-148">NOTES</span></span>

## <span data-ttu-id="4d717-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d717-149">RELATED LINKS</span></span>

[<span data-ttu-id="4d717-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4d717-151">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4d717-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4d717-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4d717-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4d717-155">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4d717-156">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4d717-156">Update-AzVmss</span></span>](./Update-AzVmss.md)


