---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 13e6a0bd8a4934df4d0426de38d7a56ddd5af19b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873987"
---
# <span data-ttu-id="05892-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="05892-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="05892-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05892-102">SYNOPSIS</span></span>
<span data-ttu-id="05892-103">작업을 시작 하 고, 상태를 보기 위해 폴링할 수 있는 작업 실행 id를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05892-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="05892-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05892-104">SYNTAX</span></span>

### <span data-ttu-id="05892-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="05892-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05892-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="05892-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05892-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="05892-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05892-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05892-108">DESCRIPTION</span></span>
<span data-ttu-id="05892-109">Start-AzSqlElasticJob cmdlet은 새 작업 실행을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="05892-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="05892-110">예제의</span><span class="sxs-lookup"><span data-stu-id="05892-110">EXAMPLES</span></span>

### <span data-ttu-id="05892-111">예제 1-새 작업 실행을 반환 하는 작업 시작</span><span class="sxs-lookup"><span data-stu-id="05892-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="05892-112">새 작업 실행을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="05892-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="05892-113">변수</span><span class="sxs-lookup"><span data-stu-id="05892-113">PARAMETERS</span></span>

### <span data-ttu-id="05892-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="05892-114">-AgentName</span></span>
<span data-ttu-id="05892-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="05892-115">The agent name</span></span>

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

### <span data-ttu-id="05892-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05892-116">-AsJob</span></span>
<span data-ttu-id="05892-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="05892-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05892-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05892-118">-DefaultProfile</span></span>
<span data-ttu-id="05892-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05892-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05892-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="05892-120">-JobName</span></span>
<span data-ttu-id="05892-121">작업 이름</span><span class="sxs-lookup"><span data-stu-id="05892-121">The job name</span></span>

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

### <span data-ttu-id="05892-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="05892-122">-ParentObject</span></span>
<span data-ttu-id="05892-123">작업 개체</span><span class="sxs-lookup"><span data-stu-id="05892-123">The job object</span></span>

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

### <span data-ttu-id="05892-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="05892-124">-ParentResourceId</span></span>
<span data-ttu-id="05892-125">작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="05892-125">The job resource id</span></span>

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

### <span data-ttu-id="05892-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05892-126">-ResourceGroupName</span></span>
<span data-ttu-id="05892-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="05892-127">The resource group name</span></span>

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

### <span data-ttu-id="05892-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="05892-128">-ServerName</span></span>
<span data-ttu-id="05892-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="05892-129">The server name</span></span>

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

### <span data-ttu-id="05892-130">-대기</span><span class="sxs-lookup"><span data-stu-id="05892-130">-Wait</span></span>
<span data-ttu-id="05892-131">작업 실행이 완료 될 때까지 대기 하는 대기 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="05892-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="05892-132">-확인</span><span class="sxs-lookup"><span data-stu-id="05892-132">-Confirm</span></span>
<span data-ttu-id="05892-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05892-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05892-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05892-134">-WhatIf</span></span>
<span data-ttu-id="05892-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05892-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05892-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05892-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05892-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05892-137">CommonParameters</span></span>
<span data-ttu-id="05892-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05892-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05892-139">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05892-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05892-140">입력</span><span class="sxs-lookup"><span data-stu-id="05892-140">INPUTS</span></span>

### <span data-ttu-id="05892-141">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="05892-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="05892-142">출력</span><span class="sxs-lookup"><span data-stu-id="05892-142">OUTPUTS</span></span>

### <span data-ttu-id="05892-143">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="05892-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="05892-144">상속자</span><span class="sxs-lookup"><span data-stu-id="05892-144">NOTES</span></span>

## <span data-ttu-id="05892-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05892-145">RELATED LINKS</span></span>

## <span data-ttu-id="05892-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05892-146">RELATED LINKS</span></span>
