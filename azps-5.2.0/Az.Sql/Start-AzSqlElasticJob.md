---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342993"
---
# <span data-ttu-id="90c74-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="90c74-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="90c74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c74-102">SYNOPSIS</span></span>
<span data-ttu-id="90c74-103">작업을 시작하고, 상태를 보기 위해 폴링할 수 있는 작업 실행 ID를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="90c74-104">구문</span><span class="sxs-lookup"><span data-stu-id="90c74-104">SYNTAX</span></span>

### <span data-ttu-id="90c74-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="90c74-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90c74-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="90c74-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c74-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="90c74-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90c74-108">설명</span><span class="sxs-lookup"><span data-stu-id="90c74-108">DESCRIPTION</span></span>
<span data-ttu-id="90c74-109">Start-AzSqlElasticJob cmdlet은 새 작업 실행을 반환하는 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="90c74-110">예제</span><span class="sxs-lookup"><span data-stu-id="90c74-110">EXAMPLES</span></span>

### <span data-ttu-id="90c74-111">예제 1 - 새 작업 실행을 반환하는 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="90c74-112">새 작업 실행을 반환하는 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="90c74-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90c74-113">PARAMETERS</span></span>

### <span data-ttu-id="90c74-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="90c74-114">-AgentName</span></span>
<span data-ttu-id="90c74-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="90c74-115">The agent name</span></span>

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

### <span data-ttu-id="90c74-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90c74-116">-AsJob</span></span>
<span data-ttu-id="90c74-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="90c74-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90c74-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c74-118">-DefaultProfile</span></span>
<span data-ttu-id="90c74-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c74-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="90c74-120">-JobName</span></span>
<span data-ttu-id="90c74-121">작업 이름</span><span class="sxs-lookup"><span data-stu-id="90c74-121">The job name</span></span>

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

### <span data-ttu-id="90c74-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="90c74-122">-ParentObject</span></span>
<span data-ttu-id="90c74-123">작업 개체</span><span class="sxs-lookup"><span data-stu-id="90c74-123">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90c74-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="90c74-124">-ParentResourceId</span></span>
<span data-ttu-id="90c74-125">작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="90c74-125">The job resource id</span></span>

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

### <span data-ttu-id="90c74-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90c74-126">-ResourceGroupName</span></span>
<span data-ttu-id="90c74-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="90c74-127">The resource group name</span></span>

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

### <span data-ttu-id="90c74-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90c74-128">-ServerName</span></span>
<span data-ttu-id="90c74-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="90c74-129">The server name</span></span>

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

### <span data-ttu-id="90c74-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="90c74-130">-Wait</span></span>
<span data-ttu-id="90c74-131">작업의 실행이 완료될 때까지 대기할 것을 나타내는 대기 플래그</span><span class="sxs-lookup"><span data-stu-id="90c74-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="90c74-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90c74-132">-Confirm</span></span>
<span data-ttu-id="90c74-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c74-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c74-134">-WhatIf</span></span>
<span data-ttu-id="90c74-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="90c74-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c74-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c74-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c74-137">CommonParameters</span></span>
<span data-ttu-id="90c74-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90c74-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c74-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90c74-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c74-140">입력</span><span class="sxs-lookup"><span data-stu-id="90c74-140">INPUTS</span></span>

### <span data-ttu-id="90c74-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="90c74-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="90c74-142">출력</span><span class="sxs-lookup"><span data-stu-id="90c74-142">OUTPUTS</span></span>

### <span data-ttu-id="90c74-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span><span class="sxs-lookup"><span data-stu-id="90c74-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="90c74-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90c74-144">NOTES</span></span>

## <span data-ttu-id="90c74-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90c74-145">RELATED LINKS</span></span>
