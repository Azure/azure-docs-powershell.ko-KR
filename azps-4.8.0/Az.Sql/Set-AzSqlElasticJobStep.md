---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213878"
---
# <span data-ttu-id="8a6a1-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="8a6a1-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="8a6a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a6a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6a1-103">작업 단계 업데이트</span><span class="sxs-lookup"><span data-stu-id="8a6a1-103">Updates a job step</span></span>

## <span data-ttu-id="8a6a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a6a1-104">SYNTAX</span></span>

### <span data-ttu-id="8a6a1-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a6a1-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8a6a1-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="8a6a1-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-108">엔터티가</span><span class="sxs-lookup"><span data-stu-id="8a6a1-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8a6a1-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8a6a1-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8a6a1-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6a1-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6a1-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6a1-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6a1-114">설명은</span><span class="sxs-lookup"><span data-stu-id="8a6a1-114">DESCRIPTION</span></span>
<span data-ttu-id="8a6a1-115">Set-AzSqlElasticJobStep cmdlet은 작업 단계를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="8a6a1-116">예제의</span><span class="sxs-lookup"><span data-stu-id="8a6a1-116">EXAMPLES</span></span>

### <span data-ttu-id="8a6a1-117">예제 1: 작업 단계의 대상 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="8a6a1-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="8a6a1-118">예제 2: 작업 단계의 T-sql 스크립트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="8a6a1-119">작업에서 작업 단계 업데이트</span><span class="sxs-lookup"><span data-stu-id="8a6a1-119">Updates a job step from a job</span></span>

### <span data-ttu-id="8a6a1-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="8a6a1-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="8a6a1-121">변수</span><span class="sxs-lookup"><span data-stu-id="8a6a1-121">PARAMETERS</span></span>

### <span data-ttu-id="8a6a1-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-122">-AgentName</span></span>
<span data-ttu-id="8a6a1-123">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-123">The agent name</span></span>

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

### <span data-ttu-id="8a6a1-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="8a6a1-124">-CommandText</span></span>
<span data-ttu-id="8a6a1-125">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="8a6a1-125">The command text</span></span>

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

### <span data-ttu-id="8a6a1-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-126">-CredentialName</span></span>
<span data-ttu-id="8a6a1-127">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-127">The credential name</span></span>

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

### <span data-ttu-id="8a6a1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6a1-128">-DefaultProfile</span></span>
<span data-ttu-id="8a6a1-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6a1-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8a6a1-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="8a6a1-131">초기 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="8a6a1-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="8a6a1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a6a1-132">-InputObject</span></span>
<span data-ttu-id="8a6a1-133">작업 단계 개체</span><span class="sxs-lookup"><span data-stu-id="8a6a1-133">The job step object</span></span>

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

### <span data-ttu-id="8a6a1-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-134">-JobName</span></span>
<span data-ttu-id="8a6a1-135">작업 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-135">The job name</span></span>

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

### <span data-ttu-id="8a6a1-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8a6a1-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="8a6a1-137">최대 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="8a6a1-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="8a6a1-138">-이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-138">-Name</span></span>
<span data-ttu-id="8a6a1-139">단계 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-139">The step name</span></span>

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

### <span data-ttu-id="8a6a1-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-140">-OutputCredentialName</span></span>
<span data-ttu-id="8a6a1-141">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-141">The output credential name</span></span>

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

### <span data-ttu-id="8a6a1-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8a6a1-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="8a6a1-143">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="8a6a1-143">The output database object</span></span>

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

### <span data-ttu-id="8a6a1-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6a1-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="8a6a1-145">출력 데이터베이스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8a6a1-145">The output database resource id</span></span>

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

### <span data-ttu-id="8a6a1-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-146">-OutputSchemaName</span></span>
<span data-ttu-id="8a6a1-147">출력 스키마 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-147">The output schema name</span></span>

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

### <span data-ttu-id="8a6a1-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-148">-OutputTableName</span></span>
<span data-ttu-id="8a6a1-149">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-149">The output table name</span></span>

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

### <span data-ttu-id="8a6a1-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8a6a1-150">-RemoveOutput</span></span>
<span data-ttu-id="8a6a1-151">출력을 제거할지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="8a6a1-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-152">-ResourceGroupName</span></span>
<span data-ttu-id="8a6a1-153">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-153">The resource group name</span></span>

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

### <span data-ttu-id="8a6a1-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6a1-154">-ResourceId</span></span>
<span data-ttu-id="8a6a1-155">작업 단계 리소스 id</span><span class="sxs-lookup"><span data-stu-id="8a6a1-155">The job step resource id</span></span>

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

### <span data-ttu-id="8a6a1-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="8a6a1-156">-RetryAttempts</span></span>
<span data-ttu-id="8a6a1-157">다시 시도 attemps</span><span class="sxs-lookup"><span data-stu-id="8a6a1-157">The retry attemps</span></span>

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

### <span data-ttu-id="8a6a1-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="8a6a1-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="8a6a1-159">다시 시도 간격 backoff 승수</span><span class="sxs-lookup"><span data-stu-id="8a6a1-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="8a6a1-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-160">-ServerName</span></span>
<span data-ttu-id="8a6a1-161">서버 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-161">The server name</span></span>

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

### <span data-ttu-id="8a6a1-162">-Stid</span><span class="sxs-lookup"><span data-stu-id="8a6a1-162">-StepId</span></span>
<span data-ttu-id="8a6a1-163">단계 id 텍스트</span><span class="sxs-lookup"><span data-stu-id="8a6a1-163">The step id text</span></span>

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

### <span data-ttu-id="8a6a1-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6a1-164">-TargetGroupName</span></span>
<span data-ttu-id="8a6a1-165">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8a6a1-165">The target group name</span></span>

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

### <span data-ttu-id="8a6a1-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="8a6a1-166">-TimeoutSeconds</span></span>
<span data-ttu-id="8a6a1-167">시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="8a6a1-167">The timeout seconds</span></span>

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

### <span data-ttu-id="8a6a1-168">-확인</span><span class="sxs-lookup"><span data-stu-id="8a6a1-168">-Confirm</span></span>
<span data-ttu-id="8a6a1-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6a1-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6a1-170">-WhatIf</span></span>
<span data-ttu-id="8a6a1-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a6a1-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6a1-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6a1-173">CommonParameters</span></span>
<span data-ttu-id="8a6a1-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6a1-175">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a6a1-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6a1-176">입력</span><span class="sxs-lookup"><span data-stu-id="8a6a1-176">INPUTS</span></span>

### <span data-ttu-id="8a6a1-177">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="8a6a1-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8a6a1-178">출력</span><span class="sxs-lookup"><span data-stu-id="8a6a1-178">OUTPUTS</span></span>

### <span data-ttu-id="8a6a1-179">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="8a6a1-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8a6a1-180">상속자</span><span class="sxs-lookup"><span data-stu-id="8a6a1-180">NOTES</span></span>

## <span data-ttu-id="8a6a1-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a6a1-181">RELATED LINKS</span></span>
