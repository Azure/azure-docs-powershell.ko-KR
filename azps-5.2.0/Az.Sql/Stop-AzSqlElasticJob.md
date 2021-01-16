---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ec5ab9706bd459a07c91e7060d3bf6da30f76ed5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325506"
---
# <span data-ttu-id="d0778-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="d0778-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="d0778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0778-102">SYNOPSIS</span></span>
<span data-ttu-id="d0778-103">작업 실행 ID가 제공된 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="d0778-104">구문</span><span class="sxs-lookup"><span data-stu-id="d0778-104">SYNTAX</span></span>

### <span data-ttu-id="d0778-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d0778-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0778-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0778-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0778-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0778-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0778-108">설명</span><span class="sxs-lookup"><span data-stu-id="d0778-108">DESCRIPTION</span></span>
<span data-ttu-id="d0778-109">이 Stop-AzSqlElasticJob cmdlet은 실행 중인 실행으로 작업의 중지를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="d0778-110">작업 실행의 현재 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="d0778-111">예제</span><span class="sxs-lookup"><span data-stu-id="d0778-111">EXAMPLES</span></span>

### <span data-ttu-id="d0778-112">예제 1: 실행 중인 작업 실행으로 작업 중지</span><span class="sxs-lookup"><span data-stu-id="d0778-112">Example 1: Stops a job with a running job execution</span></span>
```powershell
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="d0778-113">실행 중인 작업 실행을 중지하고 현재 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-113">Stops a running job execution and returns it's current status</span></span>

### <span data-ttu-id="d0778-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d0778-114">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Stop-AzSqlElasticJob -AgentName agent -JobExecutionId 00000000-0000-0000-0000-000000000000 -JobName job1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="d0778-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0778-115">PARAMETERS</span></span>

### <span data-ttu-id="d0778-116">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d0778-116">-AgentName</span></span>
<span data-ttu-id="d0778-117">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="d0778-117">The agent name</span></span>

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

### <span data-ttu-id="d0778-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0778-118">-DefaultProfile</span></span>
<span data-ttu-id="d0778-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0778-120">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="d0778-120">-JobExecutionId</span></span>
<span data-ttu-id="d0778-121">작업 실행 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-121">The job execution id.</span></span>

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

### <span data-ttu-id="d0778-122">-JobName</span><span class="sxs-lookup"><span data-stu-id="d0778-122">-JobName</span></span>
<span data-ttu-id="d0778-123">작업 이름</span><span class="sxs-lookup"><span data-stu-id="d0778-123">The job name</span></span>

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

### <span data-ttu-id="d0778-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d0778-124">-ParentObject</span></span>
<span data-ttu-id="d0778-125">에이전트 제어 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="d0778-125">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="d0778-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d0778-126">-ParentResourceId</span></span>
<span data-ttu-id="d0778-127">작업 실행 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d0778-127">The job execution resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0778-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0778-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0778-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d0778-129">The resource group name</span></span>

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

### <span data-ttu-id="d0778-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0778-130">-ServerName</span></span>
<span data-ttu-id="d0778-131">서버 이름</span><span class="sxs-lookup"><span data-stu-id="d0778-131">The server name</span></span>

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

### <span data-ttu-id="d0778-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0778-132">-Confirm</span></span>
<span data-ttu-id="d0778-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0778-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0778-134">-WhatIf</span></span>
<span data-ttu-id="d0778-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d0778-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0778-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0778-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0778-137">CommonParameters</span></span>
<span data-ttu-id="d0778-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d0778-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0778-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0778-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0778-140">입력</span><span class="sxs-lookup"><span data-stu-id="d0778-140">INPUTS</span></span>

### <span data-ttu-id="d0778-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="d0778-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d0778-142">출력</span><span class="sxs-lookup"><span data-stu-id="d0778-142">OUTPUTS</span></span>

### <span data-ttu-id="d0778-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="d0778-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="d0778-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d0778-144">NOTES</span></span>

## <span data-ttu-id="d0778-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0778-145">RELATED LINKS</span></span>
