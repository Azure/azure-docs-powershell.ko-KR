---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: f39554dacdaabfc42fe44d55a7f3034c1c8b54df
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878978"
---
# <span data-ttu-id="5526b-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="5526b-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="5526b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5526b-102">SYNOPSIS</span></span>
<span data-ttu-id="5526b-103">작업 단계 업데이트</span><span class="sxs-lookup"><span data-stu-id="5526b-103">Updates a job step</span></span>

## <span data-ttu-id="5526b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5526b-104">SYNTAX</span></span>

### <span data-ttu-id="5526b-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="5526b-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5526b-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5526b-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5526b-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="5526b-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5526b-108">엔터티가</span><span class="sxs-lookup"><span data-stu-id="5526b-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5526b-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5526b-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5526b-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5526b-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5526b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5526b-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5526b-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5526b-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5526b-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5526b-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5526b-114">설명은</span><span class="sxs-lookup"><span data-stu-id="5526b-114">DESCRIPTION</span></span>
<span data-ttu-id="5526b-115">Set-AzSqlElasticJobStep cmdlet은 작업 단계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="5526b-116">예제의</span><span class="sxs-lookup"><span data-stu-id="5526b-116">EXAMPLES</span></span>

### <span data-ttu-id="5526b-117">예제 1-작업 단계의 대상 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="5526b-117">Example 1 - Updates a job step's target group for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="5526b-118">예제 2-작업 단계의 T-sql 스크립트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-118">Example 2 - Updates a job step's T-SQL script for a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="5526b-119">작업에서 작업 단계 업데이트</span><span class="sxs-lookup"><span data-stu-id="5526b-119">Updates a job step from a job</span></span>

## <span data-ttu-id="5526b-120">변수</span><span class="sxs-lookup"><span data-stu-id="5526b-120">PARAMETERS</span></span>

### <span data-ttu-id="5526b-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5526b-121">-AgentName</span></span>
<span data-ttu-id="5526b-122">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-123">-CommandText</span><span class="sxs-lookup"><span data-stu-id="5526b-123">-CommandText</span></span>
<span data-ttu-id="5526b-124">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="5526b-124">The command text</span></span>

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

### <span data-ttu-id="5526b-125">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="5526b-125">-CredentialName</span></span>
<span data-ttu-id="5526b-126">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-126">The credential name</span></span>

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

### <span data-ttu-id="5526b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5526b-127">-DefaultProfile</span></span>
<span data-ttu-id="5526b-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5526b-129">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5526b-129">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="5526b-130">초기 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="5526b-130">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5526b-131">-InputObject</span></span>
<span data-ttu-id="5526b-132">작업 단계 개체</span><span class="sxs-lookup"><span data-stu-id="5526b-132">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="5526b-133">-JobName</span></span>
<span data-ttu-id="5526b-134">작업 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-134">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-135">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5526b-135">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="5526b-136">최대 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="5526b-136">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-137">-이름</span><span class="sxs-lookup"><span data-stu-id="5526b-137">-Name</span></span>
<span data-ttu-id="5526b-138">단계 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-138">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-139">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="5526b-139">-OutputCredentialName</span></span>
<span data-ttu-id="5526b-140">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-140">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-141">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="5526b-141">-OutputDatabaseObject</span></span>
<span data-ttu-id="5526b-142">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="5526b-142">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-143">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="5526b-143">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="5526b-144">출력 데이터베이스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="5526b-144">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-145">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="5526b-145">-OutputSchemaName</span></span>
<span data-ttu-id="5526b-146">출력 스키마 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-146">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-147">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="5526b-147">-OutputTableName</span></span>
<span data-ttu-id="5526b-148">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-148">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-149">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="5526b-149">-RemoveOutput</span></span>
<span data-ttu-id="5526b-150">출력을 제거할지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-150">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5526b-151">-ResourceGroupName</span></span>
<span data-ttu-id="5526b-152">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-152">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5526b-153">-ResourceId</span></span>
<span data-ttu-id="5526b-154">작업 단계 리소스 id</span><span class="sxs-lookup"><span data-stu-id="5526b-154">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-155">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="5526b-155">-RetryAttempts</span></span>
<span data-ttu-id="5526b-156">다시 시도 attemps</span><span class="sxs-lookup"><span data-stu-id="5526b-156">The retry attemps</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-157">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="5526b-157">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="5526b-158">다시 시도 간격 backoff 승수</span><span class="sxs-lookup"><span data-stu-id="5526b-158">The retry interval backoff multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-159">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5526b-159">-ServerName</span></span>
<span data-ttu-id="5526b-160">서버 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-160">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-161">-Stid</span><span class="sxs-lookup"><span data-stu-id="5526b-161">-StepId</span></span>
<span data-ttu-id="5526b-162">단계 id 텍스트</span><span class="sxs-lookup"><span data-stu-id="5526b-162">The step id text</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-163">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="5526b-163">-TargetGroupName</span></span>
<span data-ttu-id="5526b-164">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5526b-164">The target group name</span></span>

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

### <span data-ttu-id="5526b-165">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="5526b-165">-TimeoutSeconds</span></span>
<span data-ttu-id="5526b-166">시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="5526b-166">The timeout seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-167">-확인</span><span class="sxs-lookup"><span data-stu-id="5526b-167">-Confirm</span></span>
<span data-ttu-id="5526b-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5526b-169">-WhatIf</span></span>
<span data-ttu-id="5526b-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5526b-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-171">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5526b-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5526b-172">CommonParameters</span></span>
<span data-ttu-id="5526b-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5526b-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5526b-174">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5526b-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5526b-175">입력</span><span class="sxs-lookup"><span data-stu-id="5526b-175">INPUTS</span></span>

### <span data-ttu-id="5526b-176">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5526b-176">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5526b-177">출력</span><span class="sxs-lookup"><span data-stu-id="5526b-177">OUTPUTS</span></span>

### <span data-ttu-id="5526b-178">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="5526b-178">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="5526b-179">상속자</span><span class="sxs-lookup"><span data-stu-id="5526b-179">NOTES</span></span>

## <span data-ttu-id="5526b-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5526b-180">RELATED LINKS</span></span>
