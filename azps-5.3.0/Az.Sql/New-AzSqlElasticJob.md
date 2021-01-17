---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: e6853c3b4fa32a10e93ee281aab0b97755403671
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491605"
---
# <span data-ttu-id="5b05e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="5b05e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="5b05e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b05e-102">SYNOPSIS</span></span>
<span data-ttu-id="5b05e-103">새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-103">Creates a new job</span></span>

## <span data-ttu-id="5b05e-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b05e-104">SYNTAX</span></span>

### <span data-ttu-id="5b05e-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b05e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b05e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="5b05e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b05e-107">Recurring</span><span class="sxs-lookup"><span data-stu-id="5b05e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b05e-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="5b05e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b05e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5b05e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b05e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="5b05e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b05e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5b05e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b05e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b05e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b05e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b05e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b05e-114">설명</span><span class="sxs-lookup"><span data-stu-id="5b05e-114">DESCRIPTION</span></span>
<span data-ttu-id="5b05e-115">New-AzSqlElasticJob cmdlet에서 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="5b05e-116">예제</span><span class="sxs-lookup"><span data-stu-id="5b05e-116">EXAMPLES</span></span>

### <span data-ttu-id="5b05e-117">예제 1: 새 작업 생성</span><span class="sxs-lookup"><span data-stu-id="5b05e-117">Example 1: Creates a new job</span></span>
```powershell
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="5b05e-118">새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-118">Creates a new job</span></span>

### <span data-ttu-id="5b05e-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="5b05e-119">Example 2</span></span>

<span data-ttu-id="5b05e-120">새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-120">Creates a new job.</span></span> <span data-ttu-id="5b05e-121">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="5b05e-121">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticJob -Name job1 -RunOnce
```

## <span data-ttu-id="5b05e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b05e-122">PARAMETERS</span></span>

### <span data-ttu-id="5b05e-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="5b05e-123">-AgentName</span></span>
<span data-ttu-id="5b05e-124">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="5b05e-124">The agent name</span></span>

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

### <span data-ttu-id="5b05e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b05e-125">-DefaultProfile</span></span>
<span data-ttu-id="5b05e-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b05e-127">-Description</span><span class="sxs-lookup"><span data-stu-id="5b05e-127">-Description</span></span>
<span data-ttu-id="5b05e-128">작업 설명</span><span class="sxs-lookup"><span data-stu-id="5b05e-128">The job description</span></span>

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

### <span data-ttu-id="5b05e-129">-Enable</span><span class="sxs-lookup"><span data-stu-id="5b05e-129">-Enable</span></span>
<span data-ttu-id="5b05e-130">고객이 이 작업을 사용하도록 설정하려는 것을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-130">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="5b05e-131">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5b05e-131">-EndTime</span></span>
<span data-ttu-id="5b05e-132">작업 일정 종료 시간</span><span class="sxs-lookup"><span data-stu-id="5b05e-132">The job schedule end time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: Recurring, RecurringUsingParentObject, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b05e-133">-IntervalCount</span><span class="sxs-lookup"><span data-stu-id="5b05e-133">-IntervalCount</span></span>
<span data-ttu-id="5b05e-134">반복 일정 간격 수</span><span class="sxs-lookup"><span data-stu-id="5b05e-134">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="5b05e-135">-IntervalType</span><span class="sxs-lookup"><span data-stu-id="5b05e-135">-IntervalType</span></span>
<span data-ttu-id="5b05e-136">반복 일정 간격 유형 - 분, 시간, 일, 주, 월일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-136">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="5b05e-137">-Name</span><span class="sxs-lookup"><span data-stu-id="5b05e-137">-Name</span></span>
<span data-ttu-id="5b05e-138">작업 이름</span><span class="sxs-lookup"><span data-stu-id="5b05e-138">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b05e-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5b05e-139">-ParentObject</span></span>
<span data-ttu-id="5b05e-140">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="5b05e-140">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet, RunOnceUsingParentObject, RecurringUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b05e-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5b05e-141">-ParentResourceId</span></span>
<span data-ttu-id="5b05e-142">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5b05e-142">The agent resource id</span></span>

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

### <span data-ttu-id="5b05e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b05e-143">-ResourceGroupName</span></span>
<span data-ttu-id="5b05e-144">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="5b05e-144">The resource group name</span></span>

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

### <span data-ttu-id="5b05e-145">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="5b05e-145">-RunOnce</span></span>
<span data-ttu-id="5b05e-146">작업이 한 번 실행될 것 을 나타내는 플래그</span><span class="sxs-lookup"><span data-stu-id="5b05e-146">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="5b05e-147">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5b05e-147">-ServerName</span></span>
<span data-ttu-id="5b05e-148">서버 이름</span><span class="sxs-lookup"><span data-stu-id="5b05e-148">The server name</span></span>

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

### <span data-ttu-id="5b05e-149">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5b05e-149">-StartTime</span></span>
<span data-ttu-id="5b05e-150">작업 일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="5b05e-150">The job schedule start time</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RunOnce, Recurring, RunOnceUsingParentObject, RecurringUsingParentObject, RunOnceUsingParentResourceId, RecurringUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b05e-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b05e-151">-Confirm</span></span>
<span data-ttu-id="5b05e-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b05e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b05e-153">-WhatIf</span></span>
<span data-ttu-id="5b05e-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b05e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b05e-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b05e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b05e-156">CommonParameters</span></span>
<span data-ttu-id="5b05e-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b05e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b05e-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b05e-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b05e-159">입력</span><span class="sxs-lookup"><span data-stu-id="5b05e-159">INPUTS</span></span>

### <span data-ttu-id="5b05e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="5b05e-160">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="5b05e-161">출력</span><span class="sxs-lookup"><span data-stu-id="5b05e-161">OUTPUTS</span></span>

### <span data-ttu-id="5b05e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="5b05e-162">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="5b05e-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b05e-163">NOTES</span></span>

## <span data-ttu-id="5b05e-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b05e-164">RELATED LINKS</span></span>
