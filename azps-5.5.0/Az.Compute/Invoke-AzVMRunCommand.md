---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMRunCommand.md
ms.openlocfilehash: 77ac953e1b67ea896f15b13a2695505aabc05bbb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195028"
---
# <span data-ttu-id="706ac-101">Invoke-AzVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="706ac-101">Invoke-AzVMRunCommand</span></span>

## <span data-ttu-id="706ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="706ac-102">SYNOPSIS</span></span>
<span data-ttu-id="706ac-103">VM에서 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-103">Run a command on the VM.</span></span>

## <span data-ttu-id="706ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="706ac-104">SYNTAX</span></span>

### <span data-ttu-id="706ac-105">DefaultParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="706ac-105">DefaultParameter (Default)</span></span>
```
Invoke-AzVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="706ac-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="706ac-106">ResourceIdParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="706ac-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="706ac-107">VMParameter</span></span>
```
Invoke-AzVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="706ac-108">설명</span><span class="sxs-lookup"><span data-stu-id="706ac-108">DESCRIPTION</span></span>
<span data-ttu-id="706ac-109">VM에서 실행 명령을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="706ac-110">예제</span><span class="sxs-lookup"><span data-stu-id="706ac-110">EXAMPLES</span></span>

### <span data-ttu-id="706ac-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="706ac-111">Example 1</span></span>
```
PS C:\> Invoke-AzVMRunCommand -ResourceGroupName 'rgname' -VMName 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{param1 = "var1"; param2 = "var2"}
```

<span data-ttu-id="706ac-112">리소스 그룹 'rgname'에서 'sample.ps1' 스크립트 및 'vmname' VM의 매개 변수를 정의하여 RunPowerShellScript의 실행 명령을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="706ac-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="706ac-113">PARAMETERS</span></span>

### <span data-ttu-id="706ac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="706ac-114">-AsJob</span></span>
<span data-ttu-id="706ac-115">백그라운드에서 cmdlet을 실행하고 작업 개체를 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-115">Run cmdlet in the background and return a job object to track progress.</span></span>

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

### <span data-ttu-id="706ac-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="706ac-116">-CommandId</span></span>
<span data-ttu-id="706ac-117">실행 명령 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-117">The run command ID.</span></span>

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

### <span data-ttu-id="706ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="706ac-118">-DefaultProfile</span></span>
<span data-ttu-id="706ac-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="706ac-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="706ac-120">-Parameter</span></span>
<span data-ttu-id="706ac-121">명령 매개 변수 실행</span><span class="sxs-lookup"><span data-stu-id="706ac-121">The run command parameters.</span></span>

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

### <span data-ttu-id="706ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="706ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="706ac-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="706ac-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="706ac-124">-ResourceId</span></span>
<span data-ttu-id="706ac-125">VM에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-125">The resource ID for the VM.</span></span>

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

### <span data-ttu-id="706ac-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="706ac-126">-ScriptPath</span></span>
<span data-ttu-id="706ac-127">실행할 스크립트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-127">Path of the script to be executed.</span></span>  <span data-ttu-id="706ac-128">이 값을 지정하면 지정한 스크립트가 명령의 기본 스크립트를 다시 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="706ac-129">-VM</span><span class="sxs-lookup"><span data-stu-id="706ac-129">-VM</span></span>
<span data-ttu-id="706ac-130">PS 가상 머신 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-130">The PS virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameter
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="706ac-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="706ac-131">-VMName</span></span>
<span data-ttu-id="706ac-132">가상 머신의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-132">The name of the virtual machine.</span></span>

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

### <span data-ttu-id="706ac-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="706ac-133">-Confirm</span></span>
<span data-ttu-id="706ac-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="706ac-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="706ac-135">-WhatIf</span></span>
<span data-ttu-id="706ac-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="706ac-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="706ac-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="706ac-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="706ac-138">CommonParameters</span></span>
<span data-ttu-id="706ac-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="706ac-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="706ac-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="706ac-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="706ac-141">입력</span><span class="sxs-lookup"><span data-stu-id="706ac-141">INPUTS</span></span>

### <span data-ttu-id="706ac-142">System.String</span><span class="sxs-lookup"><span data-stu-id="706ac-142">System.String</span></span>

### <span data-ttu-id="706ac-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="706ac-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="706ac-144">출력</span><span class="sxs-lookup"><span data-stu-id="706ac-144">OUTPUTS</span></span>

### <span data-ttu-id="706ac-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="706ac-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="706ac-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="706ac-146">NOTES</span></span>

## <span data-ttu-id="706ac-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="706ac-147">RELATED LINKS</span></span>
