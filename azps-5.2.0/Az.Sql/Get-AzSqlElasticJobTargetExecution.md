---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 6e61a83d843e0ceaa7d7926060da848d80d16eae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335930"
---
# <span data-ttu-id="f41fd-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="f41fd-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="f41fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f41fd-102">SYNOPSIS</span></span>
<span data-ttu-id="f41fd-103">하나 이상의 작업 대상 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="f41fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="f41fd-104">SYNTAX</span></span>

### <span data-ttu-id="f41fd-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f41fd-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f41fd-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="f41fd-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f41fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f41fd-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f41fd-108">설명</span><span class="sxs-lookup"><span data-stu-id="f41fd-108">DESCRIPTION</span></span>
<span data-ttu-id="f41fd-109">Get-AzSqlElasticJobTargetExecution cmdlet은 작업 실행에서 하나 이상의 작업 대상 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="f41fd-110">예제</span><span class="sxs-lookup"><span data-stu-id="f41fd-110">EXAMPLES</span></span>

### <span data-ttu-id="f41fd-111">예제 1: 작업 실행에서 하나 이상의 작업 대상 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-111">Example 1: Gets one or more job target executions from a job executions</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="f41fd-112">예제 2: 작업 실행에서 하나 이상의 작업 대상 실행을 얻음 - 단계별 필터링</span><span class="sxs-lookup"><span data-stu-id="f41fd-112">Example 2: Gets one or more job target executions from a job executions - filtering by step name</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="f41fd-113">하나 이상의 작업 대상 실행을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="f41fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f41fd-114">PARAMETERS</span></span>

### <span data-ttu-id="f41fd-115">-Active</span><span class="sxs-lookup"><span data-stu-id="f41fd-115">-Active</span></span>
<span data-ttu-id="f41fd-116">활성 실행을 통해 필터링할 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-116">Flag to filter by active executions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f41fd-117">-AgentName</span></span>
<span data-ttu-id="f41fd-118">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-118">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-119">-Count</span><span class="sxs-lookup"><span data-stu-id="f41fd-119">-Count</span></span>
<span data-ttu-id="f41fd-120">Count는 상위 실행 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-120">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="f41fd-121">-CreateTimeMax</span></span>
<span data-ttu-id="f41fd-122">시간 최대 만들기로 필터링</span><span class="sxs-lookup"><span data-stu-id="f41fd-122">Filter by create time max</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="f41fd-123">-CreateTimeMin</span></span>
<span data-ttu-id="f41fd-124">시간 최소 만들기로 필터링</span><span class="sxs-lookup"><span data-stu-id="f41fd-124">Filter by create time min</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f41fd-125">-DefaultProfile</span></span>
<span data-ttu-id="f41fd-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f41fd-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="f41fd-127">-EndTimeMax</span></span>
<span data-ttu-id="f41fd-128">종료 시간 최대로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-128">Filter by end time max.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="f41fd-129">-EndTimeMin</span></span>
<span data-ttu-id="f41fd-130">종료 시간 최소 시간으로 필터링합니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-130">Filter by end time min.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="f41fd-131">-JobExecutionId</span></span>
<span data-ttu-id="f41fd-132">작업 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-132">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="f41fd-133">-JobName</span></span>
<span data-ttu-id="f41fd-134">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-134">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f41fd-135">-ParentObject</span></span>
<span data-ttu-id="f41fd-136">작업 실행 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-136">The job execution object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f41fd-137">-ParentResourceId</span></span>
<span data-ttu-id="f41fd-138">작업 실행 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-138">The job execution resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f41fd-139">-ResourceGroupName</span></span>
<span data-ttu-id="f41fd-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f41fd-141">-ServerName</span></span>
<span data-ttu-id="f41fd-142">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-142">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f41fd-143">-StepName</span><span class="sxs-lookup"><span data-stu-id="f41fd-143">-StepName</span></span>
<span data-ttu-id="f41fd-144">작업 단계 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-144">The job step name.</span></span>

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

### <span data-ttu-id="f41fd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f41fd-145">CommonParameters</span></span>
<span data-ttu-id="f41fd-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f41fd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f41fd-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f41fd-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f41fd-148">입력</span><span class="sxs-lookup"><span data-stu-id="f41fd-148">INPUTS</span></span>

### <span data-ttu-id="f41fd-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="f41fd-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="f41fd-150">출력</span><span class="sxs-lookup"><span data-stu-id="f41fd-150">OUTPUTS</span></span>

### <span data-ttu-id="f41fd-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="f41fd-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="f41fd-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f41fd-152">NOTES</span></span>

## <span data-ttu-id="f41fd-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f41fd-153">RELATED LINKS</span></span>
