---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195540"
---
# <span data-ttu-id="00ae0-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="00ae0-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="00ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="00ae0-103">Synapse Analytics Spark 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="00ae0-104">구문</span><span class="sxs-lookup"><span data-stu-id="00ae0-104">SYNTAX</span></span>

### <span data-ttu-id="00ae0-105">StopSparkJobByIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="00ae0-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00ae0-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ae0-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00ae0-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ae0-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00ae0-108">설명</span><span class="sxs-lookup"><span data-stu-id="00ae0-108">DESCRIPTION</span></span>
<span data-ttu-id="00ae0-109">**Stop-AzSynapseSparkJob** cmdlet은 Synapse Analytics Spark 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="00ae0-110">예제</span><span class="sxs-lookup"><span data-stu-id="00ae0-110">EXAMPLES</span></span>

### <span data-ttu-id="00ae0-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00ae0-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="00ae0-112">이 명령은 Synapse Analytics Spark 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="00ae0-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="00ae0-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="00ae0-114">이 명령은 파이프라인을 통해 Synapse Analytics Spark 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="00ae0-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="00ae0-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="00ae0-116">이 명령은 파이프라인을 통해 Synapse Analytics Spark 작업을 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="00ae0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00ae0-117">PARAMETERS</span></span>

### <span data-ttu-id="00ae0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ae0-118">-DefaultProfile</span></span>
<span data-ttu-id="00ae0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ae0-120">-Force</span><span class="sxs-lookup"><span data-stu-id="00ae0-120">-Force</span></span>
<span data-ttu-id="00ae0-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="00ae0-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="00ae0-122">-LivyId</span></span>
<span data-ttu-id="00ae0-123">Spark 작업의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00ae0-124">-PassThru</span></span>
<span data-ttu-id="00ae0-125">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="00ae0-126">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="00ae0-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="00ae0-127">-SparkJobObject</span></span>
<span data-ttu-id="00ae0-128">Spark 작업 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ae0-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="00ae0-129">-SparkPoolName</span></span>
<span data-ttu-id="00ae0-130">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae0-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="00ae0-131">-SparkPoolObject</span></span>
<span data-ttu-id="00ae0-132">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ae0-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="00ae0-133">-WorkspaceName</span></span>
<span data-ttu-id="00ae0-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00ae0-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00ae0-135">-Confirm</span></span>
<span data-ttu-id="00ae0-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ae0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ae0-137">-WhatIf</span></span>
<span data-ttu-id="00ae0-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="00ae0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00ae0-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ae0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ae0-140">CommonParameters</span></span>
<span data-ttu-id="00ae0-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00ae0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ae0-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00ae0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ae0-143">입력</span><span class="sxs-lookup"><span data-stu-id="00ae0-143">INPUTS</span></span>

### <span data-ttu-id="00ae0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="00ae0-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="00ae0-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="00ae0-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="00ae0-146">출력</span><span class="sxs-lookup"><span data-stu-id="00ae0-146">OUTPUTS</span></span>

### <span data-ttu-id="00ae0-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00ae0-147">System.Boolean</span></span>

## <span data-ttu-id="00ae0-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00ae0-148">NOTES</span></span>

## <span data-ttu-id="00ae0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00ae0-149">RELATED LINKS</span></span>
