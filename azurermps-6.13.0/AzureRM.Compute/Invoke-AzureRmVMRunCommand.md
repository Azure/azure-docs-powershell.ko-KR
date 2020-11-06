---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/invoke-azurermvmruncommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Invoke-AzureRmVMRunCommand.md
ms.openlocfilehash: 89d81387f8a97fe02f607ddc9d13d4645fc9688b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530407"
---
# <span data-ttu-id="d090c-101">Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="d090c-101">Invoke-AzureRmVMRunCommand</span></span>

## <span data-ttu-id="d090c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d090c-102">SYNOPSIS</span></span>
<span data-ttu-id="d090c-103">VM의 실행 명령</span><span class="sxs-lookup"><span data-stu-id="d090c-103">Run command on the VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d090c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d090c-104">SYNTAX</span></span>

### <span data-ttu-id="d090c-105">DefaultParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="d090c-105">DefaultParameter (Default)</span></span>
```
Invoke-AzureRmVMRunCommand [-ResourceGroupName] <String> [-VMName] <String> -CommandId <String>
 [-ScriptPath <String>] [-Parameter <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d090c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="d090c-106">ResourceIdParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d090c-107">VMParameter</span><span class="sxs-lookup"><span data-stu-id="d090c-107">VMParameter</span></span>
```
Invoke-AzureRmVMRunCommand -CommandId <String> [-ScriptPath <String>] [-Parameter <Hashtable>]
 [-VM] <PSVirtualMachine> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d090c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d090c-108">DESCRIPTION</span></span>
<span data-ttu-id="d090c-109">VM에서 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-109">Invoke a run command on the VM.</span></span>

## <span data-ttu-id="d090c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d090c-110">EXAMPLES</span></span>

### <span data-ttu-id="d090c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d090c-111">Example 1</span></span>
```
PS C:\> Invoke-AzureRmVMRunCommand -ResourceGroupName 'rgname' -Name 'vmname' -CommandId 'RunPowerShellScript' -ScriptPath 'sample.ps1' -Parameter @{"arg1" = "var1";"arg2" = "var2"}
```

<span data-ttu-id="d090c-112">' sample.ps1 ' 스크립트와 ' rgname ' 리소스 그룹의 ' vmname ' VM에 있는 매개 변수를 재정의 하 여 RunPowerShellScript의 실행 명령을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-112">Invoke a run command of RunPowerShellScript with overriding the script 'sample.ps1' and the parameters on the VM of 'vmname' in resource group 'rgname'.</span></span>

## <span data-ttu-id="d090c-113">변수</span><span class="sxs-lookup"><span data-stu-id="d090c-113">PARAMETERS</span></span>

### <span data-ttu-id="d090c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d090c-114">-AsJob</span></span>
<span data-ttu-id="d090c-115">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d090c-116">-CommandId</span><span class="sxs-lookup"><span data-stu-id="d090c-116">-CommandId</span></span>
<span data-ttu-id="d090c-117">실행 명령 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-117">The run command id.</span></span>

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

### <span data-ttu-id="d090c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d090c-118">-DefaultProfile</span></span>
<span data-ttu-id="d090c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d090c-120">-Parameter</span><span class="sxs-lookup"><span data-stu-id="d090c-120">-Parameter</span></span>
<span data-ttu-id="d090c-121">실행 명령 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-121">The run command parameters.</span></span>

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

### <span data-ttu-id="d090c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d090c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d090c-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d090c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d090c-124">-ResourceId</span></span>
<span data-ttu-id="d090c-125">VM의 리소스 id</span><span class="sxs-lookup"><span data-stu-id="d090c-125">The resource id for the VM</span></span>

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

### <span data-ttu-id="d090c-126">-ScriptPath</span><span class="sxs-lookup"><span data-stu-id="d090c-126">-ScriptPath</span></span>
<span data-ttu-id="d090c-127">실행할 스크립트의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-127">Path of the script to be executed.</span></span>  <span data-ttu-id="d090c-128">이 값을 지정 하면 지정 된 스크립트는 명령의 기본 스크립트를 재정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-128">When this value is given, the given script will override the default script of the command.</span></span>

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

### <span data-ttu-id="d090c-129">-VM</span><span class="sxs-lookup"><span data-stu-id="d090c-129">-VM</span></span>
<span data-ttu-id="d090c-130">PS 가상 머신 개체</span><span class="sxs-lookup"><span data-stu-id="d090c-130">The PS virtual Machine Object.</span></span>

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

### <span data-ttu-id="d090c-131">-VMName</span><span class="sxs-lookup"><span data-stu-id="d090c-131">-VMName</span></span>
<span data-ttu-id="d090c-132">가상 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-132">The name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d090c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="d090c-133">-Confirm</span></span>
<span data-ttu-id="d090c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d090c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d090c-135">-WhatIf</span></span>
<span data-ttu-id="d090c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d090c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d090c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d090c-138">CommonParameters</span></span>
<span data-ttu-id="d090c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d090c-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d090c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d090c-141">입력</span><span class="sxs-lookup"><span data-stu-id="d090c-141">INPUTS</span></span>

### <span data-ttu-id="d090c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d090c-142">System.String</span></span>

### <span data-ttu-id="d090c-143">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d090c-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d090c-144">출력</span><span class="sxs-lookup"><span data-stu-id="d090c-144">OUTPUTS</span></span>

### <span data-ttu-id="d090c-145">Microsoft. a. m a. 모델. PSRunCommandResult</span><span class="sxs-lookup"><span data-stu-id="d090c-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandResult</span></span>

## <span data-ttu-id="d090c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="d090c-146">NOTES</span></span>

## <span data-ttu-id="d090c-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d090c-147">RELATED LINKS</span></span>
