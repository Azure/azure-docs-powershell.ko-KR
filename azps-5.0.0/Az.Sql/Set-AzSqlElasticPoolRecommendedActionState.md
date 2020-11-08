---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EFDFCE12-F39C-4F52-9962-4601F0C4FD47
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpoolrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPoolRecommendedActionState.md
ms.openlocfilehash: 64a8884075bcc849deffd4083c95ec1849859a68
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218788"
---
# <span data-ttu-id="79b9c-101">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="79b9c-101">Set-AzSqlElasticPoolRecommendedActionState</span></span>

## <span data-ttu-id="79b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="79b9c-103">Azure SQL 탄력적 풀 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-103">Updates the state of an Azure SQL Elastic Pool recommended action.</span></span>

## <span data-ttu-id="79b9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79b9c-104">SYNTAX</span></span>

```
Set-AzSqlElasticPoolRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79b9c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="79b9c-106">**AzSqlElasticPoolRecommendedActionState** Cmdlet은 Azure SQL 탄력적인 풀의 권장 작업 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-106">The **Set-AzSqlElasticPoolRecommendedActionState** cmdlet updates state of an Azure SQL Elastic Pool recommended action.</span></span>
<span data-ttu-id="79b9c-107">이 cmdlet은 새 상태에 따라 권장 작업을 적용 하거나, 취소 하거나, 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-107">This cmdlet applies an recommended action, reverted, or discarded based on the new state.</span></span>

## <span data-ttu-id="79b9c-108">예제의</span><span class="sxs-lookup"><span data-stu-id="79b9c-108">EXAMPLES</span></span>

### <span data-ttu-id="79b9c-109">예제 1: 권장 작업의 상태를 보류 중으로 업데이트</span><span class="sxs-lookup"><span data-stu-id="79b9c-109">Example 1: Update the state of a recommended action to Pending</span></span>
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

<span data-ttu-id="79b9c-110">이 명령은 IR_ \[ test_schema \] _ \[ test_table_0 .0361551 _6C7AE8CC9C87E7FD5893을 보류 중으로 지정 된 탄력적 풀 권장 작업의 상태 \] 를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-110">This command updates the state of elastic pool recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 to Pending.</span></span>

## <span data-ttu-id="79b9c-111">변수</span><span class="sxs-lookup"><span data-stu-id="79b9c-111">PARAMETERS</span></span>

### <span data-ttu-id="79b9c-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="79b9c-112">-AdvisorName</span></span>
<span data-ttu-id="79b9c-113">이 권장 작업이 속하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-113">Specifies the name of the advisor for which this recommended action belongs to.</span></span>

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

### <span data-ttu-id="79b9c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b9c-114">-DefaultProfile</span></span>
<span data-ttu-id="79b9c-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="79b9c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79b9c-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79b9c-116">-ElasticPoolName</span></span>
<span data-ttu-id="79b9c-117">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-117">Specifies name of the elastic pool.</span></span>

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

### <span data-ttu-id="79b9c-118">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="79b9c-118">-RecommendedActionName</span></span>
<span data-ttu-id="79b9c-119">이 cmdlet이 상태를 업데이트 하는 데 권장 되는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-119">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

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

### <span data-ttu-id="79b9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79b9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="79b9c-121">이 탄력적 풀을 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-121">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="79b9c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79b9c-122">-ServerName</span></span>
<span data-ttu-id="79b9c-123">탄력적 풀이 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-123">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="79b9c-124">-상태</span><span class="sxs-lookup"><span data-stu-id="79b9c-124">-State</span></span>
<span data-ttu-id="79b9c-125">이 cmdlet이 권장 되는 동작 상태를 업데이트 하는 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-125">Specifies the value to which this cmdlet updates the recommended action state.</span></span>
<span data-ttu-id="79b9c-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="79b9c-127">활성</span><span class="sxs-lookup"><span data-stu-id="79b9c-127">Active</span></span>
- <span data-ttu-id="79b9c-128">중일</span><span class="sxs-lookup"><span data-stu-id="79b9c-128">Pending</span></span>
- <span data-ttu-id="79b9c-129">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="79b9c-129">PendingRevert</span></span>
- <span data-ttu-id="79b9c-130">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="79b9c-130">RevertCancelled</span></span>
- <span data-ttu-id="79b9c-131">무시할</span><span class="sxs-lookup"><span data-stu-id="79b9c-131">Ignored</span></span>
- <span data-ttu-id="79b9c-132">됨으로</span><span class="sxs-lookup"><span data-stu-id="79b9c-132">Resolved</span></span>

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

### <span data-ttu-id="79b9c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="79b9c-133">-Confirm</span></span>
<span data-ttu-id="79b9c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b9c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b9c-135">-WhatIf</span></span>
<span data-ttu-id="79b9c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79b9c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b9c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b9c-138">CommonParameters</span></span>
<span data-ttu-id="79b9c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79b9c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b9c-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79b9c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b9c-141">입력</span><span class="sxs-lookup"><span data-stu-id="79b9c-141">INPUTS</span></span>

### <span data-ttu-id="79b9c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79b9c-142">System.String</span></span>

### <span data-ttu-id="79b9c-143">RecommendedActionState를 RecommendedAction로 자동으로 명령</span><span class="sxs-lookup"><span data-stu-id="79b9c-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Cmdlet.RecommendedActionState</span></span>

## <span data-ttu-id="79b9c-144">출력</span><span class="sxs-lookup"><span data-stu-id="79b9c-144">OUTPUTS</span></span>

### <span data-ttu-id="79b9c-145">RecommendedAction. AzureSqlElasticPoolRecommendedActionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="79b9c-145">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="79b9c-146">상속자</span><span class="sxs-lookup"><span data-stu-id="79b9c-146">NOTES</span></span>
* <span data-ttu-id="79b9c-147">키워드: azure, azurerm, arm, resource, 관리, manager, sql, elasticpool, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="79b9c-147">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="79b9c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79b9c-148">RELATED LINKS</span></span>

[<span data-ttu-id="79b9c-149">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="79b9c-149">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="79b9c-150">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="79b9c-150">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="79b9c-151">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="79b9c-151">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="79b9c-152">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="79b9c-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
