---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346538"
---
# <span data-ttu-id="6c5e9-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="6c5e9-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="6c5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c5e9-103">Azure SQL 탄력적 작업 에이전트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="6c5e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c5e9-104">SYNTAX</span></span>

### <span data-ttu-id="6c5e9-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6c5e9-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5e9-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c5e9-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c5e9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6c5e9-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c5e9-108">설명</span><span class="sxs-lookup"><span data-stu-id="6c5e9-108">DESCRIPTION</span></span>
<span data-ttu-id="6c5e9-109">Get-AzSqlElasticJobAgent cmdlet은 하나 이상의 탄력적 작업 에이전트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="6c5e9-110">예제</span><span class="sxs-lookup"><span data-stu-id="6c5e9-110">EXAMPLES</span></span>

### <span data-ttu-id="6c5e9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c5e9-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="6c5e9-112">탄력적 작업 에이전트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="6c5e9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c5e9-113">PARAMETERS</span></span>

### <span data-ttu-id="6c5e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c5e9-114">-DefaultProfile</span></span>
<span data-ttu-id="6c5e9-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c5e9-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6c5e9-116">-Name</span></span>
<span data-ttu-id="6c5e9-117">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="6c5e9-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c5e9-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6c5e9-118">-ParentObject</span></span>
<span data-ttu-id="6c5e9-119">서버 입력 개체</span><span class="sxs-lookup"><span data-stu-id="6c5e9-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c5e9-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6c5e9-120">-ParentResourceId</span></span>
<span data-ttu-id="6c5e9-121">서버 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="6c5e9-121">The server resource id</span></span>

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

### <span data-ttu-id="6c5e9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c5e9-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c5e9-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6c5e9-123">The resource group name</span></span>

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

### <span data-ttu-id="6c5e9-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6c5e9-124">-ServerName</span></span>
<span data-ttu-id="6c5e9-125">서버 이름</span><span class="sxs-lookup"><span data-stu-id="6c5e9-125">The server name</span></span>

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

### <span data-ttu-id="6c5e9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c5e9-126">CommonParameters</span></span>
<span data-ttu-id="6c5e9-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c5e9-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6c5e9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c5e9-129">입력</span><span class="sxs-lookup"><span data-stu-id="6c5e9-129">INPUTS</span></span>

### <span data-ttu-id="6c5e9-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="6c5e9-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="6c5e9-131">출력</span><span class="sxs-lookup"><span data-stu-id="6c5e9-131">OUTPUTS</span></span>

### <span data-ttu-id="6c5e9-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="6c5e9-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="6c5e9-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c5e9-133">NOTES</span></span>

## <span data-ttu-id="6c5e9-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c5e9-134">RELATED LINKS</span></span>
