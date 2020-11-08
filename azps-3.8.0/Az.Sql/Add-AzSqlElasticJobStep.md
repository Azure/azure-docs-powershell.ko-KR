---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034736"
---
# <span data-ttu-id="2e64f-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="2e64f-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="2e64f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e64f-102">SYNOPSIS</span></span>
<span data-ttu-id="2e64f-103">작업에 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e64f-103">Adds a job step to a job</span></span>

## <span data-ttu-id="2e64f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e64f-104">SYNTAX</span></span>

### <span data-ttu-id="2e64f-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e64f-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e64f-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="2e64f-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e64f-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="2e64f-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e64f-108">엔터티가</span><span class="sxs-lookup"><span data-stu-id="2e64f-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e64f-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e64f-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e64f-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2e64f-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e64f-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2e64f-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2e64f-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e64f-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e64f-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e64f-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e64f-114">설명은</span><span class="sxs-lookup"><span data-stu-id="2e64f-114">DESCRIPTION</span></span>
<span data-ttu-id="2e64f-115">Add-AzSqlElasticJobStep cmdlet은 작업에 작업 단계를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="2e64f-116">예제의</span><span class="sxs-lookup"><span data-stu-id="2e64f-116">EXAMPLES</span></span>

### <span data-ttu-id="2e64f-117">예제 1-작업에 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e64f-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="2e64f-118">작업에 작업 단계 추가</span><span class="sxs-lookup"><span data-stu-id="2e64f-118">Adds a job step to a job</span></span>

## <span data-ttu-id="2e64f-119">변수</span><span class="sxs-lookup"><span data-stu-id="2e64f-119">PARAMETERS</span></span>

### <span data-ttu-id="2e64f-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2e64f-120">-AgentName</span></span>
<span data-ttu-id="2e64f-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-121">The agent name</span></span>

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

### <span data-ttu-id="2e64f-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="2e64f-122">-CommandText</span></span>
<span data-ttu-id="2e64f-123">명령 텍스트</span><span class="sxs-lookup"><span data-stu-id="2e64f-123">The command text</span></span>

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

### <span data-ttu-id="2e64f-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="2e64f-124">-CredentialName</span></span>
<span data-ttu-id="2e64f-125">자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-125">The credential name</span></span>

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

### <span data-ttu-id="2e64f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e64f-126">-DefaultProfile</span></span>
<span data-ttu-id="2e64f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e64f-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2e64f-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="2e64f-129">초기 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="2e64f-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="2e64f-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="2e64f-130">-JobName</span></span>
<span data-ttu-id="2e64f-131">작업 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-131">The job name</span></span>

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

### <span data-ttu-id="2e64f-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="2e64f-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="2e64f-133">최대 다시 시도 간격 (초)</span><span class="sxs-lookup"><span data-stu-id="2e64f-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="2e64f-134">-이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-134">-Name</span></span>
<span data-ttu-id="2e64f-135">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-135">The job step name</span></span>

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

### <span data-ttu-id="2e64f-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="2e64f-136">-OutputCredentialName</span></span>
<span data-ttu-id="2e64f-137">출력 자격 증명 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-137">The output credential name</span></span>

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

### <span data-ttu-id="2e64f-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="2e64f-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="2e64f-139">출력 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="2e64f-139">The output database object</span></span>

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

### <span data-ttu-id="2e64f-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="2e64f-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="2e64f-141">출력 데이터베이스 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2e64f-141">The output database resource id</span></span>

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

### <span data-ttu-id="2e64f-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="2e64f-142">-OutputSchemaName</span></span>
<span data-ttu-id="2e64f-143">출력 스키마 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-143">The output schema name</span></span>

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

### <span data-ttu-id="2e64f-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="2e64f-144">-OutputTableName</span></span>
<span data-ttu-id="2e64f-145">출력 테이블 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-145">The output table name</span></span>

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

### <span data-ttu-id="2e64f-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2e64f-146">-ParentObject</span></span>
<span data-ttu-id="2e64f-147">작업 개체</span><span class="sxs-lookup"><span data-stu-id="2e64f-147">The job object</span></span>

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

### <span data-ttu-id="2e64f-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2e64f-148">-ParentResourceId</span></span>
<span data-ttu-id="2e64f-149">작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="2e64f-149">The job resource id</span></span>

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

### <span data-ttu-id="2e64f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e64f-150">-ResourceGroupName</span></span>
<span data-ttu-id="2e64f-151">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-151">The resource group name</span></span>

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

### <span data-ttu-id="2e64f-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="2e64f-152">-RetryAttempts</span></span>
<span data-ttu-id="2e64f-153">다시 시도 횟수</span><span class="sxs-lookup"><span data-stu-id="2e64f-153">The retry attempts</span></span>

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

### <span data-ttu-id="2e64f-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="2e64f-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="2e64f-155">다시 시도 간격 다시 승수</span><span class="sxs-lookup"><span data-stu-id="2e64f-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="2e64f-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2e64f-156">-ServerName</span></span>
<span data-ttu-id="2e64f-157">서버 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-157">The server name</span></span>

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

### <span data-ttu-id="2e64f-158">-Stid</span><span class="sxs-lookup"><span data-stu-id="2e64f-158">-StepId</span></span>
<span data-ttu-id="2e64f-159">단계 id</span><span class="sxs-lookup"><span data-stu-id="2e64f-159">The step id</span></span>

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

### <span data-ttu-id="2e64f-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="2e64f-160">-TargetGroupName</span></span>
<span data-ttu-id="2e64f-161">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e64f-161">The target group name</span></span>

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

### <span data-ttu-id="2e64f-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="2e64f-162">-TimeoutSeconds</span></span>
<span data-ttu-id="2e64f-163">시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="2e64f-163">The time out seconds</span></span>

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

### <span data-ttu-id="2e64f-164">-확인</span><span class="sxs-lookup"><span data-stu-id="2e64f-164">-Confirm</span></span>
<span data-ttu-id="2e64f-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e64f-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e64f-166">-WhatIf</span></span>
<span data-ttu-id="2e64f-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e64f-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e64f-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e64f-169">CommonParameters</span></span>
<span data-ttu-id="2e64f-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e64f-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e64f-171">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e64f-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e64f-172">입력</span><span class="sxs-lookup"><span data-stu-id="2e64f-172">INPUTS</span></span>

### <span data-ttu-id="2e64f-173">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="2e64f-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="2e64f-174">출력</span><span class="sxs-lookup"><span data-stu-id="2e64f-174">OUTPUTS</span></span>

### <span data-ttu-id="2e64f-175">ElasticJobs. AzureSqlElasticJobStepModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="2e64f-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="2e64f-176">상속자</span><span class="sxs-lookup"><span data-stu-id="2e64f-176">NOTES</span></span>

## <span data-ttu-id="2e64f-177">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e64f-177">RELATED LINKS</span></span>
