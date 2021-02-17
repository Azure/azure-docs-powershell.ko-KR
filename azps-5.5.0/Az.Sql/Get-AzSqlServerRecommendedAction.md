---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BB513A53-48A0-4F8F-93F0-D3DFA2C3D523
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerRecommendedAction.md
ms.openlocfilehash: b27ded3d1ec4dbf011ca819ab55ddef0fb0df9c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196129"
---
# <span data-ttu-id="b580f-101">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b580f-101">Get-AzSqlServerRecommendedAction</span></span>

## <span data-ttu-id="b580f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b580f-102">SYNOPSIS</span></span>
<span data-ttu-id="b580f-103">Azure SQL Server Advisor에 대해 권장되는 하나 이상의 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-103">Gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b580f-104">구문</span><span class="sxs-lookup"><span data-stu-id="b580f-104">SYNTAX</span></span>

```
Get-AzSqlServerRecommendedAction [-RecommendedActionName <String>] -ServerName <String> -AdvisorName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b580f-105">설명</span><span class="sxs-lookup"><span data-stu-id="b580f-105">DESCRIPTION</span></span>
<span data-ttu-id="b580f-106">**Get-AzSqlServerRecommendedAction** cmdlet은 Azure SQL Server Advisor에 대해 권장되는 하나 이상의 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-106">The **Get-AzSqlServerRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b580f-107">예제</span><span class="sxs-lookup"><span data-stu-id="b580f-107">EXAMPLES</span></span>

### <span data-ttu-id="b580f-108">예제 1: 특정 Advisor에 대한 모든 권장 작업 목록</span><span class="sxs-lookup"><span data-stu-id="b580f-108">Example 1: Get a list of  all recommended actions for a specific Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="b580f-109">이 명령은 wi-runner-australia-east라는 서버에 사용할 수 있는 createIndex라는 SQL Server Advisor에 대해 권장되는 모든 작업 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-109">This command gets a list of all recommended actions of for the SQL Server Advisor named CreateIndex available for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="b580f-110">예제 2: Advisor에 대한 단일 권장 작업 수행</span><span class="sxs-lookup"><span data-stu-id="b580f-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlServerRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName 
IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
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

<span data-ttu-id="b580f-111">이 명령은 \[ \] \[ CreateIndex라는 Advisor에서 IR_ test_schema _test_table_0.0361551_6C7AE8CC9C87E7FD5893라는 권장 작업을 \] 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-111">This command gets a recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b580f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b580f-112">PARAMETERS</span></span>

### <span data-ttu-id="b580f-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="b580f-113">-AdvisorName</span></span>
<span data-ttu-id="b580f-114">이 cmdlet이 작업을 요청하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-114">Specifies the name of the advisor for which this cmdlet requests actions.</span></span>

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

### <span data-ttu-id="b580f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b580f-115">-DefaultProfile</span></span>
<span data-ttu-id="b580f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b580f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b580f-117">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="b580f-117">-RecommendedActionName</span></span>
<span data-ttu-id="b580f-118">이 cmdlet에서 얻을 권장 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-118">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b580f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b580f-119">-ResourceGroupName</span></span>
<span data-ttu-id="b580f-120">이 서버를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-120">Specifies the name of the resource group of the server that contains this server.</span></span>

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

### <span data-ttu-id="b580f-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b580f-121">-ServerName</span></span>
<span data-ttu-id="b580f-122">Advisor가 속한 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-122">Specifies the name of the server the Advisor belongs to.</span></span>

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

### <span data-ttu-id="b580f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b580f-123">CommonParameters</span></span>
<span data-ttu-id="b580f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b580f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b580f-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b580f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b580f-126">입력</span><span class="sxs-lookup"><span data-stu-id="b580f-126">INPUTS</span></span>

### <span data-ttu-id="b580f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b580f-127">System.String</span></span>

## <span data-ttu-id="b580f-128">출력</span><span class="sxs-lookup"><span data-stu-id="b580f-128">OUTPUTS</span></span>

### <span data-ttu-id="b580f-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="b580f-129">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="b580f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b580f-130">NOTES</span></span>
* <span data-ttu-id="b580f-131">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 서버, mssql, 관리자, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="b580f-131">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="b580f-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b580f-132">RELATED LINKS</span></span>

[<span data-ttu-id="b580f-133">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b580f-133">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="b580f-134">Set-AzSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="b580f-134">Set-AzSqlServerRecommendedActionState</span></span>](./Set-AzSqlServerRecommendedActionState.md)

[<span data-ttu-id="b580f-135">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b580f-135">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="b580f-136">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="b580f-136">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="b580f-137">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="b580f-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
