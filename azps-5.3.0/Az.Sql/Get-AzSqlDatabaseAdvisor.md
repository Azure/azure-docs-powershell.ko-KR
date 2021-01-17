---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5AAB22C6-8E3C-4BDC-8A54-DA5A9906B762
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseadvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAdvisor.md
ms.openlocfilehash: 05bde2ee8a5bbcae941203115c49ff6b9fbc6bae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375117"
---
# <span data-ttu-id="90bc8-101">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="90bc8-101">Get-AzSqlDatabaseAdvisor</span></span>

## <span data-ttu-id="90bc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90bc8-102">SYNOPSIS</span></span>
<span data-ttu-id="90bc8-103">Azure SQL Database에 대한 하나 이상의 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-103">Gets one or more Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="90bc8-104">구문</span><span class="sxs-lookup"><span data-stu-id="90bc8-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -DatabaseName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90bc8-105">설명</span><span class="sxs-lookup"><span data-stu-id="90bc8-105">DESCRIPTION</span></span>
<span data-ttu-id="90bc8-106">**Get-AzSqlDatabaseAdvisor** cmdlet은 Azure SQL 데이터베이스에 대한 하나 이상의 Azure SQL Database Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-106">The **Get-AzSqlDatabaseAdvisor** cmdlet gets one or more Azure SQL Database Advisors for an Azure SQL Database.</span></span>

## <span data-ttu-id="90bc8-107">예제</span><span class="sxs-lookup"><span data-stu-id="90bc8-107">EXAMPLES</span></span>

### <span data-ttu-id="90bc8-108">예제 1: 지정된 데이터베이스에 대한 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="90bc8-108">Example 1: List all the advisors for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="90bc8-109">이 명령은 wi-runner-australia-east 서버에 속하는 WIRunner라는 데이터베이스에 대한 모든 Advisor를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-109">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="90bc8-110">예제 2: 지정된 데이터베이스에 대한 단일 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-110">Example 2: Get a single advisor for the specified database</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex"
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="90bc8-111">이 명령은 WIRunner라는 데이터베이스에 대해 CreateIndex라는 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-111">This command gets the Advisor named CreateIndex for the database named WIRunner.</span></span>

### <span data-ttu-id="90bc8-112">예제 3: 응답에 포함된 권장 작업과 함께 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="90bc8-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="90bc8-113">이 명령은 응답에 포함된 권장 작업을 사용하여 'WIRunner'라는 데이터베이스에 대한 모든 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-113">This command gets all the advisors for the database named 'WIRunner' with their recommended actions included in the response.</span></span>
<span data-ttu-id="90bc8-114">이 명령은 *ExpandRecommendedActions* 매개 변수를 사용하기 때문에 cmdlet은 응답과 함께 권장되는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="90bc8-115">예제 4: 응답에 포함된 권장 작업을 통해 단일 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName "CreateIndex" -ExpandRecommendedActions
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="90bc8-116">이 명령은 응답에 포함된 권장 작업을 사용하여 WIRunner라는 데이터베이스에서 CreateIndex라는 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-116">This command gets the Advisor named CreateIndex from the database named WIRunner with its recommended actions included in the response.</span></span>
<span data-ttu-id="90bc8-117">이 명령은 *ExpandRecommendedActions* 매개 변수를 사용하기 때문에 cmdlet은 응답과 함께 권장되는 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-117">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the recommended actions with the response.</span></span>

### <span data-ttu-id="90bc8-118">예제 5: 필터링을 사용하여 지정된 데이터베이스에 대한 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="90bc8-118">Example 5: List all the advisors for the specified database using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -DatabaseName "WIRunner" -AdvisorName d*
DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

DatabaseName                   : WIRunner
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="90bc8-119">이 명령은 wi-runner-australia-east이라는 서버에 속한 WIRunner라는 데이터베이스에 대한 모든 Advisor를 나열하고 문자 "d"로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-119">This command gets lists all the advisors for the database named WIRunner that belongs to the server named wi-runner-australia-east and start with the letter "d".</span></span>

## <span data-ttu-id="90bc8-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90bc8-120">PARAMETERS</span></span>

### <span data-ttu-id="90bc8-121">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="90bc8-121">-AdvisorName</span></span>
<span data-ttu-id="90bc8-122">이 cmdlet이 얻을 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-122">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="90bc8-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90bc8-123">-DatabaseName</span></span>
<span data-ttu-id="90bc8-124">이 cmdlet이 Advisor를 요청하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-124">Specifies the name of the database for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="90bc8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bc8-125">-DefaultProfile</span></span>
<span data-ttu-id="90bc8-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90bc8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90bc8-127">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="90bc8-127">-ExpandRecommendedActions</span></span>
<span data-ttu-id="90bc8-128">이 cmdlet이 응답을 통해 권장되는 작업을 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-128">Indicates that this cmdlet gets the recommended actions with the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90bc8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90bc8-129">-ResourceGroupName</span></span>
<span data-ttu-id="90bc8-130">이 데이터베이스를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-130">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="90bc8-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90bc8-131">-ServerName</span></span>
<span data-ttu-id="90bc8-132">데이터베이스를 포함하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-132">Specifies the name of the server that contains the database.</span></span>

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

### <span data-ttu-id="90bc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bc8-133">CommonParameters</span></span>
<span data-ttu-id="90bc8-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90bc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bc8-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="90bc8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bc8-136">입력</span><span class="sxs-lookup"><span data-stu-id="90bc8-136">INPUTS</span></span>

### <span data-ttu-id="90bc8-137">System.String</span><span class="sxs-lookup"><span data-stu-id="90bc8-137">System.String</span></span>

### <span data-ttu-id="90bc8-138">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90bc8-138">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90bc8-139">출력</span><span class="sxs-lookup"><span data-stu-id="90bc8-139">OUTPUTS</span></span>

### <span data-ttu-id="90bc8-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="90bc8-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="90bc8-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90bc8-141">NOTES</span></span>
* <span data-ttu-id="90bc8-142">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 데이터베이스, mssql, 관리자</span><span class="sxs-lookup"><span data-stu-id="90bc8-142">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql, advisor</span></span>

## <span data-ttu-id="90bc8-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90bc8-143">RELATED LINKS</span></span>

[<span data-ttu-id="90bc8-144">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="90bc8-144">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="90bc8-145">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="90bc8-145">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="90bc8-146">Get-AzSqlDatabaseRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="90bc8-146">Get-AzSqlDatabaseRecommendedAction</span></span>](./Get-AzSqlDatabaseRecommendedAction.md)

[<span data-ttu-id="90bc8-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="90bc8-147">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="90bc8-148">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="90bc8-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
