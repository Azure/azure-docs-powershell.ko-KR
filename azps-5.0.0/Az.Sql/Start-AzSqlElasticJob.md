---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/start-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlElasticJob.md
ms.openlocfilehash: 5ab6b7e6e77fcfcf470c67bfdd8e300ddc4343ea
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307838"
---
# <span data-ttu-id="69c5a-101">Start-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="69c5a-101">Start-AzSqlElasticJob</span></span>

## <span data-ttu-id="69c5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69c5a-102">SYNOPSIS</span></span>
<span data-ttu-id="69c5a-103">작업을 시작 하 고, 상태를 보기 위해 폴링할 수 있는 작업 실행 id를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-103">Starts a job, returning a job execution id that can be polled to view it's status</span></span>

## <span data-ttu-id="69c5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69c5a-104">SYNTAX</span></span>

### <span data-ttu-id="69c5a-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="69c5a-105">DefaultSet (Default)</span></span>
```
Start-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69c5a-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="69c5a-106">ObjectSet</span></span>
```
Start-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobModel> [-Wait] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69c5a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69c5a-107">ResourceIdSet</span></span>
```
Start-AzSqlElasticJob [-ParentResourceId] <String> [-Wait] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c5a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="69c5a-108">DESCRIPTION</span></span>
<span data-ttu-id="69c5a-109">Start-AzSqlElasticJob cmdlet은 새 작업 실행을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-109">The Start-AzSqlElasticJob cmdlet starts a job returning a new job execution</span></span>

## <span data-ttu-id="69c5a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="69c5a-110">EXAMPLES</span></span>

### <span data-ttu-id="69c5a-111">예제 1-새 작업 실행을 반환 하는 작업 시작</span><span class="sxs-lookup"><span data-stu-id="69c5a-111">Example 1 - Starts a job returning a new job execution</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Start-AzSqlElasticJob

JobName JobExecutionId                       Lifecycle StartTime EndTime
------- --------------                       --------- --------- -------
job1    b93b3a90-987b-4565-b3d3-5fa1751fa9bc Created
```

<span data-ttu-id="69c5a-112">새 작업 실행을 반환 하는 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-112">Starts a job returning a new job execution</span></span>

## <span data-ttu-id="69c5a-113">변수</span><span class="sxs-lookup"><span data-stu-id="69c5a-113">PARAMETERS</span></span>

### <span data-ttu-id="69c5a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="69c5a-114">-AgentName</span></span>
<span data-ttu-id="69c5a-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="69c5a-115">The agent name</span></span>

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

### <span data-ttu-id="69c5a-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69c5a-116">-AsJob</span></span>
<span data-ttu-id="69c5a-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="69c5a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69c5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c5a-118">-DefaultProfile</span></span>
<span data-ttu-id="69c5a-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69c5a-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="69c5a-120">-JobName</span></span>
<span data-ttu-id="69c5a-121">작업 이름</span><span class="sxs-lookup"><span data-stu-id="69c5a-121">The job name</span></span>

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

### <span data-ttu-id="69c5a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69c5a-122">-ParentObject</span></span>
<span data-ttu-id="69c5a-123">작업 개체</span><span class="sxs-lookup"><span data-stu-id="69c5a-123">The job object</span></span>

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

### <span data-ttu-id="69c5a-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69c5a-124">-ParentResourceId</span></span>
<span data-ttu-id="69c5a-125">작업 리소스 id</span><span class="sxs-lookup"><span data-stu-id="69c5a-125">The job resource id</span></span>

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

### <span data-ttu-id="69c5a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69c5a-126">-ResourceGroupName</span></span>
<span data-ttu-id="69c5a-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="69c5a-127">The resource group name</span></span>

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

### <span data-ttu-id="69c5a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="69c5a-128">-ServerName</span></span>
<span data-ttu-id="69c5a-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="69c5a-129">The server name</span></span>

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

### <span data-ttu-id="69c5a-130">-대기</span><span class="sxs-lookup"><span data-stu-id="69c5a-130">-Wait</span></span>
<span data-ttu-id="69c5a-131">작업 실행이 완료 될 때까지 대기 하는 대기 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-131">The wait flag to indicate to wait until the job's execution is done</span></span>

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

### <span data-ttu-id="69c5a-132">-확인</span><span class="sxs-lookup"><span data-stu-id="69c5a-132">-Confirm</span></span>
<span data-ttu-id="69c5a-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c5a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c5a-134">-WhatIf</span></span>
<span data-ttu-id="69c5a-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69c5a-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c5a-137">CommonParameters</span></span>
<span data-ttu-id="69c5a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69c5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c5a-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69c5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c5a-140">입력</span><span class="sxs-lookup"><span data-stu-id="69c5a-140">INPUTS</span></span>

### <span data-ttu-id="69c5a-141">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="69c5a-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="69c5a-142">출력</span><span class="sxs-lookup"><span data-stu-id="69c5a-142">OUTPUTS</span></span>

### <span data-ttu-id="69c5a-143">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="69c5a-143">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="69c5a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="69c5a-144">NOTES</span></span>

## <span data-ttu-id="69c5a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69c5a-145">RELATED LINKS</span></span>
