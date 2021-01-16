---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: EF6C862B-A89C-48AB-A590-92CFA387305F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRecommendedAction.md
ms.openlocfilehash: fc54e470ed79593b40d25fdfc4cf655a0a8f44d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363350"
---
# <span data-ttu-id="b6397-101">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b6397-101">Get-AzSqlDatabaseRecommendedAction</span></span>

## <span data-ttu-id="b6397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6397-102">SYNOPSIS</span></span>
<span data-ttu-id="b6397-103">Azure SQL Database Advisor에 대해 권장되는 하나 이상의 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-103">Gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="b6397-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6397-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -DatabaseName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6397-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6397-105">DESCRIPTION</span></span>
<span data-ttu-id="b6397-106">**Get-AzSqlDatabaseRecommendedAction** cmdlet은 Azure SQL Database Advisor에 대해 권장되는 하나 이상의 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-106">The **Get-AzSqlDatabaseRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="b6397-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6397-107">EXAMPLES</span></span>

### <span data-ttu-id="b6397-108">예제 1: Advisor에 대한 모든 권장 작업 나열</span><span class="sxs-lookup"><span data-stu-id="b6397-108">Example 1: List all the recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
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

DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.236046_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.236046]]...} 
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
ObservedImpact             : {SpaceChange}
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
DatabaseName               : WIRunner
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.239359_6C7AE8CC9C87E7FD5893], [indexType, NONCLUSTERED], 
                             [schema, [test_schema]], [table, [test_table_0.239359]]...} 
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
RevertActionDuration       : PT10S
RevertActionInitiatedBy    : System
RevertActionInitiatedTime  : 4/21/2016 3:24:47 PM
RevertActionStartTime      : 4/21/2016 3:24:47 PM
Score                      : 3
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="b6397-109">이 명령은 wi-runner-australia-east라는 데이터베이스에 사용할 수 있는 CreateIndex라는 Advisor의 모든 권장 작업 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the database named wi-runner-australia-east.</span></span>

### <span data-ttu-id="b6397-110">예제 2: Advisor에 대한 단일 권장 작업 수행</span><span class="sxs-lookup"><span data-stu-id="b6397-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlDatabaseRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="b6397-111">이 명령은 \[ \] \[ CreateIndex라는 Advisor에 IR_ test_schema _ test_table_0.0361551 _6C7AE8CC9C87E7FD5893 권장되는 작업을 \] 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 for the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b6397-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6397-112">PARAMETERS</span></span>

### <span data-ttu-id="b6397-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b6397-113">-AdvisorName</span></span>
<span data-ttu-id="b6397-114">이 cmdlet이 권장 작업을 요청하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-114">Specifies the name of the Advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="b6397-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b6397-115">-DatabaseName</span></span>
<span data-ttu-id="b6397-116">이 cmdlet이 권장 작업을 요청하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-116">Specifies the name of the database for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="b6397-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6397-117">-DefaultProfile</span></span>
<span data-ttu-id="b6397-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6397-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6397-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b6397-119">-RecommendedActionName</span></span>
<span data-ttu-id="b6397-120">이 cmdlet에서 얻을 권장 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6397-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6397-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6397-122">이 데이터베이스를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-122">Specifies name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b6397-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b6397-123">-ServerName</span></span>
<span data-ttu-id="b6397-124">데이터베이스가 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-124">Specifies the name of the server the database is in.</span></span>

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

### <span data-ttu-id="b6397-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6397-125">CommonParameters</span></span>
<span data-ttu-id="b6397-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6397-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6397-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6397-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6397-128">입력</span><span class="sxs-lookup"><span data-stu-id="b6397-128">INPUTS</span></span>

### <span data-ttu-id="b6397-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b6397-129">System.String</span></span>

## <span data-ttu-id="b6397-130">출력</span><span class="sxs-lookup"><span data-stu-id="b6397-130">OUTPUTS</span></span>

### <span data-ttu-id="b6397-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b6397-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlDatabaseRecommendedActionModel</span></span>

## <span data-ttu-id="b6397-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6397-132">NOTES</span></span>
* <span data-ttu-id="b6397-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql, 관리자, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b6397-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b6397-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6397-134">RELATED LINKS</span></span>

[<span data-ttu-id="b6397-135">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="b6397-135">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="b6397-136">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b6397-136">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="b6397-137">Set-AzSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b6397-137">Set-AzSqlDatabaseRecommendedActionState</span></span>](./Set-AzSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="b6397-138">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b6397-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
