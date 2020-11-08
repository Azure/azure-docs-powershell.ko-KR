---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215742"
---
# <span data-ttu-id="6ea45-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="6ea45-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="6ea45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea45-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea45-103">Synapse Analytics Spark 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6ea45-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ea45-104">SYNTAX</span></span>

### <span data-ttu-id="6ea45-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ea45-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea45-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ea45-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ea45-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ea45-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ea45-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ea45-108">DESCRIPTION</span></span>
<span data-ttu-id="6ea45-109">**AzSynapseSparkSession** Cmdlet은 Synapse Analytics Spark 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="6ea45-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ea45-110">EXAMPLES</span></span>

### <span data-ttu-id="6ea45-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ea45-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="6ea45-112">이 명령은 Synapse Analytics Spark 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="6ea45-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ea45-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="6ea45-114">이 명령은 파이프라인을 통해 Synapse Analytics Spark 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="6ea45-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="6ea45-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="6ea45-116">이 명령은 파이프라인을 통해 Synapse Analytics Spark 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="6ea45-117">변수</span><span class="sxs-lookup"><span data-stu-id="6ea45-117">PARAMETERS</span></span>

### <span data-ttu-id="6ea45-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ea45-118">-AsJob</span></span>
<span data-ttu-id="6ea45-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ea45-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ea45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea45-120">-DefaultProfile</span></span>
<span data-ttu-id="6ea45-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea45-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ea45-122">-InputObject</span></span>
<span data-ttu-id="6ea45-123">일반적으로 파이프라인을 통해 전달 되는 Spark 세션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ea45-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="6ea45-124">-LivyId</span></span>
<span data-ttu-id="6ea45-125">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="6ea45-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ea45-126">-PassThru</span></span>
<span data-ttu-id="6ea45-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6ea45-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6ea45-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="6ea45-129">-SparkPoolName</span></span>
<span data-ttu-id="6ea45-130">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="6ea45-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="6ea45-131">-SparkPoolObject</span></span>
<span data-ttu-id="6ea45-132">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6ea45-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ea45-133">-WorkspaceName</span></span>
<span data-ttu-id="6ea45-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6ea45-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6ea45-135">-Confirm</span></span>
<span data-ttu-id="6ea45-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea45-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea45-137">-WhatIf</span></span>
<span data-ttu-id="6ea45-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea45-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea45-140">CommonParameters</span></span>
<span data-ttu-id="6ea45-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea45-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6ea45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea45-143">입력</span><span class="sxs-lookup"><span data-stu-id="6ea45-143">INPUTS</span></span>

### <span data-ttu-id="6ea45-144">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="6ea45-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="6ea45-145">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="6ea45-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="6ea45-146">출력</span><span class="sxs-lookup"><span data-stu-id="6ea45-146">OUTPUTS</span></span>

### <span data-ttu-id="6ea45-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6ea45-147">System.Boolean</span></span>

## <span data-ttu-id="6ea45-148">상속자</span><span class="sxs-lookup"><span data-stu-id="6ea45-148">NOTES</span></span>

## <span data-ttu-id="6ea45-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ea45-149">RELATED LINKS</span></span>
