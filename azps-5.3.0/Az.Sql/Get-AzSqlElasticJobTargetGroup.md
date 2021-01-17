---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: f68baa997fd808a6e31bbb499f621f7ce303a25a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489347"
---
# <span data-ttu-id="24f04-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="24f04-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="24f04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24f04-102">SYNOPSIS</span></span>
<span data-ttu-id="24f04-103">하나 이상의 작업 대상 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f04-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="24f04-104">구문</span><span class="sxs-lookup"><span data-stu-id="24f04-104">SYNTAX</span></span>

### <span data-ttu-id="24f04-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="24f04-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f04-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="24f04-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24f04-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="24f04-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24f04-108">설명</span><span class="sxs-lookup"><span data-stu-id="24f04-108">DESCRIPTION</span></span>
<span data-ttu-id="24f04-109">Get-AzSqlElasticJobTargetGroup cmdlet은 대상 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f04-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="24f04-110">예제</span><span class="sxs-lookup"><span data-stu-id="24f04-110">EXAMPLES</span></span>

### <span data-ttu-id="24f04-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="24f04-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="24f04-112">대상 그룹 및 대상을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="24f04-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="24f04-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="24f04-113">PARAMETERS</span></span>

### <span data-ttu-id="24f04-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="24f04-114">-AgentName</span></span>
<span data-ttu-id="24f04-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="24f04-115">The agent name</span></span>

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

### <span data-ttu-id="24f04-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24f04-116">-DefaultProfile</span></span>
<span data-ttu-id="24f04-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24f04-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24f04-118">-Name</span><span class="sxs-lookup"><span data-stu-id="24f04-118">-Name</span></span>
<span data-ttu-id="24f04-119">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="24f04-119">The target group name</span></span>

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

### <span data-ttu-id="24f04-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="24f04-120">-ParentObject</span></span>
<span data-ttu-id="24f04-121">에이전트 개체</span><span class="sxs-lookup"><span data-stu-id="24f04-121">The agent object</span></span>

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

### <span data-ttu-id="24f04-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="24f04-122">-ParentResourceId</span></span>
<span data-ttu-id="24f04-123">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="24f04-123">The agent resource id</span></span>

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

### <span data-ttu-id="24f04-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24f04-124">-ResourceGroupName</span></span>
<span data-ttu-id="24f04-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="24f04-125">The resource group name</span></span>

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

### <span data-ttu-id="24f04-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="24f04-126">-ServerName</span></span>
<span data-ttu-id="24f04-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="24f04-127">The server name</span></span>

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

### <span data-ttu-id="24f04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24f04-128">CommonParameters</span></span>
<span data-ttu-id="24f04-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="24f04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24f04-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="24f04-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24f04-131">입력</span><span class="sxs-lookup"><span data-stu-id="24f04-131">INPUTS</span></span>

### <span data-ttu-id="24f04-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="24f04-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="24f04-133">출력</span><span class="sxs-lookup"><span data-stu-id="24f04-133">OUTPUTS</span></span>

### <span data-ttu-id="24f04-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="24f04-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="24f04-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="24f04-135">NOTES</span></span>

## <span data-ttu-id="24f04-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24f04-136">RELATED LINKS</span></span>
