---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: c65c7a74d4b2edfcddf8b4e08ee3e538c32d31df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986351"
---
# <span data-ttu-id="e6f71-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="e6f71-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="e6f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6f71-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f71-103">탄력적 작업 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6f71-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="e6f71-104">구문</span><span class="sxs-lookup"><span data-stu-id="e6f71-104">SYNTAX</span></span>

### <span data-ttu-id="e6f71-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e6f71-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f71-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e6f71-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f71-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e6f71-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f71-108">설명</span><span class="sxs-lookup"><span data-stu-id="e6f71-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f71-109">Set-AzSqlElasticJobAgent cmdlet은 Elastic Job 에이전트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="e6f71-110">예제</span><span class="sxs-lookup"><span data-stu-id="e6f71-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f71-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e6f71-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="e6f71-112">탄력적 작업 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="e6f71-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="e6f71-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e6f71-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f71-114">-DefaultProfile</span></span>
<span data-ttu-id="e6f71-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f71-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f71-116">-InputObject</span></span>
<span data-ttu-id="e6f71-117">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="e6f71-117">The agent input object</span></span>

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

### <span data-ttu-id="e6f71-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e6f71-118">-Name</span></span>
<span data-ttu-id="e6f71-119">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="e6f71-119">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f71-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6f71-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e6f71-121">The resource group name</span></span>

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

### <span data-ttu-id="e6f71-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f71-122">-ResourceId</span></span>
<span data-ttu-id="e6f71-123">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e6f71-123">The agent resource id</span></span>

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

### <span data-ttu-id="e6f71-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e6f71-124">-ServerName</span></span>
<span data-ttu-id="e6f71-125">서버 이름</span><span class="sxs-lookup"><span data-stu-id="e6f71-125">The server name</span></span>

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

### <span data-ttu-id="e6f71-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6f71-126">-Tag</span></span>
<span data-ttu-id="e6f71-127">Azure SQL 데이터베이스 에이전트와 연결하기 위한 태그</span><span class="sxs-lookup"><span data-stu-id="e6f71-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f71-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e6f71-128">-Confirm</span></span>
<span data-ttu-id="e6f71-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f71-130">-WhatIf</span></span>
<span data-ttu-id="e6f71-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6f71-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f71-133">CommonParameters</span></span>
<span data-ttu-id="e6f71-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e6f71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f71-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6f71-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f71-136">입력</span><span class="sxs-lookup"><span data-stu-id="e6f71-136">INPUTS</span></span>

### <span data-ttu-id="e6f71-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e6f71-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e6f71-138">출력</span><span class="sxs-lookup"><span data-stu-id="e6f71-138">OUTPUTS</span></span>

### <span data-ttu-id="e6f71-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="e6f71-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e6f71-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e6f71-140">NOTES</span></span>

## <span data-ttu-id="e6f71-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e6f71-141">RELATED LINKS</span></span>
