---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973712"
---
# <span data-ttu-id="f673b-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="f673b-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="f673b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f673b-102">SYNOPSIS</span></span>
<span data-ttu-id="f673b-103">Synapse Analytics Spark 세션의 시간 제한을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f673b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f673b-104">SYNTAX</span></span>

### <span data-ttu-id="f673b-105">ResetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f673b-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f673b-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f673b-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f673b-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f673b-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f673b-108">설명</span><span class="sxs-lookup"><span data-stu-id="f673b-108">DESCRIPTION</span></span>
<span data-ttu-id="f673b-109">**Remove-AzSynapseSparkSessionTimeout** cmdlet은 Synapse Analytics Spark 세션의 시간 제한을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="f673b-110">예제</span><span class="sxs-lookup"><span data-stu-id="f673b-110">EXAMPLES</span></span>

### <span data-ttu-id="f673b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f673b-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="f673b-112">이 명령은 지정된 livy ID를 사용하여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="f673b-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f673b-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="f673b-114">이 명령은 파이프라인을 통해 지정된 livy ID를 사용하여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="f673b-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="f673b-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="f673b-116">이 명령은 파이프라인을 통해 지정된 livy ID를 사용하여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="f673b-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f673b-117">PARAMETERS</span></span>

### <span data-ttu-id="f673b-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f673b-118">-AsJob</span></span>
<span data-ttu-id="f673b-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f673b-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f673b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f673b-120">-DefaultProfile</span></span>
<span data-ttu-id="f673b-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f673b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f673b-122">-InputObject</span></span>
<span data-ttu-id="f673b-123">Spark 세션 입력 개체( 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f673b-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="f673b-124">-LivyId</span></span>
<span data-ttu-id="f673b-125">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f673b-126">-PassThru</span></span>
<span data-ttu-id="f673b-127">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="f673b-128">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f673b-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="f673b-129">-SparkPoolName</span></span>
<span data-ttu-id="f673b-130">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673b-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="f673b-131">-SparkPoolObject</span></span>
<span data-ttu-id="f673b-132">Spark 풀 입력 개체( 일반적으로 파이프라인을 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f673b-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f673b-133">-WorkspaceName</span></span>
<span data-ttu-id="f673b-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f673b-135">-확인</span><span class="sxs-lookup"><span data-stu-id="f673b-135">-Confirm</span></span>
<span data-ttu-id="f673b-136">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f673b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f673b-137">-WhatIf</span></span>
<span data-ttu-id="f673b-138">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f673b-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f673b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f673b-140">CommonParameters</span></span>
<span data-ttu-id="f673b-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f673b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f673b-142">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f673b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f673b-143">입력</span><span class="sxs-lookup"><span data-stu-id="f673b-143">INPUTS</span></span>

### <span data-ttu-id="f673b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="f673b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="f673b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="f673b-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="f673b-146">출력</span><span class="sxs-lookup"><span data-stu-id="f673b-146">OUTPUTS</span></span>

### <span data-ttu-id="f673b-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f673b-147">System.Boolean</span></span>

## <span data-ttu-id="f673b-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f673b-148">NOTES</span></span>

## <span data-ttu-id="f673b-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f673b-149">RELATED LINKS</span></span>
