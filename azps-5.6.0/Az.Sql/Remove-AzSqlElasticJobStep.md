---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: 788817dd9ca344501dc25bad48b71b7e24b653d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955184"
---
# <span data-ttu-id="d1046-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="d1046-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="d1046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1046-102">SYNOPSIS</span></span>
<span data-ttu-id="d1046-103">작업 단계를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-103">Removes the job step</span></span>

## <span data-ttu-id="d1046-104">구문</span><span class="sxs-lookup"><span data-stu-id="d1046-104">SYNTAX</span></span>

### <span data-ttu-id="d1046-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d1046-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1046-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1046-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1046-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d1046-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1046-108">설명</span><span class="sxs-lookup"><span data-stu-id="d1046-108">DESCRIPTION</span></span>
<span data-ttu-id="d1046-109">Remove-AzSqlElasticJobStep cmdlet은 작업에서 작업 단계를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="d1046-110">예제</span><span class="sxs-lookup"><span data-stu-id="d1046-110">EXAMPLES</span></span>

### <span data-ttu-id="d1046-111">예제 1: 작업에서 작업 단계를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="d1046-112">작업에서 작업 단계를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-112">Removes a job step from a job</span></span>

### <span data-ttu-id="d1046-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d1046-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="d1046-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1046-114">PARAMETERS</span></span>

### <span data-ttu-id="d1046-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d1046-115">-AgentName</span></span>
<span data-ttu-id="d1046-116">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="d1046-116">The agent name</span></span>

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

### <span data-ttu-id="d1046-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1046-117">-DefaultProfile</span></span>
<span data-ttu-id="d1046-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1046-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1046-119">-InputObject</span></span>
<span data-ttu-id="d1046-120">작업 단계 입력 개체</span><span class="sxs-lookup"><span data-stu-id="d1046-120">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1046-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="d1046-121">-JobName</span></span>
<span data-ttu-id="d1046-122">작업 이름</span><span class="sxs-lookup"><span data-stu-id="d1046-122">The job name</span></span>

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

### <span data-ttu-id="d1046-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d1046-123">-Name</span></span>
<span data-ttu-id="d1046-124">작업 단계 이름</span><span class="sxs-lookup"><span data-stu-id="d1046-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1046-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1046-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1046-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d1046-126">The resource group name</span></span>

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

### <span data-ttu-id="d1046-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1046-127">-ResourceId</span></span>
<span data-ttu-id="d1046-128">작업 단계 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d1046-128">The job step resource id</span></span>

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

### <span data-ttu-id="d1046-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d1046-129">-ServerName</span></span>
<span data-ttu-id="d1046-130">서버 이름</span><span class="sxs-lookup"><span data-stu-id="d1046-130">The server name</span></span>

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

### <span data-ttu-id="d1046-131">-확인</span><span class="sxs-lookup"><span data-stu-id="d1046-131">-Confirm</span></span>
<span data-ttu-id="d1046-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1046-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1046-133">-WhatIf</span></span>
<span data-ttu-id="d1046-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1046-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1046-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1046-136">CommonParameters</span></span>
<span data-ttu-id="d1046-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d1046-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1046-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1046-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1046-139">입력</span><span class="sxs-lookup"><span data-stu-id="d1046-139">INPUTS</span></span>

### <span data-ttu-id="d1046-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="d1046-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d1046-141">출력</span><span class="sxs-lookup"><span data-stu-id="d1046-141">OUTPUTS</span></span>

### <span data-ttu-id="d1046-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="d1046-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d1046-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d1046-143">NOTES</span></span>

## <span data-ttu-id="d1046-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1046-144">RELATED LINKS</span></span>
