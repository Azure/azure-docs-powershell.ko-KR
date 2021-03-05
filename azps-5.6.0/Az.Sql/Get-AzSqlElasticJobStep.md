---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: d70a0b6abd31d4104301e877fb21bf1d0589a24f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999659"
---
# <span data-ttu-id="7b375-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="7b375-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="7b375-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b375-102">SYNOPSIS</span></span>
<span data-ttu-id="7b375-103">하나 이상의 작업 단계가 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-103">Gets one or more job steps</span></span>

## <span data-ttu-id="7b375-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b375-104">SYNTAX</span></span>

### <span data-ttu-id="7b375-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7b375-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b375-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="7b375-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b375-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="7b375-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b375-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="7b375-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b375-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7b375-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b375-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b375-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b375-111">설명</span><span class="sxs-lookup"><span data-stu-id="7b375-111">DESCRIPTION</span></span>
<span data-ttu-id="7b375-112">Get-AzSqlElasticJobStep cmdlet은 작업에서 하나 이상의 작업 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="7b375-113">예제</span><span class="sxs-lookup"><span data-stu-id="7b375-113">EXAMPLES</span></span>

### <span data-ttu-id="7b375-114">예제 1: 작업에서 작업 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="7b375-115">작업에서 작업 단계를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-115">Gets a job step from a job</span></span>

## <span data-ttu-id="7b375-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b375-116">PARAMETERS</span></span>

### <span data-ttu-id="7b375-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="7b375-117">-AgentName</span></span>
<span data-ttu-id="7b375-118">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b375-119">-DefaultProfile</span></span>
<span data-ttu-id="7b375-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b375-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="7b375-121">-JobName</span></span>
<span data-ttu-id="7b375-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7b375-123">-Name</span></span>
<span data-ttu-id="7b375-124">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7b375-125">-ParentObject</span></span>
<span data-ttu-id="7b375-126">작업 입력 개체</span><span class="sxs-lookup"><span data-stu-id="7b375-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7b375-127">-ParentResourceId</span></span>
<span data-ttu-id="7b375-128">작업 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7b375-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b375-129">-ResourceGroupName</span></span>
<span data-ttu-id="7b375-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7b375-131">-ServerName</span></span>
<span data-ttu-id="7b375-132">서버 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-133">-Version</span><span class="sxs-lookup"><span data-stu-id="7b375-133">-Version</span></span>
<span data-ttu-id="7b375-134">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="7b375-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b375-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b375-135">CommonParameters</span></span>
<span data-ttu-id="7b375-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b375-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b375-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b375-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b375-138">입력</span><span class="sxs-lookup"><span data-stu-id="7b375-138">INPUTS</span></span>

### <span data-ttu-id="7b375-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="7b375-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="7b375-140">출력</span><span class="sxs-lookup"><span data-stu-id="7b375-140">OUTPUTS</span></span>

### <span data-ttu-id="7b375-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="7b375-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="7b375-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b375-142">NOTES</span></span>

## <span data-ttu-id="7b375-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b375-143">RELATED LINKS</span></span>
