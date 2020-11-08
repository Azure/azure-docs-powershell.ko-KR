---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJob.md
ms.openlocfilehash: 60dac0ad09f30f339da82d84cf6200a44fe11859
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041515"
---
# <span data-ttu-id="efcb4-101">Get-AzSqlElasticJob</span><span class="sxs-lookup"><span data-stu-id="efcb4-101">Get-AzSqlElasticJob</span></span>

## <span data-ttu-id="efcb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efcb4-102">SYNOPSIS</span></span>
<span data-ttu-id="efcb4-103">하나 이상의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-103">Gets one or more jobs</span></span>

## <span data-ttu-id="efcb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efcb4-104">SYNTAX</span></span>

### <span data-ttu-id="efcb4-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="efcb4-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJob [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efcb4-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="efcb4-106">ObjectSet</span></span>
```
Get-AzSqlElasticJob [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efcb4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="efcb4-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJob [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="efcb4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="efcb4-108">DESCRIPTION</span></span>
<span data-ttu-id="efcb4-109">Get-AzSqlElasticJob cmdlet은 하나 이상의 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-109">The Get-AzSqlElasticJob cmdlet gets one or more jobs</span></span>

## <span data-ttu-id="efcb4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="efcb4-110">EXAMPLES</span></span>

### <span data-ttu-id="efcb4-111">예제 1-작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-111">Example 1 - Gets a job</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJob -Name job1

JobName Version Description StartTime           EndTime                ScheduleType Interval Enabled
------- ------- ----------- ---------           -------                ------------ -------- -------
job1    0                   6/1/2018 9:46:29 PM 12/31/9999 11:59:59 AM Once                  False
```

<span data-ttu-id="efcb4-112">작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-112">Gets a job</span></span>

## <span data-ttu-id="efcb4-113">변수</span><span class="sxs-lookup"><span data-stu-id="efcb4-113">PARAMETERS</span></span>

### <span data-ttu-id="efcb4-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="efcb4-114">-AgentName</span></span>
<span data-ttu-id="efcb4-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="efcb4-115">The agent name</span></span>

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

### <span data-ttu-id="efcb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efcb4-116">-DefaultProfile</span></span>
<span data-ttu-id="efcb4-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efcb4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="efcb4-118">-Name</span></span>
<span data-ttu-id="efcb4-119">작업 이름</span><span class="sxs-lookup"><span data-stu-id="efcb4-119">The job name</span></span>

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

### <span data-ttu-id="efcb4-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="efcb4-120">-ParentObject</span></span>
<span data-ttu-id="efcb4-121">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="efcb4-121">The agent input object</span></span>

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

### <span data-ttu-id="efcb4-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="efcb4-122">-ParentResourceId</span></span>
<span data-ttu-id="efcb4-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="efcb4-123">The agent resource id</span></span>

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

### <span data-ttu-id="efcb4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efcb4-124">-ResourceGroupName</span></span>
<span data-ttu-id="efcb4-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="efcb4-125">The resource group name</span></span>

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

### <span data-ttu-id="efcb4-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="efcb4-126">-ServerName</span></span>
<span data-ttu-id="efcb4-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="efcb4-127">The server name</span></span>

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

### <span data-ttu-id="efcb4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efcb4-128">CommonParameters</span></span>
<span data-ttu-id="efcb4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efcb4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efcb4-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="efcb4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efcb4-131">입력</span><span class="sxs-lookup"><span data-stu-id="efcb4-131">INPUTS</span></span>

### <span data-ttu-id="efcb4-132">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="efcb4-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="efcb4-133">출력</span><span class="sxs-lookup"><span data-stu-id="efcb4-133">OUTPUTS</span></span>

### <span data-ttu-id="efcb4-134">ElasticJobs. AzureSqlElasticJobModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="efcb4-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="efcb4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="efcb4-135">NOTES</span></span>

## <span data-ttu-id="efcb4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efcb4-136">RELATED LINKS</span></span>
