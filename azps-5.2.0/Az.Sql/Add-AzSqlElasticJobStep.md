---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332433"
---
# <span data-ttu-id="2e751-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2e751-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2e751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e751-102">SYNOPSIS</span></span>
<span data-ttu-id="2e751-103">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e751-103">Adds a job step to a job</span></span>

## <span data-ttu-id="2e751-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e751-104">SYNTAX</span></span>

### <span data-ttu-id="2e751-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2e751-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e751-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="2e751-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e751-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="2e751-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e751-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2e751-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e751-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e751-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e751-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e751-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e751-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2e751-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e751-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e751-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e751-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e751-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e751-114">설명</span><span class="sxs-lookup"><span data-stu-id="2e751-114">DESCRIPTION</span></span>
<span data-ttu-id="2e751-115">Add-AzSqlElasticJobStep cmdlet은 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e751-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="2e751-116">예제</span><span class="sxs-lookup"><span data-stu-id="2e751-116">EXAMPLES</span></span>

### <span data-ttu-id="2e751-117">예제 1: 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e751-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="2e751-118">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e751-118">Adds a job step to a job</span></span>

## <span data-ttu-id="2e751-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e751-119">PARAMETERS</span></span>

### <span data-ttu-id="2e751-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2e751-120">-AgentName</span></span>
<span data-ttu-id="2e751-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="2e751-122">-CommandText</span></span>
<span data-ttu-id="2e751-123">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="2e751-123">The command text</span></span>

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

### <span data-ttu-id="2e751-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2e751-124">-CredentialName</span></span>
<span data-ttu-id="2e751-125">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-125">The credential name</span></span>

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

### <span data-ttu-id="2e751-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e751-126">-DefaultProfile</span></span>
<span data-ttu-id="2e751-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e751-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e751-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2e751-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="2e751-129">초기 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="2e751-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="2e751-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="2e751-130">-JobName</span></span>
<span data-ttu-id="2e751-131">작업 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2e751-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="2e751-133">최대 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="2e751-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="2e751-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2e751-134">-Name</span></span>
<span data-ttu-id="2e751-135">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="2e751-136">-OutputCredentialName</span></span>
<span data-ttu-id="2e751-137">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2e751-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="2e751-139">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="2e751-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="2e751-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="2e751-141">출력 데이터베이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2e751-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="2e751-142">-OutputSchemaName</span></span>
<span data-ttu-id="2e751-143">출력 스마마 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="2e751-144">-OutputTableName</span></span>
<span data-ttu-id="2e751-145">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e751-146">-ParentObject</span></span>
<span data-ttu-id="2e751-147">작업 개체</span><span class="sxs-lookup"><span data-stu-id="2e751-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e751-148">-ParentResourceId</span></span>
<span data-ttu-id="2e751-149">작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2e751-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e751-150">-ResourceGroupName</span></span>
<span data-ttu-id="2e751-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="2e751-152">-RetryAttempts</span></span>
<span data-ttu-id="2e751-153">재시도</span><span class="sxs-lookup"><span data-stu-id="2e751-153">The retry attempts</span></span>

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

### <span data-ttu-id="2e751-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="2e751-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="2e751-155">재시도 간격 백오프 승수</span><span class="sxs-lookup"><span data-stu-id="2e751-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="2e751-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e751-156">-ServerName</span></span>
<span data-ttu-id="2e751-157">서버 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="2e751-158">-StepId</span></span>
<span data-ttu-id="2e751-159">단계 ID</span><span class="sxs-lookup"><span data-stu-id="2e751-159">The step id</span></span>

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

### <span data-ttu-id="2e751-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="2e751-160">-TargetGroupName</span></span>
<span data-ttu-id="2e751-161">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e751-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e751-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="2e751-162">-TimeoutSeconds</span></span>
<span data-ttu-id="2e751-163">시간 시간(초)</span><span class="sxs-lookup"><span data-stu-id="2e751-163">The time out seconds</span></span>

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

### <span data-ttu-id="2e751-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e751-164">-Confirm</span></span>
<span data-ttu-id="2e751-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e751-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e751-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e751-166">-WhatIf</span></span>
<span data-ttu-id="2e751-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2e751-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e751-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e751-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e751-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e751-169">CommonParameters</span></span>
<span data-ttu-id="2e751-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e751-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e751-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e751-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e751-172">입력</span><span class="sxs-lookup"><span data-stu-id="2e751-172">INPUTS</span></span>

### <span data-ttu-id="2e751-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="2e751-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2e751-174">출력</span><span class="sxs-lookup"><span data-stu-id="2e751-174">OUTPUTS</span></span>

### <span data-ttu-id="2e751-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="2e751-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2e751-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e751-176">NOTES</span></span>

## <span data-ttu-id="2e751-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e751-177">RELATED LINKS</span></span>
