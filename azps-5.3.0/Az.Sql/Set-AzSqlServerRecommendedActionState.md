---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492311"
---
# <span data-ttu-id="aba90-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="aba90-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="aba90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aba90-102">SYNOPSIS</span></span>
<span data-ttu-id="aba90-103">권장되는 작업으로 Azure SQL Server 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="aba90-104">구문</span><span class="sxs-lookup"><span data-stu-id="aba90-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aba90-105">설명</span><span class="sxs-lookup"><span data-stu-id="aba90-105">DESCRIPTION</span></span>
<span data-ttu-id="aba90-106">**Set-AzSqlServerRecommendedActionState** cmdlet은 권장되는 작업으로 Azure SQL Server 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="aba90-107">이 cmdlet은 새 상태를 기반으로 권장되는 작업을 적용, 되회 또는 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="aba90-108">예제</span><span class="sxs-lookup"><span data-stu-id="aba90-108">EXAMPLES</span></span>

### <span data-ttu-id="aba90-109">예제1: 지정된 권장 작업의 상태를 보류 중으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
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

<span data-ttu-id="aba90-110">"IR_ test_schema \[ \] \[ _test_table_0.0361551 "보류 \] 중"으로 _6C7AE8CC9C87E7FD5893 서버 권장 작업의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="aba90-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aba90-111">PARAMETERS</span></span>

### <span data-ttu-id="aba90-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="aba90-112">-AdvisorName</span></span>
<span data-ttu-id="aba90-113">권장 작업을 포함하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="aba90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba90-114">-DefaultProfile</span></span>
<span data-ttu-id="aba90-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aba90-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aba90-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="aba90-116">-RecommendedActionName</span></span>
<span data-ttu-id="aba90-117">이 cmdlet이 상태를 업데이트하는 권장 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="aba90-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba90-118">-ResourceGroupName</span></span>
<span data-ttu-id="aba90-119">서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="aba90-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="aba90-120">-ServerName</span></span>
<span data-ttu-id="aba90-121">서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="aba90-122">-State</span><span class="sxs-lookup"><span data-stu-id="aba90-122">-State</span></span>
<span data-ttu-id="aba90-123">이 cmdlet이 권장 작업 상태를 업데이트하는 새 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="aba90-124">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="aba90-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aba90-125">활성</span><span class="sxs-lookup"><span data-stu-id="aba90-125">Active</span></span>
- <span data-ttu-id="aba90-126">보류 중</span><span class="sxs-lookup"><span data-stu-id="aba90-126">Pending</span></span>
- <span data-ttu-id="aba90-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="aba90-127">PendingRevert</span></span>
- <span data-ttu-id="aba90-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="aba90-128">RevertCancelled</span></span>
- <span data-ttu-id="aba90-129">무시</span><span class="sxs-lookup"><span data-stu-id="aba90-129">Ignored</span></span>
- <span data-ttu-id="aba90-130">해결</span><span class="sxs-lookup"><span data-stu-id="aba90-130">Resolved</span></span>

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

### <span data-ttu-id="aba90-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aba90-131">-Confirm</span></span>
<span data-ttu-id="aba90-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aba90-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aba90-133">-WhatIf</span></span>
<span data-ttu-id="aba90-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aba90-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aba90-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aba90-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba90-136">CommonParameters</span></span>
<span data-ttu-id="aba90-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aba90-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba90-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aba90-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba90-139">입력</span><span class="sxs-lookup"><span data-stu-id="aba90-139">INPUTS</span></span>

### <span data-ttu-id="aba90-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aba90-140">System.String</span></span>

### <span data-ttu-id="aba90-141">Microsoft.Azure.Commands.Sql.RecommendedAction.cmdlet.RecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="aba90-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="aba90-142">출력</span><span class="sxs-lookup"><span data-stu-id="aba90-142">OUTPUTS</span></span>

### <span data-ttu-id="aba90-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="aba90-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="aba90-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aba90-144">NOTES</span></span>
* <span data-ttu-id="aba90-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 서버, mssql, 관리자, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="aba90-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="aba90-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aba90-146">RELATED LINKS</span></span>

[<span data-ttu-id="aba90-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="aba90-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="aba90-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="aba90-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="aba90-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="aba90-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="aba90-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="aba90-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="aba90-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="aba90-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
