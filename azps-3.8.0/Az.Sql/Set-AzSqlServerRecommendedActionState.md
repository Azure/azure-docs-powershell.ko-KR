---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerRecommendedActionState.md
ms.openlocfilehash: 78366f70db7bd586e1e35566f167c7cae2c2dbf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878766"
---
# <span data-ttu-id="708c2-101">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="708c2-101">Set-AzSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="708c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="708c2-102">SYNOPSIS</span></span>
<span data-ttu-id="708c2-103">Azure SQL Server 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-103">Updates the state of an Azure SQL Server recommended action.</span></span>

## <span data-ttu-id="708c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="708c2-104">SYNTAX</span></span>

```
Set-AzSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="708c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="708c2-105">DESCRIPTION</span></span>
<span data-ttu-id="708c2-106">Azure SQL Server 권장 작업의 **Set-AzSqlServerRecommendedActionState** cmdlet 업데이트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-106">The **Set-AzSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="708c2-107">이 cmdlet은 새 상태에 따라 권장 작업을 적용 하거나, 취소 하거나, 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="708c2-108">예제의</span><span class="sxs-lookup"><span data-stu-id="708c2-108">EXAMPLES</span></span>

### <span data-ttu-id="708c2-109">Example1: 지정 된 권장 작업의 상태를 보류 중으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-109">Example1: Update the state of the specified recommended action to Pending</span></span>
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

<span data-ttu-id="708c2-110">"IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893"이 "보류 중" 인 서버 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="708c2-111">변수</span><span class="sxs-lookup"><span data-stu-id="708c2-111">PARAMETERS</span></span>

### <span data-ttu-id="708c2-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="708c2-112">-AdvisorName</span></span>
<span data-ttu-id="708c2-113">권장 작업을 포함 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-113">Specifies the name of the advisor that contains the recommended action.</span></span>

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

### <span data-ttu-id="708c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708c2-114">-DefaultProfile</span></span>
<span data-ttu-id="708c2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="708c2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="708c2-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="708c2-116">-RecommendedActionName</span></span>
<span data-ttu-id="708c2-117">이 cmdlet이 상태를 업데이트 하는 데 권장 되는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="708c2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708c2-118">-ResourceGroupName</span></span>
<span data-ttu-id="708c2-119">서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-119">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="708c2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="708c2-120">-ServerName</span></span>
<span data-ttu-id="708c2-121">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="708c2-122">-상태</span><span class="sxs-lookup"><span data-stu-id="708c2-122">-State</span></span>
<span data-ttu-id="708c2-123">이 cmdlet이 권장 동작 상태를 업데이트 하는 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="708c2-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-124">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="708c2-125">활성</span><span class="sxs-lookup"><span data-stu-id="708c2-125">Active</span></span>
- <span data-ttu-id="708c2-126">중일</span><span class="sxs-lookup"><span data-stu-id="708c2-126">Pending</span></span>
- <span data-ttu-id="708c2-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="708c2-127">PendingRevert</span></span>
- <span data-ttu-id="708c2-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="708c2-128">RevertCancelled</span></span>
- <span data-ttu-id="708c2-129">무시할</span><span class="sxs-lookup"><span data-stu-id="708c2-129">Ignored</span></span>
- <span data-ttu-id="708c2-130">됨으로</span><span class="sxs-lookup"><span data-stu-id="708c2-130">Resolved</span></span>

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

### <span data-ttu-id="708c2-131">-확인</span><span class="sxs-lookup"><span data-stu-id="708c2-131">-Confirm</span></span>
<span data-ttu-id="708c2-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708c2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708c2-133">-WhatIf</span></span>
<span data-ttu-id="708c2-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="708c2-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708c2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708c2-136">CommonParameters</span></span>
<span data-ttu-id="708c2-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="708c2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708c2-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="708c2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708c2-139">입력</span><span class="sxs-lookup"><span data-stu-id="708c2-139">INPUTS</span></span>

### <span data-ttu-id="708c2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="708c2-140">System.String</span></span>

### <span data-ttu-id="708c2-141">RecommendedActionState를 RecommendedAction로 자동으로 명령</span><span class="sxs-lookup"><span data-stu-id="708c2-141">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="708c2-142">출력</span><span class="sxs-lookup"><span data-stu-id="708c2-142">OUTPUTS</span></span>

### <span data-ttu-id="708c2-143">RecommendedAction. AzureSqlServerRecommendedActionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="708c2-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="708c2-144">상속자</span><span class="sxs-lookup"><span data-stu-id="708c2-144">NOTES</span></span>
* <span data-ttu-id="708c2-145">키워드: azure, azurerm, arm, resource, 관리, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="708c2-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="708c2-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="708c2-146">RELATED LINKS</span></span>

[<span data-ttu-id="708c2-147">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="708c2-147">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="708c2-148">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="708c2-148">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="708c2-149">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="708c2-149">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="708c2-150">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="708c2-150">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="708c2-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="708c2-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
