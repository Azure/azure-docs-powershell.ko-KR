---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961536"
---
# <span data-ttu-id="fdfe1-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="fdfe1-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="fdfe1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdfe1-102">SYNOPSIS</span></span>
<span data-ttu-id="fdfe1-103">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="fdfe1-103">Adds a job step to a job</span></span>

## <span data-ttu-id="fdfe1-104">구문</span><span class="sxs-lookup"><span data-stu-id="fdfe1-104">SYNTAX</span></span>

### <span data-ttu-id="fdfe1-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="fdfe1-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="fdfe1-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="fdfe1-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fdfe1-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="fdfe1-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fdfe1-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdfe1-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdfe1-114">설명</span><span class="sxs-lookup"><span data-stu-id="fdfe1-114">DESCRIPTION</span></span>
<span data-ttu-id="fdfe1-115">Add-AzSqlElasticJobStep cmdlet은 작업 단계를 작업 단계에 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="fdfe1-116">예제</span><span class="sxs-lookup"><span data-stu-id="fdfe1-116">EXAMPLES</span></span>

### <span data-ttu-id="fdfe1-117">예제 1: 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="fdfe1-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="fdfe1-118">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="fdfe1-118">Adds a job step to a job</span></span>

## <span data-ttu-id="fdfe1-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fdfe1-119">PARAMETERS</span></span>

### <span data-ttu-id="fdfe1-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-120">-AgentName</span></span>
<span data-ttu-id="fdfe1-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-121">The agent name</span></span>

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

### <span data-ttu-id="fdfe1-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="fdfe1-122">-CommandText</span></span>
<span data-ttu-id="fdfe1-123">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="fdfe1-123">The command text</span></span>

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

### <span data-ttu-id="fdfe1-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-124">-CredentialName</span></span>
<span data-ttu-id="fdfe1-125">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-125">The credential name</span></span>

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

### <span data-ttu-id="fdfe1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdfe1-126">-DefaultProfile</span></span>
<span data-ttu-id="fdfe1-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdfe1-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fdfe1-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="fdfe1-129">초기 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="fdfe1-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="fdfe1-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-130">-JobName</span></span>
<span data-ttu-id="fdfe1-131">작업 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-131">The job name</span></span>

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

### <span data-ttu-id="fdfe1-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="fdfe1-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="fdfe1-133">최대 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="fdfe1-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="fdfe1-134">-Name</span><span class="sxs-lookup"><span data-stu-id="fdfe1-134">-Name</span></span>
<span data-ttu-id="fdfe1-135">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-135">The job step name</span></span>

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

### <span data-ttu-id="fdfe1-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-136">-OutputCredentialName</span></span>
<span data-ttu-id="fdfe1-137">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-137">The output credential name</span></span>

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

### <span data-ttu-id="fdfe1-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="fdfe1-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="fdfe1-139">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="fdfe1-139">The output database object</span></span>

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

### <span data-ttu-id="fdfe1-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="fdfe1-141">출력 데이터베이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fdfe1-141">The output database resource id</span></span>

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

### <span data-ttu-id="fdfe1-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-142">-OutputSchemaName</span></span>
<span data-ttu-id="fdfe1-143">출력척도 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-143">The output schema name</span></span>

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

### <span data-ttu-id="fdfe1-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-144">-OutputTableName</span></span>
<span data-ttu-id="fdfe1-145">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-145">The output table name</span></span>

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

### <span data-ttu-id="fdfe1-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fdfe1-146">-ParentObject</span></span>
<span data-ttu-id="fdfe1-147">작업 개체</span><span class="sxs-lookup"><span data-stu-id="fdfe1-147">The job object</span></span>

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

### <span data-ttu-id="fdfe1-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-148">-ParentResourceId</span></span>
<span data-ttu-id="fdfe1-149">작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fdfe1-149">The job resource id</span></span>

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

### <span data-ttu-id="fdfe1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-150">-ResourceGroupName</span></span>
<span data-ttu-id="fdfe1-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-151">The resource group name</span></span>

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

### <span data-ttu-id="fdfe1-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="fdfe1-152">-RetryAttempts</span></span>
<span data-ttu-id="fdfe1-153">재시도 시도</span><span class="sxs-lookup"><span data-stu-id="fdfe1-153">The retry attempts</span></span>

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

### <span data-ttu-id="fdfe1-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="fdfe1-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="fdfe1-155">다시 시도 간격 다시 곱하기</span><span class="sxs-lookup"><span data-stu-id="fdfe1-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="fdfe1-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-156">-ServerName</span></span>
<span data-ttu-id="fdfe1-157">서버 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-157">The server name</span></span>

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

### <span data-ttu-id="fdfe1-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="fdfe1-158">-StepId</span></span>
<span data-ttu-id="fdfe1-159">단계 ID</span><span class="sxs-lookup"><span data-stu-id="fdfe1-159">The step id</span></span>

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

### <span data-ttu-id="fdfe1-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="fdfe1-160">-TargetGroupName</span></span>
<span data-ttu-id="fdfe1-161">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fdfe1-161">The target group name</span></span>

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

### <span data-ttu-id="fdfe1-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="fdfe1-162">-TimeoutSeconds</span></span>
<span data-ttu-id="fdfe1-163">시간 시간(초)</span><span class="sxs-lookup"><span data-stu-id="fdfe1-163">The time out seconds</span></span>

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

### <span data-ttu-id="fdfe1-164">-확인</span><span class="sxs-lookup"><span data-stu-id="fdfe1-164">-Confirm</span></span>
<span data-ttu-id="fdfe1-165">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdfe1-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdfe1-166">-WhatIf</span></span>
<span data-ttu-id="fdfe1-167">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdfe1-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdfe1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdfe1-169">CommonParameters</span></span>
<span data-ttu-id="fdfe1-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fdfe1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdfe1-171">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdfe1-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdfe1-172">입력</span><span class="sxs-lookup"><span data-stu-id="fdfe1-172">INPUTS</span></span>

### <span data-ttu-id="fdfe1-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="fdfe1-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="fdfe1-174">출력</span><span class="sxs-lookup"><span data-stu-id="fdfe1-174">OUTPUTS</span></span>

### <span data-ttu-id="fdfe1-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="fdfe1-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="fdfe1-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fdfe1-176">NOTES</span></span>

## <span data-ttu-id="fdfe1-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdfe1-177">RELATED LINKS</span></span>
