---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstepexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStepExecution.md
ms.openlocfilehash: 03c4a6dede1f60e782bbfecdec1fb18894b2ca15
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879666"
---
# <span data-ttu-id="36f21-101">Get-AzSqlElasticJobStepExecution</span><span class="sxs-lookup"><span data-stu-id="36f21-101">Get-AzSqlElasticJobStepExecution</span></span>

## <span data-ttu-id="36f21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f21-102">SYNOPSIS</span></span>
<span data-ttu-id="36f21-103">하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-103">Gets one or more job step executions</span></span>

## <span data-ttu-id="36f21-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36f21-104">SYNTAX</span></span>

### <span data-ttu-id="36f21-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="36f21-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36f21-106">WithJobStepName</span><span class="sxs-lookup"><span data-stu-id="36f21-106">WithJobStepName</span></span>
```
Get-AzSqlElasticJobStepExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -StepName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36f21-107">엔터티가</span><span class="sxs-lookup"><span data-stu-id="36f21-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f21-108">WithJobStepNameUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="36f21-108">WithJobStepNameUsingParentObject</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f21-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36f21-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36f21-110">WithJobStepNameUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="36f21-110">WithJobStepNameUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStepExecution [-ParentResourceId] <String> -StepName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f21-111">설명은</span><span class="sxs-lookup"><span data-stu-id="36f21-111">DESCRIPTION</span></span>
<span data-ttu-id="36f21-112">Get-AzSqlElasticJobStepExecution cmdlet은 작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-112">The Get-AzSqlElasticJobStepExecution cmdlet gets one or more job step executions from a job execution</span></span>

## <span data-ttu-id="36f21-113">예제의</span><span class="sxs-lookup"><span data-stu-id="36f21-113">EXAMPLES</span></span>

### <span data-ttu-id="36f21-114">예제 1-작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-114">Example 1 - Gets one or more job step executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="36f21-115">예제 2-작업 실행에서 하나 이상의 작업 단계 실행을 가져옵니다. 단계별 이름 필터링</span><span class="sxs-lookup"><span data-stu-id="36f21-115">Example 2 - Gets one or more job step executions from a job execution, filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobStepExecution -StepName step1

JobName JobVersion StepName StepId JobExecutionId                       Lifecycle StartTime            EndTime
------- ---------- -------- ------ --------------                       --------- ---------            -------
job1    1          step1    1      3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

<span data-ttu-id="36f21-116">하나 이상의 작업 단계 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-116">Gets one or more job step executions</span></span>

## <span data-ttu-id="36f21-117">변수</span><span class="sxs-lookup"><span data-stu-id="36f21-117">PARAMETERS</span></span>

### <span data-ttu-id="36f21-118">-활성</span><span class="sxs-lookup"><span data-stu-id="36f21-118">-Active</span></span>
<span data-ttu-id="36f21-119">활성 실행을 기준으로 필터링 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-119">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="36f21-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="36f21-120">-AgentName</span></span>
<span data-ttu-id="36f21-121">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-121">The agent name.</span></span>

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

### <span data-ttu-id="36f21-122">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="36f21-122">-CreateTimeMax</span></span>
<span data-ttu-id="36f21-123">생성 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="36f21-123">Filter by create time max</span></span>

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

### <span data-ttu-id="36f21-124">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="36f21-124">-CreateTimeMin</span></span>
<span data-ttu-id="36f21-125">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="36f21-125">Filter by create time min</span></span>

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

### <span data-ttu-id="36f21-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f21-126">-DefaultProfile</span></span>
<span data-ttu-id="36f21-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f21-128">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="36f21-128">-EndTimeMax</span></span>
<span data-ttu-id="36f21-129">끝 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="36f21-129">Filter by end time max.</span></span>

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

### <span data-ttu-id="36f21-130">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="36f21-130">-EndTimeMin</span></span>
<span data-ttu-id="36f21-131">끝 시간 min으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-131">Filter by end time min.</span></span>

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

### <span data-ttu-id="36f21-132">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="36f21-132">-JobExecutionId</span></span>
<span data-ttu-id="36f21-133">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-133">The job execution id.</span></span>

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

### <span data-ttu-id="36f21-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="36f21-134">-JobName</span></span>
<span data-ttu-id="36f21-135">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-135">The job name.</span></span>

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

### <span data-ttu-id="36f21-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="36f21-136">-ParentObject</span></span>
<span data-ttu-id="36f21-137">에이전트 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-137">The agent object.</span></span>

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

### <span data-ttu-id="36f21-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="36f21-138">-ParentResourceId</span></span>
<span data-ttu-id="36f21-139">작업 실행 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-139">The job execution resource id.</span></span>

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

### <span data-ttu-id="36f21-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f21-140">-ResourceGroupName</span></span>
<span data-ttu-id="36f21-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-141">The resource group name.</span></span>

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

### <span data-ttu-id="36f21-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36f21-142">-ServerName</span></span>
<span data-ttu-id="36f21-143">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-143">The server name.</span></span>

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

### <span data-ttu-id="36f21-144">-단계 이름</span><span class="sxs-lookup"><span data-stu-id="36f21-144">-StepName</span></span>
<span data-ttu-id="36f21-145">작업 단계 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-145">The job step name.</span></span>

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

### <span data-ttu-id="36f21-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f21-146">CommonParameters</span></span>
<span data-ttu-id="36f21-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36f21-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f21-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="36f21-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f21-149">입력</span><span class="sxs-lookup"><span data-stu-id="36f21-149">INPUTS</span></span>

### <span data-ttu-id="36f21-150">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="36f21-150">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="36f21-151">출력</span><span class="sxs-lookup"><span data-stu-id="36f21-151">OUTPUTS</span></span>

### <span data-ttu-id="36f21-152">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="36f21-152">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="36f21-153">상속자</span><span class="sxs-lookup"><span data-stu-id="36f21-153">NOTES</span></span>

## <span data-ttu-id="36f21-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36f21-154">RELATED LINKS</span></span>
