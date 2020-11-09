---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BDBA3AA3-DCC6-4C83-84C8-EE6D93BFE1D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaserecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseRecommendedActionState.md
ms.openlocfilehash: 6d634760080e3fb26153b747e733369b20bc8336
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310616"
---
# <span data-ttu-id="c91d6-101">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c91d6-101">Set-AzSqlDatabaseRecommendedActionState</span></span>

## <span data-ttu-id="c91d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c91d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c91d6-103">Azure SQL 데이터베이스 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-103">Updates the state of an Azure SQL Database recommended action.</span></span>

## <span data-ttu-id="c91d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c91d6-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c91d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c91d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c91d6-106">**AzSqlDatabaseRecommendedActionState** Cmdlet은 Azure SQL 데이터베이스 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-106">The **Set-AzSqlDatabaseRecommendedActionState** cmdlet updates the state of an Azure SQL Database Recommended Action.</span></span>
<span data-ttu-id="c91d6-107">이를 통해 권장 되는 작업을 새 상태에 따라 적용 하거나 취소 하거나 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-107">This allows a recommended action to be applied, reverted or discarded based on the new state.</span></span>

## <span data-ttu-id="c91d6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c91d6-108">EXAMPLES</span></span>

### <span data-ttu-id="c91d6-109">예제 1: 보류에 권장 작업 상태 적용</span><span class="sxs-lookup"><span data-stu-id="c91d6-109">Example 1: Apply a recommended action state to pending</span></span>
```
PS C:\>Set-AzSqlDatabaseRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
DatabaseName               : WIRunner

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

<span data-ttu-id="c91d6-110">이 명령은 \[ \] \[ \] wirunner에서 Pending으로 명명 된 데이터베이스에 속한 IR_ test_schema _ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893 이라는 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-110">This command updates the state of the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 that belongs to the database named WIRunner to Pending.</span></span>

## <span data-ttu-id="c91d6-111">변수</span><span class="sxs-lookup"><span data-stu-id="c91d6-111">PARAMETERS</span></span>

### <span data-ttu-id="c91d6-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="c91d6-112">-AdvisorName</span></span>
<span data-ttu-id="c91d6-113">이 권장 작업이 속하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="c91d6-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c91d6-114">-DatabaseName</span></span>
<span data-ttu-id="c91d6-115">이 cmdlet이 권장 되는 동작 상태를 설정 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-115">Specifies the name of the database for which this cmdlet sets the recommended action state.</span></span>

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

### <span data-ttu-id="c91d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c91d6-116">-DefaultProfile</span></span>
<span data-ttu-id="c91d6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c91d6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c91d6-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="c91d6-118">-RecommendedActionName</span></span>
<span data-ttu-id="c91d6-119">업데이트 되는 상태에 대해 권장 되는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-119">Specifies the name of the recommended action for which state is being updated.</span></span>

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

### <span data-ttu-id="c91d6-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c91d6-120">-ResourceGroupName</span></span>
<span data-ttu-id="c91d6-121">이 데이터베이스를 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-121">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="c91d6-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c91d6-122">-ServerName</span></span>
<span data-ttu-id="c91d6-123">데이터베이스가 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-123">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="c91d6-124">-상태</span><span class="sxs-lookup"><span data-stu-id="c91d6-124">-State</span></span>
<span data-ttu-id="c91d6-125">이 cmdlet이 권장 동작 상태를 업데이트 하는 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-125">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="c91d6-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c91d6-127">활성</span><span class="sxs-lookup"><span data-stu-id="c91d6-127">Active</span></span>
- <span data-ttu-id="c91d6-128">중일</span><span class="sxs-lookup"><span data-stu-id="c91d6-128">Pending</span></span>
- <span data-ttu-id="c91d6-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="c91d6-129">PendingRevert</span></span>
- <span data-ttu-id="c91d6-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="c91d6-130">RevertCancelled</span></span>
- <span data-ttu-id="c91d6-131">무시할</span><span class="sxs-lookup"><span data-stu-id="c91d6-131">Ignored</span></span>
- <span data-ttu-id="c91d6-132">됨으로</span><span class="sxs-lookup"><span data-stu-id="c91d6-132">Resolved</span></span>

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

### <span data-ttu-id="c91d6-133">-확인</span><span class="sxs-lookup"><span data-stu-id="c91d6-133">-Confirm</span></span>
<span data-ttu-id="c91d6-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c91d6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c91d6-135">-WhatIf</span></span>
<span data-ttu-id="c91d6-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c91d6-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c91d6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c91d6-138">CommonParameters</span></span>
<span data-ttu-id="c91d6-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c91d6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c91d6-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c91d6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c91d6-141">입력</span><span class="sxs-lookup"><span data-stu-id="c91d6-141">INPUTS</span></span>

### <span data-ttu-id="c91d6-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c91d6-142">System.String</span></span>

### <span data-ttu-id="c91d6-143">RecommendedActionState를 RecommendedAction로 자동으로 명령</span><span class="sxs-lookup"><span data-stu-id="c91d6-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="c91d6-144">출력</span><span class="sxs-lookup"><span data-stu-id="c91d6-144">OUTPUTS</span></span>

### <span data-ttu-id="c91d6-145">RecommendedAction. AzureSqlDatabaseRecommendedActionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="c91d6-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="c91d6-146">상속자</span><span class="sxs-lookup"><span data-stu-id="c91d6-146">NOTES</span></span>
* <span data-ttu-id="c91d6-147">키워드: azure, azurerm, arm, resource, 관리, manager, sql, 데이터베이스, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="c91d6-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="c91d6-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c91d6-148">RELATED LINKS</span></span>

[<span data-ttu-id="c91d6-149">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c91d6-149">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="c91d6-150">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c91d6-150">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="c91d6-151">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c91d6-151">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="c91d6-152">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c91d6-152">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="c91d6-153">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c91d6-153">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="c91d6-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c91d6-154">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c91d6-155">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c91d6-155">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="c91d6-156">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="c91d6-156">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="c91d6-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c91d6-157">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c91d6-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c91d6-158">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c91d6-159">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c91d6-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
