---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJob.md
ms.openlocfilehash: 53bd1b1cd1c2f7ba87df8cb5c27f1b2380db04af
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226309"
---
# <span data-ttu-id="504f3-101">Set-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="504f3-101">Set-AzSqlElasticJob</span></span>

## <span data-ttu-id="504f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="504f3-102">SYNOPSIS</span></span>
<span data-ttu-id="504f3-103">작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="504f3-103">Updates a job</span></span>

## <span data-ttu-id="504f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="504f3-104">SYNTAX</span></span>

### <span data-ttu-id="504f3-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="504f3-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="504f3-106">RunOnce</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-107">정기</span><span class="sxs-lookup"><span data-stu-id="504f3-107">Recurring</span></span>
```
Set-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-108">엔터티가</span><span class="sxs-lookup"><span data-stu-id="504f3-108">ObjectSet</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="504f3-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="504f3-109">RunOnceUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> [-RunOnce] [-StartTime <DateTime>]
 [-EndTime <DateTime>] [-Enable] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="504f3-110">RecurringUsingParentObject</span></span>
```
Set-AzSqlElasticJob [-InputObject] <AzureSqlElasticJobModel> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="504f3-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="504f3-112">RunOnceUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> [-RunOnce] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="504f3-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="504f3-113">RecurringUsingParentResourceId</span></span>
```
Set-AzSqlElasticJob [-ResourceId] <String> -IntervalType <String> -IntervalCount <UInt32>
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-Enable] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="504f3-114">설명은</span><span class="sxs-lookup"><span data-stu-id="504f3-114">DESCRIPTION</span></span>
<span data-ttu-id="504f3-115">Set-AzSqlElasticJob cmdlet이 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-115">The Set-AzSqlElasticJob cmdlet updates a job</span></span>

## <span data-ttu-id="504f3-116">예제의</span><span class="sxs-lookup"><span data-stu-id="504f3-116">EXAMPLES</span></span>

### <span data-ttu-id="504f3-117">예제 1: 작업을 업데이트 하 여 한 시간에 시작 하 고 1 시간 마다 반복</span><span class="sxs-lookup"><span data-stu-id="504f3-117">Example 1: Updates a job to start an hour from now and repeat every 1 hour</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Set-AzSqlElasticJob -IntervalType Hour -IntervalCount 1 -StartTime (Get-Date).AddHours(1) -Enable

JobName Version Description StartTime            EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------            -------                ------------ -------- -------
job1    0                   6/1/2018 10:50:15 PM 12/31/9999 11:59:59 AM Recurring    PT1H     True
```

<span data-ttu-id="504f3-118">작업 업데이트</span><span class="sxs-lookup"><span data-stu-id="504f3-118">Updates a job</span></span>

### <span data-ttu-id="504f3-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="504f3-119">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJob -AgentName agent -Enable -IntervalCount 1 -IntervalType Hour -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1 -StartTime '9/16/2016 11:31:12'
```

## <span data-ttu-id="504f3-120">변수</span><span class="sxs-lookup"><span data-stu-id="504f3-120">PARAMETERS</span></span>

### <span data-ttu-id="504f3-121">-AgentName</span><span class="sxs-lookup"><span data-stu-id="504f3-121">-AgentName</span></span>
<span data-ttu-id="504f3-122">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="504f3-122">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="504f3-123">-DefaultProfile</span></span>
<span data-ttu-id="504f3-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="504f3-125">-설명</span><span class="sxs-lookup"><span data-stu-id="504f3-125">-Description</span></span>
<span data-ttu-id="504f3-126">작업 설명</span><span class="sxs-lookup"><span data-stu-id="504f3-126">The job description</span></span>

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

### <span data-ttu-id="504f3-127">-사용</span><span class="sxs-lookup"><span data-stu-id="504f3-127">-Enable</span></span>
<span data-ttu-id="504f3-128">이 작업을 사용 하려는 고객을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-128">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="504f3-129">-EndTime</span><span class="sxs-lookup"><span data-stu-id="504f3-129">-EndTime</span></span>
<span data-ttu-id="504f3-130">작업 일정 종료 시간</span><span class="sxs-lookup"><span data-stu-id="504f3-130">The job schedule end time</span></span>

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

### <span data-ttu-id="504f3-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="504f3-131">-InputObject</span></span>
<span data-ttu-id="504f3-132">작업 입력 개체</span><span class="sxs-lookup"><span data-stu-id="504f3-132">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-133">-Intcount</span><span class="sxs-lookup"><span data-stu-id="504f3-133">-IntervalCount</span></span>
<span data-ttu-id="504f3-134">되풀이 일정 간격 수</span><span class="sxs-lookup"><span data-stu-id="504f3-134">The recurring schedule interval count</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-135">-간격 종류</span><span class="sxs-lookup"><span data-stu-id="504f3-135">-IntervalType</span></span>
<span data-ttu-id="504f3-136">되풀이 일정 간격 형식-분, 시간, 일, 주, 월을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

```yaml
Type: System.String
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-137">-이름</span><span class="sxs-lookup"><span data-stu-id="504f3-137">-Name</span></span>
<span data-ttu-id="504f3-138">작업 이름</span><span class="sxs-lookup"><span data-stu-id="504f3-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="504f3-139">-ResourceGroupName</span></span>
<span data-ttu-id="504f3-140">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="504f3-140">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="504f3-141">-ResourceId</span></span>
<span data-ttu-id="504f3-142">작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="504f3-142">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-143">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="504f3-143">-RunOnce</span></span>
<span data-ttu-id="504f3-144">작업을 표시 하는 플래그는 한 번만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-144">The flag to indicate job will be run once</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RunOnce, RunOnceUsingParentObject, RunOnceUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-145">-ServerName</span><span class="sxs-lookup"><span data-stu-id="504f3-145">-ServerName</span></span>
<span data-ttu-id="504f3-146">서버 이름</span><span class="sxs-lookup"><span data-stu-id="504f3-146">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, RunOnce, Recurring
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="504f3-147">-StartTime</span><span class="sxs-lookup"><span data-stu-id="504f3-147">-StartTime</span></span>
<span data-ttu-id="504f3-148">작업 일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="504f3-148">The job schedule start time</span></span>

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

### <span data-ttu-id="504f3-149">-확인</span><span class="sxs-lookup"><span data-stu-id="504f3-149">-Confirm</span></span>
<span data-ttu-id="504f3-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="504f3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="504f3-151">-WhatIf</span></span>
<span data-ttu-id="504f3-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="504f3-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="504f3-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="504f3-154">CommonParameters</span></span>
<span data-ttu-id="504f3-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="504f3-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="504f3-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="504f3-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="504f3-157">입력</span><span class="sxs-lookup"><span data-stu-id="504f3-157">INPUTS</span></span>

### <span data-ttu-id="504f3-158">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="504f3-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="504f3-159">출력</span><span class="sxs-lookup"><span data-stu-id="504f3-159">OUTPUTS</span></span>

### <span data-ttu-id="504f3-160">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="504f3-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="504f3-161">상속자</span><span class="sxs-lookup"><span data-stu-id="504f3-161">NOTES</span></span>

## <span data-ttu-id="504f3-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="504f3-162">RELATED LINKS</span></span>
