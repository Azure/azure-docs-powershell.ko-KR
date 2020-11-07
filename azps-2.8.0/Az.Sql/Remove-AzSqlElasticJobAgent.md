---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 5f8b237a6f7d08fc0339d3ba34d253bc457dd49f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873856"
---
# <span data-ttu-id="68b47-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="68b47-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="68b47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68b47-102">SYNOPSIS</span></span>
<span data-ttu-id="68b47-103">탄력적 작업 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="68b47-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68b47-104">SYNTAX</span></span>

### <span data-ttu-id="68b47-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="68b47-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b47-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="68b47-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68b47-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="68b47-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68b47-108">설명은</span><span class="sxs-lookup"><span data-stu-id="68b47-108">DESCRIPTION</span></span>
<span data-ttu-id="68b47-109">Remove-AzSqlElasticJobAgent cmdlet은 탄력적 작업 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="68b47-110">예제의</span><span class="sxs-lookup"><span data-stu-id="68b47-110">EXAMPLES</span></span>

### <span data-ttu-id="68b47-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="68b47-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="68b47-112">탄력적 작업 에이전트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="68b47-113">변수</span><span class="sxs-lookup"><span data-stu-id="68b47-113">PARAMETERS</span></span>

### <span data-ttu-id="68b47-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b47-114">-DefaultProfile</span></span>
<span data-ttu-id="68b47-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68b47-116">-Force</span><span class="sxs-lookup"><span data-stu-id="68b47-116">-Force</span></span>
<span data-ttu-id="68b47-117">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="68b47-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="68b47-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68b47-118">-InputObject</span></span>
<span data-ttu-id="68b47-119">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="68b47-119">The agent object</span></span>

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

### <span data-ttu-id="68b47-120">-이름</span><span class="sxs-lookup"><span data-stu-id="68b47-120">-Name</span></span>
<span data-ttu-id="68b47-121">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="68b47-121">The agent name</span></span>

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

### <span data-ttu-id="68b47-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b47-122">-ResourceGroupName</span></span>
<span data-ttu-id="68b47-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="68b47-123">The resource group name</span></span>

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

### <span data-ttu-id="68b47-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68b47-124">-ResourceId</span></span>
<span data-ttu-id="68b47-125">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="68b47-125">The agent resource id</span></span>

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

### <span data-ttu-id="68b47-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="68b47-126">-ServerName</span></span>
<span data-ttu-id="68b47-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="68b47-127">The server name</span></span>

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

### <span data-ttu-id="68b47-128">-확인</span><span class="sxs-lookup"><span data-stu-id="68b47-128">-Confirm</span></span>
<span data-ttu-id="68b47-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68b47-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68b47-130">-WhatIf</span></span>
<span data-ttu-id="68b47-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68b47-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68b47-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b47-133">CommonParameters</span></span>
<span data-ttu-id="68b47-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68b47-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b47-135">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="68b47-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b47-136">입력</span><span class="sxs-lookup"><span data-stu-id="68b47-136">INPUTS</span></span>

### <span data-ttu-id="68b47-137">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="68b47-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="68b47-138">출력</span><span class="sxs-lookup"><span data-stu-id="68b47-138">OUTPUTS</span></span>

### <span data-ttu-id="68b47-139">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="68b47-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="68b47-140">상속자</span><span class="sxs-lookup"><span data-stu-id="68b47-140">NOTES</span></span>

## <span data-ttu-id="68b47-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68b47-141">RELATED LINKS</span></span>
