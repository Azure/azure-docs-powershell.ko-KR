---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879654"
---
# <span data-ttu-id="9056b-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="9056b-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="9056b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9056b-102">SYNOPSIS</span></span>
<span data-ttu-id="9056b-103">하나 이상의 작업 대상 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9056b-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="9056b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9056b-104">SYNTAX</span></span>

### <span data-ttu-id="9056b-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9056b-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9056b-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="9056b-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9056b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9056b-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9056b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9056b-108">DESCRIPTION</span></span>
<span data-ttu-id="9056b-109">Get-AzSqlElasticJobTargetGroup cmdlet은 대상 그룹과 해당 대상을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9056b-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="9056b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9056b-110">EXAMPLES</span></span>

### <span data-ttu-id="9056b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9056b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="9056b-112">대상 그룹과 해당 대상을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9056b-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="9056b-113">변수</span><span class="sxs-lookup"><span data-stu-id="9056b-113">PARAMETERS</span></span>

### <span data-ttu-id="9056b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9056b-114">-AgentName</span></span>
<span data-ttu-id="9056b-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="9056b-115">The agent name</span></span>

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

### <span data-ttu-id="9056b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9056b-116">-DefaultProfile</span></span>
<span data-ttu-id="9056b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9056b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9056b-118">-이름</span><span class="sxs-lookup"><span data-stu-id="9056b-118">-Name</span></span>
<span data-ttu-id="9056b-119">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9056b-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9056b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9056b-120">-ParentObject</span></span>
<span data-ttu-id="9056b-121">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="9056b-121">The agent object</span></span>

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

### <span data-ttu-id="9056b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9056b-122">-ParentResourceId</span></span>
<span data-ttu-id="9056b-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="9056b-123">The agent resource id</span></span>

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

### <span data-ttu-id="9056b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9056b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9056b-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9056b-125">The resource group name</span></span>

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

### <span data-ttu-id="9056b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9056b-126">-ServerName</span></span>
<span data-ttu-id="9056b-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="9056b-127">The server name</span></span>

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

### <span data-ttu-id="9056b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9056b-128">CommonParameters</span></span>
<span data-ttu-id="9056b-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9056b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9056b-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9056b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9056b-131">입력</span><span class="sxs-lookup"><span data-stu-id="9056b-131">INPUTS</span></span>

### <span data-ttu-id="9056b-132">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9056b-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="9056b-133">출력</span><span class="sxs-lookup"><span data-stu-id="9056b-133">OUTPUTS</span></span>

### <span data-ttu-id="9056b-134">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9056b-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="9056b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="9056b-135">NOTES</span></span>

## <span data-ttu-id="9056b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9056b-136">RELATED LINKS</span></span>
