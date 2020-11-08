---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobexecution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobExecution.md
ms.openlocfilehash: d5583e5d7c0984b36679517859cc5a109b808a1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212134"
---
# <span data-ttu-id="2cc8c-101">Get-AzSqlElasticJobExecution</span><span class="sxs-lookup"><span data-stu-id="2cc8c-101">Get-AzSqlElasticJobExecution</span></span>

## <span data-ttu-id="2cc8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cc8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2cc8c-103">하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-103">Gets one or more job executions</span></span>

## <span data-ttu-id="2cc8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2cc8c-104">SYNTAX</span></span>

### <span data-ttu-id="2cc8c-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2cc8c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName <String>] [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>]
 [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-106">WithJobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2cc8c-106">WithJobExecutionId</span></span>
```
Get-AzSqlElasticJobExecution [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 -JobName <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-107">엔터티가</span><span class="sxs-lookup"><span data-stu-id="2cc8c-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> [-JobName <String>]
 [-Count] <Int32> [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>]
 [-EndTimeMax <DateTime>] [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-108">WithJobExecutionIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="2cc8c-108">WithJobExecutionIdUsingParentObject</span></span>
```
Get-AzSqlElasticJobExecution [-ParentObject] <AzureSqlElasticJobAgentModel> -JobName <String>
 -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2cc8c-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> [-JobName <String>] [-Count] <Int32>
 [-CreateTimeMin <DateTime>] [-CreateTimeMax <DateTime>] [-EndTimeMin <DateTime>] [-EndTimeMax <DateTime>]
 [-Active] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cc8c-110">WithJobExecutionIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc8c-110">WithJobExecutionIdUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobExecution [-ParentResourceId] <String> -JobName <String> -JobExecutionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cc8c-111">설명은</span><span class="sxs-lookup"><span data-stu-id="2cc8c-111">DESCRIPTION</span></span>
<span data-ttu-id="2cc8c-112">Get-AzSqlElasticJobExecution cmdlet은 하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-112">The Get-AzSqlElasticJobExecution cmdlet gets one or more job executions</span></span>

## <span data-ttu-id="2cc8c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="2cc8c-113">EXAMPLES</span></span>

### <span data-ttu-id="2cc8c-114">예제 1: 모든 작업에서 하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-114">Example 1: Gets one or more job executions across all jobs</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b Canceled  6/1/2018 10:13:56 PM 6/1/2018 10:13:59 PM
job1    3bcfc912-20b2-411d-a2b7-6265d13fe272 Succeeded 6/1/2018 10:11:43 PM 6/1/2018 10:11:47 PM
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

### <span data-ttu-id="2cc8c-115">예제 2: 작업에 대 한 하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-115">Example 2: Gets one or more job executions for a job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobExecution -Count 3 -JobName job2

JobName JobExecutionId                       Lifecycle StartTime            EndTime
------- --------------                       --------- ---------            -------
job2    433f798e-f35c-41de-a23c-f2b43801d7b4 Succeeded 6/1/2018 10:11:36 PM 6/1/2018 10:11:41 PM
```

<span data-ttu-id="2cc8c-116">하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-116">Gets one or more job executions</span></span>

### <span data-ttu-id="2cc8c-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="2cc8c-117">Example 3</span></span>

<span data-ttu-id="2cc8c-118">하나 이상의 작업 실행을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-118">Gets one or more job executions.</span></span> <span data-ttu-id="2cc8c-119">생성</span><span class="sxs-lookup"><span data-stu-id="2cc8c-119">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlElasticJobExecution -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1
```

## <span data-ttu-id="2cc8c-120">변수</span><span class="sxs-lookup"><span data-stu-id="2cc8c-120">PARAMETERS</span></span>

### <span data-ttu-id="2cc8c-121">-활성</span><span class="sxs-lookup"><span data-stu-id="2cc8c-121">-Active</span></span>
<span data-ttu-id="2cc8c-122">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="2cc8c-122">Filter by create time min</span></span>

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

### <span data-ttu-id="2cc8c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-123">-AgentName</span></span>
<span data-ttu-id="2cc8c-124">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-125">-카운트</span><span class="sxs-lookup"><span data-stu-id="2cc8c-125">-Count</span></span>
<span data-ttu-id="2cc8c-126">Count는 맨 위의 실행 횟수를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-126">Count returns the top number of executions.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-127">-CreateTimeMax</span><span class="sxs-lookup"><span data-stu-id="2cc8c-127">-CreateTimeMax</span></span>
<span data-ttu-id="2cc8c-128">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="2cc8c-128">Filter by create time min</span></span>

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

### <span data-ttu-id="2cc8c-129">-CreateTimeMin</span><span class="sxs-lookup"><span data-stu-id="2cc8c-129">-CreateTimeMin</span></span>
<span data-ttu-id="2cc8c-130">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="2cc8c-130">Filter by create time min</span></span>

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

### <span data-ttu-id="2cc8c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cc8c-131">-DefaultProfile</span></span>
<span data-ttu-id="2cc8c-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cc8c-133">-EndTimeMax</span><span class="sxs-lookup"><span data-stu-id="2cc8c-133">-EndTimeMax</span></span>
<span data-ttu-id="2cc8c-134">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="2cc8c-134">Filter by create time min</span></span>

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

### <span data-ttu-id="2cc8c-135">-EndTimeMin</span><span class="sxs-lookup"><span data-stu-id="2cc8c-135">-EndTimeMin</span></span>
<span data-ttu-id="2cc8c-136">만든 시간별로 필터링</span><span class="sxs-lookup"><span data-stu-id="2cc8c-136">Filter by create time min</span></span>

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

### <span data-ttu-id="2cc8c-137">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="2cc8c-137">-JobExecutionId</span></span>
<span data-ttu-id="2cc8c-138">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-138">The job execution id.</span></span>

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-139">-JobName</span></span>
<span data-ttu-id="2cc8c-140">작업 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-140">The job name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithJobExecutionId, WithJobExecutionIdUsingParentObject, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-141">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2cc8c-141">-ParentObject</span></span>
<span data-ttu-id="2cc8c-142">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-142">The job execution id.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, WithJobExecutionIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-143">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="2cc8c-143">-ParentResourceId</span></span>
<span data-ttu-id="2cc8c-144">에이전트 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-144">The agent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithJobExecutionIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-145">-ResourceGroupName</span></span>
<span data-ttu-id="2cc8c-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-146">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2cc8c-147">-ServerName</span></span>
<span data-ttu-id="2cc8c-148">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-148">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithJobExecutionId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cc8c-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cc8c-149">CommonParameters</span></span>
<span data-ttu-id="2cc8c-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cc8c-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2cc8c-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cc8c-152">입력</span><span class="sxs-lookup"><span data-stu-id="2cc8c-152">INPUTS</span></span>

### <span data-ttu-id="2cc8c-153">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="2cc8c-153">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2cc8c-154">출력</span><span class="sxs-lookup"><span data-stu-id="2cc8c-154">OUTPUTS</span></span>

### <span data-ttu-id="2cc8c-155">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="2cc8c-155">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="2cc8c-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2cc8c-156">NOTES</span></span>

## <span data-ttu-id="2cc8c-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2cc8c-157">RELATED LINKS</span></span>
