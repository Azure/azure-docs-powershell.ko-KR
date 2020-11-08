---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216609"
---
# <span data-ttu-id="79a49-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="79a49-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="79a49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a49-102">SYNOPSIS</span></span>
<span data-ttu-id="79a49-103">Synapse Analytics Spark 문을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="79a49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79a49-104">SYNTAX</span></span>

### <span data-ttu-id="79a49-105">RunSparkStatementByCodePathParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="79a49-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a49-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a49-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a49-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a49-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a49-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a49-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79a49-109">설명은</span><span class="sxs-lookup"><span data-stu-id="79a49-109">DESCRIPTION</span></span>
<span data-ttu-id="79a49-110">**AzSynapseSparkStatement** Cmdlet은 Synapse Analytics Spark 문을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="79a49-111">예제의</span><span class="sxs-lookup"><span data-stu-id="79a49-111">EXAMPLES</span></span>

### <span data-ttu-id="79a49-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="79a49-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="79a49-113">이러한 명령은 Spark 세션을 시작 하 고 파이프라인을 통해 인라인 Spark 문을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="79a49-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="79a49-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="79a49-115">이러한 명령은 Spark 세션을 시작한 다음 인라인 Spark 문을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="79a49-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="79a49-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="79a49-117">이러한 명령은 Spark 세션을 시작한 다음 파일에서 Spark 문을 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="79a49-118">변수</span><span class="sxs-lookup"><span data-stu-id="79a49-118">PARAMETERS</span></span>

### <span data-ttu-id="79a49-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a49-119">-AsJob</span></span>
<span data-ttu-id="79a49-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="79a49-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79a49-121">-코드</span><span class="sxs-lookup"><span data-stu-id="79a49-121">-Code</span></span>
<span data-ttu-id="79a49-122">실행 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-122">The execution code.</span></span>

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

### <span data-ttu-id="79a49-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a49-123">-DefaultProfile</span></span>
<span data-ttu-id="79a49-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a49-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="79a49-125">-FilePath</span></span>
<span data-ttu-id="79a49-126">실행 코드를 포함 하는 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="79a49-127">-언어</span><span class="sxs-lookup"><span data-stu-id="79a49-127">-Language</span></span>
<span data-ttu-id="79a49-128">실행 코드의 언어입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="79a49-129">-응답</span><span class="sxs-lookup"><span data-stu-id="79a49-129">-Response</span></span>
<span data-ttu-id="79a49-130">전체 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="79a49-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="79a49-131">-SessionId</span></span>
<span data-ttu-id="79a49-132">Spark 세션의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="79a49-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="79a49-133">-SessionObject</span></span>
<span data-ttu-id="79a49-134">일반적으로 파이프라인을 통해 전달 되는 Spark 세션 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="79a49-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="79a49-135">-SparkPoolName</span></span>
<span data-ttu-id="79a49-136">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="79a49-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79a49-137">-WorkspaceName</span></span>
<span data-ttu-id="79a49-138">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="79a49-139">-확인</span><span class="sxs-lookup"><span data-stu-id="79a49-139">-Confirm</span></span>
<span data-ttu-id="79a49-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a49-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a49-141">-WhatIf</span></span>
<span data-ttu-id="79a49-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79a49-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a49-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a49-144">CommonParameters</span></span>
<span data-ttu-id="79a49-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a49-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a49-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79a49-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a49-147">입력</span><span class="sxs-lookup"><span data-stu-id="79a49-147">INPUTS</span></span>

### <span data-ttu-id="79a49-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79a49-148">System.String</span></span>

### <span data-ttu-id="79a49-149">Synapse. PSSynapseSparkSession/.</span><span class="sxs-lookup"><span data-stu-id="79a49-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="79a49-150">출력</span><span class="sxs-lookup"><span data-stu-id="79a49-150">OUTPUTS</span></span>

### <span data-ttu-id="79a49-151">Synapse. PSSynapseExtendedSparkStatement/.</span><span class="sxs-lookup"><span data-stu-id="79a49-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="79a49-152">상속자</span><span class="sxs-lookup"><span data-stu-id="79a49-152">NOTES</span></span>

## <span data-ttu-id="79a49-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79a49-153">RELATED LINKS</span></span>
