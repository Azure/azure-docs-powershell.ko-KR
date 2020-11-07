---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 4652774b07ca3ae58baf29b614bd63519d537a0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873850"
---
# <span data-ttu-id="adec6-101">Remove-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="adec6-101">Remove-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="adec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adec6-102">SYNOPSIS</span></span>
<span data-ttu-id="adec6-103">대상 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-103">Removes the target group</span></span>

## <span data-ttu-id="adec6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="adec6-104">SYNTAX</span></span>

### <span data-ttu-id="adec6-105">DefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="adec6-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adec6-106">엔터티가</span><span class="sxs-lookup"><span data-stu-id="adec6-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-InputObject] <AzureSqlElasticJobTargetGroupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adec6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="adec6-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobTargetGroup [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adec6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="adec6-108">DESCRIPTION</span></span>
<span data-ttu-id="adec6-109">Remove-AzSqlElasticJobTargetGroup cmdlet은 대상 그룹과 해당 대상을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-109">The Remove-AzSqlElasticJobTargetGroup cmdlet removes a target group and it's targets</span></span>

## <span data-ttu-id="adec6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="adec6-110">EXAMPLES</span></span>

### <span data-ttu-id="adec6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="adec6-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent 
$agent | Remove-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="adec6-112">대상 그룹과 해당 대상을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-112">Removes a target group and it's targets</span></span>

## <span data-ttu-id="adec6-113">변수</span><span class="sxs-lookup"><span data-stu-id="adec6-113">PARAMETERS</span></span>

### <span data-ttu-id="adec6-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="adec6-114">-AgentName</span></span>
<span data-ttu-id="adec6-115">에이전트 이름</span><span class="sxs-lookup"><span data-stu-id="adec6-115">The agent name</span></span>

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

### <span data-ttu-id="adec6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adec6-116">-DefaultProfile</span></span>
<span data-ttu-id="adec6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adec6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="adec6-118">-Force</span></span>
<span data-ttu-id="adec6-119">작업 수행을 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="adec6-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="adec6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adec6-120">-InputObject</span></span>
<span data-ttu-id="adec6-121">대상 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="adec6-121">The target group object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adec6-122">-이름</span><span class="sxs-lookup"><span data-stu-id="adec6-122">-Name</span></span>
<span data-ttu-id="adec6-123">대상 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="adec6-123">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adec6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adec6-124">-ResourceGroupName</span></span>
<span data-ttu-id="adec6-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="adec6-125">The resource group name</span></span>

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

### <span data-ttu-id="adec6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adec6-126">-ResourceId</span></span>
<span data-ttu-id="adec6-127">대상 그룹 리소스 id</span><span class="sxs-lookup"><span data-stu-id="adec6-127">The target group resource id</span></span>

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

### <span data-ttu-id="adec6-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="adec6-128">-ServerName</span></span>
<span data-ttu-id="adec6-129">서버 이름</span><span class="sxs-lookup"><span data-stu-id="adec6-129">The server name</span></span>

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

### <span data-ttu-id="adec6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="adec6-130">-Confirm</span></span>
<span data-ttu-id="adec6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adec6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adec6-132">-WhatIf</span></span>
<span data-ttu-id="adec6-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adec6-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adec6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adec6-135">CommonParameters</span></span>
<span data-ttu-id="adec6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adec6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adec6-137">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adec6-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adec6-138">입력</span><span class="sxs-lookup"><span data-stu-id="adec6-138">INPUTS</span></span>

### <span data-ttu-id="adec6-139">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="adec6-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="adec6-140">출력</span><span class="sxs-lookup"><span data-stu-id="adec6-140">OUTPUTS</span></span>

### <span data-ttu-id="adec6-141">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="adec6-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="adec6-142">상속자</span><span class="sxs-lookup"><span data-stu-id="adec6-142">NOTES</span></span>

## <span data-ttu-id="adec6-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adec6-143">RELATED LINKS</span></span>
