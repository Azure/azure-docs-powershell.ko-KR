---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383657"
---
# <span data-ttu-id="b9c67-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b9c67-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="b9c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c67-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c67-103">Synapse Analytics Spark 문을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b9c67-104">구문</span><span class="sxs-lookup"><span data-stu-id="b9c67-104">SYNTAX</span></span>

### <span data-ttu-id="b9c67-105">RunSparkStatementByCodePathParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b9c67-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c67-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c67-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9c67-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c67-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c67-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9c67-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b9c67-109">설명</span><span class="sxs-lookup"><span data-stu-id="b9c67-109">DESCRIPTION</span></span>
<span data-ttu-id="b9c67-110">**Invoke-AzSynapseSparkStatement** cmdlet은 Synapse Analytics Spark 문을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b9c67-111">예제</span><span class="sxs-lookup"><span data-stu-id="b9c67-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c67-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9c67-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="b9c67-113">이러한 명령은 Spark 세션을 시작한 다음 파이프라인을 통해 인라인 Spark 문을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="b9c67-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9c67-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="b9c67-115">이러한 명령은 Spark 세션을 시작한 다음, 인라인 Spark 문을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="b9c67-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="b9c67-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="b9c67-117">이러한 명령은 Spark 세션을 시작한 다음 파일에서 Spark 문을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="b9c67-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9c67-118">PARAMETERS</span></span>

### <span data-ttu-id="b9c67-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9c67-119">-AsJob</span></span>
<span data-ttu-id="b9c67-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b9c67-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9c67-121">-Code</span><span class="sxs-lookup"><span data-stu-id="b9c67-121">-Code</span></span>
<span data-ttu-id="b9c67-122">실행 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c67-123">-DefaultProfile</span></span>
<span data-ttu-id="b9c67-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c67-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b9c67-125">-FilePath</span></span>
<span data-ttu-id="b9c67-126">실행 코드를 포함하는 로컬 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-127">-Language</span><span class="sxs-lookup"><span data-stu-id="b9c67-127">-Language</span></span>
<span data-ttu-id="b9c67-128">실행 코드의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-129">-Response</span><span class="sxs-lookup"><span data-stu-id="b9c67-129">-Response</span></span>
<span data-ttu-id="b9c67-130">전체 응답이 반환될 것임을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="b9c67-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="b9c67-131">-SessionId</span></span>
<span data-ttu-id="b9c67-132">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="b9c67-133">-SessionObject</span></span>
<span data-ttu-id="b9c67-134">Spark 세션 입력 개체로, 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b9c67-135">-SparkPoolName</span></span>
<span data-ttu-id="b9c67-136">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9c67-137">-WorkspaceName</span></span>
<span data-ttu-id="b9c67-138">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9c67-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9c67-139">-Confirm</span></span>
<span data-ttu-id="b9c67-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9c67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9c67-141">-WhatIf</span></span>
<span data-ttu-id="b9c67-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b9c67-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b9c67-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9c67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c67-144">CommonParameters</span></span>
<span data-ttu-id="b9c67-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c67-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b9c67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c67-147">입력</span><span class="sxs-lookup"><span data-stu-id="b9c67-147">INPUTS</span></span>

### <span data-ttu-id="b9c67-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b9c67-148">System.String</span></span>

### <span data-ttu-id="b9c67-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="b9c67-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="b9c67-150">출력</span><span class="sxs-lookup"><span data-stu-id="b9c67-150">OUTPUTS</span></span>

### <span data-ttu-id="b9c67-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b9c67-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="b9c67-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b9c67-152">NOTES</span></span>

## <span data-ttu-id="b9c67-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c67-153">RELATED LINKS</span></span>
