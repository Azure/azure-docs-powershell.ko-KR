---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/stop-Azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticJob.md
ms.openlocfilehash: ff117dfee7f660845389bd62245be4ecfd53b2f7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878714"
---
# <span data-ttu-id="a4886-101">Stop-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="a4886-101">Stop-AzSqlElasticJob</span></span>

## <span data-ttu-id="a4886-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4886-102">SYNOPSIS</span></span>
<span data-ttu-id="a4886-103">작업 실행 id가 지정 된 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-103">Stops a job given it's job execution id</span></span>

## <span data-ttu-id="a4886-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4886-104">SYNTAX</span></span>

### <span data-ttu-id="a4886-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4886-105">DefaultSet (Default)</span></span>
```
Stop-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -JobExecutionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4886-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="a4886-106">ObjectSet</span></span>
```
Stop-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobExecutionModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4886-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4886-107">ResourceIdSet</span></span>
```
Stop-AzSqlElasticJob [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4886-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a4886-108">DESCRIPTION</span></span>
<span data-ttu-id="a4886-109">Stop-AzSqlElasticJob cmdlet은 실행 중인 실행에 대 한 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-109">The Stop-AzSqlElasticJob cmdlet stops a job's with a running execution.</span></span>
<span data-ttu-id="a4886-110">작업 실행의 현재 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-110">Returns the current status of the job execution</span></span>

## <span data-ttu-id="a4886-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a4886-111">EXAMPLES</span></span>

### <span data-ttu-id="a4886-112">예제 1-실행 중인 작업 실행을 사용 하 여 작업 중지</span><span class="sxs-lookup"><span data-stu-id="a4886-112">Example 1 - Stops a job with a running job execution</span></span>
```
PS C:\> $je = Get-AzSqlElasticJobExecution -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -JobExecutionId dab0ebe8-fd52-42e9-bacf-e5f27577039b
$je | Stop-AzSqlElasticJob
JobName JobExecutionId                       Lifecycle                    StartTime            EndTime
------- --------------                       ---------                    ---------            -------
job1    dab0ebe8-fd52-42e9-bacf-e5f27577039b WaitingForChildJobExecutions 6/1/2018 10:13:56 PM
```

<span data-ttu-id="a4886-113">실행 중인 작업 실행을 중지 하 고 현재 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-113">Stops a running job execution and returns it's current status</span></span>

## <span data-ttu-id="a4886-114">변수</span><span class="sxs-lookup"><span data-stu-id="a4886-114">PARAMETERS</span></span>

### <span data-ttu-id="a4886-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a4886-115">-AgentName</span></span>
<span data-ttu-id="a4886-116">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="a4886-116">The agent name</span></span>

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

### <span data-ttu-id="a4886-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4886-117">-DefaultProfile</span></span>
<span data-ttu-id="a4886-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4886-119">-JobExecutionId</span><span class="sxs-lookup"><span data-stu-id="a4886-119">-JobExecutionId</span></span>
<span data-ttu-id="a4886-120">작업 실행 id입니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-120">The job execution id.</span></span>

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

### <span data-ttu-id="a4886-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="a4886-121">-JobName</span></span>
<span data-ttu-id="a4886-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="a4886-122">The job name</span></span>

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

### <span data-ttu-id="a4886-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a4886-123">-ParentObject</span></span>
<span data-ttu-id="a4886-124">에이전트 컨트롤 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="a4886-124">The Agent Control Database Object</span></span>

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

### <span data-ttu-id="a4886-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a4886-125">-ParentResourceId</span></span>
<span data-ttu-id="a4886-126">작업 실행 리소스 id</span><span class="sxs-lookup"><span data-stu-id="a4886-126">The job execution resource id</span></span>

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

### <span data-ttu-id="a4886-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4886-127">-ResourceGroupName</span></span>
<span data-ttu-id="a4886-128">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="a4886-128">The resource group name</span></span>

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

### <span data-ttu-id="a4886-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a4886-129">-ServerName</span></span>
<span data-ttu-id="a4886-130">서버 이름</span><span class="sxs-lookup"><span data-stu-id="a4886-130">The server name</span></span>

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

### <span data-ttu-id="a4886-131">-확인</span><span class="sxs-lookup"><span data-stu-id="a4886-131">-Confirm</span></span>
<span data-ttu-id="a4886-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4886-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4886-133">-WhatIf</span></span>
<span data-ttu-id="a4886-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4886-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4886-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4886-136">CommonParameters</span></span>
<span data-ttu-id="a4886-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4886-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4886-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4886-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4886-139">입력</span><span class="sxs-lookup"><span data-stu-id="a4886-139">INPUTS</span></span>

### <span data-ttu-id="a4886-140">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a4886-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="a4886-141">출력</span><span class="sxs-lookup"><span data-stu-id="a4886-141">OUTPUTS</span></span>

### <span data-ttu-id="a4886-142">ElasticJobs. AzureSqlElasticJobExecutionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a4886-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobExecutionModel</span></span>

## <span data-ttu-id="a4886-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a4886-143">NOTES</span></span>

## <span data-ttu-id="a4886-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4886-144">RELATED LINKS</span></span>
