---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195537"
---
# <span data-ttu-id="3ac2a-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3ac2a-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="3ac2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac2a-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac2a-103">Synapse Analytics Spark 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3ac2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ac2a-104">SYNTAX</span></span>

### <span data-ttu-id="3ac2a-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ac2a-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac2a-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ac2a-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ac2a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ac2a-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ac2a-108">설명</span><span class="sxs-lookup"><span data-stu-id="3ac2a-108">DESCRIPTION</span></span>
<span data-ttu-id="3ac2a-109">**Stop-AzSynapseSparkSession** cmdlet은 Synapse Analytics Spark 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3ac2a-110">예제</span><span class="sxs-lookup"><span data-stu-id="3ac2a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ac2a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3ac2a-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="3ac2a-112">이 명령은 Synapse Analytics Spark 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="3ac2a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="3ac2a-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="3ac2a-114">이 명령은 파이프라인을 통해 Synapse Analytics Spark 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="3ac2a-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="3ac2a-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="3ac2a-116">이 명령은 파이프라인을 통해 Synapse Analytics Spark 세션을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="3ac2a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ac2a-117">PARAMETERS</span></span>

### <span data-ttu-id="3ac2a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ac2a-118">-AsJob</span></span>
<span data-ttu-id="3ac2a-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3ac2a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3ac2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac2a-120">-DefaultProfile</span></span>
<span data-ttu-id="3ac2a-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac2a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ac2a-122">-InputObject</span></span>
<span data-ttu-id="3ac2a-123">Spark 세션 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2a-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3ac2a-124">-LivyId</span></span>
<span data-ttu-id="3ac2a-125">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ac2a-126">-PassThru</span></span>
<span data-ttu-id="3ac2a-127">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3ac2a-128">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3ac2a-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3ac2a-129">-SparkPoolName</span></span>
<span data-ttu-id="3ac2a-130">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2a-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3ac2a-131">-SparkPoolObject</span></span>
<span data-ttu-id="3ac2a-132">Spark 풀 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2a-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3ac2a-133">-WorkspaceName</span></span>
<span data-ttu-id="3ac2a-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac2a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ac2a-135">-Confirm</span></span>
<span data-ttu-id="3ac2a-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac2a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac2a-137">-WhatIf</span></span>
<span data-ttu-id="3ac2a-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3ac2a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac2a-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac2a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac2a-140">CommonParameters</span></span>
<span data-ttu-id="3ac2a-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac2a-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ac2a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac2a-143">입력</span><span class="sxs-lookup"><span data-stu-id="3ac2a-143">INPUTS</span></span>

### <span data-ttu-id="3ac2a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3ac2a-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="3ac2a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3ac2a-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3ac2a-146">출력</span><span class="sxs-lookup"><span data-stu-id="3ac2a-146">OUTPUTS</span></span>

### <span data-ttu-id="3ac2a-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3ac2a-147">System.Boolean</span></span>

## <span data-ttu-id="3ac2a-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ac2a-148">NOTES</span></span>

## <span data-ttu-id="3ac2a-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ac2a-149">RELATED LINKS</span></span>