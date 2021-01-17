---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353625"
---
# <span data-ttu-id="bd83c-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="bd83c-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="bd83c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd83c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd83c-103">탄력적 작업 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="bd83c-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd83c-104">SYNTAX</span></span>

### <span data-ttu-id="bd83c-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd83c-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd83c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="bd83c-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd83c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bd83c-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd83c-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd83c-108">DESCRIPTION</span></span>
<span data-ttu-id="bd83c-109">Remove-AzSqlElasticJobAgent cmdlet은 탄력적 작업 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="bd83c-110">예제</span><span class="sxs-lookup"><span data-stu-id="bd83c-110">EXAMPLES</span></span>

### <span data-ttu-id="bd83c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bd83c-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="bd83c-112">탄력적 작업 에이전트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="bd83c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd83c-113">PARAMETERS</span></span>

### <span data-ttu-id="bd83c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd83c-114">-DefaultProfile</span></span>
<span data-ttu-id="bd83c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd83c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bd83c-116">-Force</span></span>
<span data-ttu-id="bd83c-117">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="bd83c-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="bd83c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd83c-118">-InputObject</span></span>
<span data-ttu-id="bd83c-119">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="bd83c-119">The agent object</span></span>

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

### <span data-ttu-id="bd83c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bd83c-120">-Name</span></span>
<span data-ttu-id="bd83c-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="bd83c-121">The agent name</span></span>

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

### <span data-ttu-id="bd83c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd83c-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd83c-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bd83c-123">The resource group name</span></span>

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

### <span data-ttu-id="bd83c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd83c-124">-ResourceId</span></span>
<span data-ttu-id="bd83c-125">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bd83c-125">The agent resource id</span></span>

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

### <span data-ttu-id="bd83c-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bd83c-126">-ServerName</span></span>
<span data-ttu-id="bd83c-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="bd83c-127">The server name</span></span>

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

### <span data-ttu-id="bd83c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd83c-128">-Confirm</span></span>
<span data-ttu-id="bd83c-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd83c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd83c-130">-WhatIf</span></span>
<span data-ttu-id="bd83c-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bd83c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd83c-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd83c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd83c-133">CommonParameters</span></span>
<span data-ttu-id="bd83c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd83c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd83c-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bd83c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd83c-136">입력</span><span class="sxs-lookup"><span data-stu-id="bd83c-136">INPUTS</span></span>

### <span data-ttu-id="bd83c-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="bd83c-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="bd83c-138">출력</span><span class="sxs-lookup"><span data-stu-id="bd83c-138">OUTPUTS</span></span>

### <span data-ttu-id="bd83c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="bd83c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="bd83c-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd83c-140">NOTES</span></span>

## <span data-ttu-id="bd83c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd83c-141">RELATED LINKS</span></span>
