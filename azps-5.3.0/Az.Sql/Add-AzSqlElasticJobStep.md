---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375600"
---
# <span data-ttu-id="81672-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="81672-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="81672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81672-102">SYNOPSIS</span></span>
<span data-ttu-id="81672-103">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="81672-103">Adds a job step to a job</span></span>

## <span data-ttu-id="81672-104">구문</span><span class="sxs-lookup"><span data-stu-id="81672-104">SYNTAX</span></span>

### <span data-ttu-id="81672-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="81672-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81672-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="81672-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81672-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="81672-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81672-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="81672-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81672-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="81672-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81672-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="81672-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81672-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="81672-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81672-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="81672-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="81672-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="81672-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81672-114">설명</span><span class="sxs-lookup"><span data-stu-id="81672-114">DESCRIPTION</span></span>
<span data-ttu-id="81672-115">Add-AzSqlElasticJobStep cmdlet은 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="81672-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="81672-116">예제</span><span class="sxs-lookup"><span data-stu-id="81672-116">EXAMPLES</span></span>

### <span data-ttu-id="81672-117">예제 1: 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="81672-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="81672-118">작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="81672-118">Adds a job step to a job</span></span>

## <span data-ttu-id="81672-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81672-119">PARAMETERS</span></span>

### <span data-ttu-id="81672-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="81672-120">-AgentName</span></span>
<span data-ttu-id="81672-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="81672-121">The agent name</span></span>

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

### <span data-ttu-id="81672-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="81672-122">-CommandText</span></span>
<span data-ttu-id="81672-123">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="81672-123">The command text</span></span>

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

### <span data-ttu-id="81672-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="81672-124">-CredentialName</span></span>
<span data-ttu-id="81672-125">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="81672-125">The credential name</span></span>

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

### <span data-ttu-id="81672-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81672-126">-DefaultProfile</span></span>
<span data-ttu-id="81672-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81672-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81672-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="81672-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="81672-129">초기 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="81672-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="81672-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="81672-130">-JobName</span></span>
<span data-ttu-id="81672-131">작업 이름</span><span class="sxs-lookup"><span data-stu-id="81672-131">The job name</span></span>

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

### <span data-ttu-id="81672-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="81672-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="81672-133">최대 재시도 간격 초</span><span class="sxs-lookup"><span data-stu-id="81672-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="81672-134">-Name</span><span class="sxs-lookup"><span data-stu-id="81672-134">-Name</span></span>
<span data-ttu-id="81672-135">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="81672-135">The job step name</span></span>

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

### <span data-ttu-id="81672-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="81672-136">-OutputCredentialName</span></span>
<span data-ttu-id="81672-137">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="81672-137">The output credential name</span></span>

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

### <span data-ttu-id="81672-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="81672-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="81672-139">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="81672-139">The output database object</span></span>

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

### <span data-ttu-id="81672-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="81672-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="81672-141">출력 데이터베이스 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="81672-141">The output database resource id</span></span>

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

### <span data-ttu-id="81672-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="81672-142">-OutputSchemaName</span></span>
<span data-ttu-id="81672-143">출력 스마마 이름</span><span class="sxs-lookup"><span data-stu-id="81672-143">The output schema name</span></span>

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

### <span data-ttu-id="81672-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="81672-144">-OutputTableName</span></span>
<span data-ttu-id="81672-145">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="81672-145">The output table name</span></span>

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

### <span data-ttu-id="81672-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="81672-146">-ParentObject</span></span>
<span data-ttu-id="81672-147">작업 개체</span><span class="sxs-lookup"><span data-stu-id="81672-147">The job object</span></span>

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

### <span data-ttu-id="81672-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="81672-148">-ParentResourceId</span></span>
<span data-ttu-id="81672-149">작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="81672-149">The job resource id</span></span>

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

### <span data-ttu-id="81672-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81672-150">-ResourceGroupName</span></span>
<span data-ttu-id="81672-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="81672-151">The resource group name</span></span>

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

### <span data-ttu-id="81672-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="81672-152">-RetryAttempts</span></span>
<span data-ttu-id="81672-153">재시도</span><span class="sxs-lookup"><span data-stu-id="81672-153">The retry attempts</span></span>

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

### <span data-ttu-id="81672-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="81672-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="81672-155">재시도 간격 백오프 승수</span><span class="sxs-lookup"><span data-stu-id="81672-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="81672-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81672-156">-ServerName</span></span>
<span data-ttu-id="81672-157">서버 이름</span><span class="sxs-lookup"><span data-stu-id="81672-157">The server name</span></span>

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

### <span data-ttu-id="81672-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="81672-158">-StepId</span></span>
<span data-ttu-id="81672-159">단계 ID</span><span class="sxs-lookup"><span data-stu-id="81672-159">The step id</span></span>

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

### <span data-ttu-id="81672-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="81672-160">-TargetGroupName</span></span>
<span data-ttu-id="81672-161">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="81672-161">The target group name</span></span>

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

### <span data-ttu-id="81672-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="81672-162">-TimeoutSeconds</span></span>
<span data-ttu-id="81672-163">시간 시간(초)</span><span class="sxs-lookup"><span data-stu-id="81672-163">The time out seconds</span></span>

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

### <span data-ttu-id="81672-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="81672-164">-Confirm</span></span>
<span data-ttu-id="81672-165">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="81672-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81672-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81672-166">-WhatIf</span></span>
<span data-ttu-id="81672-167">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="81672-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81672-168">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="81672-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81672-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81672-169">CommonParameters</span></span>
<span data-ttu-id="81672-170">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81672-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81672-171">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="81672-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81672-172">입력</span><span class="sxs-lookup"><span data-stu-id="81672-172">INPUTS</span></span>

### <span data-ttu-id="81672-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="81672-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="81672-174">출력</span><span class="sxs-lookup"><span data-stu-id="81672-174">OUTPUTS</span></span>

### <span data-ttu-id="81672-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="81672-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="81672-176">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81672-176">NOTES</span></span>

## <span data-ttu-id="81672-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81672-177">RELATED LINKS</span></span>
