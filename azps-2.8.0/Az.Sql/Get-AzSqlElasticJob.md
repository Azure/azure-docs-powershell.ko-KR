---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 688926d05b56234ce11d4524afdcce326c5e09e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873674"
---
# <span data-ttu-id="df419-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="df419-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="df419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df419-102">SYNOPSIS</span></span>
<span data-ttu-id="df419-103">하나 이상의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df419-103">Gets one or more jobs</span></span>

## <span data-ttu-id="df419-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df419-104">SYNTAX</span></span>

### <span data-ttu-id="df419-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="df419-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df419-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="df419-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df419-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df419-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df419-108">설명은</span><span class="sxs-lookup"><span data-stu-id="df419-108">DESCRIPTION</span></span>
<span data-ttu-id="df419-109">Get-AzSqlElasticJob cmdlet은 하나 이상의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df419-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="df419-110">예제의</span><span class="sxs-lookup"><span data-stu-id="df419-110">EXAMPLES</span></span>

### <span data-ttu-id="df419-111">예제 1-작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df419-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="df419-112">작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df419-112">Gets a job</span></span>

## <span data-ttu-id="df419-113">변수</span><span class="sxs-lookup"><span data-stu-id="df419-113">PARAMETERS</span></span>

### <span data-ttu-id="df419-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="df419-114">-AgentName</span></span>
<span data-ttu-id="df419-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="df419-115">The agent name</span></span>

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

### <span data-ttu-id="df419-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df419-116">-DefaultProfile</span></span>
<span data-ttu-id="df419-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df419-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df419-118">-이름</span><span class="sxs-lookup"><span data-stu-id="df419-118">-Name</span></span>
<span data-ttu-id="df419-119">작업 이름</span><span class="sxs-lookup"><span data-stu-id="df419-119">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df419-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="df419-120">-ParentObject</span></span>
<span data-ttu-id="df419-121">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="df419-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df419-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="df419-122">-ParentResourceId</span></span>
<span data-ttu-id="df419-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="df419-123">The agent resource id</span></span>

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

### <span data-ttu-id="df419-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df419-124">-ResourceGroupName</span></span>
<span data-ttu-id="df419-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="df419-125">The resource group name</span></span>

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

### <span data-ttu-id="df419-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="df419-126">-ServerName</span></span>
<span data-ttu-id="df419-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="df419-127">The server name</span></span>

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

### <span data-ttu-id="df419-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df419-128">CommonParameters</span></span>
<span data-ttu-id="df419-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df419-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df419-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df419-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df419-131">입력</span><span class="sxs-lookup"><span data-stu-id="df419-131">INPUTS</span></span>

### <span data-ttu-id="df419-132">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="df419-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="df419-133">출력</span><span class="sxs-lookup"><span data-stu-id="df419-133">OUTPUTS</span></span>

### <span data-ttu-id="df419-134">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="df419-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="df419-135">상속자</span><span class="sxs-lookup"><span data-stu-id="df419-135">NOTES</span></span>

## <span data-ttu-id="df419-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df419-136">RELATED LINKS</span></span>
