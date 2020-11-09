---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309445"
---
# <span data-ttu-id="0d80c-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="0d80c-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="0d80c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d80c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d80c-103">탄력적 작업 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="0d80c-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="0d80c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d80c-104">SYNTAX</span></span>

### <span data-ttu-id="0d80c-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d80c-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d80c-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="0d80c-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d80c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0d80c-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d80c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0d80c-108">DESCRIPTION</span></span>
<span data-ttu-id="0d80c-109">Set-AzSqlElasticJobAgent cmdlet은 탄력적 작업 에이전트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="0d80c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d80c-110">EXAMPLES</span></span>

### <span data-ttu-id="0d80c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d80c-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="0d80c-112">탄력적 작업 에이전트 업데이트</span><span class="sxs-lookup"><span data-stu-id="0d80c-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="0d80c-113">변수</span><span class="sxs-lookup"><span data-stu-id="0d80c-113">PARAMETERS</span></span>

### <span data-ttu-id="0d80c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d80c-114">-DefaultProfile</span></span>
<span data-ttu-id="0d80c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d80c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d80c-116">-InputObject</span></span>
<span data-ttu-id="0d80c-117">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="0d80c-117">The agent input object</span></span>

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

### <span data-ttu-id="0d80c-118">-이름</span><span class="sxs-lookup"><span data-stu-id="0d80c-118">-Name</span></span>
<span data-ttu-id="0d80c-119">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="0d80c-119">The agent name</span></span>

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

### <span data-ttu-id="0d80c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d80c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d80c-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="0d80c-121">The resource group name</span></span>

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

### <span data-ttu-id="0d80c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d80c-122">-ResourceId</span></span>
<span data-ttu-id="0d80c-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="0d80c-123">The agent resource id</span></span>

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

### <span data-ttu-id="0d80c-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0d80c-124">-ServerName</span></span>
<span data-ttu-id="0d80c-125">서버 이름</span><span class="sxs-lookup"><span data-stu-id="0d80c-125">The server name</span></span>

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

### <span data-ttu-id="0d80c-126">태그</span><span class="sxs-lookup"><span data-stu-id="0d80c-126">-Tag</span></span>
<span data-ttu-id="0d80c-127">Azure SQL 데이터베이스 에이전트와 연결할 태그</span><span class="sxs-lookup"><span data-stu-id="0d80c-127">The tags to associate with the Azure SQL Database Agent</span></span>

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

### <span data-ttu-id="0d80c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0d80c-128">-Confirm</span></span>
<span data-ttu-id="0d80c-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d80c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d80c-130">-WhatIf</span></span>
<span data-ttu-id="0d80c-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d80c-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d80c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d80c-133">CommonParameters</span></span>
<span data-ttu-id="0d80c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d80c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d80c-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d80c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d80c-136">입력</span><span class="sxs-lookup"><span data-stu-id="0d80c-136">INPUTS</span></span>

### <span data-ttu-id="0d80c-137">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="0d80c-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0d80c-138">출력</span><span class="sxs-lookup"><span data-stu-id="0d80c-138">OUTPUTS</span></span>

### <span data-ttu-id="0d80c-139">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="0d80c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="0d80c-140">상속자</span><span class="sxs-lookup"><span data-stu-id="0d80c-140">NOTES</span></span>

## <span data-ttu-id="0d80c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d80c-141">RELATED LINKS</span></span>
