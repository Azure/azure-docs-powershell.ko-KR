---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176748"
---
# <span data-ttu-id="1632a-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1632a-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="1632a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1632a-102">SYNOPSIS</span></span>
<span data-ttu-id="1632a-103">탄력적 풀 권장 SQL Azure의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="1632a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1632a-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1632a-105">설명</span><span class="sxs-lookup"><span data-stu-id="1632a-105">DESCRIPTION</span></span>
<span data-ttu-id="1632a-106">**Set-AzSqlElasticPoolRecommendedActionState** cmdlet은 Azure SQL 탄력적 풀 권장 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="1632a-107">이 cmdlet은 새 상태를 기반으로 권장되는 작업을 적용하거나, 되 돌리거나, 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="1632a-108">예제</span><span class="sxs-lookup"><span data-stu-id="1632a-108">EXAMPLES</span></span>

### <span data-ttu-id="1632a-109">예제 1: 권장 작업의 상태를 보류 중으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="1632a-109">Example 1: Update the state of a recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlElasticPoolRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ElasticPoolName            : WIRunnerPool
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="1632a-110">이 명령은 IR_ test_schema \[ \] \[ _test_table_0.0361551 _6C7AE8CC9C87E7FD5893 탄력적 풀 권장 작업의 상태를 \] 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="1632a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1632a-111">PARAMETERS</span></span>

### <span data-ttu-id="1632a-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="1632a-112">-AdvisorName</span></span>
<span data-ttu-id="1632a-113">이 권장 작업이 속한 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1632a-114">-DefaultProfile</span></span>
<span data-ttu-id="1632a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1632a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1632a-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1632a-116">-ElasticPoolName</span></span>
<span data-ttu-id="1632a-117">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-117">Specifies name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="1632a-118">-RecommendedActionName</span></span>
<span data-ttu-id="1632a-119">이 cmdlet이 상태를 업데이트하는 권장 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1632a-120">-ResourceGroupName</span></span>
<span data-ttu-id="1632a-121">이 탄력적 풀을 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1632a-122">-ServerName</span></span>
<span data-ttu-id="1632a-123">탄력적 풀이 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-123">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-124">-State</span><span class="sxs-lookup"><span data-stu-id="1632a-124">-State</span></span>
<span data-ttu-id="1632a-125">이 cmdlet이 권장 작업 상태를 업데이트하는 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="1632a-126">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1632a-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1632a-127">활성</span><span class="sxs-lookup"><span data-stu-id="1632a-127">Active</span></span>
- <span data-ttu-id="1632a-128">보류 중</span><span class="sxs-lookup"><span data-stu-id="1632a-128">Pending</span></span>
- <span data-ttu-id="1632a-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="1632a-129">PendingRevert</span></span>
- <span data-ttu-id="1632a-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="1632a-130">RevertCancelled</span></span>
- <span data-ttu-id="1632a-131">무시</span><span class="sxs-lookup"><span data-stu-id="1632a-131">Ignored</span></span>
- <span data-ttu-id="1632a-132">해결되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-132">Resolved</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1632a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1632a-133">-Confirm</span></span>
<span data-ttu-id="1632a-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1632a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1632a-135">-WhatIf</span></span>
<span data-ttu-id="1632a-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1632a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1632a-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1632a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1632a-138">CommonParameters</span></span>
<span data-ttu-id="1632a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1632a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1632a-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1632a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1632a-141">입력</span><span class="sxs-lookup"><span data-stu-id="1632a-141">INPUTS</span></span>

### <span data-ttu-id="1632a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1632a-142">System.String</span></span>

### <span data-ttu-id="1632a-143">Microsoft.Azure.Commands.Sql.RecommendedAction.cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1632a-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="1632a-144">출력</span><span class="sxs-lookup"><span data-stu-id="1632a-144">OUTPUTS</span></span>

### <span data-ttu-id="1632a-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="1632a-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="1632a-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1632a-146">NOTES</span></span>
* <span data-ttu-id="1632a-147">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, elasticpool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="1632a-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="1632a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1632a-148">RELATED LINKS</span></span>

[<span data-ttu-id="1632a-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="1632a-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="1632a-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1632a-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="1632a-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="1632a-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="1632a-152">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1632a-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
