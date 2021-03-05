---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 9a80504f1b3aff814d50b5b4aba98b488d1e55b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970219"
---
# <span data-ttu-id="8894e-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="8894e-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="8894e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8894e-102">SYNOPSIS</span></span>
<span data-ttu-id="8894e-103">새 대상 그룹 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-103">Creates a new target group</span></span>

## <span data-ttu-id="8894e-104">구문</span><span class="sxs-lookup"><span data-stu-id="8894e-104">SYNTAX</span></span>

### <span data-ttu-id="8894e-105">DefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="8894e-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8894e-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8894e-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8894e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8894e-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8894e-108">설명</span><span class="sxs-lookup"><span data-stu-id="8894e-108">DESCRIPTION</span></span>
<span data-ttu-id="8894e-109">New-AzSqlElasticJobTargetGroup cmdlet에서 새 대상 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="8894e-110">예제</span><span class="sxs-lookup"><span data-stu-id="8894e-110">EXAMPLES</span></span>

### <span data-ttu-id="8894e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8894e-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="8894e-112">빈 대상 그룹 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-112">Creates an empty target group</span></span>

## <span data-ttu-id="8894e-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8894e-113">PARAMETERS</span></span>

### <span data-ttu-id="8894e-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8894e-114">-AgentName</span></span>
<span data-ttu-id="8894e-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="8894e-115">The agent name</span></span>

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

### <span data-ttu-id="8894e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8894e-116">-DefaultProfile</span></span>
<span data-ttu-id="8894e-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8894e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8894e-118">-Name</span></span>
<span data-ttu-id="8894e-119">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8894e-119">The target group name</span></span>

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

### <span data-ttu-id="8894e-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8894e-120">-ParentObject</span></span>
<span data-ttu-id="8894e-121">에이전트 입력 개체</span><span class="sxs-lookup"><span data-stu-id="8894e-121">The agent input object</span></span>

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

### <span data-ttu-id="8894e-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8894e-122">-ParentResourceId</span></span>
<span data-ttu-id="8894e-123">에이전트 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="8894e-123">The agent resource id</span></span>

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

### <span data-ttu-id="8894e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8894e-124">-ResourceGroupName</span></span>
<span data-ttu-id="8894e-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8894e-125">The resource group name</span></span>

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

### <span data-ttu-id="8894e-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8894e-126">-ServerName</span></span>
<span data-ttu-id="8894e-127">서버 이름</span><span class="sxs-lookup"><span data-stu-id="8894e-127">The server name</span></span>

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

### <span data-ttu-id="8894e-128">-확인</span><span class="sxs-lookup"><span data-stu-id="8894e-128">-Confirm</span></span>
<span data-ttu-id="8894e-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8894e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8894e-130">-WhatIf</span></span>
<span data-ttu-id="8894e-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8894e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8894e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8894e-133">CommonParameters</span></span>
<span data-ttu-id="8894e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8894e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8894e-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8894e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8894e-136">입력</span><span class="sxs-lookup"><span data-stu-id="8894e-136">INPUTS</span></span>

### <span data-ttu-id="8894e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8894e-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8894e-138">출력</span><span class="sxs-lookup"><span data-stu-id="8894e-138">OUTPUTS</span></span>

### <span data-ttu-id="8894e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="8894e-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="8894e-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8894e-140">NOTES</span></span>

## <span data-ttu-id="8894e-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8894e-141">RELATED LINKS</span></span>
