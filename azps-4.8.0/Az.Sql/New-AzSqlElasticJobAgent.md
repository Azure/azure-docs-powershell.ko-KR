---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobAgent.md
ms.openlocfilehash: f00c2e9cb7b9d0d35efdf99a6f81f24488dd8387
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204816"
---
# <span data-ttu-id="214d2-101">New-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="214d2-101">New-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="214d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="214d2-102">SYNOPSIS</span></span>
<span data-ttu-id="214d2-103">새 탄력적 작업 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-103">Creates a new elastic job agent</span></span>

## <span data-ttu-id="214d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="214d2-104">SYNTAX</span></span>

### <span data-ttu-id="214d2-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="214d2-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-Name] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="214d2-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="214d2-106">ObjectSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseObject] <AzureSqlDatabaseModel> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="214d2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="214d2-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobAgent [-DatabaseResourceId] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="214d2-108">DESCRIPTION</span></span>
<span data-ttu-id="214d2-109">New-AzSqlElasticJobAgent cmdlet은 새 탄력적인 작업 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-109">The New-AzSqlElasticJobAgent cmdlet creates a new Elastic Job agent</span></span>

## <span data-ttu-id="214d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="214d2-110">EXAMPLES</span></span>

### <span data-ttu-id="214d2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="214d2-111">Example 1</span></span>
```
PS C:\> New-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -DatabaseName jobdb -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="214d2-112">새 탄력적 작업 에이전트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-112">Creates a new Elastic Job agent</span></span>

## <span data-ttu-id="214d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="214d2-113">PARAMETERS</span></span>

### <span data-ttu-id="214d2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="214d2-114">-DatabaseName</span></span>
<span data-ttu-id="214d2-115">데이터베이스 이름</span><span class="sxs-lookup"><span data-stu-id="214d2-115">The database name</span></span>

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

### <span data-ttu-id="214d2-116">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="214d2-116">-DatabaseObject</span></span>
<span data-ttu-id="214d2-117">에이전트 컨트롤 데이터베이스 개체</span><span class="sxs-lookup"><span data-stu-id="214d2-117">The Agent Control Database Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="214d2-118">-DatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="214d2-118">-DatabaseResourceId</span></span>
<span data-ttu-id="214d2-119">에이전트 컨트롤 데이터베이스 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="214d2-119">The Agent Control Database Resource Id</span></span>

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

### <span data-ttu-id="214d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214d2-120">-DefaultProfile</span></span>
<span data-ttu-id="214d2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214d2-122">-이름</span><span class="sxs-lookup"><span data-stu-id="214d2-122">-Name</span></span>
<span data-ttu-id="214d2-123">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="214d2-123">The Agent Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214d2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="214d2-124">-ResourceGroupName</span></span>
<span data-ttu-id="214d2-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="214d2-125">The resource group name</span></span>

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

### <span data-ttu-id="214d2-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="214d2-126">-ServerName</span></span>
<span data-ttu-id="214d2-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="214d2-127">The server name</span></span>

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

### <span data-ttu-id="214d2-128">태그</span><span class="sxs-lookup"><span data-stu-id="214d2-128">-Tag</span></span>
<span data-ttu-id="214d2-129">에이전트 태그</span><span class="sxs-lookup"><span data-stu-id="214d2-129">The Agent Tags</span></span>

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

### <span data-ttu-id="214d2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="214d2-130">-Confirm</span></span>
<span data-ttu-id="214d2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214d2-132">-WhatIf</span></span>
<span data-ttu-id="214d2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214d2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214d2-135">CommonParameters</span></span>
<span data-ttu-id="214d2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="214d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214d2-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="214d2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214d2-138">입력</span><span class="sxs-lookup"><span data-stu-id="214d2-138">INPUTS</span></span>

### <span data-ttu-id="214d2-139">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="214d2-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="214d2-140">출력</span><span class="sxs-lookup"><span data-stu-id="214d2-140">OUTPUTS</span></span>

### <span data-ttu-id="214d2-141">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="214d2-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="214d2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="214d2-142">NOTES</span></span>

## <span data-ttu-id="214d2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="214d2-143">RELATED LINKS</span></span>
