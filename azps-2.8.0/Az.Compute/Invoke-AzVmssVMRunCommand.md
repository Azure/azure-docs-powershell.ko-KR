---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmssvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVmssVMRunCommand.md
ms.openlocfilehash: 01273acf5c7e8b92128117def981336fba0eeac1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697396"
---
# <span data-ttu-id="9f06b-101">Invoke-AzVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="9f06b-101">Invoke-AzVmssVMRunCommand</span></span>

## <span data-ttu-id="9f06b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f06b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f06b-103">가상 머신 확장 집합 VM의 실행 명령</span><span class="sxs-lookup"><span data-stu-id="9f06b-103">Run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="9f06b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f06b-104">SYNTAX</span></span>

### <span data-ttu-id="9f06b-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="9f06b-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVmssVMRunCommand [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String>
 -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f06b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9f06b-106">ResourceIdParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f06b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9f06b-107">ObjectParameter</span></span>
```
Invoke-AzVmssVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f06b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9f06b-108">DESCRIPTION</span></span>
<span data-ttu-id="9f06b-109">가상 머신 확장 집합 VM에서 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-109">Invoke a run command on the Virtual Machine Scale Set VM.</span></span>

## <span data-ttu-id="9f06b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9f06b-110">EXAMPLES</span></span>

### <span data-ttu-id="9f06b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f06b-111">Example 1</span></span>
```
PS C:\> Invoke-AzVmssVMRunCommand -ResourceGroupName 'rgname' -VMScaleSetName 'vmssname' -InstanceId '0' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="9f06b-112">' sample.ps1 ' 스크립트와 ' rgname ' 리소스 그룹의 ' vmssname ' 집합에 있는 ' 0 ' VM의 매개 변수를 재정의 하 여 RunPowerShellScript의 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

### <span data-ttu-id="9f06b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9f06b-113">Example 2</span></span>
```
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Invoke-AzVmssVMRunCommand -VirtualMachineScaleSetVM $VmssVM -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="9f06b-114">' sample.ps1 ' 스크립트와 ' rgname ' 리소스 그룹의 ' vmssname ' 집합에 있는 ' 0 ' VM의 매개 변수를 재정의 하 여 RunPowerShellScript의 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-114">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the ID '0' VM in the virtual machine scale set of 'vmssname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="9f06b-115">변수</span><span class="sxs-lookup"><span data-stu-id="9f06b-115">PARAMETERS</span></span>

### <span data-ttu-id="9f06b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f06b-116">-AsJob</span></span>
<span data-ttu-id="9f06b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9f06b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f06b-118">-CommandId</span><span class="sxs-lookup"><span data-stu-id="9f06b-118">-CommandId</span></span>
<span data-ttu-id="9f06b-119">실행 명령 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-119">The run command id.</span></span>

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

### <span data-ttu-id="9f06b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f06b-120">-DefaultProfile</span></span>
<span data-ttu-id="9f06b-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f06b-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9f06b-122">-InstanceId</span></span>
<span data-ttu-id="9f06b-123">가상 머신 확장 집합 VM의 인스턴스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-123">The instance ID of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="9f06b-124">-Parameter</span><span class="sxs-lookup"><span data-stu-id="9f06b-124">-Parameter</span></span>
<span data-ttu-id="9f06b-125">실행 명령 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-125">The run command parameters.</span></span>

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

### <span data-ttu-id="9f06b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f06b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f06b-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f06b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f06b-128">-ResourceId</span></span>
<span data-ttu-id="9f06b-129">가상 머신 확장 집합 VM에 대 한 리소스 id</span><span class="sxs-lookup"><span data-stu-id="9f06b-129">The resource id for the virtual machine scale set VM</span></span>

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

### <span data-ttu-id="9f06b-130">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="9f06b-130">-ScriptPath</span></span>
<span data-ttu-id="9f06b-131">실행할 스크립트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-131">Path of the script to be executed.</span></span>  <span data-ttu-id="9f06b-132">이 값을 지정 하면 지정 된 스크립트는 명령의 기본 스크립트를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-132">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="9f06b-133">-VirtualMachineScaleSetVM</span><span class="sxs-lookup"><span data-stu-id="9f06b-133">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="9f06b-134">PS 가상 머신 확장 집합 VM 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-134">The PS Virtual Machine Scale Set VM Object.</span></span>

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

### <span data-ttu-id="9f06b-135">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9f06b-135">-VMScaleSetName</span></span>
<span data-ttu-id="9f06b-136">가상 컴퓨터 확장 집합 VM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-136">The name of the virtual machine scale set VM.</span></span>

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

### <span data-ttu-id="9f06b-137">-확인</span><span class="sxs-lookup"><span data-stu-id="9f06b-137">-Confirm</span></span>
<span data-ttu-id="9f06b-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f06b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f06b-139">-WhatIf</span></span>
<span data-ttu-id="9f06b-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f06b-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f06b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f06b-142">CommonParameters</span></span>
<span data-ttu-id="9f06b-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f06b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f06b-144">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9f06b-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f06b-145">입력</span><span class="sxs-lookup"><span data-stu-id="9f06b-145">INPUTS</span></span>

### <span data-ttu-id="9f06b-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9f06b-146">System.String</span></span>

### <span data-ttu-id="9f06b-147">PSVirtualMachineScaleSetVM의. m a.</span><span class="sxs-lookup"><span data-stu-id="9f06b-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="9f06b-148">출력</span><span class="sxs-lookup"><span data-stu-id="9f06b-148">OUTPUTS</span></span>

### <span data-ttu-id="9f06b-149">Microsoft. a. m a. 모델. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="9f06b-149">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="9f06b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="9f06b-150">NOTES</span></span>

## <span data-ttu-id="9f06b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f06b-151">RELATED LINKS</span></span>
