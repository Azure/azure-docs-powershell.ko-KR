---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3FC9E586-3962-437E-B89F-BB4EA1FBF403
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendedaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendedAction.md
ms.openlocfilehash: 83abaaceffd58ea3e1d6277cc0142bf36deb2cae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176929"
---
# <span data-ttu-id="ea31b-101">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ea31b-101">Get-AzSqlElasticPoolRecommendedAction</span></span>

## <span data-ttu-id="ea31b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea31b-102">SYNOPSIS</span></span>
<span data-ttu-id="ea31b-103">Azure SQL 탄력적 풀 Advisor에 대한 하나 이상의 권장 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-103">Gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="ea31b-104">구문</span><span class="sxs-lookup"><span data-stu-id="ea31b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendedAction [-RecommendedActionName <String>] -ServerName <String>
 -ElasticPoolName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea31b-105">설명</span><span class="sxs-lookup"><span data-stu-id="ea31b-105">DESCRIPTION</span></span>
<span data-ttu-id="ea31b-106">**Get-AzSqlElasticPoolRecommendedAction** cmdlet은 Azure SQL 탄력적 풀 Advisor에 대해 권장되는 하나 이상의 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-106">The **Get-AzSqlElasticPoolRecommendedAction** cmdlet gets one or more recommended actions for an Azure SQL Elastic Pool Advisor.</span></span>

## <span data-ttu-id="ea31b-107">예제</span><span class="sxs-lookup"><span data-stu-id="ea31b-107">EXAMPLES</span></span>

### <span data-ttu-id="ea31b-108">예제 1: Advisor에 대한 모든 권장 작업 나열</span><span class="sxs-lookup"><span data-stu-id="ea31b-108">Example 1: List all recommended actions for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
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

ElasticPoolName            : WIRunnerPool
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

ElasticPoolName            : WIRunnerPool
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

<span data-ttu-id="ea31b-109">이 명령은 WIRunnerPool이라는 탄력적 풀에 사용할 수 있는 CreateIndex라는 Advisor의 모든 권장 작업 목록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-109">This command gets a list of all recommended actions of the Advisor named CreateIndex available for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="ea31b-110">예제 2: Advisor에 대한 단일 권장 작업 수행</span><span class="sxs-lookup"><span data-stu-id="ea31b-110">Example 2: Get a single recommended action for an Advisor</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendedAction -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893"
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

<span data-ttu-id="ea31b-111">이 명령은 \[ \] \[ CreateIndex라는 Advisor에서 IR_ test_schema _test_table_0.0361551 _6C7AE8CC9C87E7FD5893 권장되는 작업을 \] 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-111">This command gets the recommended action named IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893 from the Advisor named CreateIndex.</span></span>

## <span data-ttu-id="ea31b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea31b-112">PARAMETERS</span></span>

### <span data-ttu-id="ea31b-113">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="ea31b-113">-AdvisorName</span></span>
<span data-ttu-id="ea31b-114">이 cmdlet이 권장 작업을 요청하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-114">Specifies the name of the advisor for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="ea31b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea31b-115">-DefaultProfile</span></span>
<span data-ttu-id="ea31b-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ea31b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea31b-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ea31b-117">-ElasticPoolName</span></span>
<span data-ttu-id="ea31b-118">이 cmdlet이 권장 작업을 요청하는 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-118">Specifies the name of the elastic pool for which this cmdlet requests recommended actions.</span></span>

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

### <span data-ttu-id="ea31b-119">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="ea31b-119">-RecommendedActionName</span></span>
<span data-ttu-id="ea31b-120">이 cmdlet에서 얻을 권장 작업의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-120">Specifies the name of the recommended action that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ea31b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea31b-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea31b-122">이 탄력적 풀을 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-122">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="ea31b-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ea31b-123">-ServerName</span></span>
<span data-ttu-id="ea31b-124">탄력적 풀이 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-124">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="ea31b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea31b-125">CommonParameters</span></span>
<span data-ttu-id="ea31b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ea31b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea31b-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea31b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea31b-128">입력</span><span class="sxs-lookup"><span data-stu-id="ea31b-128">INPUTS</span></span>

### <span data-ttu-id="ea31b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ea31b-129">System.String</span></span>

## <span data-ttu-id="ea31b-130">출력</span><span class="sxs-lookup"><span data-stu-id="ea31b-130">OUTPUTS</span></span>

### <span data-ttu-id="ea31b-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span><span class="sxs-lookup"><span data-stu-id="ea31b-131">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlElasticPoolRecommendedActionModel</span></span>

## <span data-ttu-id="ea31b-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ea31b-132">NOTES</span></span>
* <span data-ttu-id="ea31b-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, elasticpool, mssql, 관리자, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="ea31b-133">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="ea31b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea31b-134">RELATED LINKS</span></span>

[<span data-ttu-id="ea31b-135">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ea31b-135">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="ea31b-136">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="ea31b-136">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="ea31b-137">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="ea31b-137">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="ea31b-138">Set-AzSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="ea31b-138">Set-AzSqlElasticPoolRecommendedActionState</span></span>](./Set-AzSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="ea31b-139">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ea31b-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
