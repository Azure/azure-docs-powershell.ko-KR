---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetExecution.md
ms.openlocfilehash: 566bfb8caae85c6f4e6ef75a38bdd5363ddb1eaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879657"
---
# <span data-ttu-id="4227a-101">Get-AzSqlElasticJobTargetExecution</span><span class="sxs-lookup"><span data-stu-id="4227a-101">Get-AzSqlElasticJobTargetExecution</span></span>

## <span data-ttu-id="4227a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4227a-102">SYNOPSIS</span></span>
<span data-ttu-id="4227a-103">하나 이상의 작업 대상 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-103">Gets one or more job target executions</span></span>

## <span data-ttu-id="4227a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4227a-104">SYNTAX</span></span>

### <span data-ttu-id="4227a-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4227a-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> -Count <Int32> [-StepName <String>] [-CreateTimeMin <DateTime>]
 [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4227a-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="4227a-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentObject] <AzureSqlElasticJobExecutionModel> -Count <Int32>
 [-StepName <String>] [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4227a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4227a-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetExecution [-ParentResourceId] <String> -Count <Int32> [-StepName <String>]
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4227a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4227a-108">DESCRIPTION</span></span>
<span data-ttu-id="4227a-109">Get-AzSqlElasticJobTargetExecution cmdlet은 작업 실행에서 하나 이상의 작업 대상 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-109">The Get-AzSqlElasticJobTargetExecution cmdlet gets one or more job target executions from a job execution</span></span>

## <span data-ttu-id="4227a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4227a-110">EXAMPLES</span></span>

### <span data-ttu-id="4227a-111">예제 1-작업 실행에서 하나 이상의 작업 대상 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-111">Example 1 - Gets one or more job target executions from a job executions</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
job1    1          step1    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db1                6/1/2018 10:11:44 PM 6/1/2018 10:11:47 PM
```

### <span data-ttu-id="4227a-112">예제 2-작업 실행에서 하나 이상의 작업 대상 실행을 가져옵니다.-단계별 이름 필터링</span><span class="sxs-lookup"><span data-stu-id="4227a-112">Example 2 - Gets one or more job target executions from a job executions - filtering by step name</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId 3bcfc912-20b2-411d-a2b7-6265d13fe272
$je | Get-AzSqlElasticJobTargetExecution -Count 2 -StepName step2
JobName JobVersion StepName StepId JobExecutionId                       Lifecycle       TargetServerName TargetDatabaseName StartTime            EndTime
------- ---------- -------- ------ --------------                       ---------       ---------------- ------------------ ---------            -------
job1    1          step2    1      ea0a870b-dfe3-427e-9f95-d229d7815b65 Succeeded       s1               db2                6/1/2018 10:11:47 PM 6/1/2018 10:11:50 PM
```

<span data-ttu-id="4227a-113">하나 이상의 작업 대상 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-113">Gets one or more job target executions</span></span>

## <span data-ttu-id="4227a-114">변수</span><span class="sxs-lookup"><span data-stu-id="4227a-114">PARAMETERS</span></span>

### <span data-ttu-id="4227a-115">-활성</span><span class="sxs-lookup"><span data-stu-id="4227a-115">-Active</span></span>
<span data-ttu-id="4227a-116">활성 실행을 기준으로 필터링 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-116">Flag to filter by active executions.</span></span>

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

### <span data-ttu-id="4227a-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4227a-117">-AgentName</span></span>
<span data-ttu-id="4227a-118">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-118">The agent name.</span></span>

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

### <span data-ttu-id="4227a-119">-카운트</span><span class="sxs-lookup"><span data-stu-id="4227a-119">-Count</span></span>
<span data-ttu-id="4227a-120">Count는 맨 위의 실행 횟수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-120">Count returns the top number of executions.</span></span>

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

### <span data-ttu-id="4227a-121">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="4227a-121">-CreateTimeMax</span></span>
<span data-ttu-id="4227a-122">생성 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="4227a-122">Filter by create time max</span></span>

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

### <span data-ttu-id="4227a-123">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="4227a-123">-CreateTimeMin</span></span>
<span data-ttu-id="4227a-124">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="4227a-124">Filter by create time min</span></span>

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

### <span data-ttu-id="4227a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4227a-125">-DefaultProfile</span></span>
<span data-ttu-id="4227a-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4227a-127">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="4227a-127">-EndTimeMax</span></span>
<span data-ttu-id="4227a-128">끝 시간 최대값으로 필터링</span><span class="sxs-lookup"><span data-stu-id="4227a-128">Filter by end time max.</span></span>

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

### <span data-ttu-id="4227a-129">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="4227a-129">-EndTimeMin</span></span>
<span data-ttu-id="4227a-130">끝 시간 min으로 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-130">Filter by end time min.</span></span>

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

### <span data-ttu-id="4227a-131">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="4227a-131">-JobExecutionId</span></span>
<span data-ttu-id="4227a-132">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-132">The job execution id.</span></span>

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

### <span data-ttu-id="4227a-133">-JobName</span><span class="sxs-lookup"><span data-stu-id="4227a-133">-JobName</span></span>
<span data-ttu-id="4227a-134">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-134">The job name.</span></span>

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

### <span data-ttu-id="4227a-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4227a-135">-ParentObject</span></span>
<span data-ttu-id="4227a-136">작업 실행 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-136">The job execution object.</span></span>

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

### <span data-ttu-id="4227a-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4227a-137">-ParentResourceId</span></span>
<span data-ttu-id="4227a-138">작업 실행 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-138">The job execution resource id.</span></span>

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

### <span data-ttu-id="4227a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4227a-139">-ResourceGroupName</span></span>
<span data-ttu-id="4227a-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-140">The resource group name.</span></span>

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

### <span data-ttu-id="4227a-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4227a-141">-ServerName</span></span>
<span data-ttu-id="4227a-142">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-142">The server name.</span></span>

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

### <span data-ttu-id="4227a-143">-단계 이름</span><span class="sxs-lookup"><span data-stu-id="4227a-143">-StepName</span></span>
<span data-ttu-id="4227a-144">작업 단계 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-144">The job step name.</span></span>

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

### <span data-ttu-id="4227a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4227a-145">CommonParameters</span></span>
<span data-ttu-id="4227a-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4227a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4227a-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4227a-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4227a-148">입력</span><span class="sxs-lookup"><span data-stu-id="4227a-148">INPUTS</span></span>

### <span data-ttu-id="4227a-149">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4227a-149">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4227a-150">출력</span><span class="sxs-lookup"><span data-stu-id="4227a-150">OUTPUTS</span></span>

### <span data-ttu-id="4227a-151">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="4227a-151">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="4227a-152">상속자</span><span class="sxs-lookup"><span data-stu-id="4227a-152">NOTES</span></span>

## <span data-ttu-id="4227a-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4227a-153">RELATED LINKS</span></span>
