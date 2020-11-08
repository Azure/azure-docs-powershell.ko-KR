---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044256"
---
# <span data-ttu-id="79903-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="79903-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="79903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79903-102">SYNOPSIS</span></span>
<span data-ttu-id="79903-103">새 대상 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79903-103">Creates a new target group</span></span>

## <span data-ttu-id="79903-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79903-104">SYNTAX</span></span>

### <span data-ttu-id="79903-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="79903-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79903-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="79903-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79903-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="79903-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79903-108">설명은</span><span class="sxs-lookup"><span data-stu-id="79903-108">DESCRIPTION</span></span>
<span data-ttu-id="79903-109">New-AzSqlElasticJobTargetGroup cmdlet은 새 대상 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79903-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="79903-110">예제의</span><span class="sxs-lookup"><span data-stu-id="79903-110">EXAMPLES</span></span>

### <span data-ttu-id="79903-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="79903-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="79903-112">빈 대상 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79903-112">Creates an empty target group</span></span>

## <span data-ttu-id="79903-113">변수</span><span class="sxs-lookup"><span data-stu-id="79903-113">PARAMETERS</span></span>

### <span data-ttu-id="79903-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="79903-114">-AgentName</span></span>
<span data-ttu-id="79903-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="79903-115">The agent name</span></span>

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

### <span data-ttu-id="79903-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79903-116">-DefaultProfile</span></span>
<span data-ttu-id="79903-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79903-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79903-118">-이름</span><span class="sxs-lookup"><span data-stu-id="79903-118">-Name</span></span>
<span data-ttu-id="79903-119">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="79903-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79903-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79903-120">-ParentObject</span></span>
<span data-ttu-id="79903-121">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="79903-121">The agent input object</span></span>

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

### <span data-ttu-id="79903-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79903-122">-ParentResourceId</span></span>
<span data-ttu-id="79903-123">에이전트 리소스 id</span><span class="sxs-lookup"><span data-stu-id="79903-123">The agent resource id</span></span>

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

### <span data-ttu-id="79903-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79903-124">-ResourceGroupName</span></span>
<span data-ttu-id="79903-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="79903-125">The resource group name</span></span>

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

### <span data-ttu-id="79903-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79903-126">-ServerName</span></span>
<span data-ttu-id="79903-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="79903-127">The server name</span></span>

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

### <span data-ttu-id="79903-128">-확인</span><span class="sxs-lookup"><span data-stu-id="79903-128">-Confirm</span></span>
<span data-ttu-id="79903-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79903-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79903-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79903-130">-WhatIf</span></span>
<span data-ttu-id="79903-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79903-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79903-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79903-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79903-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79903-133">CommonParameters</span></span>
<span data-ttu-id="79903-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79903-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79903-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79903-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79903-136">입력</span><span class="sxs-lookup"><span data-stu-id="79903-136">INPUTS</span></span>

### <span data-ttu-id="79903-137">ElasticJobs. AzureSqlElasticJobAgentModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="79903-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="79903-138">출력</span><span class="sxs-lookup"><span data-stu-id="79903-138">OUTPUTS</span></span>

### <span data-ttu-id="79903-139">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="79903-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="79903-140">상속자</span><span class="sxs-lookup"><span data-stu-id="79903-140">NOTES</span></span>

## <span data-ttu-id="79903-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79903-141">RELATED LINKS</span></span>
