---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJob.md
ms.openlocfilehash: 98c019c8dedf767fc2b75bb2133f7c545ffd03ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877618"
---
# <span data-ttu-id="c090e-101">New-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="c090e-101">New-AzSqlElasticJob</span></span>

## <span data-ttu-id="c090e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c090e-102">SYNOPSIS</span></span>
<span data-ttu-id="c090e-103">새 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="c090e-103">Creates a new job</span></span>

## <span data-ttu-id="c090e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c090e-104">SYNTAX</span></span>

### <span data-ttu-id="c090e-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c090e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c090e-106">RunOnce</span><span class="sxs-lookup"><span data-stu-id="c090e-106">RunOnce</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 [-RunOnce] [-StartTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c090e-107">정기</span><span class="sxs-lookup"><span data-stu-id="c090e-107">Recurring</span></span>
```
New-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name] <String>
 -IntervalType <String> -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c090e-108">엔터티가</span><span class="sxs-lookup"><span data-stu-id="c090e-108">ObjectSet</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-Description <String>]
 [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c090e-109">RunOnceUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c090e-109">RunOnceUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> [-RunOnce]
 [-StartTime <DateTime>] [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c090e-110">RecurringUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="c090e-110">RecurringUsingParentObject</span></span>
```
New-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c090e-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c090e-111">ResourceIdSet</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c090e-112">RunOnceUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c090e-112">RunOnceUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> [-RunOnce] [-StartTime <DateTime>]
 [-Description <String>] [-Enable] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c090e-113">RecurringUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c090e-113">RecurringUsingParentResourceId</span></span>
```
New-AzSqlElasticJob [-ParentResourceId] <String> [-Name] <String> -IntervalType <String>
 -IntervalCount <UInt32> [-StartTime <DateTime>] [-EndTime <DateTime>] [-Description <String>] [-Enable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c090e-114">설명은</span><span class="sxs-lookup"><span data-stu-id="c090e-114">DESCRIPTION</span></span>
<span data-ttu-id="c090e-115">New-AzSqlElasticJob cmdlet은 새 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-115">The New-AzSqlElasticJob cmdlet creates a new job</span></span>

## <span data-ttu-id="c090e-116">예제의</span><span class="sxs-lookup"><span data-stu-id="c090e-116">EXAMPLES</span></span>

### <span data-ttu-id="c090e-117">예제 1-새 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="c090e-117">Example 1 - Creates a new job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="c090e-118">새 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="c090e-118">Creates a new job</span></span>

## <span data-ttu-id="c090e-119">변수</span><span class="sxs-lookup"><span data-stu-id="c090e-119">PARAMETERS</span></span>

### <span data-ttu-id="c090e-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c090e-120">-AgentName</span></span>
<span data-ttu-id="c090e-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="c090e-121">The agent name</span></span>

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

### <span data-ttu-id="c090e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c090e-122">-DefaultProfile</span></span>
<span data-ttu-id="c090e-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c090e-124">-설명</span><span class="sxs-lookup"><span data-stu-id="c090e-124">-Description</span></span>
<span data-ttu-id="c090e-125">작업 설명</span><span class="sxs-lookup"><span data-stu-id="c090e-125">The job description</span></span>

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

### <span data-ttu-id="c090e-126">-사용</span><span class="sxs-lookup"><span data-stu-id="c090e-126">-Enable</span></span>
<span data-ttu-id="c090e-127">이 작업을 사용 하려는 고객을 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-127">The flag to indicate customer wants this job to be enabled.</span></span>

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

### <span data-ttu-id="c090e-128">-EndTime</span><span class="sxs-lookup"><span data-stu-id="c090e-128">-EndTime</span></span>
<span data-ttu-id="c090e-129">작업 일정 종료 시간</span><span class="sxs-lookup"><span data-stu-id="c090e-129">The job schedule end time</span></span>

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

### <span data-ttu-id="c090e-130">-Intcount</span><span class="sxs-lookup"><span data-stu-id="c090e-130">-IntervalCount</span></span>
<span data-ttu-id="c090e-131">되풀이 일정 간격 수</span><span class="sxs-lookup"><span data-stu-id="c090e-131">The recurring schedule interval count</span></span>

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

### <span data-ttu-id="c090e-132">-간격 종류</span><span class="sxs-lookup"><span data-stu-id="c090e-132">-IntervalType</span></span>
<span data-ttu-id="c090e-133">되풀이 일정 간격 형식-분, 시간, 일, 주, 월을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-133">The recurring schedule interval type - Can be Minute, Hour, Day, Week, Month</span></span>

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

### <span data-ttu-id="c090e-134">-이름</span><span class="sxs-lookup"><span data-stu-id="c090e-134">-Name</span></span>
<span data-ttu-id="c090e-135">작업 이름</span><span class="sxs-lookup"><span data-stu-id="c090e-135">The job name</span></span>

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

### <span data-ttu-id="c090e-136">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c090e-136">-ParentObject</span></span>
<span data-ttu-id="c090e-137">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c090e-137">The agent input object</span></span>

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

### <span data-ttu-id="c090e-138">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c090e-138">-ParentResourceId</span></span>
<span data-ttu-id="c090e-139">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="c090e-139">The agent resource id</span></span>

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

### <span data-ttu-id="c090e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c090e-140">-ResourceGroupName</span></span>
<span data-ttu-id="c090e-141">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c090e-141">The resource group name</span></span>

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

### <span data-ttu-id="c090e-142">-RunOnce</span><span class="sxs-lookup"><span data-stu-id="c090e-142">-RunOnce</span></span>
<span data-ttu-id="c090e-143">작업을 표시 하는 플래그는 한 번만 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-143">The flag to indicate job will be run once</span></span>

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

### <span data-ttu-id="c090e-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c090e-144">-ServerName</span></span>
<span data-ttu-id="c090e-145">서버 이름</span><span class="sxs-lookup"><span data-stu-id="c090e-145">The server name</span></span>

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

### <span data-ttu-id="c090e-146">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c090e-146">-StartTime</span></span>
<span data-ttu-id="c090e-147">작업 일정 시작 시간</span><span class="sxs-lookup"><span data-stu-id="c090e-147">The job schedule start time</span></span>

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

### <span data-ttu-id="c090e-148">-확인</span><span class="sxs-lookup"><span data-stu-id="c090e-148">-Confirm</span></span>
<span data-ttu-id="c090e-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c090e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c090e-150">-WhatIf</span></span>
<span data-ttu-id="c090e-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c090e-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c090e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c090e-153">CommonParameters</span></span>
<span data-ttu-id="c090e-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c090e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c090e-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c090e-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c090e-156">입력</span><span class="sxs-lookup"><span data-stu-id="c090e-156">INPUTS</span></span>

### <span data-ttu-id="c090e-157">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c090e-157">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="c090e-158">출력</span><span class="sxs-lookup"><span data-stu-id="c090e-158">OUTPUTS</span></span>

### <span data-ttu-id="c090e-159">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c090e-159">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="c090e-160">상속자</span><span class="sxs-lookup"><span data-stu-id="c090e-160">NOTES</span></span>

## <span data-ttu-id="c090e-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c090e-161">RELATED LINKS</span></span>
