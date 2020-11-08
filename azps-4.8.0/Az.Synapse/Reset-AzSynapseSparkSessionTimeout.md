---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: cccc0d3cffd9eb313e2983d81a3492bdf89e9e44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213462"
---
# <span data-ttu-id="26f7c-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="26f7c-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="26f7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="26f7c-103">Synapse Analytics Spark 세션의 시간 제한을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="26f7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26f7c-104">SYNTAX</span></span>

### <span data-ttu-id="26f7c-105">ResetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="26f7c-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f7c-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f7c-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26f7c-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26f7c-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26f7c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26f7c-108">DESCRIPTION</span></span>
<span data-ttu-id="26f7c-109">**AzSynapseSparkSessionTimeout** Cmdlet은 Synapse Analytics Spark 세션의 시간 제한을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="26f7c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="26f7c-110">EXAMPLES</span></span>

### <span data-ttu-id="26f7c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="26f7c-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="26f7c-112">이 명령은 지정 된 livy ID를 사용 하 여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="26f7c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="26f7c-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="26f7c-114">이 명령은 지정 된 livy ID를 통해 파이프라인을 사용 하 여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="26f7c-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="26f7c-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="26f7c-116">이 명령은 지정 된 livy ID를 통해 파이프라인을 사용 하 여 Synapse Analytics Spark 세션의 시간 제한을 다시 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="26f7c-117">변수</span><span class="sxs-lookup"><span data-stu-id="26f7c-117">PARAMETERS</span></span>

### <span data-ttu-id="26f7c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26f7c-118">-AsJob</span></span>
<span data-ttu-id="26f7c-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="26f7c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26f7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26f7c-120">-DefaultProfile</span></span>
<span data-ttu-id="26f7c-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26f7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26f7c-122">-InputObject</span></span>
<span data-ttu-id="26f7c-123">일반적으로 파이프라인을 통해 전달 되는 Spark 세션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-123">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="26f7c-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="26f7c-124">-LivyId</span></span>
<span data-ttu-id="26f7c-125">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="26f7c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26f7c-126">-PassThru</span></span>
<span data-ttu-id="26f7c-127">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="26f7c-128">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="26f7c-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="26f7c-129">-SparkPoolName</span></span>
<span data-ttu-id="26f7c-130">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="26f7c-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="26f7c-131">-SparkPoolObject</span></span>
<span data-ttu-id="26f7c-132">일반적으로 파이프라인을 통해 전달 되는 Spark 풀 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="26f7c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="26f7c-133">-WorkspaceName</span></span>
<span data-ttu-id="26f7c-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="26f7c-135">-확인</span><span class="sxs-lookup"><span data-stu-id="26f7c-135">-Confirm</span></span>
<span data-ttu-id="26f7c-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26f7c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26f7c-137">-WhatIf</span></span>
<span data-ttu-id="26f7c-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26f7c-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26f7c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26f7c-140">CommonParameters</span></span>
<span data-ttu-id="26f7c-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26f7c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26f7c-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26f7c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26f7c-143">입력</span><span class="sxs-lookup"><span data-stu-id="26f7c-143">INPUTS</span></span>

### <span data-ttu-id="26f7c-144">Synapse. PSSynapseSparkPool/.</span><span class="sxs-lookup"><span data-stu-id="26f7c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="26f7c-145">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="26f7c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="26f7c-146">출력</span><span class="sxs-lookup"><span data-stu-id="26f7c-146">OUTPUTS</span></span>

### <span data-ttu-id="26f7c-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="26f7c-147">System.Boolean</span></span>

## <span data-ttu-id="26f7c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="26f7c-148">NOTES</span></span>

## <span data-ttu-id="26f7c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26f7c-149">RELATED LINKS</span></span>
