---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056964"
---
# <span data-ttu-id="340fc-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="340fc-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="340fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340fc-102">SYNOPSIS</span></span>
<span data-ttu-id="340fc-103">Azure SQL 탄력적 작업 에이전트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="340fc-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="340fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="340fc-104">SYNTAX</span></span>

### <span data-ttu-id="340fc-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="340fc-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="340fc-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="340fc-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="340fc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="340fc-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="340fc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="340fc-108">DESCRIPTION</span></span>
<span data-ttu-id="340fc-109">Get-AzSqlElasticJobAgent cmdlet은 하나 이상의 탄력적 작업 에이전트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="340fc-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="340fc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="340fc-110">EXAMPLES</span></span>

### <span data-ttu-id="340fc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="340fc-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="340fc-112">탄력적 작업 에이전트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="340fc-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="340fc-113">변수</span><span class="sxs-lookup"><span data-stu-id="340fc-113">PARAMETERS</span></span>

### <span data-ttu-id="340fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340fc-114">-DefaultProfile</span></span>
<span data-ttu-id="340fc-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="340fc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340fc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="340fc-116">-Name</span></span>
<span data-ttu-id="340fc-117">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="340fc-117">The agent name</span></span>

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

### <span data-ttu-id="340fc-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="340fc-118">-ParentObject</span></span>
<span data-ttu-id="340fc-119">서버 입력 개체</span><span class="sxs-lookup"><span data-stu-id="340fc-119">The server input object</span></span>

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

### <span data-ttu-id="340fc-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="340fc-120">-ParentResourceId</span></span>
<span data-ttu-id="340fc-121">서버 리소스 id</span><span class="sxs-lookup"><span data-stu-id="340fc-121">The server resource id</span></span>

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

### <span data-ttu-id="340fc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340fc-122">-ResourceGroupName</span></span>
<span data-ttu-id="340fc-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="340fc-123">The resource group name</span></span>

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

### <span data-ttu-id="340fc-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="340fc-124">-ServerName</span></span>
<span data-ttu-id="340fc-125">서버 이름</span><span class="sxs-lookup"><span data-stu-id="340fc-125">The server name</span></span>

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

### <span data-ttu-id="340fc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340fc-126">CommonParameters</span></span>
<span data-ttu-id="340fc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="340fc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340fc-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="340fc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340fc-129">입력</span><span class="sxs-lookup"><span data-stu-id="340fc-129">INPUTS</span></span>

### <span data-ttu-id="340fc-130">AzureSqlServerModel를 통해 서의 명령</span><span class="sxs-lookup"><span data-stu-id="340fc-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="340fc-131">출력</span><span class="sxs-lookup"><span data-stu-id="340fc-131">OUTPUTS</span></span>

### <span data-ttu-id="340fc-132">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="340fc-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="340fc-133">상속자</span><span class="sxs-lookup"><span data-stu-id="340fc-133">NOTES</span></span>

## <span data-ttu-id="340fc-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="340fc-134">RELATED LINKS</span></span>
