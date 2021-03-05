---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 9918c314d239bf822fa789bcab6a9de923b8c2e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999632"
---
# <span data-ttu-id="42205-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="42205-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="42205-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42205-102">SYNOPSIS</span></span>
<span data-ttu-id="42205-103">하나 이상의 작업 단계 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42205-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="42205-104">구문</span><span class="sxs-lookup"><span data-stu-id="42205-104">SYNTAX</span></span>

### <span data-ttu-id="42205-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="42205-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42205-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="42205-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42205-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="42205-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42205-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="42205-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42205-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="42205-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42205-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="42205-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42205-111">설명</span><span class="sxs-lookup"><span data-stu-id="42205-111">DESCRIPTION</span></span>
<span data-ttu-id="42205-112">Get-AzSqlElasticJobStepExecution cmdlet은 작업 실행에서 하나 이상의 작업 단계 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42205-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="42205-113">예제</span><span class="sxs-lookup"><span data-stu-id="42205-113">EXAMPLES</span></span>

### <span data-ttu-id="42205-114">예제 1 - 작업 실행에서 하나 이상의 작업 단계 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42205-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="42205-115">예제 2 - 작업 실행에서 하나 이상의 작업 단계 실행을 얻습니다. 단계 이름으로 필터링</span><span class="sxs-lookup"><span data-stu-id="42205-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="42205-116">하나 이상의 작업 단계 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="42205-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="42205-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42205-117">PARAMETERS</span></span>

### <span data-ttu-id="42205-118">-Active</span><span class="sxs-lookup"><span data-stu-id="42205-118">-Active</span></span>
<span data-ttu-id="42205-119">활성 실행을 통해 필터링할 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42205-119">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="42205-120">-AgentName</span></span>
<span data-ttu-id="42205-121">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-121">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="42205-122">-CreateTimeMax</span></span>
<span data-ttu-id="42205-123">시간 최대 만들기로 필터링</span><span class="sxs-lookup"><span data-stu-id="42205-123">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="42205-124">-CreateTimeMin</span></span>
<span data-ttu-id="42205-125">시간 최소 만들기로 필터링</span><span class="sxs-lookup"><span data-stu-id="42205-125">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42205-126">-DefaultProfile</span></span>
<span data-ttu-id="42205-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42205-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="42205-128">-EndTimeMax</span></span>
<span data-ttu-id="42205-129">종료 시간 최대로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="42205-129">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="42205-130">-EndTimeMin</span></span>
<span data-ttu-id="42205-131">종료 시간 최소로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="42205-131">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="42205-132">-JobExecutionId</span></span>
<span data-ttu-id="42205-133">작업 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-133">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="42205-134">-JobName</span></span>
<span data-ttu-id="42205-135">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-135">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42205-136">-ParentObject</span></span>
<span data-ttu-id="42205-137">에이전트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-137">The agent object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet, WithJobStepNameUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42205-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="42205-138">-ParentResourceId</span></span>
<span data-ttu-id="42205-139">작업 실행 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-139">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42205-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42205-140">-ResourceGroupName</span></span>
<span data-ttu-id="42205-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="42205-142">-ServerName</span></span>
<span data-ttu-id="42205-143">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-143">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobStepName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-144">-StepName</span><span class="sxs-lookup"><span data-stu-id="42205-144">-StepName</span></span>
<span data-ttu-id="42205-145">작업 단계 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42205-145">The job step name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobStepName, WithJobStepNameUsingParentObject, WithJobStepNameUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42205-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42205-146">CommonParameters</span></span>
<span data-ttu-id="42205-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42205-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42205-148">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42205-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42205-149">입력</span><span class="sxs-lookup"><span data-stu-id="42205-149">INPUTS</span></span>

### <span data-ttu-id="42205-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="42205-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="42205-151">출력</span><span class="sxs-lookup"><span data-stu-id="42205-151">OUTPUTS</span></span>

### <span data-ttu-id="42205-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="42205-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="42205-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42205-153">NOTES</span></span>

## <span data-ttu-id="42205-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42205-154">RELATED LINKS</span></span>
