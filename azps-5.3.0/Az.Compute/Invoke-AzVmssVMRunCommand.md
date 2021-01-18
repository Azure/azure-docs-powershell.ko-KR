---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: a63f945c5af1d5b979a0d8b70546d48233d14f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493850"
---
# <span data-ttu-id="71790-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="71790-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="71790-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71790-102">SYNOPSIS</span></span>
<span data-ttu-id="71790-103">Virtual Machine Scale Set VM에서 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="71790-104">구문</span><span class="sxs-lookup"><span data-stu-id="71790-104">SYNTAX</span></span>

### <span data-ttu-id="71790-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="71790-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71790-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="71790-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71790-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="71790-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71790-108">설명</span><span class="sxs-lookup"><span data-stu-id="71790-108">DESCRIPTION</span></span>
<span data-ttu-id="71790-109">Virtual Machine Scale Set VM에서 실행 명령을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="71790-110">예제</span><span class="sxs-lookup"><span data-stu-id="71790-110">EXAMPLES</span></span>

### <span data-ttu-id="71790-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="71790-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="71790-112">리소스 그룹 'rgname'에서 'vmssname'의 가상 머신 확장 집합에 있는 'sample.ps1' 및 ID '0' VM의 매개 변수를 정의하여 RunPowerShellScript의 실행 명령을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="71790-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="71790-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="71790-114">리소스 그룹 'rgname'에서 'vmssname'의 가상 머신 확장 집합에 있는 'sample.ps1' 및 ID '0' VM의 매개 변수를 정의하여 RunPowerShellScript의 실행 명령을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="71790-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71790-115">PARAMETERS</span></span>

### <span data-ttu-id="71790-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71790-116">-AsJob</span></span>
<span data-ttu-id="71790-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="71790-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="71790-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="71790-118">-CommandId</span></span>
<span data-ttu-id="71790-119">실행 명령 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-119">The run command id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71790-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71790-120">-DefaultProfile</span></span>
<span data-ttu-id="71790-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71790-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="71790-122">-InstanceId</span></span>
<span data-ttu-id="71790-123">가상 머신 확장 집합 VM의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-123">The instance ID of the virtual machine scale set VM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71790-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="71790-124">-Parameter</span></span>
<span data-ttu-id="71790-125">명령 매개 변수 실행</span><span class="sxs-lookup"><span data-stu-id="71790-125">The run command parameters.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71790-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71790-126">-ResourceGroupName</span></span>
<span data-ttu-id="71790-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="71790-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71790-128">-ResourceId</span></span>
<span data-ttu-id="71790-129">가상 머신 확장 집합 VM에 대한 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="71790-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="71790-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="71790-130">-ScriptPath</span></span>
<span data-ttu-id="71790-131">실행할 스크립트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-131">Path of the script to be executed.</span></span>  <span data-ttu-id="71790-132">이 값을 지정하면 제공된 스크립트가 명령의 기본 스크립트를 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-132">When this value is given, the given script will override the default script of the command.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71790-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="71790-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="71790-134">PS Virtual Machine Scale Set VM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-134">The PS Virtual Machine Scale Set VM Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: ObjectParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71790-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="71790-135">-VMScaleSetName</span></span>
<span data-ttu-id="71790-136">가상 머신 확장 집합 VM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="71790-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="71790-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71790-137">-Confirm</span></span>
<span data-ttu-id="71790-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71790-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71790-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71790-139">-WhatIf</span></span>
<span data-ttu-id="71790-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71790-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71790-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71790-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71790-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71790-142">CommonParameters</span></span>
<span data-ttu-id="71790-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71790-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71790-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71790-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71790-145">입력</span><span class="sxs-lookup"><span data-stu-id="71790-145">INPUTS</span></span>

### <span data-ttu-id="71790-146">System.String</span><span class="sxs-lookup"><span data-stu-id="71790-146">System.String</span></span>

### <span data-ttu-id="71790-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="71790-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="71790-148">출력</span><span class="sxs-lookup"><span data-stu-id="71790-148">OUTPUTS</span></span>

### <span data-ttu-id="71790-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="71790-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="71790-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71790-150">NOTES</span></span>

## <span data-ttu-id="71790-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71790-151">RELATED LINKS</span></span>
